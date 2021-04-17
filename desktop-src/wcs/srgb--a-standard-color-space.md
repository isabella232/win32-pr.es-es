---
title: 'sRGB: espacio de color estándar'
description: Como resultado de las consideraciones de ancho de banda de Internet, Hewlett-Packard y Microsoft han propuesto la adopción de un espacio de colores predefinido estándar conocido como sRGB (IEC 61966-2-1), para permitir una asignación de color precisa con muy poca sobrecarga de datos.
ms.assetid: b9017702-7dca-4d79-bed0-936f97cb6109
keywords:
- Sistema de color de Windows (WCS), espacio de color sRGB
- WCS (sistema de colores de Windows), espacio de color sRGB
- Administración del color de imagen, espacio de color sRGB
- Administración del color, espacio de color sRGB
- colores, espacio de color sRGB
- espacio de color sRGB
- espacios de colores, sRGB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed3167e44f149982a809826bcb9b64b3ec6e3c24
ms.sourcegitcommit: da13d459791d115df883fa4dd348931d0902c2cc
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/30/2021
ms.locfileid: "105721155"
---
# <a name="srgb-a-standard-color-space"></a>sRGB: un espacio de colores estándar

Como resultado de las consideraciones de ancho de banda de Internet, Hewlett-Packard y Microsoft han propuesto la adopción de un [espacio de colores](c.md) predefinido estándar conocido como *sRGB* (IEC 61966-2-1), para permitir una asignación de [color](c.md) precisa con muy poca sobrecarga de datos.

Hay disponible una versión de archivo de ayuda de una nota del producto en la que se describen los detalles técnicos de sRGB, sRGB. HLP, en la \\ carpeta help de la referencia del programador de WCS 1,0.

Los distintos formatos de archivo pueden usar o agregar una marca para especificar que la imagen está en el espacio de color sRGB. En el formato de mapa de bits independiente del dispositivo (DIB) de Windows, al establecer el miembro **bV5CSType** de la estructura [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) en **LCS \_ sRGB** , se especifica que los colores DIB están en el espacio de color sRGB.

WCS 1,0 proporciona compatibilidad nativa con sRGB. Hay dos maneras de usar WCS 1,0 para representar una imagen definida en el espacio de color sRGB:

**Para representar una imagen dentro del contexto del dispositivo**

1.  Cree un contexto de dispositivo (DC) en el dispositivo de pantalla.
2.  Establezca la administración del color mediante la función [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) .
3.  Utilice la función [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) para transferir el DIB al controlador de dominio. Siempre que el miembro **bV5CSMType** de la estructura DIB [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) esté establecido en **LCS \_ sRGB**, el sistema llevará a cabo la administración de color adecuada.

**Para representar una imagen fuera del contexto del dispositivo**

1.  Cree una transformación mediante [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw). El miembro **lcsCSType** de la estructura [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) señalada por el parámetro *PLogColorSpace* debe establecerse en **LCS \_ sRGB**. El parámetro *hDestProfile* indica el espacio de colores del dispositivo de la pantalla.
2.  Use la transformación color creada para que el color coincida con la imagen antes de mostrarla en el dispositivo.

## <a name="wcs-10-defaults-for-input-color-space-and-output-profile"></a>Valores predeterminados de WCS 1,0 para el espacio de colores de entrada y el perfil de salida

Cuando no se especifica ningún espacio de colores de entrada, de forma predeterminada, WCS 1,0 usa el espacio de color sRGB como espacio de colores de entrada para la [asignación de colores](c.md).

Cuando no se especifica ningún perfil de salida, pero se especifica un dispositivo predeterminado, WCS 1,0 selecciona un perfil de salida predeterminado. Si el dispositivo predeterminado no tiene un perfil asociado, WCS 1,0 usa el espacio de color sRGB como perfil de salida.

En la tabla siguiente se muestran las transformaciones de color resultantes cuando un dispositivo predeterminado no está disponible.



|                                 | Perfil de salida especificado                              | No se ha especificado el perfil de salida                             |
|---------------------------------|-------------------------------------------------------|----------------------------------------------------------|
| Espacio de colores de entrada especificado     | La transformación utiliza los perfiles especificados.                | La transformación convierte el espacio de colores de entrada conocido en sRGB. |
| No se ha especificado el espacio de colores de entrada | La transformación convierte de sRGB a Perfil de salida conocido. | Se presupone la transformación de sRGB a sRGB; no se hace nada. |



 

## <a name="srgb-and-embedded-profiles"></a>Perfiles de sRGB y Embedded

A partir de la versión 2,0 de ICM, las aplicaciones que usan WCS pueden insertar perfiles en las imágenes. Los perfiles incrustados ayudan a las aplicaciones de los usuarios a mantener una apariencia de color coherente incluso si las imágenes se transmiten a través de Internet.

Las imágenes que usan el espacio de colores sRGB no necesitan un perfil de color incrustado. Dado que no tienen ningún perfil incrustado, las imágenes basadas en sRGB son más pequeñas y se pueden transferir más fácilmente entre los canales de datos con ancho de banda limitado.

Las aplicaciones deben establecer la marca de **LCS \_ sRGB** en el encabezado de mapa de bits de la imagen para indicar que la imagen usa el espacio de color sRGB. Para obtener más información, vea [estructuras de encabezado de mapa de bits de Windows](using-structures-in-wcs-1-0.md) y [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).

 

 