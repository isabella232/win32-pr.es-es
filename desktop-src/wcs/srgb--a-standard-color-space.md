---
title: 'sRGB: espacio de color estándar'
description: Como resultado de las consideraciones sobre el ancho de banda de Internet, Hewlett-Packard y Microsoft han propuesto la adopción de un espacio de colores predefinido estándar conocido como sRGB (IEC 61966-2-1), para permitir una asignación de color precisa con muy poca sobrecarga de datos.
ms.assetid: b9017702-7dca-4d79-bed0-936f97cb6109
keywords:
- Windows Sistema de colores (WCS), espacio de colores sRGB
- WCS (Windows de colores), espacio de colores sRGB
- administración de colores de imagen, espacio de colores sRGB
- administración de colores, espacio de colores sRGB
- colors,sRGB color space
- espacio de colores sRGB
- espacios de colores, sRGB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0779ec79868a6ec6d78e447b7ee3473847b8fdc1ffa165897abd2dcbcb7a0793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965924"
---
# <a name="srgb-a-standard-color-space"></a>sRGB: un espacio de colores estándar

Como resultado de las consideraciones sobre el ancho de banda de Internet, Hewlett-Packard y Microsoft han propuesto la adopción de un espacio de [colores](c.md) predefinido estándar conocido como *sRGB* (IEC 61966-2-1), para permitir una asignación de [color](c.md) precisa con muy poca sobrecarga de datos.

Hay disponible una versión del archivo de ayuda de un documento técnico que describe los detalles técnicos de sRGB, sRGB.hlp, en la carpeta Ayuda de la referencia del programador de \\ WCS 1.0.

Diferentes formatos de archivo pueden usar o agregar una marca para especificar que la imagen está en un espacio de colores sRGB. En el formato de mapa de bits independiente del dispositivo (DIB) de Windows, al establecer el miembro **bV5CSType** de la estructura [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) en **LCS \_ sRGB** se especifica que los colores DIB están en el espacio de colores sRGB.

WCS 1.0 proporciona compatibilidad nativa con sRGB. Hay dos maneras de usar WCS 1.0 para representar una imagen definida en el espacio de colores sRGB:

**Para representar una imagen dentro del contexto del dispositivo**

1.  Cree un contexto de dispositivo (DC) en el dispositivo de visualización.
2.  Establezca la administración de colores mediante [**la función SetICMMode.**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)
3.  Use la [**función SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) para transferir la DIB al controlador de dominio. Siempre que el miembro **bV5CSMType** de la estructura DIBs [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) esté establecido en **LCS \_ sRGB,** el sistema realizará la administración de colores adecuada.

**Para representar una imagen fuera del contexto del dispositivo**

1.  Cree una transformación mediante [**CreateColorTransformW.**](/windows/win32/api/icm/nf-icm-createcolortransformw) El **miembro lcsCSType** de la estructura [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) a la que apunta el parámetro *pLogColorSpace* debe establecerse en **LCS \_ sRGB.** El *parámetro hDestProfile* indica el espacio de color del dispositivo para mostrar.
2.  Use la transformación de color creada para que el color coincida con la imagen antes de mostrarla en el dispositivo.

## <a name="wcs-10-defaults-for-input-color-space-and-output-profile"></a>Valores predeterminados de WCS 1.0 para el espacio de color de entrada y el perfil de salida

Cuando no se especifica ningún espacio de color de entrada, de forma predeterminada WCS 1.0 usa el espacio de colores sRGB como espacio de color de entrada para la asignación [de colores](c.md).

Cuando no se especifica ningún perfil de salida, pero se especifica un dispositivo predeterminado, WCS 1.0 selecciona un perfil de salida predeterminado. Si el dispositivo predeterminado no tiene un perfil asociado, WCS 1.0 usa el espacio de color sRGB como perfil de salida.

En la tabla siguiente se muestran las transformaciones de color resultantes cuando un dispositivo predeterminado no está disponible.



|  &nbsp;                               | Perfil de salida especificado                              | Perfil de salida no especificado                             |
|---------------------------------|-------------------------------------------------------|----------------------------------------------------------|
| Espacio de color de entrada especificado     | La transformación usa los perfiles especificados.                | La transformación convierte el espacio de color de entrada conocido en sRGB. |
| Espacio de color de entrada no especificado | La transformación convierte de sRGB a un perfil de salida conocido. | Se supone que la transformación de sRGB a sRGB; no se hace nada. |



 

## <a name="srgb-and-embedded-profiles"></a>sRGB y perfiles incrustados

A partir ICM versión 2.0, las aplicaciones que usan WCS pueden insertar perfiles en imágenes. Los perfiles insertados ayudan a las aplicaciones de los usuarios a mantener una apariencia de color coherente, incluso si las imágenes se transmiten a través de Internet.

Las imágenes que usan el espacio de colores sRGB no necesitan un perfil de color incrustado. Dado que no tienen ningún perfil incrustado, las imágenes basadas en sRGB son más pequeñas y fáciles de transferir a través de canales de datos con ancho de banda limitado.

Las aplicaciones deben establecer la **marca \_ sRGB** de LCS en el encabezado de mapa de bits de la imagen para indicar que la imagen usa el espacio de colores sRGB. Para obtener más información, [vea Windows De encabezado de mapa de bits](using-structures-in-wcs-1-0.md) y [**LOGCOLORSPACE.**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea)

 

 