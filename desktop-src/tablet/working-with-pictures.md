---
description: En este tema se describe cómo ajustar imágenes mediante la propiedad System. Windows. Forms. PictureBox. SizeMode y cómo mostrar imágenes en Microsoft Visual Studio .NET.
ms.assetid: 9f4f0f96-68a3-447d-a239-599c9fd3e343
title: Trabajar con imágenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3a90c0d18253eaf4aea60eafc48bd1c24fcc3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696593"
---
# <a name="working-with-pictures"></a><span data-ttu-id="f5bfa-103">Trabajar con imágenes</span><span class="sxs-lookup"><span data-stu-id="f5bfa-103">Working with Pictures</span></span>

<span data-ttu-id="f5bfa-104">En este tema se describe cómo ajustar imágenes mediante la propiedad [System. Windows. Forms. PictureBox. SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) y cómo mostrar imágenes en Microsoft Visual Studio .net.</span><span class="sxs-lookup"><span data-stu-id="f5bfa-104">This topic describes how to adjust pictures using the [System.Windows.Forms.PictureBox.SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) property, and how to display pictures in Microsoft Visual Studio .NET.</span></span>

## <a name="the-sizemode-property"></a><span data-ttu-id="f5bfa-105">La propiedad SizeMode</span><span class="sxs-lookup"><span data-stu-id="f5bfa-105">The SizeMode Property</span></span>

<span data-ttu-id="f5bfa-106">Puede especificar cómo encaja una imagen en el control con la propiedad [SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="f5bfa-106">You can specify how an image fits in the control with the [SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) property.</span></span> <span data-ttu-id="f5bfa-107">La propiedad SizeMode está disponible en la biblioteca administrada y en la biblioteca de Automation.</span><span class="sxs-lookup"><span data-stu-id="f5bfa-107">The SizeMode property is available in both the Managed Library and in the Automation Library.</span></span> <span data-ttu-id="f5bfa-108">Con SizeMode puede:</span><span class="sxs-lookup"><span data-stu-id="f5bfa-108">With SizeMode you can:</span></span>

-   <span data-ttu-id="f5bfa-109">Cambiar el tamaño de los bordes del control para ajustarse a una imagen.</span><span class="sxs-lookup"><span data-stu-id="f5bfa-109">Resize the control borders to fit an image.</span></span>
-   <span data-ttu-id="f5bfa-110">Estire una imagen para ajustarla a los bordes del control.</span><span class="sxs-lookup"><span data-stu-id="f5bfa-110">Stretch an image to fit the control borders.</span></span>
-   <span data-ttu-id="f5bfa-111">Centrar una imagen dentro de los bordes del control.</span><span class="sxs-lookup"><span data-stu-id="f5bfa-111">Center an image within the control borders.</span></span>
-   <span data-ttu-id="f5bfa-112">Anclar una imagen en el área superior izquierda del control sin cambiar el tamaño de la imagen o el control (es posible que parte de la imagen no sea visible si no se cambia el tamaño de la imagen o el control).</span><span class="sxs-lookup"><span data-stu-id="f5bfa-112">Anchor an image to the upper-left area of the control without resizing the image or control (some of the image may not be viewable if you do not resize the image or control).</span></span>

## <a name="working-with-pictures-in-visual-studio-net"></a><span data-ttu-id="f5bfa-113">Trabajar con imágenes en Visual Studio .NET</span><span class="sxs-lookup"><span data-stu-id="f5bfa-113">Working with Pictures in Visual Studio .NET</span></span>

<span data-ttu-id="f5bfa-114">Para mostrar una imagen en tiempo de diseño en Visual Studio .NET:</span><span class="sxs-lookup"><span data-stu-id="f5bfa-114">To display an image at design time in Visual Studio .NET:</span></span>

1.  <span data-ttu-id="f5bfa-115">Arrastre un control [InkPicture](/previous-versions/aa514604(v=msdn.10)) en un formulario o haga doble clic en el control InkPicture en el cuadro de herramientas.</span><span class="sxs-lookup"><span data-stu-id="f5bfa-115">Drag an [InkPicture](/previous-versions/aa514604(v=msdn.10)) control on a form, or double-click the InkPicture control in the Toolbox.</span></span>
2.  <span data-ttu-id="f5bfa-116">En la ventana **propiedades** , seleccione la propiedad **imagen** y, a continuación, haga clic en el botón de puntos suspensivos para abrir el cuadro de diálogo **abrir** .</span><span class="sxs-lookup"><span data-stu-id="f5bfa-116">In the **Properties** window, select the **Image** property, and then click the ellipsis button to open the **Open** dialog box.</span></span>
3.  <span data-ttu-id="f5bfa-117">Si busca un tipo de archivo específico (por ejemplo, archivos. jpg), selecciónelo en el cuadro **archivos de tipo** .</span><span class="sxs-lookup"><span data-stu-id="f5bfa-117">If you are looking for a specific file type (for example, .jpg files), select it in the **Files of type** box.</span></span>
4.  <span data-ttu-id="f5bfa-118">Seleccione el archivo que desea mostrar.</span><span class="sxs-lookup"><span data-stu-id="f5bfa-118">Select the file you want to display.</span></span>

<span data-ttu-id="f5bfa-119">Para borrar la imagen en tiempo de diseño:</span><span class="sxs-lookup"><span data-stu-id="f5bfa-119">To clear the picture at design time:</span></span>

1.  <span data-ttu-id="f5bfa-120">En la ventana **propiedades** , seleccione la propiedad **imagen** y haga clic con el botón secundario en la imagen en miniatura.</span><span class="sxs-lookup"><span data-stu-id="f5bfa-120">In the **Properties** window, select the **Image** property and right-click the thumbnail image.</span></span>
2.  <span data-ttu-id="f5bfa-121">Haga clic en **Restablecer**.</span><span class="sxs-lookup"><span data-stu-id="f5bfa-121">Click **Reset**.</span></span>

<span data-ttu-id="f5bfa-122">El control [InkPicture](/previous-versions/aa514604(v=msdn.10)) se muestra de forma predeterminada sin ningún borde.</span><span class="sxs-lookup"><span data-stu-id="f5bfa-122">The [InkPicture](/previous-versions/aa514604(v=msdn.10)) control is displayed by default without any borders.</span></span> <span data-ttu-id="f5bfa-123">Puede proporcionar un borde estándar o tridimensional mediante la propiedad [BorderStyle](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) para distinguir el cuadro InkPicture del resto del formulario, aunque no contenga ninguna imagen.</span><span class="sxs-lookup"><span data-stu-id="f5bfa-123">You can provide a standard or three-dimensional border using the [BorderStyle](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) property to distinguish the InkPicture box from the rest of the form, even if it contains no image.</span></span>

<span data-ttu-id="f5bfa-124">Puede mostrar una imagen en tiempo de ejecución con el método [FromFile](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) del objeto [System. Drawing. Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) :</span><span class="sxs-lookup"><span data-stu-id="f5bfa-124">You can display an image at run time with the [System.Drawing.Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) object's [FromFile](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) method:</span></span>


```C++
ctlInkPicture.Image = Image.FromFile("c:\myImageFile")
```



<span data-ttu-id="f5bfa-125">También puede incluir una imagen de fondo con la propiedad [BackgroundImage](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) del objeto de [imagen](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) heredado. sin embargo, no se puede cambiar el tamaño de esa imagen.</span><span class="sxs-lookup"><span data-stu-id="f5bfa-125">You can also include a background image with the inherited [Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) object's [BackgroundImage](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) property; however, that image cannot be resized.</span></span>

 

 
