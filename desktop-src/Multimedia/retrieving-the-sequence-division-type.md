---
title: Recuperar el tipo de división de secuencia
description: Recuperar el tipo de división de secuencia
ms.assetid: 9c7e3482-93a3-4f9c-8b70-a9c733de14fe
keywords:
- Interfaz digital de instrumentos musicales (MIDI), tipo de división de secuencia
- MIDI (interfaz digital de instrumentos musicales), tipo de división de secuencia
- Secuenciador MIDI de MCI, tipo de división
- Comando MCI_STATUS
- tipo de división de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6586a33fe4a5225fdcdca21e413104388d5831d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994178"
---
# <a name="retrieving-the-sequence-division-type"></a>Recuperar el tipo de división de secuencia

El *tipo de división* de una secuencia MIDI determina la cantidad de tiempo entre los eventos MIDI de la secuencia. Para determinar el tipo de división de una secuencia, use el comando [**MCI \_ status**](mci-status.md) y establezca el miembro **DwItem** de la estructura [**MCI \_ status \_ parms**](mci-status-parms.md) en MCI \_ Seq \_ status \_ DIVTYPE.

Si el comando de **\_ Estado de MCI** se ejecuta correctamente, el miembro **dwReturn** de la estructura de **\_ \_ parms de estado de MCI** contendrá uno de los valores siguientes para indicar el tipo de división.



| Value                        | Tipo de división                     |
|------------------------------|-----------------------------------|
| MCI \_ Seq \_ div \_ PPQN          | PPQN (nota de elementos por trimestre)     |
| MCI \_ Seq \_ div \_ SMPTE \_ 24     | SMPTE, 24 fps (fotogramas por segundo) |
| MCI \_ Seq \_ div \_ SMPTE \_ 25     | SMPTE, 25 fps                     |
| MCI \_ Seq \_ div \_ SMPTE \_ 30     | SMPTE, 30 fps                     |
| MCI \_ Seq \_ div \_ SMPTE \_ 30DROP | SMPTE, 30 fps (fotograma)          |



 

Debe conocer el tipo de división de una secuencia para cambiar o consultar su Temp. No se puede cambiar el tipo de división de una secuencia mediante MCI Sequencer.

 

 




