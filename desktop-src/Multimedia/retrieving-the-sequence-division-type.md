---
title: Recuperar el tipo de división de secuencia
description: Recuperar el tipo de división de secuencia
ms.assetid: 9c7e3482-93a3-4f9c-8b70-a9c733de14fe
keywords:
- Interfaz digital instrumentada (MIDI), tipo de división de secuencia
- MIDI (Interfaz digital instrumentada), tipo de división de secuencia
- Secuenciador DE MCI MIDI, tipo de división
- MCI_STATUS comando
- tipo de división de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b28bb7e32097b888cdd3dec739eaccfc2a37dfe14060168fb11f0a7ca3d00e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801809"
---
# <a name="retrieving-the-sequence-division-type"></a>Recuperar el tipo de división de secuencia

El *tipo de división* de una secuencia de MIDI determina la cantidad de tiempo entre los eventos DE MIDI en la secuencia. Para determinar el tipo de división de una secuencia, use el comando [**MCI \_ STATUS**](mci-status.md) y establezca el **miembro dwItem** de la estructura [**\_ MCI STATUS \_ PARMS**](mci-status-parms.md) en MCI \_ SEQ STATUS \_ \_ DIVTYPE .

Si el **comando MCI \_ STATUS** es correcto, el miembro **dwReturn** de la estructura **MCI \_ STATUS \_ PARMS** contendrá uno de los siguientes valores para indicar el tipo de división.



| Valor                        | Tipo de división                     |
|------------------------------|-----------------------------------|
| MCI \_ SEQ \_ DIV \_ PPQN          | PPQN (nota de partes por trimestre)     |
| MCI \_ SEQ \_ DIV \_ SMPTE \_ 24     | SMPTE, 24 fps (fotogramas por segundo) |
| MCI \_ SEQ \_ DIV \_ SMPTE \_ 25     | SMPTE, 25 fps                     |
| MCI \_ SEQ \_ DIV \_ SMPTE \_ 30     | SMPTE, 30 fps                     |
| MCI \_ SEQ \_ DIV \_ SMPTE \_ 30DROP | SMPTE, fotograma de colocación de 30 fps          |



 

Debe conocer el tipo de división de una secuencia para cambiar o consultar su tempo. No se puede cambiar el tipo de división de una secuencia mediante el secuenciador MCI.

 

 




