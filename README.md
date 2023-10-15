import cv2

def enhance_photo(image_path):
    # Load the image
    image = cv2.imread(image_path)

    # Increase contrast and brightness
    alpha = 1.5  # Contrast control (1.0-3.0)
    beta = 50  # Brightness control (0-100)
    enhanced_image = cv2.convertScaleAbs(image, alpha=alpha, beta=beta)

    # Display the original and enhanced images
    cv2.imshow("Original Image", image)
    cv2.imshow("Enhanced Image", enhanced_image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

# Specify the path of the image you want to enhance
image_path = "path/to/your/image.jpg"

# Call the function to enhance the photo
enhance_photo(image_path)
