---
description: En este tema se proporciona información sobre las consideraciones de seguridad relacionadas con la programación con Windows GDI+.
ms.assetid: 411e16e4-ad8f-4567-8964-564f08283ba5
title: 'Consideraciones de seguridad: GDI+'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d8c9d50393708e58651566ee90adcb4339cb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997449"
---
# <a name="security-considerations-gdi"></a><span data-ttu-id="81de4-103">Consideraciones de seguridad: GDI+</span><span class="sxs-lookup"><span data-stu-id="81de4-103">Security Considerations: GDI+</span></span>

<span data-ttu-id="81de4-104">En este tema se proporciona información sobre las consideraciones de seguridad relacionadas con la programación con Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="81de4-104">This topic provides information about security considerations related to programming with Windows GDI+.</span></span> <span data-ttu-id="81de4-105">En este tema no se proporciona todo lo que necesita saber acerca de los problemas de seguridad, sino que debe usarlo como punto de partida y referencia para esta área tecnológica.</span><span class="sxs-lookup"><span data-stu-id="81de4-105">This topic doesn't provide all you need to know about security issues—instead, use it as a starting point and reference for this technology area.</span></span>

-   [<span data-ttu-id="81de4-106">Comprobando el éxito de los constructores</span><span class="sxs-lookup"><span data-stu-id="81de4-106">Verifying the Success of Constructors</span></span>](#verifying-the-success-of-constructors)
-   [<span data-ttu-id="81de4-107">Asignar búferes</span><span class="sxs-lookup"><span data-stu-id="81de4-107">Allocating Buffers</span></span>](#allocating-buffers)
-   [<span data-ttu-id="81de4-108">Comprobación de errores</span><span class="sxs-lookup"><span data-stu-id="81de4-108">Error Checking</span></span>](#error-checking)
-   [<span data-ttu-id="81de4-109">Sincronización de subprocesos</span><span class="sxs-lookup"><span data-stu-id="81de4-109">Thread Synchronization</span></span>](#thread-synchronization)
-   [<span data-ttu-id="81de4-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="81de4-110">Related topics</span></span>](#related-topics)

## <a name="verifying-the-success-of-constructors"></a><span data-ttu-id="81de4-111">Comprobando el éxito de los constructores</span><span class="sxs-lookup"><span data-stu-id="81de4-111">Verifying the Success of Constructors</span></span>

<span data-ttu-id="81de4-112">Muchas de las clases GDI+ proporcionan un método [**Image:: GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) al que se puede llamar para determinar si los métodos invocados en un objeto son correctos.</span><span class="sxs-lookup"><span data-stu-id="81de4-112">Many of the GDI+ classes provide a [**Image::GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) method that you can call to determine whether methods invoked on an object are successful.</span></span> <span data-ttu-id="81de4-113">También puede llamar a **Image:: GetLastStatus** para determinar si un constructor se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="81de4-113">You can also call **Image::GetLastStatus** to determine whether a constructor is successful.</span></span>

<span data-ttu-id="81de4-114">En el ejemplo siguiente se muestra cómo construir un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) y llamar al método [**Image:: GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) para determinar si el constructor fue correcto.</span><span class="sxs-lookup"><span data-stu-id="81de4-114">The following example shows how to construct an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and call the [**Image::GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) method to determine whether the constructor was successful.</span></span> <span data-ttu-id="81de4-115">Los valores **OK** y **InvalidParameter** son elementos de la enumeración [**status**](/windows/desktop/api/Gdiplustypes/ne-gdiplustypes-status) .</span><span class="sxs-lookup"><span data-stu-id="81de4-115">The values **Ok** and **InvalidParameter** are elements of the [**Status**](/windows/desktop/api/Gdiplustypes/ne-gdiplustypes-status) enumeration.</span></span>


```C++
Image myImage(L"Climber.jpg");
Status st = myImage.GetLastStatus();

if(Ok == st)
   // The constructor was successful. Use myImage.
else if(InvalidParameter == st)
   // The constructor failed because of an invalid parameter.
else
   // Compare st to other elements of the Status 
   // enumeration or do general error processing.
```



## <a name="allocating-buffers"></a><span data-ttu-id="81de4-116">Asignar búferes</span><span class="sxs-lookup"><span data-stu-id="81de4-116">Allocating Buffers</span></span>

<span data-ttu-id="81de4-117">Varios métodos de GDI+ devuelven datos numéricos o de caracteres en un búfer asignado por el llamador.</span><span class="sxs-lookup"><span data-stu-id="81de4-117">Several GDI+ methods return numeric or character data in a buffer that is allocated by the caller.</span></span> <span data-ttu-id="81de4-118">Para cada uno de esos métodos, hay un método complementario que proporciona el tamaño del búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="81de4-118">For each of those methods, there is a companion method that gives the size of the required buffer.</span></span> <span data-ttu-id="81de4-119">Por ejemplo, el método [**GraphicsPath:: GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) devuelve una matriz de objetos [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) .</span><span class="sxs-lookup"><span data-stu-id="81de4-119">For example, the [**GraphicsPath::GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) method returns an array of [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) objects.</span></span> <span data-ttu-id="81de4-120">Antes de llamar a **GraphicsPath:: GetPathPoints**, debe asignar un búfer lo suficientemente grande como para contener esa matriz.</span><span class="sxs-lookup"><span data-stu-id="81de4-120">Before you call **GraphicsPath::GetPathPoints**, you must allocate a buffer large enough to hold that array.</span></span> <span data-ttu-id="81de4-121">Puede determinar el tamaño del búfer necesario llamando al método [**GraphicsPath:: GetPointCount**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-getpointcount) de un objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) .</span><span class="sxs-lookup"><span data-stu-id="81de4-121">You can determine the size of the required buffer by calling the [**GraphicsPath::GetPointCount**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-getpointcount) method of a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span>

<span data-ttu-id="81de4-122">En el ejemplo siguiente se muestra cómo determinar el número de puntos de un objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) , asignar un búfer lo suficientemente grande como para albergar muchos puntos y, a continuación, llamar a [**GraphicsPath:: GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) para rellenar el búfer.</span><span class="sxs-lookup"><span data-stu-id="81de4-122">The following example shows how to determine the number of points in a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object, allocate a buffer large enough to hold that many points, and then call [**GraphicsPath::GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) to fill the buffer.</span></span> <span data-ttu-id="81de4-123">Antes de que el código llame a **GraphicsPath:: GetPathPoints**, comprueba que la asignación de búfer se realizó correctamente asegurándose de que el puntero de búfer no es **null**.</span><span class="sxs-lookup"><span data-stu-id="81de4-123">Before the code calls **GraphicsPath::GetPathPoints**, it verifies that the buffer allocation was successful by making sure that the buffer pointer is not **NULL**.</span></span>


```C++
GraphicsPath path;
path.AddEllipse(10, 10, 200, 100);

INT count = path.GetPointCount();          // get the size
Point* pointArray = new Point[count];      // allocate the buffer

if(pointArray)  // Check for successful allocation.
{
   path.GetPathPoints(pointArray, count);  // get the data
   ...                                     // use pointArray
   delete[] pointArray;                    // release the buffer
   pointArray = NULL;
}
```



<span data-ttu-id="81de4-124">En el ejemplo anterior se usa el operador New para asignar un búfer.</span><span class="sxs-lookup"><span data-stu-id="81de4-124">The previous example uses the new operator to allocate a buffer.</span></span> <span data-ttu-id="81de4-125">El operador new era práctico porque el búfer se rellenó con un número conocido de objetos de [**punto**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) .</span><span class="sxs-lookup"><span data-stu-id="81de4-125">The new operator was convenient because the buffer was filled with a known number of [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) objects.</span></span> <span data-ttu-id="81de4-126">En algunos casos, GDI+ escribe más en el búfer que una matriz de objetos GDI+.</span><span class="sxs-lookup"><span data-stu-id="81de4-126">In some cases, GDI+ writes more into buffer than an array of GDI+ objects.</span></span> <span data-ttu-id="81de4-127">A veces, un búfer se rellena con una matriz de objetos GDI+ junto con datos adicionales a los que apuntan los miembros de esos objetos.</span><span class="sxs-lookup"><span data-stu-id="81de4-127">Sometimes a buffer is filled with an array of GDI+ objects along with additional data that is pointed to by members of those objects.</span></span> <span data-ttu-id="81de4-128">Por ejemplo, el método [**Image:: GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) devuelve una matriz de objetos [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) , uno para cada elemento de propiedad (fragmento de metadatos) almacenado en la imagen.</span><span class="sxs-lookup"><span data-stu-id="81de4-128">For example, the [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) method returns an array of [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) objects, one for each property item (piece of metadata) stored in the image.</span></span> <span data-ttu-id="81de4-129">Pero **Image:: GetAllPropertyItems** devuelve más que simplemente la matriz de objetos **PropertyItem** ; anexa la matriz con datos adicionales.</span><span class="sxs-lookup"><span data-stu-id="81de4-129">But **Image::GetAllPropertyItems** returns more than just the array of **PropertyItem** objects; it appends the array with additional data.</span></span>

<span data-ttu-id="81de4-130">Antes de llamar a [**Image:: GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems), debe asignar un búfer lo suficientemente grande como para contener la matriz de objetos [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) junto con los datos adicionales.</span><span class="sxs-lookup"><span data-stu-id="81de4-130">Before you call [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems), you must allocate a buffer large enough to hold the array of [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) objects along with the additional data.</span></span> <span data-ttu-id="81de4-131">Puede llamar al método [**Image:: GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) de un objeto Image para determinar el tamaño total del búfer requerido.</span><span class="sxs-lookup"><span data-stu-id="81de4-131">You can call the [**Image::GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) method of an Image object to determine the total size of the required buffer.</span></span>

<span data-ttu-id="81de4-132">En el ejemplo siguiente se muestra cómo crear un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) y después llamar al método [**Image:: GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) de ese objeto de **imagen** para recuperar todos los elementos de propiedad (metadatos) almacenados en la imagen.</span><span class="sxs-lookup"><span data-stu-id="81de4-132">The following example shows how to create an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and later call the [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) method of that **Image** object to retrieve all the property items (metadata) stored in the image.</span></span> <span data-ttu-id="81de4-133">El código asigna un búfer basado en un valor de tamaño devuelto por el método [**Image:: GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) .</span><span class="sxs-lookup"><span data-stu-id="81de4-133">The code allocates a buffer based on a size value returned by the [**Image::GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) method.</span></span> <span data-ttu-id="81de4-134">**Image:: GetPropertySize** también devuelve un valor de recuento que proporciona el número de elementos de propiedad de la imagen.</span><span class="sxs-lookup"><span data-stu-id="81de4-134">**Image::GetPropertySize** also returns a count value that gives the number of property items in the image.</span></span> <span data-ttu-id="81de4-135">Observe que el código no calcula el tamaño del búfer como `count*sizeof(PropertyItem)` .</span><span class="sxs-lookup"><span data-stu-id="81de4-135">Notice that the code does not calculate the buffer size as `count*sizeof(PropertyItem)`.</span></span> <span data-ttu-id="81de4-136">Un búfer calculado de esta manera sería demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="81de4-136">A buffer calculated that way would be too small.</span></span>


```C++
UINT count = 0;
UINT size = 0;
Image myImage(L"FakePhoto.jpg");
myImage.GetPropertySize(&size, &count);

// GetAllPropertyItems returns an array of PropertyItem objects
// along with additional data. Allocate a buffer large enough to 
// receive the array and the additional data.
PropertyItem* propBuffer =(PropertyItem*)malloc(size);

if(propBuffer)
{
   myImage.GetAllPropertyItems(size, count, propBuffer);
   ...
   free(propBuffer);
   propBuffer = NULL;
}
```



## <a name="error-checking"></a><span data-ttu-id="81de4-137">Comprobación de errores</span><span class="sxs-lookup"><span data-stu-id="81de4-137">Error Checking</span></span>

<span data-ttu-id="81de4-138">La mayoría de los ejemplos de código de la documentación de GDI+ no muestran la comprobación de errores.</span><span class="sxs-lookup"><span data-stu-id="81de4-138">Most of the code examples in the GDI+ documentation do not show error checking.</span></span> <span data-ttu-id="81de4-139">La comprobación de errores completa es mucho más larga y puede ocultar el punto que se muestra en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="81de4-139">Complete error checking makes a code example much longer and can obscure the point being illustrated by the example.</span></span> <span data-ttu-id="81de4-140">No debe pegar los ejemplos de la documentación directamente en el código de producción. en su lugar, debe mejorar los ejemplos agregando su propia comprobación de errores.</span><span class="sxs-lookup"><span data-stu-id="81de4-140">You should not paste examples from the documentation directly into production code; rather, you should enhance the examples by adding your own error checking.</span></span>

<span data-ttu-id="81de4-141">En el ejemplo siguiente se muestra una manera de implementar la comprobación de errores con GDI+.</span><span class="sxs-lookup"><span data-stu-id="81de4-141">The following example shows one way of implementing error checking with GDI+.</span></span> <span data-ttu-id="81de4-142">Cada vez que se construye un objeto GDI+, el código comprueba para ver si el constructor se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="81de4-142">Each time a GDI+ object is constructed, the code checks to see whether the constructor was successful.</span></span> <span data-ttu-id="81de4-143">Esta comprobación es especialmente importante para el constructor de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , que se basa en leer un archivo.</span><span class="sxs-lookup"><span data-stu-id="81de4-143">That check is especially important for the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) constructor, which relies on reading a file.</span></span> <span data-ttu-id="81de4-144">Si los cuatro objetos GDI+ ([**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath), **Image** y [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)) se construyen correctamente, el código llama a los métodos en esos objetos.</span><span class="sxs-lookup"><span data-stu-id="81de4-144">If all four of the GDI+ objects ([**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath), **Image**, and [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)) are constructed successfully, the code calls methods on those objects.</span></span> <span data-ttu-id="81de4-145">Se comprueba si se ha realizado correctamente cada llamada al método y, en caso de error, se omiten las llamadas de método restantes.</span><span class="sxs-lookup"><span data-stu-id="81de4-145">Each method call is checked for success, and in the event of failure, the remaining method calls are skipped.</span></span>


