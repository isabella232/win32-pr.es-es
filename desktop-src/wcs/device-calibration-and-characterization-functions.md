---
title: Funciones de calibración y caracterización de dispositivos
description: Las siguientes funciones son útiles para escribir herramientas de calibración y caracterización de dispositivos necesarias para instalar y calibrar dispositivos de visualización de color, como monitores e impresoras.
ms.assetid: e66115cc-b6a9-4df5-b774-38619881bdb0
keywords:
- Windows Sistema de colores (WCS), funciones
- WCS (Windows de color), funciones
- administración de colores de imagen, funciones
- administración de colores, funciones
- colors,functions
- WCS reference,functions
- referencia de WCS,functions
- Windows Sistema de colores (WCS), calibración del dispositivo
- WCS (Windows color), calibración del dispositivo
- administración del color de la imagen, calibración del dispositivo
- administración de colores, calibración del dispositivo
- colors,device calibration
- Referencia de WCS, calibración del dispositivo
- referencia de WCS, calibración del dispositivo
- Windows Sistema de colores (WCS), caracterización
- WCS (Windows de color), caracterización
- administración de colores de imagen, caracterización
- administración de colores, caracterización
- colors,characterization
- Referencia de WCS, caracterización
- referencia de WCS, caracterización
- calibración del dispositivo
- Calibración
- Caracterización
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aea24f0a1e033df62c70674c44c9b5e9c6c0e0de1011b9ea95b9e5389d6004c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452035"
---
# <a name="device-calibration-and-characterization-functions"></a>Funciones de calibración y caracterización de dispositivos

Las siguientes funciones son útiles para escribir herramientas de calibración y caracterización de dispositivos necesarias para instalar y calibrar dispositivos de visualización de color, como monitores e impresoras.



| Función | Descripción |
|-|-|
| [**CloseColorProfile**](/windows/win32/api/icm/nf-icm-closecolorprofile) | Cierra un identificador de perfil abierto. |
| [**CreateDeviceLinkProfile**](/windows/win32/api/icm/nf-icm-createdevicelinkprofile) | Crea un perfil de  vínculo de dispositivo de International Color Consortium (ICC) a partir de un conjunto de perfiles de color, utilizando las intenciones especificadas. |
| [**GetColorProfileElement**](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | Copia los datos de un elemento de perfil etiquetado especificado de un perfil de color especificado en un búfer. |
| [**GetColorProfileElementTag**](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | Recupera el nombre de etiqueta especificado por *dwIndex* en la tabla de etiquetas de un perfil de color determinado de International Color Consortium (DOW), donde *dwIndex* es un índice basado en uno en esa tabla. |
| [**GetColorProfileFromHandle**](/windows/win32/api/icm/nf-icm-getcolorprofilefromhandle)| Recupera el contenido del perfil de color dado un identificador a un perfil de color abierto.     |
| [**GetColorProfileHeader**](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | Recupera o deriva la estructura de encabezados DE CORTE a partir del perfil de color DE LA FILA o del perfil XML de WCS. Los controladores y las aplicaciones deben asumir que devolver **TRUE** solo indica que se devuelve un encabezado estructurado correctamente. Cada etiqueta tendrá que validarse de forma independiente mediante las API ICM2 heredadas o las API de esquema XML. |
| [**GetCountColorProfileElements**](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | Recupera el número de elementos etiquetados en un perfil de color determinado. |
| [**GetPS2ColorRenderingDictionary**](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | Recupera el diccionario de PostScript de representación de colores de nivel 2 del perfil de color DE LAN especificado. |
| [**GetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | Recupera la intención de PostScript de [color](r.md) nivel 2 de un perfil de color DE COLOR DE COLOR DE NIVEL 2. |
| [**GetPS2ColorSpaceArray**](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | Recupera la matriz PostScript espacio [de colores](c.md) nivel 2 de un perfil de color DE COLOR DE COLOR DE NIVEL 2. |
| [**IsColorProfileTagPresent**](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | Indica si una etiqueta especificada de International Color Consortium (ICC) está presente en el perfil de color especificado. |
| [**IsColorProfileValid**](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | Permite determinar si el perfil especificado es un perfil válido de International Color Consortium (ICC) o un identificador de perfil válido de Windows Color System (WCS) que se puede usar para la administración de colores. |
| [**OpenColorProfileW**](/windows/win32/api/icm/nf-icm-opencolorprofilew) | Crea un identificador para un perfil de color especificado. A continuación, el identificador se puede usar en otras funciones de administración de perfiles. |
| [**SetColorProfileElement**](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | Establece los datos del elemento para un elemento de perfil etiquetado en un perfil de color DE COLOR DE COLOR. |
| [**SetColorProfileElementReference**](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | Crea en un perfil de color DE LAN especificado una nueva etiqueta que hace referencia a los mismos datos que una etiqueta existente. |
| [**SetColorProfileElementSize**](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | Establece el tamaño de un elemento etiquetado en un perfil de color DECTE. |
| [**SetColorProfileHeader**](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | Establece los datos de encabezado en un perfil de color DE LAN especificado. |
| [**WcsGetIntegrabrationManagementState**](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | Determina si la administración del sistema del estado de calibración de pantalla está habilitada. |
| [**WcsSetIntegrabrationManagementState**](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | Determina si la administración del sistema del estado de calibración de pantalla está habilitada. |



 

 

 




