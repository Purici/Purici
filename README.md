border: none;
    cursor: pointer;
}

form input[type="submit"]:hover {
    background-color: #005599;
}

#gallery img {
    width: 100%;
    max-width: 300px;
    margin: 10px;
}
"""

# Example images
image1_path = '/mnt/data/project/gallery/image1.jpg'
image2_path = '/mnt/data/project/gallery/image2.jpg'
image3_path = '/mnt/data/project/gallery/image3.jpg'

# Create example images
from PIL import Image, ImageDraw

def create_example_image(path, text):
    img = Image.new('RGB', (300, 200), color = (73, 109, 137))
    d = ImageDraw.Draw(img)
    d.text((10,10), text, fill=(255,255,255))
    img.save(path)

create_example_image(image1_path, "Пример работы 1")
create_example_image(image2_path, "Пример работы 2")
create_example_image(image3_path, "Пример работы 3")

# Write files
with open('/mnt/data/project/index.html', 'w', encoding='utf-8') as file:
    file.write(html_content)

with open('/mnt/data/project/styles.css', 'w', encoding='utf-8') as file:
    file.write(css_content)

# Create zip file
zip_path = '/mnt/data/project.zip'
with zipfile.ZipFile(zip_path, 'w') as zipf:
    zipf.write('/mnt/data/project/index.html', 'index.html')
    zipf.write('/mnt/data/project/styles.css', 'styles.css')
    zipf.write(image1_path, 'gallery/image1.jpg')
    zipf.write(image2_path, 'gallery/image2.jpg')
    zipf.write(image3_path, 'gallery/image3.jpg')

zip_path
