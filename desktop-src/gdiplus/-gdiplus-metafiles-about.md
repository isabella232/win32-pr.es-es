---
description: Windows GDI+ proporciona la clase Metafile para que pueda grabar y mostrar metarchivos.
ms.assetid: a9f9bac4-f3c7-44a1-9f0f-59ff1a27b077
title: Metaarchivos (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae75c2185670563f9a9e624d868da5b0e299cbec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360280"
---
# <a name="metafiles-gdi"></a><span data-ttu-id="2d78b-103">Metaarchivos (GDI+)</span><span class="sxs-lookup"><span data-stu-id="2d78b-103">Metafiles (GDI+)</span></span>

<span data-ttu-id="2d78b-104">Windows GDI+ proporciona la clase Metafile para que pueda grabar y mostrar [**metarchivos**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) .</span><span class="sxs-lookup"><span data-stu-id="2d78b-104">Windows GDI+ provides the [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class so that you can record and display metafiles.</span></span> <span data-ttu-id="2d78b-105">Un metarchivo, también denominado imagen vectorial, es una imagen que se almacena como una secuencia de comandos y valores de dibujo.</span><span class="sxs-lookup"><span data-stu-id="2d78b-105">A metafile, also called a vector image, is an image that is stored as a sequence of drawing commands and settings.</span></span> <span data-ttu-id="2d78b-106">Los comandos y la configuración registrados en un objeto de **metarchivo** se pueden almacenar en memoria o guardar en un archivo o una secuencia.</span><span class="sxs-lookup"><span data-stu-id="2d78b-106">The commands and settings recorded in a **Metafile** object can be stored in memory or saved to a file or stream.</span></span>

<span data-ttu-id="2d78b-107">GDI+ puede mostrar los metaarchivos que se han almacenado en los formatos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2d78b-107">GDI+ can display metafiles that have been stored in the following formats:</span></span>

-   <span data-ttu-id="2d78b-108">Formato WMF (WMF)</span><span class="sxs-lookup"><span data-stu-id="2d78b-108">Windows Metafile Format (WMF)</span></span>
-   <span data-ttu-id="2d78b-109">Metarchivo mejorado (EMF)</span><span class="sxs-lookup"><span data-stu-id="2d78b-109">Enhanced Metafile (EMF)</span></span>
-   <span data-ttu-id="2d78b-110">EMF +</span><span class="sxs-lookup"><span data-stu-id="2d78b-110">EMF+</span></span>

<span data-ttu-id="2d78b-111">GDI+ puede grabar metaarchivos en los formatos EMF y EMF +, pero no en formato WMF.</span><span class="sxs-lookup"><span data-stu-id="2d78b-111">GDI+ can record metafiles in the EMF and EMF+ formats, but not in the WMF format.</span></span>

<span data-ttu-id="2d78b-112">EMF + es una extensión de EMF que permite almacenar registros GDI+.</span><span class="sxs-lookup"><span data-stu-id="2d78b-112">EMF+ is an extension to EMF that allows GDI+ records to be stored.</span></span> <span data-ttu-id="2d78b-113">Hay dos variaciones en el formato EMF +: EMF + only y EMF + dual.</span><span class="sxs-lookup"><span data-stu-id="2d78b-113">There are two variations on the EMF+ format: EMF+ Only and EMF+ Dual.</span></span> <span data-ttu-id="2d78b-114">Los metaarchivos EMF + Only solo contienen registros GDI+.</span><span class="sxs-lookup"><span data-stu-id="2d78b-114">EMF+ Only metafiles contain only GDI+ records.</span></span> <span data-ttu-id="2d78b-115">Estos metaarchivos se pueden mostrar en GDI+, pero no en Windows Interfaz de dispositivo gráfico (GDI).</span><span class="sxs-lookup"><span data-stu-id="2d78b-115">Such metafiles can be displayed by GDI+ but not by Windows Graphics Device Interface (GDI).</span></span> <span data-ttu-id="2d78b-116">Los metaarchivos EMF + dual contienen registros GDI+ y GDI.</span><span class="sxs-lookup"><span data-stu-id="2d78b-116">EMF+ Dual metafiles contain GDI+ and GDI records.</span></span> <span data-ttu-id="2d78b-117">Cada registro de GDI+ de un metarchivo EMF + dual se empareja con un registro GDI alternativo.</span><span class="sxs-lookup"><span data-stu-id="2d78b-117">Each GDI+ record in an EMF+ Dual metafile is paired with an alternate GDI record.</span></span> <span data-ttu-id="2d78b-118">Estos metaarchivos se pueden mostrar en GDI+ o en GDI.</span><span class="sxs-lookup"><span data-stu-id="2d78b-118">Such metafiles can be displayed by GDI+ or by GDI.</span></span>

<span data-ttu-id="2d78b-119">En el ejemplo siguiente se registra una configuración y un comando de dibujo en un archivo de disco.</span><span class="sxs-lookup"><span data-stu-id="2d78b-119">The following example records one setting and one drawing command in a disk file.</span></span> <span data-ttu-id="2d78b-120">Tenga en cuenta que en el ejemplo se crea un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y que el constructor del objeto **Graphics** recibe la dirección de un objeto de [**metarchivo**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) como argumento.</span><span class="sxs-lookup"><span data-stu-id="2d78b-120">Note that the example creates a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and that the constructor for the **Graphics** object receives the address of a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object as an argument.</span></span>


```
myMetafile = new Metafile(L"MyDiskFile.emf", hdc);
myGraphics = new Graphics(myMetafile);
   myPen = new Pen(Color(255, 0, 0, 200));
   myGraphics->SetSmoothingMode(SmoothingModeAntiAlias);
   myGraphics->DrawLine(myPen, 0, 0, 60, 40);
delete myGraphics;
delete myPen;
delete myMetafile;
```



<span data-ttu-id="2d78b-121">Como se muestra en el ejemplo anterior, la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) es la clave para registrar instrucciones y configuraciones en un objeto de [**metarchivo**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) .</span><span class="sxs-lookup"><span data-stu-id="2d78b-121">As the preceding example shows, the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class is the key to recording instructions and settings in a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="2d78b-122">Cualquier llamada realizada a un método de un objeto **Graphics** se puede grabar en un objeto de **metarchivo** .</span><span class="sxs-lookup"><span data-stu-id="2d78b-122">Any call made to a method of a **Graphics** object can be recorded in a **Metafile** object.</span></span> <span data-ttu-id="2d78b-123">Del mismo modo, puede establecer cualquier propiedad de un objeto **Graphics** y grabar esa configuración en un objeto de **metarchivo** .</span><span class="sxs-lookup"><span data-stu-id="2d78b-123">Likewise, you can set any property of a **Graphics** object and record that setting in a **Metafile** object.</span></span> <span data-ttu-id="2d78b-124">La grabación finaliza cuando el objeto **Graphics** se elimina o sale del ámbito.</span><span class="sxs-lookup"><span data-stu-id="2d78b-124">The recording ends when the **Graphics** object is deleted or goes out of scope.</span></span>

<span data-ttu-id="2d78b-125">En el ejemplo siguiente se muestra el metarchivo creado en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="2d78b-125">The following example displays the metafile created in the preceding example.</span></span> <span data-ttu-id="2d78b-126">El metarchivo se muestra con la esquina superior izquierda en (100, 100).</span><span class="sxs-lookup"><span data-stu-id="2d78b-126">The metafile is displayed with its upper-left corner at (100, 100).</span></span>


```
Graphics myGraphics(hdc);
Image myImage(L"MyDiskFile.emf");
myGraphics.DrawImage(&myImage, 100, 100);
```



<span data-ttu-id="2d78b-127">En el ejemplo siguiente se registran varios valores de propiedades (región de recorte, transformación universal y modo de suavizado) en un objeto de [**metarchivo**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) .</span><span class="sxs-lookup"><span data-stu-id="2d78b-127">The following example records several property settings (clipping region, world transformation, and smoothing mode) in a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="2d78b-128">Después, el código registra varias instrucciones de dibujo.</span><span class="sxs-lookup"><span data-stu-id="2d78b-128">Then the code records several drawing instructions.</span></span> <span data-ttu-id="2d78b-129">Las instrucciones y la configuración se guardan en un archivo de disco.</span><span class="sxs-lookup"><span data-stu-id="2d78b-129">The instructions and settings are saved in a disk file.</span></span>


```
myMetafile = new Metafile(L"MyDiskFile2.emf", hdc); 
myGraphics = new Graphics(myMetafile);
   myGraphics->SetSmoothingMode(SmoothingModeAntiAlias);
   myGraphics->RotateTransform(30);

   // Create an elliptical clipping region.
   GraphicsPath myPath;
   myPath.AddEllipse(0, 0, 200, 100);
   Region myRegion(&myPath);
   myGraphics->SetClip(&myRegion);

   Pen myPen(Color(255, 0, 0, 255));
   myGraphics->DrawPath(&myPen, &myPath);

   for(INT j = 0; j <= 300; j += 10)
   {
      myGraphics->DrawLine(&myPen, 0, 0, 300 - j, j);
   }
delete myGraphics;
delete myMetafile;
```



<span data-ttu-id="2d78b-130">En el ejemplo siguiente se muestra la imagen de metarchivo creada en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="2d78b-130">The following example displays the metafile image created in the preceding example.</span></span>


```
myGraphics = new Graphics(hdc);
myMetafile = new Metafile(L"MyDiskFile.emf");
myGraphics->DrawImage(myMetafile, 10, 10);
```



<span data-ttu-id="2d78b-131">En la ilustración siguiente se muestra la salida del código anterior.</span><span class="sxs-lookup"><span data-stu-id="2d78b-131">The following illustration shows the output of the preceding code.</span></span> <span data-ttu-id="2d78b-132">Observe el suavizado de contorno, la región de recorte elíptica y la rotación de 30 grados.</span><span class="sxs-lookup"><span data-stu-id="2d78b-132">Note the antialiasing, the elliptical clipping region, and the 30-degree rotation.</span></span>

![captura de pantalla de una ventana que contiene una elipse rellena con líneas que se originan en un punto fuera de la elipse](images/aboutgdip05-art00.png)

 

 



