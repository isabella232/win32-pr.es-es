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
ms.openlocfilehash: 55df4cd89a04bf1d3dd34512c4014928b6d5d4fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169533"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-saving"></a>Generar un cuadro de diálogo para seleccionar un formato para guardar

Es posible que quiera que una aplicación guarde los datos existentes de audio de forma de onda en otro formato. Por ejemplo, un editor de audio de forma de onda podría guardar un archivo de audio de forma de onda como un archivo comprimido. Para enumerar solo los formatos de destino sugeridos para un formato de origen especificado en el cuadro de diálogo creado por la función [**acmFormatChoose,**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) especifique el formato de origen en el miembro **pwfxEnum** y la marca SUGGEST de ACM FORMATENUMF en el miembro fdwEnum de la estructura \_ \_ [**ACMFORMATCHOOSE.**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) 

De forma similar, para enumerar los formatos de destino válidos para un formato especificado, use la marca CONVERT de ACM FORMATENUMF en lugar de la marca SUGGEST de \_ \_ ACM \_ FORMATENUMF. \_

 

 




