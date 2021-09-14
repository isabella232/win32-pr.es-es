---
description: Si se establece este bit, las imágenes del cuadro de diálogo se crean con la paleta personalizada (una por cada diálogo recibido del primer control creado). Si el bit no está establecido, las imágenes se representan mediante una paleta predeterminada.
ms.assetid: 9cfc7fd9-27a3-4208-b42c-48369890a74b
title: Usar bit de estilo de diálogoCustomPalette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507ed1c900c564e3e791f4d0bbc5f8658798fdb4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069605"
---
# <a name="usecustompalette-dialog-style-bit"></a>Usar bit de estilo de diálogoCustomPalette

Si se establece este bit, las imágenes del cuadro de diálogo se crean con la paleta personalizada (una por cada diálogo recibido del primer control creado). Si el bit no está establecido, las imágenes se representan mediante una paleta predeterminada.

Normalmente, se establecería este bit si el cuadro de diálogo contiene una imagen con una paleta especial o varias imágenes que comparten una paleta personalizada. El bit no debe establecerse si el cuadro de diálogo contiene varias imágenes con paletas diferentes. En este caso, es más probable que la paleta predeterminada dé un resultado satisfactorio para todas las imágenes.

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                                  |
|---------|-------------|-------------------------------------------|
| 64      | 0x00000040  | **msidbDialogAttributesUseCustomPalette** |



 

 

 



