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
# <a name="retrieving-the-sequence-division-type"></a><span data-ttu-id="58de5-108">Recuperar el tipo de división de secuencia</span><span class="sxs-lookup"><span data-stu-id="58de5-108">Retrieving the Sequence Division Type</span></span>

<span data-ttu-id="58de5-109">El *tipo de división* de una secuencia MIDI determina la cantidad de tiempo entre los eventos MIDI de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="58de5-109">The *division type* of a MIDI sequence determines the amount of time between MIDI events in the sequence.</span></span> <span data-ttu-id="58de5-110">Para determinar el tipo de división de una secuencia, use el comando [**MCI \_ status**](mci-status.md) y establezca el miembro **DwItem** de la estructura [**MCI \_ status \_ parms**](mci-status-parms.md) en MCI \_ Seq \_ status \_ DIVTYPE.</span><span class="sxs-lookup"><span data-stu-id="58de5-110">To determine the division type of a sequence, use the [**MCI\_STATUS**](mci-status.md) command and set the **dwItem** member of the [**MCI\_STATUS\_PARMS**](mci-status-parms.md) structure to MCI\_SEQ\_STATUS\_DIVTYPE .</span></span>

<span data-ttu-id="58de5-111">Si el comando de **\_ Estado de MCI** se ejecuta correctamente, el miembro **dwReturn** de la estructura de **\_ \_ parms de estado de MCI** contendrá uno de los valores siguientes para indicar el tipo de división.</span><span class="sxs-lookup"><span data-stu-id="58de5-111">If the **MCI\_STATUS** command is successful, the **dwReturn** member of the **MCI\_STATUS\_PARMS** structure will contain one of the following values to indicate the division type.</span></span>



| <span data-ttu-id="58de5-112">Value</span><span class="sxs-lookup"><span data-stu-id="58de5-112">Value</span></span>                        | <span data-ttu-id="58de5-113">Tipo de división</span><span class="sxs-lookup"><span data-stu-id="58de5-113">Division type</span></span>                     |
|------------------------------|-----------------------------------|
| <span data-ttu-id="58de5-114">MCI \_ Seq \_ div \_ PPQN</span><span class="sxs-lookup"><span data-stu-id="58de5-114">MCI\_SEQ\_DIV\_PPQN</span></span>          | <span data-ttu-id="58de5-115">PPQN (nota de elementos por trimestre)</span><span class="sxs-lookup"><span data-stu-id="58de5-115">PPQN (parts-per-quarter note)</span></span>     |
| <span data-ttu-id="58de5-116">MCI \_ Seq \_ div \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="58de5-116">MCI\_SEQ\_DIV\_SMPTE\_24</span></span>     | <span data-ttu-id="58de5-117">SMPTE, 24 fps (fotogramas por segundo)</span><span class="sxs-lookup"><span data-stu-id="58de5-117">SMPTE, 24 fps (frames per second)</span></span> |
| <span data-ttu-id="58de5-118">MCI \_ Seq \_ div \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="58de5-118">MCI\_SEQ\_DIV\_SMPTE\_25</span></span>     | <span data-ttu-id="58de5-119">SMPTE, 25 fps</span><span class="sxs-lookup"><span data-stu-id="58de5-119">SMPTE, 25 fps</span></span>                     |
| <span data-ttu-id="58de5-120">MCI \_ Seq \_ div \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="58de5-120">MCI\_SEQ\_DIV\_SMPTE\_30</span></span>     | <span data-ttu-id="58de5-121">SMPTE, 30 fps</span><span class="sxs-lookup"><span data-stu-id="58de5-121">SMPTE, 30 fps</span></span>                     |
| <span data-ttu-id="58de5-122">MCI \_ Seq \_ div \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="58de5-122">MCI\_SEQ\_DIV\_SMPTE\_30DROP</span></span> | <span data-ttu-id="58de5-123">SMPTE, 30 fps (fotograma)</span><span class="sxs-lookup"><span data-stu-id="58de5-123">SMPTE, 30 fps drop frame</span></span>          |



 

<span data-ttu-id="58de5-124">Debe conocer el tipo de división de una secuencia para cambiar o consultar su Temp.</span><span class="sxs-lookup"><span data-stu-id="58de5-124">You must know the division type of a sequence to change or query its tempo.</span></span> <span data-ttu-id="58de5-125">No se puede cambiar el tipo de división de una secuencia mediante MCI Sequencer.</span><span class="sxs-lookup"><span data-stu-id="58de5-125">You cannot change the division type of a sequence by using the MCI sequencer.</span></span>

 

 




