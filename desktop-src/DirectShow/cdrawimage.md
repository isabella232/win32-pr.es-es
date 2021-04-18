---
description: La clase CDrawImage es una clase auxiliar que administra el dibujo de un filtro de representador de vídeo.
ms.assetid: 7a6b3726-dbf5-4b60-8cf1-42034a321293
title: Clase CDrawImage (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 001b91338b2956f663d777cbc9597fa2d9a478f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671764"
---
# <a name="cdrawimage-class"></a>Clase CDrawImage

La `CDrawImage` clase es una clase auxiliar que administra el dibujo de un filtro de representador de vídeo. Todas las operaciones de dibujo se realizan mediante GDI. Esta clase no proporciona compatibilidad para la representación con DirectDraw. La `CDrawImage` clase requiere que el filtro propietario también use la clase [**CBaseWindow**](cbasewindow.md) , que administra la ventana de vídeo. El `CDrawImage` constructor toma un puntero al objeto **CBaseWindow** .

En el diagrama siguiente se muestra la manera preferida de usar esta clase en un filtro personalizado de representador de vídeo.

![Representador de vídeo personalizado mediante cdrawimage](images/videorenderer.png)

Para usar esta clase, haga lo siguiente:

-   Cuando se conecten los pin, llame a los métodos [**CDrawImage:: NotifyMediaType**](cdrawimage-notifymediatype.md) y [**CDrawImage:: NotifyAllocator**](cdrawimage-notifyallocator.md) .
-   Siempre que cambie el tipo de medio, vuelva a llamar a **NotifyMediaType** .
-   Antes de que se produzca cualquier representación, llame a [**CDrawImage:: SetDrawContext**](cdrawimage-setdrawcontext.md).
-   Llame a [**CDrawImage:: SetSourceRect**](cdrawimage-setsourcerect.md) si el rectángulo de origen cambia y [**CDrawImage:: SetTargetRect**](cdrawimage-settargetrect.md) si cambia el rectángulo de destino.
-   Administre la paleta para imágenes de paleta, tal como se describe en la sección sobre las paletas que se indican a continuación.

## <a name="allocators"></a>Asignadores

El filtro mostrado en el diagrama anterior usa una clase de asignador personalizado, [**CImageAllocator**](cimageallocator.md). Este asignador crea DIB en la memoria compartida, utilizando la función **CreateDIBSection** de GDI. Los ejemplos creados por el asignador son objetos [**CImageSample**](cimagesample.md) .

Si el filtro posee el asignador para la conexión, se garantiza que los ejemplos de medios son objetos [**CImageSample**](cimagesample.md) . En ese caso, el objeto **CDrawImage** puede optimizar el dibujo mediante **bitblt** o StretchBlt. De lo contrario, debe usar las funciones **SetDIBitsToDevice** o **StretchDIBits** más lentas. La opción más rápida se implementa mediante el método [**CDrawImage:: FastRender**](cdrawimage-fastrender.md) , la opción más lenta por el método [**CDrawImage:: SlowRender**](cdrawimage-slowrender.md) . (A pesar del nombre, probablemente no verá una gran disminución del rendimiento en **SlowRender**, especialmente en el hardware más reciente).

## <a name="palettes"></a>Las paletas

Si el método [**FastRender**](cdrawimage-fastrender.md) se usa para dibujar y la imagen es de paleta, el filtro debe administrar la paleta de la siguiente manera:

-   La clase [**CImageSample**](cimagesample.md) contiene un número de versión de la paleta, almacenado en la estructura [**DIBDATA**](dibdata.md) . El valor se inicializa cuando el asignador crea el ejemplo.
-   La clase **CDrawImage** también contiene un número de versión de la paleta, que se inicializa al crearse.
-   Siempre que el tipo de medio cambie a un nuevo formato de paleta, llame a [**CDrawImage:: IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md). Este método incrementa el número de versión de la paleta del objeto **CDrawImage** . Si el filtro usa la clase [**CImagePalette**](cimagepalette.md) para administrar la información de la paleta, puede llamar simplemente a [**CImagePalette::P reparepalette**](cimagepalette-preparepalette.md) cada vez que cambie el tipo de medio. El método **PreparePalette** incrementa la versión de la paleta solo cuando es necesario.
-   El método [**FastRender**](cdrawimage-fastrender.md) compara la versión de la paleta de **CDrawImage** con la versión de la paleta del ejemplo. Si el número de versión del ejemplo se retrasa detrás del número de versión de **CDrawImage** , el método **FastRender** llama a [**CDrawImage:: UpdateColourTable**](cdrawimage-updatecolourtable.md). El método **UpdateColourTable** establece la tabla de colores en el contexto del dispositivo, mediante la función **SetDIBColorTable** de GDI. Además, la versión de la paleta en el ejemplo se actualiza al número de versión actual.
-   Si el PIN se vuelve a conectar, el filtro debe llamar a [**CDrawImage:: ResetPaletteVersion**](cdrawimage-resetpaletteversion.md) para restablecer la versión de la paleta. En la reconexión del PIN, el asignador vuelve a asignar todos los ejemplos.



| Variables de miembro protegidas                                            | Descripción                                                                                                                     |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ bStretch**](cdrawimage-m-bstretch.md)                          | Indica si la imagen de vídeo debe ajustarse para ajustarse a la ventana de destino.                                              |
| [**m \_ bUsingImageAllocator**](cdrawimage-m-busingimageallocator.md)  | Indica si el asignador de la conexión de PIN es un objeto **CImageAllocator** .                                         |
| [**m \_ EndSample**](cdrawimage-m-endsample.md)                        | Especifica la hora de detención de la muestra más reciente.                                                                              |
| [**m \_ HDC**](cdrawimage-m-hdc.md)                                    | Identificador del contexto de dispositivo de la ventana propietaria.                                                                              |
| [**m \_ MemoryDC**](cdrawimage-m-memorydc.md)                          | Identificador del contexto de dispositivo de memoria de la ventana propietaria.                                                                       |
| [**m \_ PaletteVersion**](cdrawimage-m-paletteversion.md)              | Se usa para realizar el seguimiento cuando cambia la paleta.                                                                                         |
| [**m \_ pBaseWindow**](cdrawimage-m-pbasewindow.md)                    | Puntero al objeto **CBaseWindow** propietario.                                                                                   |
| [**m \_ pMediaType**](cdrawimage-m-pmediatype.md)                      | Puntero al tipo de medio actual.                                                                                              |
| [**m \_ SourceRect**](cdrawimage-m-sourcerect.md)                      | Especifica el rectángulo de origen para dibujar.                                                                                     |
| [**m \_ StartSample**](cdrawimage-m-startsample.md)                    | Especifica la hora de inicio del ejemplo más reciente.                                                                             |
| [**m \_ TargetRect**](cdrawimage-m-targetrect.md)                      | Especifica el rectángulo de destino del dibujo.                                                                                     |
| Métodos protegidos                                                     | Descripción                                                                                                                     |
| [**DisplaySampleTimes**](cdrawimage-displaysampletimes.md)           | Dibuja las marcas de tiempo de un ejemplo multimedia en la parte superior de la imagen de vídeo.                                                              |
| [**FastRender**](cdrawimage-fastrender.md)                           | Dibuja la imagen de vídeo mediante las funciones **bitblt** o **StretchBlt** .                                                         |
| [**SetStretchMode**](cdrawimage-setstretchmode.md)                   | Calcula si se debe ajustar la imagen de vídeo.                                                                           |
| [**SlowRender**](cdrawimage-slowrender.md)                           | Dibuja la imagen de vídeo mediante las funciones **SetDIBitsToDevice** o **StretchDIBits** .                                           |
| [**UpdateColourTable**](cdrawimage-updatecolourtable.md)             | Actualiza la tabla de colores con una nueva paleta.                                                                                     |
| Métodos públicos                                                        | Descripción                                                                                                                     |
| [**CDrawImage**](cdrawimage-cdrawimage.md)                           | Método de constructor.                                                                                                             |
| [**DrawImage**](cdrawimage-drawimage.md)                             | Dibuja un fotograma de vídeo en la ventana de vídeo.                                                                                        |
| [**DrawVideoImageHere**](cdrawimage-drawvideoimagehere.md)           | Dibuja una imagen de un ejemplo multimedia en un contexto de dispositivo especificado.                                                               |
| [**GetPaletteVersion**](cdrawimage-getpaletteversion.md)             | Recupera la versión de la paleta.                                                                                                  |
| [**GetSourceRect**](cdrawimage-getsourcerect.md)                     | Recupera el rectángulo de origen actual.                                                                                         |
| [**GetTargetRect**](cdrawimage-gettargetrect.md)                     | Recupera el rectángulo de destino actual.                                                                                    |
| [**IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) | Incrementa la versión de la paleta.                                                                                                 |
| [**NotifyAllocator**](cdrawimage-notifyallocator.md)                 | Informa al objeto de `CDrawImage` si el asignador de la conexión es un objeto **CImageAllocator** .                       |
| [**NotifyEndDraw**](cdrawimage-notifyenddraw.md)                     | No se admite.                                                                                                                  |
| [**NotifyMediaType**](cdrawimage-notifymediatype.md)                 | Notifica al objeto del tipo de medio actual.                                                                                  |
| [**NotifyStartDraw**](cdrawimage-notifystartdraw.md)                 | No se admite.                                                                                                                  |
| [**ResetPaletteVersion**](cdrawimage-resetpaletteversion.md)         | Restablece la versión de la paleta.                                                                                                     |
| [**ScaleSourceRect**](cdrawimage-scalesourcerect.md)                 | Escala un rectángulo de origen especificado, si hay una diferencia entre el tamaño de vídeo nativo y el formato de tipo de medio. Virtualiza. |
| [**SetDrawContext**](cdrawimage-setdrawcontext.md)                   | Establece los contextos de dispositivo usados para dibujar.                                                                                      |
| [**SetSourceRect**](cdrawimage-setsourcerect.md)                     | Establece el rectángulo de origen.                                                                                                      |
| [**SetTargetRect**](cdrawimage-settargetrect.md)                     | Establece el rectángulo de destino.                                                                                                      |
| [**UsingImageAllocator**](cdrawimage-usingimageallocator.md)         | Indica si el asignador actual es un objeto [**CImageAllocator**](cimageallocator.md) .                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




