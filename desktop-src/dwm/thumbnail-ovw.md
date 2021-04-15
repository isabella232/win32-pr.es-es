---
title: Información general sobre las miniaturas de DWM
description: Administrador de ventanas de escritorio (DWM) permite mostrar representaciones en miniatura de las ventanas de la aplicación.
ms.assetid: 6d71fcda-0cf0-463c-8c60-0415109d154f
keywords:
- Administrador de ventanas de escritorio (DWM), miniaturas
- DWM (Administrador de ventanas de escritorio), miniaturas
- Administrador de ventanas de escritorio (DWM), relaciones en miniatura
- DWM (Administrador de ventanas de escritorio), relaciones en miniatura
- vistas en miniatura
- relaciones en miniatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3e0f1e6875e447a18ff5e63d703460ff909b25
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104569640"
---
# <a name="dwm-thumbnail-overview"></a>Información general sobre las miniaturas de DWM

Administrador de ventanas de escritorio (DWM) permite mostrar representaciones en miniatura de las ventanas de la aplicación. No son instantáneas estáticas de una ventana, sino que son dinámicas, las conexiones constantes entre una ventana de código fuente en miniatura y una ubicación en una ventana de destino que recibe la representación en miniatura activa. Esto permite una vista rápida de las aplicaciones en ejecución si mantiene el puntero sobre la aplicación en la barra de tareas o usa el gesto de tecla ALT-TAB para ver y cambiar rápidamente a una aplicación.

En la imagen siguiente se muestra la miniatura dinámica de Windows Vista que se muestra al mantener el mouse sobre la aplicación en la barra de tareas.

![Captura de pantalla que muestra la miniatura D W M que se ve al mantener el mouse sobre una aplicación en la barra de tareas.](images/dwm-livethumbnail.png)

En la imagen siguiente se muestra el volteo de Windows Vista (ALT-TAB) habilitada por DWM.

![captura de pantalla de la pestaña Alt-Tab habilitada para DWM](images/dwm-flip.png)

> [!Note]  
> Las miniaturas de DWM no permiten a los desarrolladores crear aplicaciones como la característica Flip3D (WINKEY-TAB) de Windows Vista. Las miniaturas se representan directamente en la ventana de destino en 2-D.

 

## <a name="dwm-thumbnail-relationships"></a>Relaciones en miniatura de DWM

Para mostrar las miniaturas en la aplicación, primero debe establecer una relación entre una ventana de código fuente y una ventana de destino. Esto se realiza mediante una llamada a la función [**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) .

[**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) no representa una miniatura en la ventana de destino, sino que simplemente crea la relación y proporciona el identificador de miniatura. La miniatura se representa una vez que se han establecido las [**\_ \_ propiedades de miniatura de DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) y se ha llamado a la función [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) . Las llamadas posteriores a **DwmUpdateThumbnailProperties** actualizan la miniatura con un nuevo conjunto de propiedades. DWM también proporciona la función auxiliar [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) para obtener el tamaño de la ventana de código fuente de la miniatura.

Para finalizar una relación de miniatura, llame a la función [**DwmUnregisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail) .

En el ejemplo siguiente se muestra cómo crear un releationship con el escritorio de Windows y mostrarlo en una aplicación.


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

[Consideraciones de rendimiento y prácticas recomendadas](bestpractices-ovw.md)
</dt> </dl>

 

 




