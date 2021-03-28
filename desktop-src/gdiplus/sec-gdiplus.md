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
# <a name="security-considerations-gdi"></a>Consideraciones de seguridad: GDI+

En este tema se proporciona información sobre las consideraciones de seguridad relacionadas con la programación con Windows GDI+. En este tema no se proporciona todo lo que necesita saber acerca de los problemas de seguridad, sino que debe usarlo como punto de partida y referencia para esta área tecnológica.

-   [Comprobando el éxito de los constructores](#verifying-the-success-of-constructors)
-   [Asignar búferes](#allocating-buffers)
-   [Comprobación de errores](#error-checking)
-   [Sincronización de subprocesos](#thread-synchronization)
-   [Temas relacionados](#related-topics)

## <a name="verifying-the-success-of-constructors"></a>Comprobando el éxito de los constructores

Muchas de las clases GDI+ proporcionan un método [**Image:: GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) al que se puede llamar para determinar si los métodos invocados en un objeto son correctos. También puede llamar a **Image:: GetLastStatus** para determinar si un constructor se realiza correctamente.

En el ejemplo siguiente se muestra cómo construir un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) y llamar al método [**Image:: GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) para determinar si el constructor fue correcto. Los valores **OK** y **InvalidParameter** son elementos de la enumeración [**status**](/windows/desktop/api/Gdiplustypes/ne-gdiplustypes-status) .


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



## <a name="allocating-buffers"></a>Asignar búferes

Varios métodos de GDI+ devuelven datos numéricos o de caracteres en un búfer asignado por el llamador. Para cada uno de esos métodos, hay un método complementario que proporciona el tamaño del búfer necesario. Por ejemplo, el método [**GraphicsPath:: GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) devuelve una matriz de objetos [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) . Antes de llamar a **GraphicsPath:: GetPathPoints**, debe asignar un búfer lo suficientemente grande como para contener esa matriz. Puede determinar el tamaño del búfer necesario llamando al método [**GraphicsPath:: GetPointCount**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-getpointcount) de un objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) .

En el ejemplo siguiente se muestra cómo determinar el número de puntos de un objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) , asignar un búfer lo suficientemente grande como para albergar muchos puntos y, a continuación, llamar a [**GraphicsPath:: GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) para rellenar el búfer. Antes de que el código llame a **GraphicsPath:: GetPathPoints**, comprueba que la asignación de búfer se realizó correctamente asegurándose de que el puntero de búfer no es **null**.


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



En el ejemplo anterior se usa el operador New para asignar un búfer. El operador new era práctico porque el búfer se rellenó con un número conocido de objetos de [**punto**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) . En algunos casos, GDI+ escribe más en el búfer que una matriz de objetos GDI+. A veces, un búfer se rellena con una matriz de objetos GDI+ junto con datos adicionales a los que apuntan los miembros de esos objetos. Por ejemplo, el método [**Image:: GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) devuelve una matriz de objetos [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) , uno para cada elemento de propiedad (fragmento de metadatos) almacenado en la imagen. Pero **Image:: GetAllPropertyItems** devuelve más que simplemente la matriz de objetos **PropertyItem** ; anexa la matriz con datos adicionales.

Antes de llamar a [**Image:: GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems), debe asignar un búfer lo suficientemente grande como para contener la matriz de objetos [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) junto con los datos adicionales. Puede llamar al método [**Image:: GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) de un objeto Image para determinar el tamaño total del búfer requerido.

En el ejemplo siguiente se muestra cómo crear un objeto de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) y después llamar al método [**Image:: GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) de ese objeto de **imagen** para recuperar todos los elementos de propiedad (metadatos) almacenados en la imagen. El código asigna un búfer basado en un valor de tamaño devuelto por el método [**Image:: GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) . **Image:: GetPropertySize** también devuelve un valor de recuento que proporciona el número de elementos de propiedad de la imagen. Observe que el código no calcula el tamaño del búfer como `count*sizeof(PropertyItem)` . Un búfer calculado de esta manera sería demasiado pequeño.


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



## <a name="error-checking"></a>Comprobación de errores

La mayoría de los ejemplos de código de la documentación de GDI+ no muestran la comprobación de errores. La comprobación de errores completa es mucho más larga y puede ocultar el punto que se muestra en el ejemplo. No debe pegar los ejemplos de la documentación directamente en el código de producción. en su lugar, debe mejorar los ejemplos agregando su propia comprobación de errores.

En el ejemplo siguiente se muestra una manera de implementar la comprobación de errores con GDI+. Cada vez que se construye un objeto GDI+, el código comprueba para ver si el constructor se ha realizado correctamente. Esta comprobación es especialmente importante para el constructor de [**imagen**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , que se basa en leer un archivo. Si los cuatro objetos GDI+ ([**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath), **Image** y [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)) se construyen correctamente, el código llama a los métodos en esos objetos. Se comprueba si se ha realizado correctamente cada llamada al método y, en caso de error, se omiten las llamadas de método restantes.


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



## <a name="thread-synchronization"></a>Sincronización de subprocesos

Es posible que más de un subproceso tenga acceso a un solo objeto GDI+. Sin embargo, GDI+ no proporciona ningún mecanismo de sincronización automática. Por tanto, si dos subprocesos de la aplicación tienen un puntero al mismo objeto GDI+, es responsabilidad suya sincronizar el acceso a ese objeto.

Algunos métodos de GDI+ devuelven **ObjectBusy** si un subproceso intenta llamar a un método mientras otro subproceso está ejecutando un método en el mismo objeto. No intente sincronizar el acceso a un objeto basado en el valor devuelto de **ObjectBusy** . En su lugar, cada vez que se accede a un miembro o se llama a un método del objeto, se coloca la llamada dentro de una sección crítica o se usa otra técnica de sincronización estándar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Centro para desarrolladores de software de seguridad de MSDN](https://msdn.microsoft.com/security/)
</dt> <dt>

[Recursos de How-To de seguridad](/previous-versions/msp-n-p/ff650055(v=pandp.10))
</dt> <dt>

[Security Center TechNet](https://technet.microsoft.com/security/)
</dt> </dl>

 

 
