---
description: Las funcionalidades de color de los dispositivos, como las pantallas y las impresoras, pueden oscilar entre monocromática y miles de colores.
ms.assetid: 3d71c24c-77f4-4344-91c3-439052402fae
title: Conceptos básicos de color
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 992953bef75b2bab1f33dbd044a9c80387b5ccd1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258092"
---
# <a name="color-basics"></a>Conceptos básicos de color

Las funcionalidades de color de los dispositivos, como las pantallas y las impresoras, pueden oscilar entre monocromática y miles de colores. Dado que una aplicación puede necesitar generar salidas para dispositivos a lo largo de este intervalo, debe estar preparada para controlar distintas funcionalidades de color.

Una aplicación puede detectar el número de colores disponibles para un dispositivo determinado mediante la función [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) para recuperar el valor NUMCOLORS. Este valor especifica el recuento de colores disponibles para su uso por la aplicación. Normalmente, este recuento corresponde a una propiedad física del dispositivo de salida, como el número de entrada de lápiz en la impresora o el número de señales de color distintas que el adaptador de pantalla puede transmitir al monitor.

Aunque el valor NUMCOLORS especifica el recuento de colores, no identifica cuáles son los colores disponibles. Una aplicación puede detectar qué colores están disponibles enumerando todos los lápices que tienen el tipo PS \_ SOLID. Dado que el controlador de dispositivo que admite un dispositivo determinado normalmente tiene una gama completa de lápices sólidos y porque el sistema requiere que los lápices sólidos solo tengan colores que el dispositivo pueda generar, enumerar estos lápices suele ser equivalente a enumerar los colores. Una aplicación puede enumerar los lápices mediante la [**función EnumObjects.**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) Para obtener un ejemplo de código, [vea Enumerating Colors](enumerating-colors.md).

Para obtener más información, vea los temas siguientes:

-   [Valores de color](color-values.md)
-   [Aproximaciones y dithering de colores](color-approximations-and-dithering.md)
-   [Color en mapas de bits](color-in-bitmaps.md)
-   [Combinación de colores](color-mixing.md)

 

 



