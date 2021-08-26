---
description: La clase CDrawImage es una clase auxiliar que administra el dibujo para un filtro de representador de vídeo.
ms.assetid: 7a6b3726-dbf5-4b60-8cf1-42034a321293
title: CDrawImage (clase, Winutil.h)
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
ms.openlocfilehash: 951744cded927707ac0b39e562b4207acbecdd92420c91a2b130f0b493444b01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999564"
---
# <a name="cdrawimage-class"></a>CDrawImage (clase)

La `CDrawImage` clase es una clase auxiliar que administra el dibujo para un filtro de representador de vídeo. Todas las operaciones de dibujo se realizan mediante GDI. Esta clase no proporciona ninguna compatibilidad para la representación con DirectDraw. La `CDrawImage` clase requiere que el filtro propietario también use la clase [**CBaseWindow,**](cbasewindow.md) que administra la ventana de vídeo. El `CDrawImage` constructor toma un puntero al objeto **CBaseWindow.**

En el diagrama siguiente se muestra la manera preferida de usar esta clase en un filtro de representador de vídeo personalizado.

![representador de vídeo personalizado mediante cdrawimage](images/videorenderer.png)

Para usar esta clase, haga lo siguiente:

-   Cuando se conecten los pines, llame a los [**métodos CDrawImage::NotifyMediaType**](cdrawimage-notifymediatype.md) y [**CDrawImage::NotifyAllocator.**](cdrawimage-notifyallocator.md)
-   Cada vez que cambie el tipo de medio, vuelva **a llamar a NotifyMediaType.**
-   Antes de que se produzca cualquier representación, llame [**a CDrawImage::SetDrawContext**](cdrawimage-setdrawcontext.md).
-   Llame [**a CDrawImage::SetSourceRect**](cdrawimage-setsourcerect.md) si cambia el rectángulo de origen y [**a CDrawImage::SetTargetRect**](cdrawimage-settargetrect.md) si cambia el rectángulo de destino.
-   Administre la paleta de imágenes con color verde, como se describe en la sección sobre las paletas siguientes.

## <a name="allocators"></a>Asignadores

El filtro que se muestra en el diagrama anterior usa una clase de asignador personalizada, [**CImageAllocator**](cimageallocator.md). Este asignador crea dibs en memoria compartida mediante la **función CreateDIBSection de** GDI. Los ejemplos creados por el asignador son [**objetos CImageSample.**](cimagesample.md)

Si el filtro posee el asignador para la conexión, se garantiza que los ejemplos multimedia sean [**objetos CImageSample.**](cimagesample.md) En ese caso, el **objeto CDrawImage** puede optimizar el dibujo mediante **BitBlt** o StretchBlt. De lo contrario, debe usar las funciones **SetDIBitsToDevice** o **StretchDIBits más lentas.** La opción más rápida se implementa mediante el método [**CDrawImage::FastRender,**](cdrawimage-fastrender.md) la opción más lenta por el [**método CDrawImage::SlowRender.**](cdrawimage-slowrender.md) (A pesar del nombre, probablemente no verá un gran rendimiento en **SlowRender,** especialmente en hardware más reciente).

## <a name="palettes"></a>Paletas

Si el [**método FastRender**](cdrawimage-fastrender.md) se usa para dibujar y la imagen está en desenlazado, el filtro debe administrar la paleta, como se muestra a continuación:

-   La [**clase CImageSample**](cimagesample.md) contiene un número de versión de paleta, almacenado en la [**estructura DIBDATA.**](dibdata.md) El valor se inicializa cuando el asignador crea el ejemplo.
-   La **clase CDrawImage** también contiene un número de versión de paleta, que se inicializa al crearse.
-   Cada vez que el tipo de medio cambie a un nuevo formato de color, llame a [**CDrawImage::IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md). Este método incrementa el número de versión de la paleta del objeto **CDrawImage.** Si el filtro usa la clase [**CImagePalette**](cimagepalette.md) para administrar la información de la paleta, puede llamar simplemente a [**CImagePalette::P reparePalette**](cimagepalette-preparepalette.md) siempre que cambie el tipo de medio. El **método PreparePalette** incrementa la versión de la paleta solo cuando sea necesario.
-   El [**método FastRender**](cdrawimage-fastrender.md) compara la versión **de la paleta CDrawImage** con la versión de la paleta del ejemplo. Si el número de versión del ejemplo está por detrás del número de versión **de CDrawImage,** el método **FastRender** llama a [**CDrawImage::UpdateColourTable**](cdrawimage-updatecolourtable.md). El **método UpdateColourTable** establece la tabla de colores en el contexto del dispositivo mediante la función **SetDIBColorTable de** GDI. Además, la versión de la paleta del ejemplo se actualiza al número de versión actual.
-   Si el pin se vuelve a conectar, el filtro debe llamar a [**CDrawImage::ResetPaletteVersion para**](cdrawimage-resetpaletteversion.md) restablecer la versión de la paleta. Al volver a conectar el pin, el asignador vuelve a asignar todos los ejemplos.



