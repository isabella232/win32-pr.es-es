---
description: 'Más información acerca de: estructura de JET_SETINFO'
title: Estructura de JET_SETINFO
TOCTitle: JET_SETINFO Structure
ms:assetid: cbc41175-e48f-46b0-aeb1-1120fa2cd981
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294090(v=EXCHG.10)
ms:contentKeyID: 32765705
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
ms.openlocfilehash: 69602aad89142d9f5dc202074ca54cf278767892
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104548182"
---
# <a name="jet_setinfo-structure"></a><span data-ttu-id="7ffa6-103">Estructura de JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="7ffa6-103">JET_SETINFO Structure</span></span>


<span data-ttu-id="7ffa6-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7ffa6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_setinfo-structure"></a><span data-ttu-id="7ffa6-105">Estructura de JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="7ffa6-105">JET_SETINFO Structure</span></span>

<span data-ttu-id="7ffa6-106">La estructura **JET_SETINFO** contiene parámetros de entrada opcionales para [JetSetColumn](./jetsetcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="7ffa6-106">The **JET_SETINFO** structure contains optional input parameters for [JetSetColumn](./jetsetcolumn-function.md).</span></span> <span data-ttu-id="7ffa6-107">Se puede pasar un puntero **null** en el caso de que se pasara un puntero a esta estructura.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-107">A **NULL** pointer can be passed where a pointer to this structure would otherwise be passed.</span></span> <span data-ttu-id="7ffa6-108">El significado de pasar un **valor null** equivale a pasar **JET_SETINFO** con **cbStruct** establecido en sizeof (JET_SETINFO), **ibLongValue** establecido en 0 (cero) y **itagSequence** establecido en 1.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-108">The meaning of passing a **NULL** is the same as passing **JET_SETINFO** with **cbStruct** set to sizeof(JET_SETINFO), **ibLongValue** set to 0 (zero) and **itagSequence** set to 1.</span></span>

```cpp
typedef struct {
  unsigned long cbStruct;
  unsigned long ibLongValue;
  unsigned long itagSequence;
} JET_SETINFO;
```

### <a name="members"></a><span data-ttu-id="7ffa6-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="7ffa6-109">Members</span></span>

<span data-ttu-id="7ffa6-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="7ffa6-110">**cbStruct**</span></span>

<span data-ttu-id="7ffa6-111">Tamaño, en bytes, del **JET_SETINFO**.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-111">The size, in bytes, of the **JET_SETINFO**.</span></span> <span data-ttu-id="7ffa6-112">Este valor confirma la presencia de los campos siguientes.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-112">This value confirms the presence of the following fields.</span></span>

<span data-ttu-id="7ffa6-113">**ibLongValue**</span><span class="sxs-lookup"><span data-stu-id="7ffa6-113">**ibLongValue**</span></span>

<span data-ttu-id="7ffa6-114">Desplazamiento al primer byte que se va a establecer en una columna de tipo [JET_coltypLongBinary](./jet-coltyp.md) o [JET_coltypLongText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="7ffa6-114">The offset to the first byte to be set in a column of type [JET_coltypLongBinary](./jet-coltyp.md) or [JET_coltypLongText](./jet-coltyp.md).</span></span>

<span data-ttu-id="7ffa6-115">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="7ffa6-115">**itagSequence**</span></span>

<span data-ttu-id="7ffa6-116">Describe el número de secuencia del valor de una columna con varios valores que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-116">Describes the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="7ffa6-117">La matriz de valores se basa en uno.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-117">The array of values is one-based.</span></span> <span data-ttu-id="7ffa6-118">El primer valor es Sequence 1, no 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="7ffa6-118">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="7ffa6-119">Si la columna de registro solo tiene un valor, se debe pasar 1 como **itagSequence** si ese valor se va a reemplazar.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-119">If the record column has only one value then 1 should be passed as the **itagSequence** if that value is being replaced.</span></span> <span data-ttu-id="7ffa6-120">Un valor de 0 (cero) significa agregar una nueva instancia de valor de columna al final de la secuencia de valores de columna.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-120">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span>

<span data-ttu-id="7ffa6-121">Con una columna que puede contener varios valores, solo es posible usar un número de secuencia mayor que 1 en [JetSetColumn](./jetsetcolumn-function.md) y [JetRetrieveColumn](./jetretrievecolumn-function.md) o 0 en [JetSetColumn](./jetsetcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="7ffa6-121">With a column that can contain multiple values, it is only possible to use a sequence number larger than 1 in [JetSetColumn](./jetsetcolumn-function.md) and [JetRetrieveColumn](./jetretrievecolumn-function.md) or 0 in [JetSetColumn](./jetsetcolumn-function.md).</span></span> <span data-ttu-id="7ffa6-122">En la implementación actual del motor, cualquier columna creada con JET_bitColumnTagged puede contener varios valores.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-122">In the current implementation of the engine, any column that was created with JET_bitColumnTagged can contain multiple values.</span></span> <span data-ttu-id="7ffa6-123">Las columnas creadas con JET_bitColumnMultiValued solo se diferencian de las columnas etiquetadas con varios valores en la forma en que se indexan.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-123">Columns created with JET_bitColumnMultiValued differ from multi-valued tagged columns only in the way that they are indexed.</span></span> <span data-ttu-id="7ffa6-124">Consulte [JET_INDEXCREATE](./jet-indexcreate-structure.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-124">See [JET_INDEXCREATE](./jet-indexcreate-structure.md) for more information.</span></span>

### <a name="requirements"></a><span data-ttu-id="7ffa6-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ffa6-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ffa6-126"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="7ffa6-126"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7ffa6-127">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-127">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ffa6-128"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7ffa6-128"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7ffa6-129">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-129">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ffa6-130"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="7ffa6-130"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7ffa6-131">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="7ffa6-131">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="7ffa6-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7ffa6-132">See Also</span></span>

[<span data-ttu-id="7ffa6-133">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="7ffa6-133">JetSetColumn</span></span>](./jetsetcolumn-function.md)
