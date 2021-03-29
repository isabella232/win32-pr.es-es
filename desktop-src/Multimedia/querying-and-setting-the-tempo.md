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
# <a name="querying-and-setting-the-tempo"></a><span data-ttu-id="b7d43-109">Consultar y establecer el tempo</span><span class="sxs-lookup"><span data-stu-id="b7d43-109">Querying and Setting the Tempo</span></span>

<span data-ttu-id="b7d43-110">Para recuperar el tempo de una secuencia, use el comando [**MCI \_ status**](mci-status.md) y establezca el miembro **dwItem** de la estructura de [**\_ \_ parms status de MCI**](mci-status-parms.md) en el valor de MCI \_ Seq \_ status \_ .</span><span class="sxs-lookup"><span data-stu-id="b7d43-110">To retrieve the tempo of a sequence, use the [**MCI\_STATUS**](mci-status.md) command and set the **dwItem** member of the [**MCI\_STATUS\_PARMS**](mci-status-parms.md) structure to MCI\_SEQ\_STATUS\_TEMPO.</span></span> <span data-ttu-id="b7d43-111">Si el comando de **\_ Estado de MCI** es correcto, el miembro **dwReturn** de la estructura de **\_ \_ parms de estado de MCI** contiene el tempo actual.</span><span class="sxs-lookup"><span data-stu-id="b7d43-111">If the **MCI\_STATUS** command is successful, the **dwReturn** member of the **MCI\_STATUS\_PARMS** structure contains the current tempo.</span></span>

<span data-ttu-id="b7d43-112">Para cambiar el tempo, use el comando [**MCI \_ set**](mci-set.md) con la estructura [**MCI \_ Seq \_ set \_ parms**](mci-seq-set-parms.md) , especificando la \_ marca MCI SEQ \_ set \_ temp y estableciendo el miembro **dwTempo** de la estructura en el tempo deseado.</span><span class="sxs-lookup"><span data-stu-id="b7d43-112">To change tempo, use the [**MCI\_SET**](mci-set.md) command with the [**MCI\_SEQ\_SET\_PARMS**](mci-seq-set-parms.md) structure, specifying the MCI\_SEQ\_SET\_TEMPO flag and setting the **dwTempo** member of the structure to the desired tempo.</span></span>

<span data-ttu-id="b7d43-113">La forma en que se representa el tempo depende del tipo de división de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b7d43-113">The way tempo is represented depends on the division type of the sequence.</span></span> <span data-ttu-id="b7d43-114">Si el tipo de división es PPQN, el tempo se representa en pulsaciones por minuto.</span><span class="sxs-lookup"><span data-stu-id="b7d43-114">If the division type is PPQN, the tempo is represented in beats per minute.</span></span> <span data-ttu-id="b7d43-115">Si el tipo de división es uno de los tipos de división SMPTE, el tempo se representa en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="b7d43-115">If the division type is one of the SMPTE division types, the tempo is represented in frames per second.</span></span> <span data-ttu-id="b7d43-116">Para obtener información sobre cómo determinar el tipo de división de una secuencia, vea [recuperar el tipo de división de secuencia](retrieving-the-sequence-division-type.md).</span><span class="sxs-lookup"><span data-stu-id="b7d43-116">For information about determining the division type of a sequence, see [Retrieving the Sequence Division Type](retrieving-the-sequence-division-type.md).</span></span>

 

 




