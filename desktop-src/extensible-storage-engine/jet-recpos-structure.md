---
description: 'Más información acerca de: estructura de JET_RECPOS'
title: Estructura de JET_RECPOS
TOCTitle: JET_RECPOS Structure
ms:assetid: 7c335120-4b84-4095-8f13-e5315d4996b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269308(v=EXCHG.10)
ms:contentKeyID: 32765598
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e24e16aaac4228f35350f55f57a14f2820add0cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716515"
---
# <a name="jet_recpos-structure"></a><span data-ttu-id="86e8f-103">Estructura de JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="86e8f-103">JET_RECPOS Structure</span></span>


<span data-ttu-id="86e8f-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="86e8f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recpos-structure"></a><span data-ttu-id="86e8f-105">Estructura de JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="86e8f-105">JET_RECPOS Structure</span></span>

<span data-ttu-id="86e8f-106">La estructura **JET_RECPOS** contiene una colección de enteros que representan una posición fraccionaria dentro de un índice.</span><span class="sxs-lookup"><span data-stu-id="86e8f-106">The **JET_RECPOS** structure contains a collection of integers that represent a fractional position within an index.</span></span> <span data-ttu-id="86e8f-107">**centriesLT** es el número de entradas de índice menor que la clave de índice actual.</span><span class="sxs-lookup"><span data-stu-id="86e8f-107">**centriesLT** is the number of index entries less than the current index key.</span></span> <span data-ttu-id="86e8f-108">**centriesInRange** es el número de entradas de índice igual a la clave actual.</span><span class="sxs-lookup"><span data-stu-id="86e8f-108">**centriesInRange** is the number of index entries equal to the current key.</span></span> <span data-ttu-id="86e8f-109">**centriesInRange** no se admite y siempre se devuelve como 1.</span><span class="sxs-lookup"><span data-stu-id="86e8f-109">**centriesInRange** is not supported and is always returned as 1.</span></span> <span data-ttu-id="86e8f-110">**centriesTotal** es el número de entradas de índice en el índice.</span><span class="sxs-lookup"><span data-stu-id="86e8f-110">**centriesTotal** is the number of index entries in the index.</span></span> <span data-ttu-id="86e8f-111">Todos los valores son aproximaciones sin ninguna garantía de precisión.</span><span class="sxs-lookup"><span data-stu-id="86e8f-111">All values are approximations with no guarantee of accuracy.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long centriesLT;
      unsigned long centriesInRange;
      unsigned long centriesTotal;
    } JET_RECPOS;
```

### <a name="members"></a><span data-ttu-id="86e8f-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="86e8f-112">Members</span></span>

<span data-ttu-id="86e8f-113">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="86e8f-113">**cbStruct**</span></span>

<span data-ttu-id="86e8f-114">Tamaño de la estructura de [JET_RETINFO](./jet-retinfo-structure.md) , en bytes.</span><span class="sxs-lookup"><span data-stu-id="86e8f-114">The size of the [JET_RETINFO](./jet-retinfo-structure.md) structure, in bytes.</span></span> <span data-ttu-id="86e8f-115">Este valor confirma la presencia de los campos siguientes.</span><span class="sxs-lookup"><span data-stu-id="86e8f-115">This value confirms the presence of the following fields.</span></span>

<span data-ttu-id="86e8f-116">**centriesLT**</span><span class="sxs-lookup"><span data-stu-id="86e8f-116">**centriesLT**</span></span>

<span data-ttu-id="86e8f-117">Número aproximado de entradas de índice que son menores que la clave actual.</span><span class="sxs-lookup"><span data-stu-id="86e8f-117">The approximate number of index entries less than the current key.</span></span>

<span data-ttu-id="86e8f-118">**centriesInRange**</span><span class="sxs-lookup"><span data-stu-id="86e8f-118">**centriesInRange**</span></span>

<span data-ttu-id="86e8f-119">El número aproximado de entradas de índice igual a la clave actual.</span><span class="sxs-lookup"><span data-stu-id="86e8f-119">The approximate number of index entries equal to the current key.</span></span> <span data-ttu-id="86e8f-120">Este campo siempre se establece en 1, independientemente del número de entradas de índice que sean realmente iguales a la clave actual.</span><span class="sxs-lookup"><span data-stu-id="86e8f-120">This field is always set to 1, regardless of the number of index entries that are actually equal to the current key.</span></span>

<span data-ttu-id="86e8f-121">**centriesTotal**</span><span class="sxs-lookup"><span data-stu-id="86e8f-121">**centriesTotal**</span></span>

<span data-ttu-id="86e8f-122">Número aproximado de entradas en el índice.</span><span class="sxs-lookup"><span data-stu-id="86e8f-122">The approximate number of entries in the index.</span></span>

### <a name="requirements"></a><span data-ttu-id="86e8f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86e8f-123">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86e8f-124"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="86e8f-124"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="86e8f-125">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="86e8f-125">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86e8f-126"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="86e8f-126"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="86e8f-127">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="86e8f-127">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86e8f-128"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="86e8f-128"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="86e8f-129">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="86e8f-129">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="86e8f-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="86e8f-130">See Also</span></span>

[<span data-ttu-id="86e8f-131">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="86e8f-131">JET_RETINFO</span></span>](./jet-retinfo-structure.md)  
[<span data-ttu-id="86e8f-132">JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="86e8f-132">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)
