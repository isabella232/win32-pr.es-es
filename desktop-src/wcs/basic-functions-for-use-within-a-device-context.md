---
title: Funciones básicas para usar en un contexto de dispositivo
description: Las siguientes funciones de WCS ofrecen funcionalidades básicas de asignación de colores en contextos de dispositivo. Son útiles para todas las aplicaciones que necesitan implementar la administración de colores con poca sobrecarga y mínima intervención del usuario.
ms.assetid: 199fac5e-daba-4aa3-a631-bb1eb2270b2e
keywords:
- Windows Sistema de colores (WCS), funciones
- WCS (Windows Color System),functions
- administración de colores de imagen, funciones
- administración de colores, funciones
- colors,functions
- Referencia de WCS, funciones
- referencia de WCS,functions
- Windows Sistema de colores (WCS), contextos de dispositivo
- WCS (Windows color), contextos de dispositivo
- administración de colores de imagen, contextos de dispositivo
- administración de colores, contextos de dispositivo
- colors,device contexts
- Referencia de WCS, contextos de dispositivo
- referencia de WCS, contextos de dispositivo
- contextos de dispositivo
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a934c1737a7eea8b32a9589325e73300db82334a40ee47b411922b89cb61f568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118210984"
---
# <a name="basic-functions-for-use-within-a-device-context"></a>Funciones básicas para usar en un contexto de dispositivo

Las siguientes funciones de WCS ofrecen funcionalidades básicas de [asignación de](c.md) colores en contextos de dispositivo. Son útiles para todas las aplicaciones que necesitan implementar la administración de colores con poca sobrecarga y mínima intervención del usuario.



| Función                                                           | Descripción                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CheckColorsInGamut**](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                   | Comprueba si los colores dados están en la gama de un dispositivo.                                                                                                     |
| [**ColorCorrectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                 | Corrige las entradas de una paleta para un contexto de dispositivo.                                                                                             |
| [**ColorMatchToTarget**](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                   | Realiza la asignación de colores con fines de vista previa.                                                                                                        |
| [**CreateColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                       | Crea un espacio de colores.                                                                                                                              |
| [**DeleteColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                       | Elimina un espacio de colores.                                                                                                                              |
| [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                         | Enumera los perfiles de color de salida disponibles para un contexto de dispositivo determinado.                                                                              |
| [**EnumICMProfilesProcCallback**](/windows/desktop/api/Wingdi/) | Función de devolución de llamada definida por la aplicación [**para EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa). La aplicación también define el nombre de esta función. |
| [**GetColorSpace**](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | Obtiene el espacio de color de entrada actual en un contexto de dispositivo. |
| [**GetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                             | Obtiene el perfil de color de salida actual de un contexto de dispositivo.                                                                                          |
| [**GetLogColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                       | Obtiene la [**estructura LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) de un contexto de dispositivo.                                                                      |
| [**SetColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                             | Establece el espacio de color de entrada de un contexto de dispositivo.                                                                                                          |
| [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                   | Activa o desactiva la administración de colores en un contexto de dispositivo.                                                                                               |
| [**SetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                             | Establece el perfil de color de salida para un contexto de dispositivo determinado.                                                                                           |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)               | Enumera todos los perfiles de color que cumplen los criterios de enumeración en el ámbito de administración de perfiles especificado.                                      |



 

 

 




