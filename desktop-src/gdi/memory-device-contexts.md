---
description: Para permitir que las aplicaciones colocan la salida en memoria en lugar de enviarla a un dispositivo real, use un contexto de dispositivo especial para las operaciones de mapa de bits denominado contexto de dispositivo de memoria.
ms.assetid: 0a682dc4-31a4-43c8-b0b1-ab01986b1dac
title: Contextos de dispositivo de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095de04fdf965a87011895015ad7ea6c9782e286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811936"
---
# <a name="memory-device-contexts"></a>Contextos de dispositivo de memoria

Para permitir que las aplicaciones colocan la salida en memoria en lugar de enviarla a un dispositivo real, use un contexto de dispositivo especial para las operaciones de mapa de bits denominado *contexto de dispositivo de memoria*. Un controlador de dominio de memoria permite al sistema tratar una parte de la memoria como un dispositivo virtual. Es una matriz de bits en memoria que una aplicación puede usar temporalmente para almacenar los datos de color de los mapas de bits creados en una superficie de dibujo normal. Dado que el mapa de bits es compatible con el dispositivo, a veces también se hace referencia a un controlador de dominio de memoria como *contexto de dispositivo compatible*.

El controlador de dominio de memoria almacena imágenes de mapa de bits para un dispositivo determinado. Una aplicación puede crear un controlador de memoria mediante una llamada a la función [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc) .

El mapa de bits original de un controlador de dominio de memoria es simplemente un marcador de posición. Sus dimensiones son un píxel en un píxel. Antes de que una aplicación pueda comenzar a dibujar, debe seleccionar un mapa de bits con el ancho y el alto adecuados en el controlador de dominio mediante una llamada a la función [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) . Para crear un mapa de bits de las dimensiones adecuadas, utilice la función [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)o [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) . Una vez seleccionado el mapa de bits en el controlador de dominio de memoria, el sistema reemplaza la matriz de un solo bit por una matriz lo suficientemente grande como para almacenar información de color para el rectángulo de píxeles especificado.

Cuando una aplicación pasa el identificador devuelto por [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc) a una de las funciones de dibujo, la salida solicitada no aparece en la superficie de dibujo de un dispositivo. En su lugar, el sistema almacena la información de color de la línea, curva, texto o región resultante en la matriz de bits. La aplicación puede volver a copiar la imagen almacenada en memoria en una superficie de dibujo llamando a la función [**bitblt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) , identificando el controlador de dominio de memoria como el contexto de dispositivo de origen y un controlador de dominio de pantalla o ventana como el contexto de dispositivo de destino.

Al mostrar un DIB o un DDB creado a partir de un DIB en un dispositivo de paleta, puede mejorar la velocidad a la que se dibuja la imagen organizando la paleta lógica para que coincida con el diseño de la paleta del sistema. Para ello, llame a [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) con el valor NUMRESERVED para obtener el número de colores reservados en el sistema. A continuación, llame a [**GetSystemPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteentries) y rellene la primera y la última entrada de NUMRESERVED/2 de la paleta lógica con los colores del sistema correspondientes. Por ejemplo, si NUMRESERVED es 20, debe rellenar la primera y la última 10 entradas de la paleta lógica con los colores del sistema. A continuación, rellene los colores 256-NUMRESERVED restantes de la paleta lógica (en nuestro ejemplo, los 236 colores restantes) con los colores del DIB y establezca la \_ marca PC nocollapse en cada uno de estos colores.

Para obtener más información sobre el color y las paletas, vea [colores](colors.md). Para obtener más información sobre los mapas de bits y las operaciones de mapa de bits, vea [mapas de bits](bitmaps.md).

 

 



