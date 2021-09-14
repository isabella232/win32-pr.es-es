---
title: Recuperar el tipo de división de secuencia
description: Recuperar el tipo de división de secuencia
ms.assetid: 9c7e3482-93a3-4f9c-8b70-a9c733de14fe
keywords:
- Interfaz digital de instrumentar música (MIDI), tipo de división de secuencia
- MIDI (Interfaz digital instrumentada), tipo de división de secuencia
- Secuenciador DE MCI MIDI, tipo de división
- MCI_STATUS comando
- tipo de división de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6586a33fe4a5225fdcdca21e413104388d5831d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171530"
---
# <a name="retrieving-the-sequence-division-type"></a>Recuperar el tipo de división de secuencia

El *tipo de división* de una secuencia MIDI determina la cantidad de tiempo entre los eventos DE MIDI de la secuencia. Para determinar el tipo de división de una secuencia, use el comando STATUS de [**MCI \_**](mci-status.md) y establezca el **miembro dwItem** de la estructura [**\_ MCI STATUS \_ PARMS**](mci-status-parms.md) en MCI \_ SEQ STATUS \_ \_ DIVTYPE .

Si el **comando STATUS \_ de MCI** es correcto, el **miembro dwReturn** de la estructura **\_ MCI STATUS \_ PARMS** contendrá uno de los siguientes valores para indicar el tipo de división.



| Value                        | Tipo de división                     |
|------------------------------|-----------------------------------|
| MCI \_ SEQ \_ DIV \_ PPQN          | PPQN (nota de partes por trimestre)     |
| MCI \_ SEQ \_ DIV \_ SMPTE \_ 24     | SMPTE, 24 fps (fotogramas por segundo) |
| MCI \_ SEQ \_ DIV \_ SMPTE \_ 25     | SMPTE, 25 fps                     |
| MCI \_ SEQ \_ DIV \_ SMPTE \_ 30     | SMPTE, 30 fps                     |
| MCI \_ SEQ \_ DIV \_ SMPTE \_ 30DROP | SMPTE, fotograma desplegable de 30 fps          |



 

Debe conocer el tipo de división de una secuencia para cambiar o consultar su tempo. No se puede cambiar el tipo de división de una secuencia mediante el secuenciador MCI.

 

 




