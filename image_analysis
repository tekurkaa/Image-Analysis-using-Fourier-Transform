from PIL import Image
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = Image.open("image.jpeg")

# Preprocess the image if necessary (e.g., resizing, converting to grayscale)
# Resize the image to a specific size
image = image.resize((width, height))

# Convert the image to grayscale
gray_image = image.convert("L")

# Convert the grayscale image to a NumPy array
image_array = np.array(gray_image)

# Apply the Fourier transform
fourier_transform = np.fft.fft2(image_array)

# Shift the zero frequency component to the center of the spectrum
fourier_transform_shifted = np.fft.fftshift(fourier_transform)

# Calculate the magnitude spectrum
magnitude_spectrum = 20 * np.log(np.abs(fourier_transform_shifted))

# Display the original image
plt.subplot(131)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Image')
plt.xticks([])
plt.yticks([])

# Display the magnitude spectrum as a 2D plot
plt.subplot(132)
plt.imshow(magnitude_spectrum, cmap='gray')
plt.title('Magnitude Spectrum')
plt.xticks([])
plt.yticks([])

plt.tight_layout()
plt.show()

