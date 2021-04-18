---
title: Funciones de WCS para los módulos de administración de color (CMM) que se van a implementar
description: Los módulos de administración del color (CMMs) implementan las siguientes funciones y se exportan para que el sistema operativo llame a.
ms.assetid: e05129ec-9128-44f0-82c7-f4e01536d7a8
keywords:
- Sistema de color de Windows (WCS), funciones
- WCS (sistema de colores de Windows), funciones
- Administración del color de imagen, funciones
- Administración del color, funciones
- colores, funciones
- Referencia WCS, funciones
- referencia de las funciones WCS,
- Sistema de color de Windows (WCS), módulo de administración de color (CMM)
- WCS (sistema de colores de Windows), módulo de administración del color (CMM)
- Administración del color de imagen, módulo de administración del color (CMM)
- Administración del color, módulo de administración del color (CMM)
- colores, módulo de administración del color (CMM)
- Referencia WCS, módulo de administración de color (CMM)
- referencia de WCS, módulo de administración del color (CMM)
- Módulo de administración del color (CMM)
- CMM (módulo de administración del color)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e9092c49077b1b4dda9e06829329194ec2e261
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721367"
---
# <a name="wcs-functions-for-color-management-modules-cmms-to-implement"></a>Funciones de WCS para los módulos de administración de color (CMM) que se van a implementar

Los módulos de administración del color (CMMs) implementan las siguientes funciones y se exportan para que el sistema operativo llame a.



| Función                                                                     | Descripción                                                                               |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**CMCheckColors**](/windows/win32/api/icm/nf-icm-cmcheckcolors) | Determina si los colores especificados se encuentran dentro de la [gama](./g.md) de salida de una transformación especificada. |
| [**CMCheckColorsInGamut**](/windows/win32/api/icm/nf-icm-cmcheckcolorsingamut) | Determina si los triples de RGB especificados se encuentran en la [gama](./g.md) de salida de una transformación especificada. |
| [**CMCheckRGBs**](/windows/desktop/api/Wingdi/)                                           | Comprueba los colores del mapa de bits con una gama de salida.                                             |
| [**CMConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-cmconvertcolornametoindex) | Convierte los nombres de colores de un espacio de colores con nombre en números de índice de un perfil de color. |
| [**CMConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-cmconvertindextocolorname) | Transforma índices en un espacio de colores en una matriz de nombres de un espacio de colores con nombre. |
| [**CMCreateDeviceLinkProfile**](/windows/win32/api/icm/nf-icm-cmcreatedevicelinkprofile) | Crea un [Perfil de vínculo de dispositivo](./d.md) en el formato especificado por el consorcio de color internacional en su especificación de formato de perfil ICC. |
| [**CMCreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-cmcreatemultiprofiletransform) | Acepta una matriz de perfiles o un [Perfil de vínculo de dispositivo](./d.md) único y crea una transformación de color. Esta transformación es una asignación desde el espacio de colores especificado por el primer perfil hasta el del segundo perfil, y así sucesivamente hasta el último. |
| [**CMCreateProfile**](/windows/win32/api/icm/nf-icm-cmcreateprofile) | Crea un perfil de color de presentación a partir de una estructura [**LOGCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) . |
| [**CMCreateProfileW**](/windows/win32/api/icm/nf-icm-cmcreateprofilew) | Crea un perfil de color de presentación a partir de una estructura [**LOGCOLORSPACEW**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) . |
| [**CMCreateTransform**](/windows/win32/api/icm/nf-icm-cmcreatetransform) | En desuso. No hay ninguna API de reemplazo porque ya no se usaba. No es necesario que los desarrolladores de módulos de CMM alternativos lo implementen. |
| [**CMCreateTransformExt**](/windows/win32/api/icm/nf-icm-cmcreatetransformext) | Crea una transformación de color que se asigna desde una [**LOGCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) de entrada a un espacio de destino opcional y, a continuación, a un dispositivo de salida, utilizando un conjunto de marcas que definen cómo se debe crear la transformación. |
| [**CMCreateTransformExtW**](/windows/win32/api/icm/nf-icm-cmcreatetransformextw) | Crea una transformación de color que se asigna desde una [**LOGCOLORSPACEW**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) de entrada a un espacio de destino opcional y, a continuación, a un dispositivo de salida, utilizando un conjunto de marcas que definen cómo se debe crear la transformación. |
| [**CMCreateTransformW**](/windows/win32/api/icm/nf-icm-cmcreatetransformw) | En desuso. No hay ninguna API de reemplazo porque ya no se usaba. No es necesario que los desarrolladores de módulos de CMM alternativos lo implementen. |
| [**CMDeleteTransform**](/windows/win32/api/icm/nf-icm-cmdeletetransform) | Elimina una transformación de color especificada y libera cualquier memoria asociada a ella. |
| [**CMGetInfo**](/windows/win32/api/icm/nf-icm-cmgetinfo) | Recupera diversa información sobre el módulo de administración del color (CMM). |
| [**CMGetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-cmgetnamedprofileinfo) | Recupera información sobre el perfil de color con nombre especificado. |
| [**CMGetPS2ColorRenderingDictionary**](/windows/desktop/api/Wingdi/) | Obtiene un diccionario de representación de color PostScript.                                             |
| [**CMGetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-cmgetps2colorrenderingintent) | Recupera el [intento de representación](rendering-intents.md) de color PostScript de nivel 2 de un perfil. |
| [**CMGetPS2ColorSpaceArray**](/windows/desktop/api/Wingdi/)                   | Obtiene una matriz de espacio de colores PostScript.                                                      |
| [**CMIsProfileValid**](/windows/win32/api/icm/nf-icm-cmisprofilevalid) | Indica si el perfil determinado es un perfil ICC válido que se puede usar para la administración del color. |
| [**CMTranslateColors**](/windows/win32/api/icm/nf-icm-cmtranslatecolors) | Traduce una matriz de colores de un [espacio de colores](rendering-intents.md) de origen a un espacio de colores de destino usando una transformación de color. |
| [**CMTranslateRGB**](/windows/win32/api/icm/nf-icm-cmtranslatergb) | Convierte un RGBQuad proporcionado por la aplicación en el espacio de [colores](color-spaces.md)del dispositivo. |
| [**CMTranslateRGBs**](/windows/win32/api/icm/nf-icm-cmtranslatergbs) | Convierte un mapa de bits de un [espacio de colores](color-spaces.md) a otro usando una transformación de color. |
| [**CMTranslateRGBsExt**](/windows/win32/api/icm/nf-icm-cmtranslatergbsext) | Convierte un mapa de bits de un formato definido a un formato definido diferente y llama periódicamente a una función de devolución de llamada, si se especifica una, para informar del progreso y permitir que la aplicación que realiza la llamada termine la traducción. |



 

 

 