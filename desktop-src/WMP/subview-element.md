---
title: Elemento de la subvista
description: Elemento de la subvista
ms.assetid: 6201df82-8688-4ada-a660-b66e93723f63
keywords:
- Aspectos de Windows Media Player, elemento de subvista
- máscaras, elemento de subvista
- Elemento de la subvista
- referencia de máscaras, elemento de subvista
- elementos, subvistas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f6ed8088d2e79677e542785b4bab1c3c90dcdcf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357568"
---
# <a name="subview-element"></a>Elemento de la subvista

El elemento de la **subvista** proporciona una manera de manipular una parte de una máscara, por ejemplo, para proporcionar un panel de control que se puede ocultar cuando no se está utilizando. Los elementos de la **vista** secundaria siempre son elementos secundarios de los elementos de la **vista** primaria y pueden contener otros elementos de máscara, excepto **Ver**, **tema** y **otros elementos de la vista secundaria** .

El elemento de la **subvista** admite los atributos siguientes, que se definen bajo el elemento de **vista** .



| Atributo                                                       | Descripción                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [backgroundColor](view-backgroundcolor.md)                     | Especifica o recupera el color de fondo del control de la **subvista** . El valor predeterminado es "none".        |
| [backgroundImage](view-backgroundimage.md)                     | Especifica o recupera la imagen de fondo del control de **subvista** .                                     |
| [backgroundImageHueShift](view-backgroundimagehueshift.md)     | Especifica o recupera la cantidad por la que se desplaza el matiz de la imagen de fondo.                      |
| [backgroundImageSaturation](view-backgroundimagesaturation.md) | Especifica o recupera el valor de saturación de la imagen de fondo.                                        |
| [backgroundTiled](view-backgroundtiled.md)                     | Especifica o recupera un valor que indica si la imagen de fondo del control de **subvista** está en mosaico. |
| [resizeBackgroundImage](view-resizebackgroundimage.md)         | Especifica o recupera un valor que indica si se puede cambiar el tamaño de la imagen de fondo.                      |
| [Property](view-transparencycolor.md)                 | Especifica o recupera el color de transparencia de la imagen de fondo.                                      |



 

El elemento de la **subvista** admite los atributos de ambiente, excepto donde se indique. Para obtener más información, consulte [atributos de ambiente](ambient-attributes.md).

El elemento de la **subvista** puede implementar los controladores de eventos ambiente siguientes: [onendmove](onendmove.md) y [OnResize](onresize.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de máscara**](skin-programming-reference.md)
</dt> <dt>

[**Elemento de vista**](view-element.md)
</dt> </dl>

 

 




