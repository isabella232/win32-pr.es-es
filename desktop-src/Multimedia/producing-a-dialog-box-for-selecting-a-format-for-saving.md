---
title: Generar un cuadro de diálogo para seleccionar un formato para guardar
description: Generar un cuadro de diálogo para seleccionar un formato para guardar
ms.assetid: f833b28c-13e1-497c-bfc4-2e3bc84d7fff
keywords:
- Administrador de compresión de audio (ACM), generar cuadros de diálogo
- ACM (administrador de compresión de audio), generar cuadros de diálogo
- Ejemplos de ACM, generar cuadros de diálogo
- generar cuadros de diálogo
- Función acmFormatChoose
- Administrador de compresión de audio (ACM), selección del formato para guardar
- ACM (administrador de compresión de audio), selección del formato para guardar
- Ejemplos de ACM, selección del formato para guardar
- selección del formato para guardar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65288e4a15712ec86bcf48a8f8088da9f6d5944f298119b21766be238168bf3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805785"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-saving"></a>Generar un cuadro de diálogo para seleccionar un formato para guardar

Es posible que desee que una aplicación guarde los datos existentes de audio de forma de onda en otro formato. Por ejemplo, un editor de audio de forma de onda podría guardar un archivo de audio de forma de onda como un archivo comprimido. Para enumerar solo los formatos de destino sugeridos para un formato de origen especificado en el cuadro de diálogo creado por la función [**acmFormatChoose,**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) especifique el formato de origen en el miembro **pwfxEnum** y la marca SUGGEST de ACM FORMATENUMF en el miembro fdwEnum de la estructura \_ \_ [**ACMFORMATCHOOSE.**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) 

De forma similar, para enumerar los formatos de destino válidos para un formato especificado, use la marca ACM FORMATENUMF CONVERT en lugar de la marca \_ \_ \_ ACM FORMATENUMF \_ SUGGEST.

 

 




