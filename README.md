# 🎨 GPT Image 1 Mask Generator

A simple, interactive **mask generator** for image editing with OpenAI's **GPT Image 1 API**.  
This tool allows you to upload an image, draw over regions you want to edit, and download a compatible mask file.

---

## 🚀 Features

- **Image Upload** – Click or drag & drop to upload your image.
- **Drawing & Erasing** – Switch between brush and eraser modes.
- **Custom Brush Settings** – Adjust size, opacity, and color.
- **Two API Modes**:
  - **GPT Image 1 Mode** – Transparent = editable, White = protected (with alpha channel).
  - **Standard Mode** – Black = protected, White = editable.
- **Clear / Fill / Download** – Easy controls to manage your mask.
- **Mobile-Friendly** – Works on both desktop and mobile devices.

---

## 📸 Screenshots

![Screenshot](screenshot.png)  
*(Optional – Add your own screenshot)*

---

## 🛠 How to Use

1. **Upload an image** by clicking the upload area or dragging & dropping a file.
2. **Draw** over the areas you want to edit.
3. **Adjust** brush size, opacity, and color as needed.
4. **Switch modes** between GPT Image 1 and Standard Mode depending on your use case.
5. **Download the mask** and use it with:
   ```python
   client.images.edit(
       model="gpt-image-1",
       image=open("your_image.png", "rb"),
       mask=open("gpt-image-mask.png", "rb"),
       prompt="Describe your edit"
   )