```C++
Status GdipExample(HDC hdc)
{
   Status status = GenericError;
   INT count = 0;
   Point* points = NULL;

   Graphics graphics(hdc);
   status = graphics.GetLastStatus();
   if(Ok != status)
      return status;

   GraphicsPath path;
   status = path.GetLastStatus();
   if(Ok != status)
      return status;

   Image image(L"MyTexture.bmp");
   status = image.GetLastStatus();
   if(Ok != status)
      return status;

   TextureBrush brush(&image);
   status = brush.GetLastStatus();
   if(Ok != status)
      return status;

   status = path.AddEllipse(10, 10, 200, 100);

   if(Ok == status)
   {
      status = path.AddBezier(40, 130, 200, 130, 200, 200, 60, 200);
   }
  
   if(Ok == status)
   {
      count = path.GetPointCount();
      status = path.GetLastStatus();
   }

   if(Ok == status)
   {
      points = new Point[count];

      if(NULL == points)
         status = OutOfMemory;
   }

   if(Ok == status)
   {
      status = path.GetPathPoints(points, count);  
   }
  
   if(Ok == status)
   {
      status = graphics.FillPath(&brush, &path);
   }
   
   if(Ok == status)
   {
      for(int j = 0; j < count; ++j)
      {
         status = graphics.FillEllipse(
         &brush, points[j].X - 5, points[j].Y - 5, 10, 10);
      }
   }

   if(points)
   {
      delete[] points;
      points = NULL;
   }

   return status;
}
```



