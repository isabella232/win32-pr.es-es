---
description: La clase Metafile, que hereda de la clase Image, permite grabar una secuencia de comandos de dibujo.
ms.assetid: 062de6c2-9f82-415d-860e-2d1afd2ac027
title: Grabar metaarchivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 129b8fe810b1394921c60540488c93676341c562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984439"
---
# <a name="recording-metafiles"></a><span data-ttu-id="fc3bc-103">Grabar metaarchivos</span><span class="sxs-lookup"><span data-stu-id="fc3bc-103">Recording Metafiles</span></span>

<span data-ttu-id="fc3bc-104">La clase [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) , que hereda de la clase [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , permite grabar una secuencia de comandos de dibujo.</span><span class="sxs-lookup"><span data-stu-id="fc3bc-104">The [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class, which inherits from the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, allows you to record a sequence of drawing commands.</span></span> <span data-ttu-id="fc3bc-105">Los comandos grabados se pueden almacenar en memoria, guardar en un archivo o guardar en una secuencia.</span><span class="sxs-lookup"><span data-stu-id="fc3bc-105">The recorded commands can be stored in memory, saved to a file, or saved to a stream.</span></span> <span data-ttu-id="fc3bc-106">Los metaarchivos pueden contener gráficos vectoriales, imágenes de trama y texto.</span><span class="sxs-lookup"><span data-stu-id="fc3bc-106">Metafiles can contain vector graphics, raster images, and text.</span></span>

<span data-ttu-id="fc3bc-107">En el ejemplo siguiente se crea un objeto de [**metarchivo**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) .</span><span class="sxs-lookup"><span data-stu-id="fc3bc-107">The following example creates a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="fc3bc-108">El código usa el objeto de **metarchivo** para registrar una secuencia de comandos de gráficos y, a continuación, guarda los comandos grabados en un archivo denominado SampleMetafile. EMF.</span><span class="sxs-lookup"><span data-stu-id="fc3bc-108">The code uses the **Metafile** object to record a sequence of graphics commands and then saves the recorded commands in a file named SampleMetafile.emf.</span></span> <span data-ttu-id="fc3bc-109">Tenga en cuenta que el constructor de **metarchivo** recibe un identificador de contexto de dispositivo y el constructor de [**gráficos**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) recibe la dirección del objeto de **metarchivo** .</span><span class="sxs-lookup"><span data-stu-id="fc3bc-109">Note that the **Metafile** constructor receives a device context handle, and the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor receives the address of the **Metafile** object.</span></span> <span data-ttu-id="fc3bc-110">La grabación se detiene (y los comandos grabados se guardan en el archivo) cuando el objeto **gráfico** sale del ámbito.</span><span class="sxs-lookup"><span data-stu-id="fc3bc-110">The recording stops (and the recorded commands are saved to the file) when the **Graphics** object goes out of scope.</span></span> <span data-ttu-id="fc3bc-111">Las dos últimas líneas de código muestran el metarchivo creando un nuevo objeto **Graphics** y pasando la dirección del objeto de **metarchivo** al método **DrawImage** de ese objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="fc3bc-111">The last two lines of code display the metafile by creating a new **Graphics** object and passing the address of the **Metafile** object to the **DrawImage** method of that **Graphics** object.</span></span> <span data-ttu-id="fc3bc-112">Tenga en cuenta que el código utiliza el mismo objeto de **metarchivo** para grabar y mostrar (reproducir) el metarchivo.</span><span class="sxs-lookup"><span data-stu-id="fc3bc-112">Note that the code uses the same **Metafile** object to record and to display (play back) the metafile.</span></span>


```
Metafile metafile(L"SampleMetafile.emf", hdc); 
{
   Graphics graphics(&metafile);
   Pen greenPen(Color(255, 0, 255, 0));
   SolidBrush solidBrush(Color(255, 0, 0, 255));

   // Add a rectangle and an ellipse to the metafile.
   graphics.DrawRectangle(&greenPen, Rect(50, 10, 25, 75));
   graphics.DrawEllipse(&greenPen, Rect(100, 10, 25, 75));

   // Add an ellipse (drawn with antialiasing) to the metafile.
   graphics.SetSmoothingMode(SmoothingModeHighQuality);
   graphics.DrawEllipse(&greenPen, Rect(150, 10, 25, 75));

   // Add some text (drawn with antialiasing) to the metafile.
   FontFamily fontFamily(L"Arial");
   Font font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   
   graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
   graphics.RotateTransform(30.0f);
   graphics.DrawString(L"Smooth Text", 11, &font, 
      PointF(50.0f, 50.0f), &solidBrush);
} // End of recording metafile.

// Play back the metafile.
Graphics playbackGraphics(hdc);
playbackGraphics.DrawImage(&metafile, 200, 100);
```



> [!Note]  
> <span data-ttu-id="fc3bc-113">Para grabar un metarchivo, debe construir un objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) basado en un objeto de [**metarchivo**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) .</span><span class="sxs-lookup"><span data-stu-id="fc3bc-113">To record a metafile, you must construct a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object based on a [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) object.</span></span> <span data-ttu-id="fc3bc-114">La grabación del metarchivo finaliza cuando ese objeto **gráfico** se elimina o sale del ámbito.</span><span class="sxs-lookup"><span data-stu-id="fc3bc-114">The recording of the metafile ends when that **Graphics** object is deleted or goes out of scope.</span></span>

 

<span data-ttu-id="fc3bc-115">Un metarchivo contiene su propio estado de gráficos, que se define mediante el objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) que se usa para grabar el metarchivo.</span><span class="sxs-lookup"><span data-stu-id="fc3bc-115">A metafile contains its own graphics state, which is defined by the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object used to record the metafile.</span></span> <span data-ttu-id="fc3bc-116">Cualquier propiedad del objeto **Graphics** (la región de recorte, la transformación universal, el modo de suavizado y el parecido) que establezca al grabar el metarchivo se almacenará en el metarchivo.</span><span class="sxs-lookup"><span data-stu-id="fc3bc-116">Any properties of the **Graphics** object (clip region, world transformation, smoothing mode, and the like) that you set while recording the metafile will be stored in the metafile.</span></span> <span data-ttu-id="fc3bc-117">Al mostrar el metarchivo, el dibujo se realizará según las propiedades almacenadas.</span><span class="sxs-lookup"><span data-stu-id="fc3bc-117">When you display the metafile, the drawing will be done according to those stored properties.</span></span>

