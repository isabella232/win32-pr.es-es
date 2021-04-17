---
description: Si se establece este bit, se crean las imágenes en el cuadro de diálogo con la paleta personalizada (una por cada cuadro de diálogo recibido del primer control creado). Si no se establece el bit, las imágenes se representan utilizando una paleta predeterminada.
ms.assetid: 9cfc7fd9-27a3-4208-b42c-48369890a74b
title: Bit de estilo del cuadro de diálogo UseCustomPalette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507ed1c900c564e3e791f4d0bbc5f8658798fdb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653049"
---
# <a name="usecustompalette-dialog-style-bit"></a>Bit de estilo del cuadro de diálogo UseCustomPalette

Si se establece este bit, se crean las imágenes en el cuadro de diálogo con la paleta personalizada (una por cada cuadro de diálogo recibido del primer control creado). Si no se establece el bit, las imágenes se representan utilizando una paleta predeterminada.

Normalmente, se establece este bit si el cuadro de diálogo contiene una imagen con una paleta especial o varias imágenes que comparten una paleta personalizada. No se debe establecer el bit si el cuadro de diálogo contiene varias imágenes con diferentes paletas. En este caso, es más probable que la paleta predeterminada proporcione un resultado satisfactorio para todas las imágenes.

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                                  |
|---------|-------------|-------------------------------------------|
| 64      | 0x00000040  | **msidbDialogAttributesUseCustomPalette** |



 

 

 



