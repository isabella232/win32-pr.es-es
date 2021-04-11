---
description: Las capacidades de color de los dispositivos, como las pantallas e impresoras, pueden oscilar entre monocromo y miles de colores.
ms.assetid: 3d71c24c-77f4-4344-91c3-439052402fae
title: Conceptos básicos de color
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 992953bef75b2bab1f33dbd044a9c80387b5ccd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276017"
---
# <a name="color-basics"></a>Conceptos básicos de color

Las capacidades de color de los dispositivos, como las pantallas e impresoras, pueden oscilar entre monocromo y miles de colores. Dado que es posible que una aplicación tenga que generar la salida de los dispositivos a lo largo de este intervalo, debe estar preparado para controlar las diversas funcionalidades de color.

Una aplicación puede detectar el número de colores disponibles para un dispositivo determinado mediante la función [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) para recuperar el valor NUMCOLORS. Este valor especifica el número de colores disponibles para que la aplicación los use. Normalmente, este recuento corresponde a una propiedad física del dispositivo de salida, como el número de tintas de la impresora o el número de señales de color distintas que el adaptador de pantalla puede transmitir al monitor.

Aunque el valor NUMCOLORS especifica el número de colores, no identifica Cuáles son los colores disponibles. Una aplicación puede detectar qué colores están disponibles enumerando todos los lápices que tienen el \_ tipo sólido de PS. Dado que el controlador de dispositivo que admite un dispositivo determinado normalmente tiene una gama completa de lápices sólidos y porque el sistema requiere que los lápices sólidos solo tengan colores que el dispositivo pueda generar, la enumeración de estos lápices suele ser equivalente a la enumeración de los colores. Una aplicación puede enumerar los lápices mediante la función [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) . Para obtener un ejemplo de código, vea [enumerar colores](enumerating-colors.md).

Para obtener más información, vea los temas siguientes:

-   [Valores de color](color-values.md)
-   [Aproximaciones de color y interpolación](color-approximations-and-dithering.md)
-   [Color en mapas de bits](color-in-bitmaps.md)
-   [Combinación de colores](color-mixing.md)

 

 



