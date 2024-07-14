# Introduction to Adversarial Attacks
Adversarial attacks are techniques used to deceive machine learning models by introducing small, carefully crafted perturbations to the input data. These perturbations are often imperceptible to humans but can cause significant errors in the model’s predictions. The goal of adversarial attacks is to exploit the vulnerabilities of machine learning algorithms, leading them to make incorrect classifications or decisions.
Adversarial attacks can be broadly categorized into two types:

Evasion Attacks: These attacks occur during the model’s inference phase, where the attacker modifies the input data to cause the model to misclassify it.
Poisoning Attacks: These attacks happen during the training phase, where the attacker injects malicious data into the training set to corrupt the model.

# Fast Gradient Sign Method (FGSM)
The Fast Gradient Sign Method (FGSM) is one of the simplest and most widely used techniques for generating adversarial examples. Introduced by Goodfellow et al. in 2014, FGSM creates adversarial examples by adding a small perturbation to the input data in the direction of the gradient of the loss function with respect to the input. The perturbation is calculated as follows:
xadv​=x+ϵ⋅sign(∇x​J(θ,x,y))
where:

( x_{\text{adv}} ) is the adversarial example.
( x ) is the original input.
( \epsilon ) is a small constant that controls the magnitude of the perturbation.
( \nabla_x J(\theta, x, y) ) is the gradient of the loss function ( J ) with respect to the input ( x ).
( \theta ) represents the model parameters.
( y ) is the true label of the input.

FGSM is a white-box attack, meaning it requires access to the model’s parameters and gradients.
Projected Gradient Descent (PGD)
Projected Gradient Descent (PGD) is an iterative method for generating adversarial examples. It extends FGSM by applying the perturbation multiple times, refining the adversarial example with each iteration. PGD is considered one of the most powerful adversarial attack methods. The process can be described as follows:


Start with the original input ( x ).


At each iteration ( i ), update the adversarial example using the gradient of the loss function:
xadv(i+1)​=Projϵ​(xadv(i)​+α⋅sign(∇x​J(θ,xadv(i)​,y)))
where:

( x_{\text{adv}}^{(i)} ) is the adversarial example at iteration ( i ).
( \alpha ) is the step size.
( \text{Proj}_{\epsilon} ) is the projection operator that ensures the perturbation remains within the allowed ( \epsilon )-ball around the original input.



Repeat the process for a predefined number of iterations or until convergence.


PGD is also a white-box attack and is known for its effectiveness in creating robust adversarial examples.
These methods highlight the importance of developing robust machine learning models that can withstand adversarial attacks, ensuring their reliability and safety in real-world applications12345.
I
