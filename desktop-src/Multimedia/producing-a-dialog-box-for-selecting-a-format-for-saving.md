---
title: Generar un cuadro de diálogo para seleccionar un formato para guardar
description: Generar un cuadro de diálogo para seleccionar un formato para guardar
ms.assetid: f833b28c-13e1-497c-bfc4-2e3bc84d7fff
keywords:
- Administrador de compresión de audio (ACM), generar cuadros de diálogo
- ACM (Administrador de compresión de audio), generar cuadros de diálogo
- Ejemplos de ACM, generar cuadros de diálogo
- generar cuadros de diálogo
- acmFormatChoose función)
- Administrador de compresión de audio (ACM), seleccionar formato para guardar
- ACM (Administrador de compresión de audio), seleccionar formato para guardar
- Ejemplos de ACM, seleccionar formato para guardar
- Seleccionar formato para guardar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55df4cd89a04bf1d3dd34512c4014928b6d5d4fb
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/27/2020
ms.locfileid: "104420381"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-saving"></a>Generar un cuadro de diálogo para seleccionar un formato para guardar

Es posible que desee que una aplicación guarde los datos de audio de forma de onda existentes en otro formato. Por ejemplo, un editor de audio de forma de onda podría guardar un archivo de audio de forma de onda como archivo comprimido. Para mostrar solo los formatos de destino sugeridos para un formato de origen especificado en el cuadro de diálogo creado por la función [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , especifique el formato de origen en el miembro **pwfxEnum** y el \_ marcador ACM FORMATENUMF \_ sugerir en el miembro **fdwEnum** de la estructura [**acmFormatChoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) .

Del mismo modo, para obtener una lista de formatos de destino válidos para un formato especificado, use la \_ marca de conversión ACM FORMATENUMF \_ en lugar de la \_ marca de sugerencia FORMATENUMF de ACM \_ .

 

 




