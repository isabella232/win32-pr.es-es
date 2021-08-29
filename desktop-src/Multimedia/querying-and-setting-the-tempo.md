---
title: Consulta y establecimiento del tempo
description: Consulta y establecimiento del tempo
ms.assetid: 84eba230-88b6-4cba-9e90-ba0b4bcfc691
keywords:
- Interfaz digital de instrumentar música (MIDI), tempo
- MIDI (Interfaz digital instrumenta de música), tempo
- Secuenciador DE MCI MIDI, tempo
- MCI_STATUS comando
- sequence tempo
- Tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5db1c703272a477b36399335b68a81ce1e8711618acf205e702045704b24974
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805725"
---
# <a name="querying-and-setting-the-tempo"></a>Consulta y establecimiento del tempo

Para recuperar el tempo de una secuencia, use el comando [**MCI \_ STATUS**](mci-status.md) y establezca el **miembro dwItem** de la estructura [**\_ MCI STATUS \_ PARMS**](mci-status-parms.md) en MCI \_ SEQ STATUS \_ \_ TEMPO. Si el **comando MCI \_ STATUS** es correcto, el **miembro dwReturn** de la estructura **MCI STATUS \_ \_ PARMS** contiene el tempo actual.

Para cambiar el tempo, use el comando [**MCI \_ SET**](mci-set.md) con la estructura [**MCI \_ SEQ \_ SET \_ PARMS,**](mci-seq-set-parms.md) especificando la marca MCI SEQ SET TEMPO y estableciendo el miembro \_ \_ \_ **dwTempo** de la estructura en el tempo deseado.

La forma en que se representa el tempo depende del tipo de división de la secuencia. Si el tipo de división es PPQN, el tempo se representa en latidos por minuto. Si el tipo de división es uno de los tipos de división SMPTE, el tempo se representa en fotogramas por segundo. Para obtener información sobre cómo determinar el tipo de división de una secuencia, vea [Recuperar el tipo de división de secuencia](retrieving-the-sequence-division-type.md).

 

 




