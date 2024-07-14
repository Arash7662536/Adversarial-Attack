# Adversarial Attacks
Adversarial attacks are techniques used to deceive machine learning models by introducing small, carefully crafted perturbations to the input data. These perturbations are often imperceptible to humans but can cause significant errors in the model’s predictions. The goal of adversarial attacks is to exploit the vulnerabilities of machine learning algorithms, leading them to make incorrect classifications or decisions.
Adversarial attacks can be broadly categorized into two types:

Evasion Attacks: These attacks occur during the model’s inference phase, where the attacker modifies the input data to cause the model to misclassify it.
Poisoning Attacks: These attacks happen during the training phase, where the attacker injects malicious data into the training set to corrupt the model.

# Fast Gradient Sign Method (FGSM)
The Fast Gradient Sign Method (FGSM) is a straightforward and widely used technique for generating adversarial examples. It was introduced by Goodfellow et al. in 2014. FGSM creates adversarial examples by adding a small perturbation to the input data in the direction of the gradient of the loss function with respect to the input. The perturbation is calculated as follows:

![images](https://github.com/user-attachments/assets/8e2d4368-eedd-40bb-9263-7da31af86d66)

FGSM is a white-box attack, meaning it requires access to the model’s parameters and gradients. This method is effective in demonstrating the vulnerability of machine learning models to adversarial perturbations, highlighting the need for robust defenses.

# Projected Gradient Descent (PGD)
Projected Gradient Descent (PGD) is an iterative method for generating adversarial examples, extending the Fast Gradient Sign Method (FGSM) by applying the perturbation multiple times. PGD is considered one of the most powerful adversarial attack methods. The process can be described as follows:

1-Initialization: Start with the original input ( x ).
2-Iteration: At each iteration ( i ), update the adversarial example using the gradient of the loss function
3- Repetition: Repeat the process for a predefined number of iterations or until convergence.
PGD is a white-box attack, meaning it requires access to the model’s parameters and gradients. This method is known for its effectiveness in creating robust adversarial examples, making it a crucial tool for testing and improving the robustness of machine learning models.


![Capture](https://github.com/user-attachments/assets/9ccad6e1-0e50-4b59-9cc5-126318a42a5c)