| Variables miembro protegidas                                            | Descripción                                                                                                                     |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ bStretch**](cdrawimage-m-bstretch.md)                          | Indica si la imagen de vídeo debe ajustarse a la ventana de destino.                                              |
| [**m \_ bUsingImageAllocator**](cdrawimage-m-busingimageallocator.md)  | Indica si el asignador de la conexión de pin es **un objeto CImageAllocator.**                                         |
| [**m \_ EndSample**](cdrawimage-m-endsample.md)                        | Especifica la hora de detenerse del ejemplo más reciente.                                                                              |
| [**m \_ hdc**](cdrawimage-m-hdc.md)                                    | Controle el contexto del dispositivo de la ventana propietaria.                                                                              |
| [**m \_ MemoryDC**](cdrawimage-m-memorydc.md)                          | Controle el contexto del dispositivo de memoria de la ventana propietaria.                                                                       |
| [**m \_ PaletteVersion**](cdrawimage-m-paletteversion.md)              | Se usa para realizar un seguimiento de cuándo cambia la paleta.                                                                                         |
| [**m \_ pBaseWindow**](cdrawimage-m-pbasewindow.md)                    | Puntero al objeto **CBaseWindow** propietario.                                                                                   |
| [**m \_ pMediaType**](cdrawimage-m-pmediatype.md)                      | Puntero al tipo de medio actual.                                                                                              |
| [**m \_ SourceRect**](cdrawimage-m-sourcerect.md)                      | Especifica el rectángulo de origen para dibujar.                                                                                     |
| [**m \_ StartSample**](cdrawimage-m-startsample.md)                    | Especifica la hora de inicio del ejemplo más reciente.                                                                             |
| [**m \_ TargetRect**](cdrawimage-m-targetrect.md)                      | Especifica el rectángulo de destino para dibujar.                                                                                     |
| Métodos protegidos                                                     | Descripción                                                                                                                     |
| [**DisplaySampleTimes**](cdrawimage-displaysampletimes.md)           | Dibuja las marcas de tiempo de un ejemplo multimedia sobre la imagen de vídeo.                                                              |
| [**FastRender**](cdrawimage-fastrender.md)                           | Dibuja la imagen de vídeo mediante las **funciones BitBlt** **o StretchBlt.**                                                         |
| [**SetStretchMode**](cdrawimage-setstretchmode.md)                   | Calcula si se debe extender la imagen de vídeo.                                                                           |
| [**SlowRender**](cdrawimage-slowrender.md)                           | Dibuja la imagen de vídeo mediante las **funciones SetDIBitsToDevice** **o StretchDIBits.**                                           |
| [**UpdateColourTable**](cdrawimage-updatecolourtable.md)             | Actualiza la tabla de colores con una nueva paleta.                                                                                     |
| Métodos públicos                                                        | Descripción                                                                                                                     |
| [**CDrawImage**](cdrawimage-cdrawimage.md)                           | Método constructor.                                                                                                             |
| [**Drawimage**](cdrawimage-drawimage.md)                             | Dibuja un fotograma de vídeo en la ventana de vídeo.                                                                                        |
| [**DrawVideoImageHere**](cdrawimage-drawvideoimagehere.md)           | Dibuja una imagen de un ejemplo multimedia en un contexto de dispositivo especificado.                                                               |
| [**GetPaletteVersion**](cdrawimage-getpaletteversion.md)             | Recupera la versión de la paleta.                                                                                                  |
| [**GetSourceRect**](cdrawimage-getsourcerect.md)                     | Recupera el rectángulo de origen actual.                                                                                         |
| [**GetTargetRect**](cdrawimage-gettargetrect.md)                     | Recupera el rectángulo de destino actual.                                                                                    |
| [**IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) | Incrementa la versión de la paleta.                                                                                                 |
| [**NotifyAllocator**](cdrawimage-notifyallocator.md)                 | Informa al objeto `CDrawImage` si el asignador de la conexión es **un objeto CImageAllocator.**                       |
| [**NotifyEndDraw**](cdrawimage-notifyenddraw.md)                     | No compatible.                                                                                                                  |
| [**NotifyMediaType**](cdrawimage-notifymediatype.md)                 | Notifica al objeto del tipo de medio actual.                                                                                  |
| [**NotifyStartDraw**](cdrawimage-notifystartdraw.md)                 | No compatible.                                                                                                                  |
| [**ResetPaletteVersion**](cdrawimage-resetpaletteversion.md)         | Restablece la versión de la paleta.                                                                                                     |
| [**ScaleSourceRect**](cdrawimage-scalesourcerect.md)                 | Escala un rectángulo de origen especificado, si hay una diferencia entre el tamaño de vídeo nativo y el formato de tipo de medio. Virtual. |
| [**SetDrawContext**](cdrawimage-setdrawcontext.md)                   | Establece los contextos de dispositivo usados para dibujar.                                                                                      |
| [**SetSourceRect**](cdrawimage-setsourcerect.md)                     | Establece el rectángulo de origen.                                                                                                      |
| [**SetTargetRect**](cdrawimage-settargetrect.md)                     | Establece el rectángulo de destino.                                                                                                      |
| [**UsingImageAllocator**](cdrawimage-usingimageallocator.md)         | Indica si el asignador actual es un [**objeto CImageAllocator.**](cimageallocator.md)                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




