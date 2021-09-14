---
title: Introducción a las miniaturas de DWM
description: Administrador de ventanas de escritorio (DWM) permite mostrar representaciones en miniatura de ventanas de aplicación.
ms.assetid: 6d71fcda-0cf0-463c-8c60-0415109d154f
keywords:
- Administrador de ventanas de escritorio (DWM),miniaturas
- DWM (Administrador de ventanas de escritorio),miniaturas
- Administrador de ventanas de escritorio (DWM), relaciones en miniatura
- DWM (Administrador de ventanas de escritorio),relaciones en miniatura
- vistas en miniatura
- relaciones en miniatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3e0f1e6875e447a18ff5e63d703460ff909b25
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072660"
---
# <a name="dwm-thumbnail-overview"></a>Introducción a las miniaturas de DWM

Administrador de ventanas de escritorio (DWM) permite mostrar representaciones en miniatura de ventanas de aplicación. No se trata de instantáneas estáticas de una ventana, sino que son conexiones dinámicas y constantes entre una ventana de origen de miniaturas y una ubicación en una ventana de destino que recibe la representación en miniatura activa. Esto permite una vista rápida de las aplicaciones en ejecución al mantener el puntero sobre la aplicación en la barra de tareas o mediante el gesto de tecla ALT-TAB para ver y cambiar rápidamente a una aplicación.

En la imagen siguiente se muestra Windows vista en directo vista al mantener el puntero sobre la aplicación en la barra de tareas.

![Captura de pantalla que muestra la miniatura de D W M que se ve al mantener el puntero sobre una aplicación en la barra de tareas.](images/dwm-livethumbnail.png)

En la imagen siguiente se muestra el Windows Vista Flip (ALT-TAB) habilitado por DWM.

![captura de pantalla de la pestaña alt habilitada para dwm](images/dwm-flip.png)

> [!Note]  
> Las miniaturas de DWM no permiten a los desarrolladores crear aplicaciones como la Windows Vista Flip3D (WINKEY-TAB). Las miniaturas se representan directamente en la ventana de destino en 2D.

 

## <a name="dwm-thumbnail-relationships"></a>Relaciones de miniaturas de DWM

Para mostrar miniaturas en la aplicación, primero debe establecer una relación entre una ventana de origen y una ventana de destino. Para ello, se llama a la [**función DwmRegisterThumbnail.**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail)

[**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) no representa una miniatura en la ventana de destino, sino que simplemente crea la relación y proporciona el identificador de miniatura. La miniatura se representa después de que se hayan establecido las PROPIEDADES DE LA MINIATURA DE [**DWM \_ \_**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) y se haya llamado a la función [**DwmUpdateThumbnailProperties.**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) Las llamadas posteriores **a DwmUpdateThumbnailProperties** actualizan la miniatura con un nuevo conjunto de propiedades. DwM también proporciona la función auxiliar [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) para obtener el tamaño de la ventana de origen de la miniatura.

Para finalizar una relación en miniatura, llame a la [**función DwmUnregisterThumbnail.**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail)

En el ejemplo siguiente se muestra cómo crear una reevaluación con Windows escritorio y mostrarla en una aplicación.


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

 

 




