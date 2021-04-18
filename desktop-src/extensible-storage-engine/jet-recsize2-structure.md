---
description: 'Más información acerca de: estructura de JET_RECSIZE2'
title: Estructura de JET_RECSIZE2
TOCTitle: JET_RECSIZE2 Structure
ms:assetid: 02a13b5b-d904-49b2-baaa-c60328d70290
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269174(v=EXCHG.10)
ms:contentKeyID: 32765477
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
ms.openlocfilehash: 2fd16480f0ec059c977d07f8e445a35094c5f2fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706720"
---
# <a name="jet_recsize2-structure"></a><span data-ttu-id="f9640-103">Estructura de JET_RECSIZE2</span><span class="sxs-lookup"><span data-stu-id="f9640-103">JET_RECSIZE2 Structure</span></span>


<span data-ttu-id="f9640-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f9640-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recsize2-structure"></a><span data-ttu-id="f9640-105">Estructura de JET_RECSIZE2</span><span class="sxs-lookup"><span data-stu-id="f9640-105">JET_RECSIZE2 Structure</span></span>

<span data-ttu-id="f9640-106">[JetGetRecordSize2](./jetgetrecordsize2-function.md) utiliza la estructura de **JET_RECSIZE2** para devolver información sobre los requisitos de uso de un registro en el espacio de datos del usuario, el número de columnas establecidas, el número de valores y el espacio de sobrecarga de la estructura de los registros de ese.</span><span class="sxs-lookup"><span data-stu-id="f9640-106">The **JET_RECSIZE2** structure is used by [JetGetRecordSize2](./jetgetrecordsize2-function.md) to return information about a record's usage requirements in user data space, number of set columns, number of values, and ESE record structure overhead space.</span></span>

<span data-ttu-id="f9640-107">**Windows 7:** La estructura de **JET_RECSIZE2** se introduce en el sistema operativo Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f9640-107">**Windows 7:** The **JET_RECSIZE2** structure is introduced in the Windows 7 operating system.</span></span>

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
      unsigned __int64 cCompressedColumns;
      unsigned __int64 cbDataCompressed;
      unsigned __int64 cbLongValueDataCompressed;
    } JET_RECSIZE2;
