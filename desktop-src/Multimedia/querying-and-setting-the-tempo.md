---
title: Consultar y establecer el tempo
description: Consultar y establecer el tempo
ms.assetid: 84eba230-88b6-4cba-9e90-ba0b4bcfc691
keywords:
- Interfaz digital de instrumentos musicales (MIDI), Temp.
- MIDI (interfaz digital de instrumentos musicales), Temp.
- Secuenciador MIDI de MCI, Temp.
- Comando MCI_STATUS
- Temp. de secuencia
- ritmo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3927d2f04e1b073b25c262437620325dc5cd040
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780113"
---
# <a name="querying-and-setting-the-tempo"></a>Consultar y establecer el tempo

Para recuperar el tempo de una secuencia, use el comando [**MCI \_ status**](mci-status.md) y establezca el miembro **dwItem** de la estructura de [**\_ \_ parms status de MCI**](mci-status-parms.md) en el valor de MCI \_ Seq \_ status \_ . Si el comando de **\_ Estado de MCI** es correcto, el miembro **dwReturn** de la estructura de **\_ \_ parms de estado de MCI** contiene el tempo actual.

Para cambiar el tempo, use el comando [**MCI \_ set**](mci-set.md) con la estructura [**MCI \_ Seq \_ set \_ parms**](mci-seq-set-parms.md) , especificando la \_ marca MCI SEQ \_ set \_ temp y estableciendo el miembro **dwTempo** de la estructura en el tempo deseado.

La forma en que se representa el tempo depende del tipo de división de la secuencia. Si el tipo de división es PPQN, el tempo se representa en pulsaciones por minuto. Si el tipo de división es uno de los tipos de división SMPTE, el tempo se representa en fotogramas por segundo. Para obtener información sobre cómo determinar el tipo de división de una secuencia, vea [recuperar el tipo de división de secuencia](retrieving-the-sequence-division-type.md).

 

 




