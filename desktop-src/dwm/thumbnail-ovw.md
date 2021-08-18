---
title: Introducción a las miniaturas de DWM
description: Administrador de ventanas de escritorio (DWM) permite mostrar representaciones en miniatura de ventanas de aplicación.
ms.assetid: 6d71fcda-0cf0-463c-8c60-0415109d154f
keywords:
- Administrador de ventanas de escritorio (DWM),thumbnails
- DWM (Administrador de ventanas de escritorio),thumbnails
- Administrador de ventanas de escritorio (DWM),relaciones en miniatura
- DWM (Administrador de ventanas de escritorio),relaciones en miniatura
- vistas en miniatura
- relaciones en miniatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b333d84496828c451ff6e0eb7dbf3a86f91d629623d9939f66e874cfa82ee47d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279780"
---
# <a name="dwm-thumbnail-overview"></a>Introducción a las miniaturas de DWM

Administrador de ventanas de escritorio (DWM) permite mostrar representaciones en miniatura de ventanas de aplicación. No se trata de instantáneas estáticas de una ventana, sino que son conexiones dinámicas y constantes entre una ventana de origen de miniaturas y una ubicación en una ventana de destino que recibe la representación en miniatura activa. Esto permite una vista rápida de las aplicaciones en ejecución; para ello, mantenga el puntero sobre la aplicación en la barra de tareas o use el gesto de tecla ALT-TAB para ver y cambiar rápidamente a una aplicación.

En la imagen siguiente se muestra el Windows vista en vivo que se ve al mantener el puntero sobre la aplicación en la barra de tareas.

![Captura de pantalla que muestra la miniatura de D W M que se ve al mantener el puntero sobre una aplicación en la barra de tareas.](images/dwm-livethumbnail.png)

En la imagen siguiente se muestra Windows Vista Flip (ALT-TAB) habilitada por DWM.

![captura de pantalla de la pestaña alt habilitada para dwm](images/dwm-flip.png)

> [!Note]  
> Las miniaturas dwm no permiten a los desarrolladores crear aplicaciones como Windows vista Flip3D (WINKEY-TAB). Las miniaturas se representan directamente en la ventana de destino en 2D.

 

## <a name="dwm-thumbnail-relationships"></a>Relaciones de miniaturas de DWM

Para mostrar miniaturas en la aplicación, primero debe establecer una relación entre una ventana de origen y una ventana de destino. Para ello, llame a la [**función DwmRegisterThumbnail.**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail)

[**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) no representa una miniatura en la ventana de destino, sino que simplemente crea la relación y proporciona el identificador de miniatura. La miniatura se representa una vez establecidas las PROPIEDADES DE MINIATURA DE [**DWM \_ \_**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) y se ha llamado a la función [**DwmUpdateThumbnailProperties.**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) Las llamadas posteriores **a DwmUpdateThumbnailProperties** actualizan la miniatura con un nuevo conjunto de propiedades. DwM también proporciona la función auxiliar [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) para obtener el tamaño de la ventana de origen de la miniatura.

Para finalizar una relación en miniatura, llame a [**la función DwmUnregisterThumbnail.**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail)

En el ejemplo siguiente se muestra cómo crear una releationship con Windows escritorio y mostrarla en una aplicación.


```
HRESULT hr = S_OK;
HTHUMBNAIL thumbnail = NULL;

// Register the thumbnail
hr = DwmRegisterThumbnail(hwnd, FindWindow(_T("Progman"), NULL), &thumbnail);
if (SUCCEEDED(hr))
{
    // Specify the destination rectangle size
    RECT dest = {0,50,100,150};

    // Set the thumbnail properties for use
    DWM_THUMBNAIL_PROPERTIES dskThumbProps;
    dskThumbProps.dwFlags = DWM_TNP_SOURCECLIENTAREAONLY | DWM_TNP_VISIBLE | DWM_TNP_OPACITY | DWM_TNP_RECTDESTINATION;
    dskThumbProps.fSourceClientAreaOnly = FALSE; 
    dskThumbProps.fVisible = TRUE;
    dskThumbProps.opacity = (255 * 70)/100;
    dskThumbProps.rcDestination = dest;

    // Display the thumbnail
    hr = DwmUpdateThumbnailProperties(thumbnail,&dskThumbProps);
    if (SUCCEEDED(hr))
    {
        // ...
    }
}
return hr;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desktop Window Manager Overview](dwm-overview.md) (Administrador de ventanas de escritorio)
</dt> <dt>

[Habilitar y controlar la composición de DWM](composition-ovw.md)
</dt> <dt>

[Consideraciones de rendimiento y procedimientos recomendados](bestpractices-ovw.md)
</dt> </dl>

 

 