```

### <a name="members"></a><span data-ttu-id="f9640-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f9640-108">Members</span></span>

<span data-ttu-id="f9640-109">**cbData**</span><span class="sxs-lookup"><span data-stu-id="f9640-109">**cbData**</span></span>

<span data-ttu-id="f9640-110">Conjunto de datos de usuario en el registro.</span><span class="sxs-lookup"><span data-stu-id="f9640-110">User data set in the record.</span></span>

<span data-ttu-id="f9640-111">**Nota:**  El tamaño de la clave no se incluye en este.</span><span class="sxs-lookup"><span data-stu-id="f9640-111">**Note**  The key size is not included in this.</span></span>

<span data-ttu-id="f9640-112">**cbLongValueData**</span><span class="sxs-lookup"><span data-stu-id="f9640-112">**cbLongValueData**</span></span>

<span data-ttu-id="f9640-113">Datos de usuario asociados al registro pero almacenados en el árbol de valores largos.</span><span class="sxs-lookup"><span data-stu-id="f9640-113">User data associated with the record but stored in the long-value tree.</span></span>

<span data-ttu-id="f9640-114">**Nota:**  Esto no cuenta los valores largos intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="f9640-114">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="f9640-115">**cbOverhead**</span><span class="sxs-lookup"><span data-stu-id="f9640-115">**cbOverhead**</span></span>

<span data-ttu-id="f9640-116">Sobrecarga de la estructura de registros de ESE para este registro.</span><span class="sxs-lookup"><span data-stu-id="f9640-116">The overhead of the ESE record structure for this record.</span></span> <span data-ttu-id="f9640-117">Esto incluye el tamaño de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="f9640-117">This includes the record's key size.</span></span>

<span data-ttu-id="f9640-118">**cbLongValueOverhead**</span><span class="sxs-lookup"><span data-stu-id="f9640-118">**cbLongValueOverhead**</span></span>

<span data-ttu-id="f9640-119">Sobrecarga de los datos de valor largo.</span><span class="sxs-lookup"><span data-stu-id="f9640-119">The overhead of the long-value data.</span></span>

<span data-ttu-id="f9640-120">**Nota:**  Esto no cuenta los valores largos intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="f9640-120">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="f9640-121">**cNonTaggedColumns**</span><span class="sxs-lookup"><span data-stu-id="f9640-121">**cNonTaggedColumns**</span></span>

<span data-ttu-id="f9640-122">Número total de columnas fijas y variables establecidas en este registro.</span><span class="sxs-lookup"><span data-stu-id="f9640-122">Total number of fixed and variable columns set in this record.</span></span>

<span data-ttu-id="f9640-123">**cTaggedColumns**</span><span class="sxs-lookup"><span data-stu-id="f9640-123">**cTaggedColumns**</span></span>

<span data-ttu-id="f9640-124">Número total de columnas etiquetadas establecidas en este registro.</span><span class="sxs-lookup"><span data-stu-id="f9640-124">Total number of tagged columns set in this record.</span></span>

<span data-ttu-id="f9640-125">**cLongValues**</span><span class="sxs-lookup"><span data-stu-id="f9640-125">**cLongValues**</span></span>

<span data-ttu-id="f9640-126">Número total de valores Long almacenados en el árbol de valor largo para este registro.</span><span class="sxs-lookup"><span data-stu-id="f9640-126">Total number of long values stored in the long-value tree for this record.</span></span>

<span data-ttu-id="f9640-127">**Nota:**  Esto no cuenta los valores largos intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="f9640-127">**Note**  This does not count intrinsic long-values.</span></span>

<span data-ttu-id="f9640-128">**cMultiValues**</span><span class="sxs-lookup"><span data-stu-id="f9640-128">**cMultiValues**</span></span>

<span data-ttu-id="f9640-129">La acumulación del número total de valores más allá de la primera para todas las columnas del registro.</span><span class="sxs-lookup"><span data-stu-id="f9640-129">The accumulation of the total number of values beyond the first for all columns in the record.</span></span>

<span data-ttu-id="f9640-130">**cCompressedColumns**</span><span class="sxs-lookup"><span data-stu-id="f9640-130">**cCompressedColumns**</span></span>

<span data-ttu-id="f9640-131">Número total de columnas comprimidas.</span><span class="sxs-lookup"><span data-stu-id="f9640-131">The total number of compressed columns.</span></span>

<span data-ttu-id="f9640-132">**cbDataCompressed**</span><span class="sxs-lookup"><span data-stu-id="f9640-132">**cbDataCompressed**</span></span>

<span data-ttu-id="f9640-133">Tamaño comprimido de los datos de usuario en este registro.</span><span class="sxs-lookup"><span data-stu-id="f9640-133">The compressed size of user data in this record.</span></span> <span data-ttu-id="f9640-134">Es lo mismo que cbData si no se comprimen valores largos intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="f9640-134">This is the same as cbData if no intrinsic long-values are compressed.</span></span>

<span data-ttu-id="f9640-135">**cbLongValueDataCompressed**</span><span class="sxs-lookup"><span data-stu-id="f9640-135">**cbLongValueDataCompressed**</span></span>

<span data-ttu-id="f9640-136">Tamaño comprimido de los datos de usuario en el árbol de valores largos.</span><span class="sxs-lookup"><span data-stu-id="f9640-136">The compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="f9640-137">Esto es lo mismo que los datos de cbLongValue si no se comprimen valores largos separados.</span><span class="sxs-lookup"><span data-stu-id="f9640-137">This is the same as cbLongValue data if no separated long values are compressed.</span></span>

### <a name="remarks"></a><span data-ttu-id="f9640-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9640-138">Remarks</span></span>

<span data-ttu-id="f9640-139">El número total de valores del registro sería **cMultiValues**  +  **cNonTaggedColumns**  +  **cTaggedColumns**.</span><span class="sxs-lookup"><span data-stu-id="f9640-139">The total number of values in the record would be **cMultiValues** + **cNonTaggedColumns** + **cTaggedColumns**.</span></span>

<span data-ttu-id="f9640-140">Los datos lógicos del registro son (cbData + cbLongValueData) y el tamaño físico de los datos es (cbDataCompressed + cbLongValueDataCompressed).</span><span class="sxs-lookup"><span data-stu-id="f9640-140">The logical data in the record is (cbData+cbLongValueData) and the physical size of the data is (cbDataCompressed+cbLongValueDataCompressed).</span></span> <span data-ttu-id="f9640-141">Se puede usar para calcular la razón de compresión de los datos almacenados.</span><span class="sxs-lookup"><span data-stu-id="f9640-141">This can be used to calculate the compression ratio of stored data.</span></span>

### <a name="requirements"></a><span data-ttu-id="f9640-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9640-142">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9640-143"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="f9640-143"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f9640-144">Requiere el sistema operativo Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f9640-144">Requires Windows Vista operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9640-145"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f9640-145"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f9640-146">Requiere el sistema operativo Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f9640-146">Requires Windows Server 2008 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9640-147"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="f9640-147"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f9640-148">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="f9640-148">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="f9640-149">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f9640-149">See Also</span></span>

[<span data-ttu-id="f9640-150">JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="f9640-150">JetGetRecordSize</span></span>](./jetgetrecordsize-function.md)  
[<span data-ttu-id="f9640-151">JetGetRecordSize2</span><span class="sxs-lookup"><span data-stu-id="f9640-151">JetGetRecordSize2</span></span>](./jetgetrecordsize2-function.md)
