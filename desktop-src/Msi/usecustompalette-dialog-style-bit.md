---
description: Si se establece este bit, las imágenes del cuadro de diálogo se crean con la paleta personalizada (una por cada diálogo recibido del primer control creado). Si no se establece el bit, las imágenes se representan mediante una paleta predeterminada.
ms.assetid: 9cfc7fd9-27a3-4208-b42c-48369890a74b
title: Usar bit de estilo de diálogoCustomPalette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9863f9b20ad85caf3712c3cfa00fd88de72f82b947a329d367d06f02ba06163
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809485"
---
# <a name="usecustompalette-dialog-style-bit"></a>Usar bit de estilo de diálogoCustomPalette

Si se establece este bit, las imágenes del cuadro de diálogo se crean con la paleta personalizada (una por cada diálogo recibido del primer control creado). Si no se establece el bit, las imágenes se representan mediante una paleta predeterminada.

Normalmente se establecería este bit si el cuadro de diálogo contiene una imagen con una paleta especial o varias imágenes que comparten una paleta personalizada. El bit no debe establecerse si el cuadro de diálogo contiene varias imágenes con paletas diferentes. En este caso, es más probable que la paleta predeterminada dé un resultado satisfactorio para todas las imágenes.

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                                  |
|---------|-------------|-------------------------------------------|
| 64      | 0x00000040  | **msidbDialogAttributesUseCustomPalette** |



 

 

 



