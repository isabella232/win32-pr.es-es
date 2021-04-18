---
title: Funciones de calibración y caracterización de dispositivos
description: Las siguientes funciones son útiles para escribir herramientas de calibración y caracterización de dispositivos necesarias para instalar y calibrar los dispositivos de pantalla de color, como monitores e impresoras.
ms.assetid: e66115cc-b6a9-4df5-b774-38619881bdb0
keywords:
- Sistema de color de Windows (WCS), funciones
- WCS (sistema de colores de Windows), funciones
- Administración del color de imagen, funciones
- Administración del color, funciones
- colores, funciones
- Referencia WCS, funciones
- referencia de las funciones WCS,
- Sistema de color de Windows (WCS), calibración de dispositivos
- WCS (sistema de colores de Windows), calibración de dispositivos
- Administración del color de imagen, calibración de dispositivos
- Administración del color, calibración de dispositivos
- colores, calibración de dispositivos
- Referencia WCS, calibración de dispositivos
- referencia de WCS, calibración de dispositivos
- Sistema de color de Windows (WCS), caracterización
- WCS (sistema de colores de Windows), caracterización
- Administración del color de imagen, caracterización
- Administración del color, caracterización
- colores, caracterización
- Referencia WCS, caracterización
- referencia de WCS, caracterización
- calibración de dispositivos
- curva
- caracterización
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3367bbc6385cc21c8dbff3a88bed685616fb3f29
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "105721423"
---
# <a name="device-calibration-and-characterization-functions"></a>Funciones de calibración y caracterización de dispositivos

Las siguientes funciones son útiles para escribir herramientas de calibración y caracterización de dispositivos necesarias para instalar y calibrar los dispositivos de pantalla de color, como monitores e impresoras.



| Función | Descripción |
|-|-|
| [**CloseColorProfile**](/windows/win32/api/icm/nf-icm-closecolorprofile) | Cierra un identificador de perfil abierto. |
| [**CreateDeviceLinkProfile**](/windows/win32/api/icm/nf-icm-createdevicelinkprofile) | Crea un *Perfil de vínculo de dispositivo* de International color Consortium (ICC) a partir de un conjunto de perfiles de color, con las intenciones especificadas. |
| [**GetColorProfileElement**](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | Copia datos de un elemento de perfil etiquetado especificado de un perfil de color especificado en un búfer. |
| [**GetColorProfileElementTag**](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | Recupera el nombre de etiqueta especificado por *dwIndex* en la tabla de etiquetas de un perfil de color de International color Consortium (ICC) determinado, donde *dwIndex* es un índice basado en uno de la tabla. |
| [**GetColorProfileFromHandle**](/windows/win32/api/icm/nf-icm-getcolorprofilefromhandle)| Recupera el contenido del perfil de color dado un identificador a un perfil de color abierto.     |
| [**GetColorProfileHeader**](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | Recupera o deriva la estructura de encabezado de ICC de un perfil de color ICC o de un perfil XML WCS. Los controladores y las aplicaciones deben suponer que devolver **true** solo indica que se devuelve un encabezado estructurado correctamente. Cada etiqueta todavía tendrá que validarse de forma independiente mediante las API de ICM2 heredadas o las API de esquemas XML. |
| [**GetCountColorProfileElements**](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | Recupera el número de elementos etiquetados en un perfil de color determinado. |
| [**GetPS2ColorRenderingDictionary**](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | Recupera el Diccionario de representación del color PostScript de nivel 2 del perfil de color ICC especificado. |
| [**GetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | Recupera el [intento de representación](r.md) de color PostScript de nivel 2 de un perfil de color ICC. |
| [**GetPS2ColorSpaceArray**](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | Recupera la matriz de [espacio de colores](c.md) PostScript de nivel 2 de un perfil de color ICC. |
| [**IsColorProfileTagPresent**](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | Indica si una etiqueta del consorcio de color internacional (ICC) especificada está presente en el perfil de color especificado. |
| [**IsColorProfileValid**](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | Permite determinar si el perfil especificado es un perfil de International color Consortium (ICC) válido o un identificador de perfil del sistema de colores de Windows (WCS) válido que se puede usar para la administración del color. |
| [**OpenColorProfileW**](/windows/win32/api/icm/nf-icm-opencolorprofilew) | Crea un identificador para un perfil de color especificado. El identificador se puede usar en otras funciones de administración de perfiles. |
| [**SetColorProfileElement**](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | Establece los datos del elemento para un elemento de perfil etiquetado en un perfil de color de ICC. |
| [**SetColorProfileElementReference**](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | Crea en un perfil de color ICC especificado una nueva etiqueta que hace referencia a los mismos datos que una etiqueta existente. |
| [**SetColorProfileElementSize**](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | Establece el tamaño de un elemento etiquetado en un perfil de color de ICC. |
| [**SetColorProfileHeader**](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | Establece los datos de encabezado de un perfil de color ICC especificado. |
| [**WcsGetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | Determina si la administración del sistema del estado de calibración de pantalla está habilitada. |
| [**WcsSetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | Determina si la administración del sistema del estado de calibración de pantalla está habilitada. |



 

 

 




