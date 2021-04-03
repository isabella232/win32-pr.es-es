---
description: 'Más información acerca de: estructura de JET_RETINFO'
title: Estructura de JET_RETINFO
TOCTitle: JET_RETINFO Structure
ms:assetid: a47a7902-3ecd-4d42-941f-89d25d78eb4c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294049(v=EXCHG.10)
ms:contentKeyID: 32765648
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
ms.openlocfilehash: 3452c4fab7155ea33b556ac7aa2c777b11a3f954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908149"
---
# <a name="jet_retinfo-structure"></a><span data-ttu-id="daa00-103">Estructura de JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="daa00-103">JET_RETINFO Structure</span></span>


<span data-ttu-id="daa00-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="daa00-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_retinfo-structure"></a><span data-ttu-id="daa00-105">Estructura de JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="daa00-105">JET_RETINFO Structure</span></span>

<span data-ttu-id="daa00-106">La estructura **JET_RETINFO** contiene parámetros de entrada y salida opcionales para [JetRetrieveColumn](./jetretrievecolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="daa00-106">The **JET_RETINFO** structure contains optional input and output parameters for [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span> <span data-ttu-id="daa00-107">Se puede pasar un puntero NULL en el caso de que se pasara un puntero a esta estructura.</span><span class="sxs-lookup"><span data-stu-id="daa00-107">A null pointer can be passed where a pointer to this structure would otherwise be passed.</span></span> <span data-ttu-id="daa00-108">Pasar un puntero nulo es igual que pasar **JET_RETINFO** con **cbStruct** establecido en sizeof (JET_RETINFO), **ibLongValue** establecido en 0 (cero) y **itagSequence** establecido en 1.</span><span class="sxs-lookup"><span data-stu-id="daa00-108">Passing a null pointer is the same as passing **JET_RETINFO** with **cbStruct** set to sizeof(JET_RETINFO), **ibLongValue** set to 0 (zero) and **itagSequence** set to 1.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
    } JET_RETINFO;
```

### <a name="members"></a><span data-ttu-id="daa00-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="daa00-109">Members</span></span>

<span data-ttu-id="daa00-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="daa00-110">**cbStruct**</span></span>

<span data-ttu-id="daa00-111">Debe establecerse en el tamaño de la estructura **JET_RETINFO** , en bytes, y sirve para confirmar la presencia de los campos siguientes.</span><span class="sxs-lookup"><span data-stu-id="daa00-111">Must be set to the size of the **JET_RETINFO** structure, in bytes, and serves to confirm the presence of the following fields.</span></span>

<span data-ttu-id="daa00-112">**ibLongValue**</span><span class="sxs-lookup"><span data-stu-id="daa00-112">**ibLongValue**</span></span>

<span data-ttu-id="daa00-113">Desplazamiento al primer byte que se va a recuperar de una columna de tipo [JET_coltypLongBinary](./jet-coltyp.md), o [JET_coltypLongText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="daa00-113">The offset to the first byte to be retrieved from a column of type [JET_coltypLongBinary](./jet-coltyp.md), or [JET_coltypLongText](./jet-coltyp.md).</span></span> <span data-ttu-id="daa00-114">Observe que la cantidad de datos recuperados de este desplazamiento es el menor del tamaño del búfer de salida y el tamaño de los datos en el valor real después de este desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="daa00-114">Note that the amount of data retrieved from this offset is the lower of the size of the output buffer and the size of data in the actual value after this offset.</span></span>

<span data-ttu-id="daa00-115">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="daa00-115">**itagSequence**</span></span>

<span data-ttu-id="daa00-116">Describe el número de secuencia de un valor en una columna con varios valores.</span><span class="sxs-lookup"><span data-stu-id="daa00-116">Describes the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="daa00-117">Tenga en cuenta que la matriz de valores se basa en uno.</span><span class="sxs-lookup"><span data-stu-id="daa00-117">Note that the array of values is one-based.</span></span> <span data-ttu-id="daa00-118">El primer valor es Sequence 1, no 0.</span><span class="sxs-lookup"><span data-stu-id="daa00-118">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="daa00-119">Si la columna de registro solo tiene un valor, se debe pasar 1 como **itagSequence**</span><span class="sxs-lookup"><span data-stu-id="daa00-119">If the record column has only one value then 1 should be passed as the **itagSequence**</span></span>

<span data-ttu-id="daa00-120">Con una columna que puede contener varios valores, solo es posible usar un número de secuencia mayor que 1 en [JetSetColumn](./jetsetcolumn-function.md) y [JetRetrieveColumn](./jetretrievecolumn-function.md) o 0 en [JetSetColumn](./jetsetcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="daa00-120">With a column that can contain multiple values, it is only possible to use a sequence number larger than 1 in [JetSetColumn](./jetsetcolumn-function.md) and [JetRetrieveColumn](./jetretrievecolumn-function.md) or 0 in [JetSetColumn](./jetsetcolumn-function.md).</span></span> <span data-ttu-id="daa00-121">En la implementación actual del motor, cualquier columna creada con JET_bitColumnTagged puede contener varios valores.</span><span class="sxs-lookup"><span data-stu-id="daa00-121">In the current implementation of the engine, any column that was created with JET_bitColumnTagged can contain multiple values.</span></span> <span data-ttu-id="daa00-122">Las columnas creadas con JET_bitColumnMultiValued solo se diferencian de las columnas etiquetadas con varios valores en la forma en que se indexan.</span><span class="sxs-lookup"><span data-stu-id="daa00-122">Columns created with JET_bitColumnMultiValued differ from multi-valued tagged columns only in the way that they are indexed.</span></span> <span data-ttu-id="daa00-123">Consulte [JET_INDEXCREATE](./jet-indexcreate-structure.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="daa00-123">See [JET_INDEXCREATE](./jet-indexcreate-structure.md) for more information.</span></span>

<span data-ttu-id="daa00-124">**columnidNextTagged**</span><span class="sxs-lookup"><span data-stu-id="daa00-124">**columnidNextTagged**</span></span>

<span data-ttu-id="daa00-125">Devuelve el columnid de la columna etiquetada, con varios valores o dispersos recuperados cuando se recuperan todas las columnas etiquetadas pasando 0 como columnid a [JetRetrieveColumn](./jetretrievecolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="daa00-125">Returns the columnid of the retrieved tagged, multi-valued or sparse, column when all tagged columns are retrieved by passing 0 as the columnid to [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="daa00-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="daa00-126">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="daa00-127"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="daa00-127"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="daa00-128">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="daa00-128">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daa00-129"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="daa00-129"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="daa00-130">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="daa00-130">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daa00-131"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="daa00-131"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="daa00-132">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="daa00-132">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="daa00-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="daa00-133">See Also</span></span>

[<span data-ttu-id="daa00-134">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="daa00-134">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="daa00-135">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="daa00-135">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="daa00-136">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="daa00-136">JET_RETINFO</span></span>]()  
[<span data-ttu-id="daa00-137">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="daa00-137">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)
