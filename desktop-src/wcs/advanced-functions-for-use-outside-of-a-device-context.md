---
title: Funciones avanzadas para usar fuera de un contexto de dispositivo
description: Estas funciones proporcionan funcionalidades avanzadas de administración de colores fuera de los contextos del dispositivo.
ms.assetid: 2f742743-094a-44b8-816b-24246607caeb
keywords:
- Windows Sistema de colores (WCS), funciones
- WCS (Windows Color System),functions
- administración de colores de imagen, funciones
- administración de colores, funciones
- colors,functions
- Referencia de WCS, funciones
- referencia de WCS,functions
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685b9fe1c7139be1c54e1b158a03c1de54d01b2b80ec4cab4b86603680c6d957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814624"
---
# <a name="advanced-functions-for-use-outside-of-a-device-context"></a>Funciones avanzadas para usar fuera de un contexto de dispositivo

Estas funciones proporcionan funcionalidades avanzadas de administración de colores fuera de los contextos del dispositivo.



| Función                                                           | Descripción                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PCMSCALLBACKW**](/windows/win32/api/icm/nc-icm-pcmscallbackw) | \**PCMSCALLBACKW** (o **ApplyCallbackFunction**) es una función de devolución de llamada que se implementa que actualiza los datos de configuración de WCS mientras se ejecuta el cuadro de diálogo que muestra la función [**SetupColorMatchingW.**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) |
| [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Comprueba si los píxeles de un mapa de bits especificado se encuentran dentro de la [gama de salida](g.md) de una transformación especificada. |
| [**CheckColors**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Determina si los colores de una matriz se encuentran dentro de la [gama de salida](g.md) de una transformación especificada. |
| [**ConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-convertcolornametoindex) | Convierte los nombres de color de un espacio de colores con nombre en números de índice en un perfil de color de International Color Consortium (ICC). |
| [**ConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-convertindextocolorname) | Transforma los índices de un espacio de colores en una matriz de nombres en un espacio de colores con nombre. |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) | Transforma los índices de un espacio de colores en una matriz de nombres en un espacio de colores con nombre. |
| [**CreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) | Acepta una matriz de perfiles o un perfil de vínculo de dispositivo único y crea una transformación de color que las aplicaciones pueden usar para realizar la asignación de colores. [](d.md) |
| [**DeleteColorTransform**](/windows/win32/api/icm/nf-icm-deletecolortransform) | Elimina una transformación de color determinada. |
| [**GetCMMInfo**](/windows/win32/api/icm/nf-icm-getcmminfo) | Recupera diversas información sobre el módulo de administración de colores (CMM) que creó la transformación de color especificada. |
| [**GetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-getnamedprofileinfo) | Recupera información sobre el perfil de color con nombre de International Color Consortium (ICC) que se especifica en el primer parámetro. |
| [**ICMProgressProcCallback**](icmprogressproccallback.md)         | Función de devolución de llamada proporcionada por la aplicación para informar del progreso. La aplicación también define el nombre de esta función.                                                 |
| [**SeleccioneCMM.**](/windows/win32/api/icm/nf-icm-selectcmm) | Permite seleccionar el módulo de administración de colores (CMM) preferido que se va a usar. |
| [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw)                   | Proporciona control de usuario sobre la administración de colores mediante un cuadro de diálogo.                                                                                                      |
| [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)                 | Convierte los colores de mapa de bits mediante una transformación de color.                                                                                                                          |
| [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) | Convierte una matriz de colores del espacio [de colores de origen](c.md) al espacio de colores de destino, tal como se define en una transformación de color. |
| [**WcsCheckColors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)                           | Determina si los colores de una matriz están dentro de la gama de salida de una transformación de color WCS especificada.                                                                |
| [**WcsTranslateColors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors) | Convierte una matriz de colores del espacio de colores de origen al espacio de colores de destino, tal como se define en una transformación de color.                                                |



 

 

 




