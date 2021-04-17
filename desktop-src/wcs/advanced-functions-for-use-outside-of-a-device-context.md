---
title: Funciones avanzadas para usar fuera de un contexto de dispositivo
description: Estas funciones proporcionan capacidades avanzadas de administración del color fuera de los contextos del dispositivo.
ms.assetid: 2f742743-094a-44b8-816b-24246607caeb
keywords:
- Sistema de color de Windows (WCS), funciones
- WCS (sistema de colores de Windows), funciones
- Administración del color de imagen, funciones
- Administración del color, funciones
- colores, funciones
- Referencia WCS, funciones
- referencia de las funciones WCS,
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d04b7afe98f468fd3f580adf3eff145bce3aa1ac
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "105721169"
---
# <a name="advanced-functions-for-use-outside-of-a-device-context"></a>Funciones avanzadas para usar fuera de un contexto de dispositivo

Estas funciones proporcionan capacidades avanzadas de administración del color fuera de los contextos del dispositivo.



| Función                                                           | Descripción                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PCMSCALLBACKW**](/windows/win32/api/icm/nc-icm-pcmscallbackw) | \**PCMSCALLBACKW** (o **ApplyCallbackFunction**) es una función de devolución de llamada que se implementa y que actualiza los datos de configuración de WCS mientras se está ejecutando el cuadro de diálogo que muestra la función [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) . |
| [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Comprueba si los píxeles de un mapa de bits especificado se encuentran dentro de la [gama](g.md) de salida de una transformación especificada. |
| [**CheckColors**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Determina si los colores de una matriz se encuentran dentro de la [gama](g.md) de salida de una transformación especificada. |
| [**ConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-convertcolornametoindex) | Convierte los nombres de colores de un espacio de colores con nombre en números de índice en un perfil de color de International color Consortium (ICC). |
| [**ConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-convertindextocolorname) | Transforma índices en un espacio de colores en una matriz de nombres de un espacio de colores con nombre. |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) | Transforma índices en un espacio de colores en una matriz de nombres de un espacio de colores con nombre. |
| [**CreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) | Acepta una matriz de perfiles o un [Perfil de vínculo de dispositivo](d.md) único y crea una transformación de color que las aplicaciones pueden usar para realizar la asignación de colores. |
| [**DeleteColorTransform**](/windows/win32/api/icm/nf-icm-deletecolortransform) | Elimina una transformación de color determinada. |
| [**GetCMMInfo**](/windows/win32/api/icm/nf-icm-getcmminfo) | Recupera diversa información sobre el módulo de administración del color (CMM) que creó la transformación de color especificada. |
| [**GetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-getnamedprofileinfo) | Recupera información sobre el perfil de color International color Consortium (ICC) especificado en el primer parámetro. |
| [**ICMProgressProcCallback**](icmprogressproccallback.md)         | Función de devolución de llamada proporcionada por la aplicación para notificar el progreso. La aplicación también define el nombre de esta función.                                                 |
| [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) | Permite seleccionar el módulo de administración del color preferido (CMM) que se va a usar. |
| [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw)                   | Proporciona control de usuario sobre la administración del color por medio de un cuadro de diálogo.                                                                                                      |
| [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)                 | Convierte los colores del mapa de bits mediante una transformación de color.                                                                                                                          |
| [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) | Convierte una matriz de colores del [espacio de colores](c.md) de origen en el espacio de colores de destino, tal y como se define en una transformación de color. |
| [**WcsCheckColors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)                           | Determina si los colores de una matriz están dentro de la gama de salida de una transformación de color WCS especificada.                                                                |
| [**WcsTranslateColors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors) | Convierte una matriz de colores del espacio de colores de origen en el espacio de colores de destino, tal y como se define en una transformación de color.                                                |



 

 

 