<span data-ttu-id="fc3bc-118">En el ejemplo siguiente, supongamos que el modo de suavizado se estableció en SmoothingModeNormal durante la grabación del metarchivo.</span><span class="sxs-lookup"><span data-stu-id="fc3bc-118">In the following example, assume that the smoothing mode was set to SmoothingModeNormal during the recording of the metafile.</span></span> <span data-ttu-id="fc3bc-119">Aunque el modo de suavizado del objeto de [**gráficos**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) que se usa para la reproducción está establecido en SmoothingModeHighQuality, el metarchivo se reproducirá según la configuración de SmoothingModeNormal.</span><span class="sxs-lookup"><span data-stu-id="fc3bc-119">Even though the smoothing mode of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object used for playback is set to SmoothingModeHighQuality, the metafile will be played according to the SmoothingModeNormal setting.</span></span> <span data-ttu-id="fc3bc-120">Es el modo de suavizado establecido durante la grabación que es importante, no el modo de suavizado establecido antes de la reproducción.</span><span class="sxs-lookup"><span data-stu-id="fc3bc-120">It is the smoothing mode set during the recording that is important, not the smoothing mode set prior to playback.</span></span>


```
graphics.SetSmoothingMode(SmoothingModeHighQuality);
graphics.DrawImage(&meta, 0, 0);
```



 

 



