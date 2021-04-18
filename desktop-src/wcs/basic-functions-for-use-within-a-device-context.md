---
title: Funciones básicas para usar en un contexto de dispositivo
description: Las siguientes funciones WCS proporcionan funciones de asignación de color básicas dentro de los contextos de dispositivo. Son útiles para todas las aplicaciones que necesitan implementar la administración del color con baja sobrecarga y mínima intervención del usuario.
ms.assetid: 199fac5e-daba-4aa3-a631-bb1eb2270b2e
keywords:
- Sistema de color de Windows (WCS), funciones
- WCS (sistema de colores de Windows), funciones
- Administración del color de imagen, funciones
- Administración del color, funciones
- colores, funciones
- Referencia WCS, funciones
- referencia de las funciones WCS,
- Sistema de color de Windows (WCS), contextos de dispositivo
- WCS (sistema de colores de Windows), contextos de dispositivo
- Administración del color de imagen, contextos de dispositivo
- Administración del color, contextos de dispositivo
- colores, contextos de dispositivo
- Referencia WCS, contextos de dispositivo
- referencia de WCS, contextos de dispositivo
- contextos de dispositivo
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde99ed077af108ddc20c73f86e17bedfe1d4a8c
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "105721167"
---
# <a name="basic-functions-for-use-within-a-device-context"></a>Funciones básicas para usar en un contexto de dispositivo

Las siguientes funciones WCS proporcionan funciones de [asignación de color](c.md) básicas dentro de los contextos de dispositivo. Son útiles para todas las aplicaciones que necesitan implementar la administración del color con baja sobrecarga y mínima intervención del usuario.



| Función                                                           | Descripción                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CheckColorsInGamut**](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                   | Comprueba si determinados colores se encuentran en la gama de un dispositivo.                                                                                                     |
| [**ColorCorrectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                 | Corrige las entradas de una paleta para un contexto de dispositivo.                                                                                             |
| [**ColorMatchToTarget**](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                   | Realiza la asignación de colores para fines de vista previa.                                                                                                        |
| [**CreateColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                       | Crea un espacio de colores.                                                                                                                              |
| [**DeleteColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                       | Elimina un espacio de colores.                                                                                                                              |
| [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                         | Enumera los perfiles de color de salida disponibles para un contexto de dispositivo determinado.                                                                              |
| [**EnumICMProfilesProcCallback**](/windows/desktop/api/Wingdi/) | Función de devolución de llamada definida por la aplicación para [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa). La aplicación también define el nombre de esta función. |
| [**GetColorSpace**](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | Obtiene el espacio de colores de entrada actual en un contexto de dispositivo. |
| [**GetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                             | Obtiene el perfil de color de salida actual de un contexto de dispositivo.                                                                                          |
| [**GetLogColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                       | Obtiene la estructura [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) de un contexto de dispositivo.                                                                      |
| [**SetColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                             | Establece el espacio de colores de entrada de un contexto de dispositivo.                                                                                                          |
| [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                   | Activa o desactiva la administración del color en un contexto de dispositivo.                                                                                               |
| [**SetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                             | Establece el perfil de color de salida para un contexto de dispositivo determinado.                                                                                           |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)               | Enumera todos los perfiles de color que cumplen los criterios de enumeración en el ámbito de administración de perfiles especificado.                                      |



 

 

 




