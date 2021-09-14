---
title: Consultar y establecer el tempo
description: Consultar y establecer el tempo
ms.assetid: 84eba230-88b6-4cba-9e90-ba0b4bcfc691
keywords:
- Interfaz digital de instrumentar música (MIDI),tempo
- MIDI (Interfaz digital de instrumentar música),tempo
- Secuenciador DE MCI MIDI, tempo
- MCI_STATUS comando
- sequence tempo
- Tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3927d2f04e1b073b25c262437620325dc5cd040
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171586"
---
# <a name="querying-and-setting-the-tempo"></a>Consultar y establecer el tempo

Para recuperar el tempo de una secuencia, use el comando STATUS de [**MCI \_**](mci-status.md) y establezca el **miembro dwItem** de la estructura [**\_ MCI STATUS \_ PARMS**](mci-status-parms.md) en MCI \_ SEQ STATUS \_ \_ TEMPO. Si el **comando STATUS \_ de MCI** es correcto, el **miembro dwReturn** de la estructura **\_ MCI STATUS \_ PARMS** contiene el tempo actual.

Para cambiar el tempo, use el comando [**MCI \_ SET**](mci-set.md) con la estructura [**MCI \_ SEQ \_ SET \_ PARMS,**](mci-seq-set-parms.md) especificando la marca MCI SEQ SET TEMPO y estableciendo el miembro \_ \_ \_ **dwTempo** de la estructura en el tempo deseado.

La forma en que se representa el tempo depende del tipo de división de la secuencia. Si el tipo de división es PPQN, el tempo se representa en latidos por minuto. Si el tipo de división es uno de los tipos de división SMPTE, el tempo se representa en fotogramas por segundo. Para obtener información sobre cómo determinar el tipo de división de una secuencia, vea [Recuperar el tipo de división de secuencia](retrieving-the-sequence-division-type.md).

 

 




