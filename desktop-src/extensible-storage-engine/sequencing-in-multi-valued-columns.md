---
description: Más información acerca de la secuenciación en columnas con varios valores
title: Secuenciación en columnas con varios valores
TOCTitle: Sequencing in Multi-Valued Columns
ms:assetid: 825a1e51-6b18-4bcf-87f2-4223f302186c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269319(v=EXCHG.10)
ms:contentKeyID: 32765609
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 54f4bd7734cb8c1bf5a87eb444c3205d89f4a6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104553578"
---
# <a name="sequencing-in-multi-valued-columns"></a><span data-ttu-id="d5c67-103">Secuenciación en columnas con varios valores</span><span class="sxs-lookup"><span data-stu-id="d5c67-103">Sequencing in Multi-Valued Columns</span></span>


<span data-ttu-id="d5c67-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d5c67-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="sequencing-in-multi-valued-columns"></a><span data-ttu-id="d5c67-105">Secuenciación en columnas con varios valores</span><span class="sxs-lookup"><span data-stu-id="d5c67-105">Sequencing in Multi-Valued Columns</span></span>

<span data-ttu-id="d5c67-106">Los valores de una columna con varios valores se identifican mediante un número de índice denominado *itagSequence*.</span><span class="sxs-lookup"><span data-stu-id="d5c67-106">The values in a multi-valued column are identified by an index number called the *itagSequence*.</span></span> <span data-ttu-id="d5c67-107">Este número es una referencia a un valor único de la columna.</span><span class="sxs-lookup"><span data-stu-id="d5c67-107">This number is a reference to a single value of the column.</span></span> <span data-ttu-id="d5c67-108">Este número se usa cuando se establecen, recuperan o enumeran nuevos valores en la columna.</span><span class="sxs-lookup"><span data-stu-id="d5c67-108">This number is used when new values are set, retrieved, or enumerated in the column.</span></span> <span data-ttu-id="d5c67-109">*ItagSequence* se utiliza en varias estructuras, entre las que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="d5c67-109">The *itagSequence* is used in various structures, including:</span></span>

  - [<span data-ttu-id="d5c67-110">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="d5c67-110">JET_RETINFO</span></span>](./jet-retinfo-structure.md)

  - [<span data-ttu-id="d5c67-111">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="d5c67-111">JET_SETINFO</span></span>](./jet-setinfo-structure.md)

  - [<span data-ttu-id="d5c67-112">JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="d5c67-112">JET_SETCOLUMN</span></span>](./jet-setcolumn-structure.md)

  - [<span data-ttu-id="d5c67-113">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="d5c67-113">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)

  - [<span data-ttu-id="d5c67-114">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="d5c67-114">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)

<span data-ttu-id="d5c67-115">Este *itagSequence* se inicia en 1 para cada valor de la columna con varios valores.</span><span class="sxs-lookup"><span data-stu-id="d5c67-115">This *itagSequence* starts at 1 for every value in the multi-valued column.</span></span> <span data-ttu-id="d5c67-116">El número de secuencia aumenta cuando se agregan nuevos valores a la columna.</span><span class="sxs-lookup"><span data-stu-id="d5c67-116">The sequence number is increased when new values are added to the column.</span></span> <span data-ttu-id="d5c67-117">Al establecer un valor en una columna con un *itagSequence* de 0, se indica que el valor se va a anexar al conjunto de valores que ya se encuentra en esa columna.</span><span class="sxs-lookup"><span data-stu-id="d5c67-117">Setting a value in a column with an *itagSequence* of 0 indicates that the value is to be appended to the set of values already in that column.</span></span> <span data-ttu-id="d5c67-118">El uso de un valor de *itagSequence* mayor que el número de valores establecidos actualmente para una columna tendrá el mismo efecto.</span><span class="sxs-lookup"><span data-stu-id="d5c67-118">Using an *itagSequence* greater than the number of values currently set for a column will have the same effect.</span></span> <span data-ttu-id="d5c67-119">Si se especifica *itagSequence* de un valor existente, se sobrescribirá ese valor, no se insertará uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="d5c67-119">Specifying the *itagSequence* of an existing value will overwrite that value, not insert a new one.</span></span> <span data-ttu-id="d5c67-120">Si se establece un valor existente en NULL, se quitará ese valor del conjunto de valores que ya se encuentra en esa columna.</span><span class="sxs-lookup"><span data-stu-id="d5c67-120">Setting an existing value to NULL will remove that value from the set of values already in that column.</span></span> <span data-ttu-id="d5c67-121">De esta forma, se desactivarán todos los valores subsiguientes de la columna en una ranura, de modo que el acceso posterior a esos valores por *itagSequence* estará en una cantidad inferior a la que se usó anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d5c67-121">This will move all the subsequent values in the column down by one slot such that subsequent access to those values by *itagSequence* will be by a number one less than what was previously used.</span></span>

<span data-ttu-id="d5c67-122">En el diagrama siguiente se muestra un *itagSequence* en una columna con varios valores.</span><span class="sxs-lookup"><span data-stu-id="d5c67-122">The following diagram shows an *itagSequence* in a multi-valued column.</span></span> <span data-ttu-id="d5c67-123">La columna denominada ColA tiene tres entradas: Val1, Val2 y Val3 con *itagSequence* de 1, 2 y 3, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d5c67-123">The column named ColA has three entries: Val1, Val2 and Val3 with *itagSequence* of 1, 2, and 3 respectively.</span></span>

<span data-ttu-id="d5c67-124">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span><span class="sxs-lookup"><span data-stu-id="d5c67-124">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span></span>