## <a name="thread-synchronization"></a><span data-ttu-id="81de4-146">Sincronización de subprocesos</span><span class="sxs-lookup"><span data-stu-id="81de4-146">Thread Synchronization</span></span>

<span data-ttu-id="81de4-147">Es posible que más de un subproceso tenga acceso a un solo objeto GDI+.</span><span class="sxs-lookup"><span data-stu-id="81de4-147">It is possible for more than one thread to have access to a single GDI+ object.</span></span> <span data-ttu-id="81de4-148">Sin embargo, GDI+ no proporciona ningún mecanismo de sincronización automática.</span><span class="sxs-lookup"><span data-stu-id="81de4-148">However, GDI+ does not provide any automatic synchronization mechanism.</span></span> <span data-ttu-id="81de4-149">Por tanto, si dos subprocesos de la aplicación tienen un puntero al mismo objeto GDI+, es responsabilidad suya sincronizar el acceso a ese objeto.</span><span class="sxs-lookup"><span data-stu-id="81de4-149">So if two threads in your application have a pointer to the same GDI+ object, it is your responsibility to synchronize access to that object.</span></span>

<span data-ttu-id="81de4-150">Algunos métodos de GDI+ devuelven **ObjectBusy** si un subproceso intenta llamar a un método mientras otro subproceso está ejecutando un método en el mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="81de4-150">Some GDI+ methods return **ObjectBusy** if a thread attempts to call a method while another thread is executing a method on the same object.</span></span> <span data-ttu-id="81de4-151">No intente sincronizar el acceso a un objeto basado en el valor devuelto de **ObjectBusy** .</span><span class="sxs-lookup"><span data-stu-id="81de4-151">Do not try to synchronize access to an object based on the **ObjectBusy** return value.</span></span> <span data-ttu-id="81de4-152">En su lugar, cada vez que se accede a un miembro o se llama a un método del objeto, se coloca la llamada dentro de una sección crítica o se usa otra técnica de sincronización estándar.</span><span class="sxs-lookup"><span data-stu-id="81de4-152">Instead, each time you access a member or call a method of the object, place the call inside a critical section, or use some other standard synchronization technique.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81de4-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="81de4-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81de4-154">Centro para desarrolladores de software de seguridad de MSDN</span><span class="sxs-lookup"><span data-stu-id="81de4-154">MSDN Security Developer Center</span></span>](https://msdn.microsoft.com/security/)
</dt> <dt>

<span data-ttu-id="81de4-155">[Recursos de How-To de seguridad](/previous-versions/msp-n-p/ff650055(v=pandp.10))</span><span class="sxs-lookup"><span data-stu-id="81de4-155">[Security How-To Resources](/previous-versions/msp-n-p/ff650055(v=pandp.10))</span></span>
</dt> <dt>

[<span data-ttu-id="81de4-156">Security Center TechNet</span><span class="sxs-lookup"><span data-stu-id="81de4-156">TechNet Security Center</span></span>](https://technet.microsoft.com/security/)
</dt> </dl>

 

 
