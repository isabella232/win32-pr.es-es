---
description: 'Más información acerca de: estructura de JET_RECSIZE'
title: Estructura de JET_RECSIZE
TOCTitle: JET_RECSIZE Structure
ms:assetid: bb2a63bb-7956-46c2-9791-0d0678a6c366
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294072(v=EXCHG.10)
ms:contentKeyID: 32765687
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4e6b2f313a5411ba5bfeea73db3b01afe007612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808540"
---
# <a name="jet_recsize-structure"></a><span data-ttu-id="7e8f6-103">Estructura de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="7e8f6-103">JET_RECSIZE Structure</span></span>


<span data-ttu-id="7e8f6-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7e8f6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recsize-structure"></a><span data-ttu-id="7e8f6-105">Estructura de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="7e8f6-105">JET_RECSIZE Structure</span></span>

<span data-ttu-id="7e8f6-106">[JetGetRecordSize](./jetgetrecordsize-function.md) utiliza la estructura de **JET_RECSIZE** para devolver información sobre los requisitos de uso de un registro en el espacio de datos del usuario, el número de columnas establecidas, el número de valores y el espacio de sobrecarga de la estructura de los registros de ese.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-106">The **JET_RECSIZE** structure is used by [JetGetRecordSize](./jetgetrecordsize-function.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESE record structure overhead space.</span></span>

<span data-ttu-id="7e8f6-107">**Windows Vista:** La estructura de **JET_RECSIZE** se introduce en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-107">**Windows Vista:** The **JET_RECSIZE** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct {
      unsigned __int64 cbData;
      unsigned __int64 cbLongValueData;
      unsigned __int64 cbOverhead;
      unsigned __int64 cbLongValueOverhead;
      unsigned __int64 cNonTaggedColumns;
      unsigned __int64 cTaggedColumns;
      unsigned __int64 cLongValues;
      unsigned __int64 cMultiValues;
    } JET_RECSIZE;
```

### <a name="members"></a><span data-ttu-id="7e8f6-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7e8f6-108">Members</span></span>

<span data-ttu-id="7e8f6-109">**cbData**</span><span class="sxs-lookup"><span data-stu-id="7e8f6-109">**cbData**</span></span>

<span data-ttu-id="7e8f6-110">Conjunto de datos de usuario en el registro.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-110">User data set in the record.</span></span>

<span data-ttu-id="7e8f6-111">**Nota:**  El tamaño de la clave no se incluye en este.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-111">**Note**  The key size is not included in this.</span></span>

<span data-ttu-id="7e8f6-112">**cbLongValueData**</span><span class="sxs-lookup"><span data-stu-id="7e8f6-112">**cbLongValueData**</span></span>

<span data-ttu-id="7e8f6-113">Datos de usuario asociados al registro pero almacenados en el árbol de valores largos.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-113">User data associated with the record but stored in the long-value tree.</span></span>

<span data-ttu-id="7e8f6-114">**Nota:**  Esto no cuenta los valores largos intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-114">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="7e8f6-115">**cbOverhead**</span><span class="sxs-lookup"><span data-stu-id="7e8f6-115">**cbOverhead**</span></span>

<span data-ttu-id="7e8f6-116">Sobrecarga de la estructura de registros de ESE para este registro.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-116">The overhead of the ESE record structure for this record.</span></span> <span data-ttu-id="7e8f6-117">Esto incluye el tamaño de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-117">This includes the record's key size.</span></span>

<span data-ttu-id="7e8f6-118">**cbLongValueOverhead**</span><span class="sxs-lookup"><span data-stu-id="7e8f6-118">**cbLongValueOverhead**</span></span>

<span data-ttu-id="7e8f6-119">Sobrecarga de los datos de valor largo.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-119">The overhead of the long-value data.</span></span>

<span data-ttu-id="7e8f6-120">**Nota:**  Esto no cuenta los valores largos intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-120">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="7e8f6-121">**cNonTaggedColumns**</span><span class="sxs-lookup"><span data-stu-id="7e8f6-121">**cNonTaggedColumns**</span></span>

<span data-ttu-id="7e8f6-122">Número total de columnas fijas y variables establecidas en este registro.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-122">Total number of fixed and variable columns set in this record.</span></span>

<span data-ttu-id="7e8f6-123">**cTaggedColumns**</span><span class="sxs-lookup"><span data-stu-id="7e8f6-123">**cTaggedColumns**</span></span>

<span data-ttu-id="7e8f6-124">Número total de columnas etiquetadas establecidas en este registro.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-124">Total number of tagged columns set in this record.</span></span>

<span data-ttu-id="7e8f6-125">**cLongValues**</span><span class="sxs-lookup"><span data-stu-id="7e8f6-125">**cLongValues**</span></span>

<span data-ttu-id="7e8f6-126">Número total de valores Long almacenados en el árbol de valor largo para este registro.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-126">Total number of long values stored in the long-value tree for this record.</span></span>

<span data-ttu-id="7e8f6-127">**Nota:**  Esto no cuenta los valores largos intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-127">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="7e8f6-128">**cMultiValues**</span><span class="sxs-lookup"><span data-stu-id="7e8f6-128">**cMultiValues**</span></span>

<span data-ttu-id="7e8f6-129">La acumulación del número total de valores más allá de la primera para todas las columnas del registro.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-129">The accumulation of the total number of values beyond the first for all columns in the record.</span></span>

### <a name="remarks"></a><span data-ttu-id="7e8f6-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e8f6-130">Remarks</span></span>

<span data-ttu-id="7e8f6-131">El número total de valores del registro sería **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-131">The total number of values in the record would be **cMultiValues** + **cNonTaggedColumns** + **cTaggedColumns**.</span></span>

### <a name="requirements"></a><span data-ttu-id="7e8f6-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e8f6-132">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e8f6-133"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="7e8f6-133"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7e8f6-134">Requiere Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-134">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e8f6-135"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7e8f6-135"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7e8f6-136">Requiere Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-136">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e8f6-137"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="7e8f6-137"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7e8f6-138">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="7e8f6-138">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="7e8f6-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7e8f6-139">See Also</span></span>

[<span data-ttu-id="7e8f6-140">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="7e8f6-140">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)
