---
description: 'Más información acerca de: estructura de JET_CONDITIONALCOLUMN'
title: Estructura de JET_CONDITIONALCOLUMN
TOCTitle: JET_CONDITIONALCOLUMN Structure
ms:assetid: 2ca6b4ba-0dc4-47d5-b072-324e5a381d0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269214(v=EXCHG.10)
ms:contentKeyID: 32765517
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
ms.openlocfilehash: 27d0add64adeb7b609e84d6102a06230df55ebbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687058"
---
# <a name="jet_conditionalcolumn-structure"></a><span data-ttu-id="4e163-103">Estructura de JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="4e163-103">JET_CONDITIONALCOLUMN Structure</span></span>


<span data-ttu-id="4e163-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4e163-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_conditionalcolumn-structure"></a><span data-ttu-id="4e163-105">Estructura de JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="4e163-105">JET_CONDITIONALCOLUMN Structure</span></span>

<span data-ttu-id="4e163-106">La estructura **JET_CONDITIONALCOLUMN** define cómo se realiza la indización condicional para un índice determinado.</span><span class="sxs-lookup"><span data-stu-id="4e163-106">The **JET_CONDITIONALCOLUMN** structure defines how conditional indexing is performed for a given index.</span></span> <span data-ttu-id="4e163-107">Un índice condicional solo contiene una entrada de índice para las filas que coincidan con la condición especificada.</span><span class="sxs-lookup"><span data-stu-id="4e163-107">A conditional index contains an index entry for only those rows that match the specified condition.</span></span> <span data-ttu-id="4e163-108">Sin embargo, la columna condicional no forma parte de la clave del índice, sino que solo controla la presencia de la entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="4e163-108">However, the conditional column is not part of the index's key, it only controls the presence of the index entry.</span></span>

```cpp
    typedef struct tagJET_CONDITIONALCOLUMN {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_GRBIT grbit;
    } JET_CONDITIONALCOLUMN;
```

### <a name="members"></a><span data-ttu-id="4e163-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="4e163-109">Members</span></span>

<span data-ttu-id="4e163-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="4e163-110">**cbStruct**</span></span>

<span data-ttu-id="4e163-111">Este campo debe inicializarse en sizeof (JET_CONDITIONALCOLUMN), en bytes.</span><span class="sxs-lookup"><span data-stu-id="4e163-111">This field must be initialized to sizeof( JET_CONDITIONALCOLUMN ), in bytes.</span></span>

<span data-ttu-id="4e163-112">**szColumnName**</span><span class="sxs-lookup"><span data-stu-id="4e163-112">**szColumnName**</span></span>

<span data-ttu-id="4e163-113">Nombre de la columna que contiene los datos en los que el motor de base de datos está indizando condicionalmente la fila.</span><span class="sxs-lookup"><span data-stu-id="4e163-113">The name of the column that contains the data on which the database engine is conditionally indexing the row.</span></span>

<span data-ttu-id="4e163-114">**grbit** Grupo de bits que proporciona las opciones para el índice condicional.</span><span class="sxs-lookup"><span data-stu-id="4e163-114">**grbit** A group of bits that gives the options for the conditional index.</span></span> <span data-ttu-id="4e163-115">No es válido pasar valores de cero o lógicamente **o** de ed para **JET_CONDITIONALCOLUMN**.</span><span class="sxs-lookup"><span data-stu-id="4e163-115">Passing in zero or logically-**OR** ed values is not valid for **JET_CONDITIONALCOLUMN**.</span></span> <span data-ttu-id="4e163-116">El campo de bits debe ser exactamente uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="4e163-116">The bit field must be exactly one of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4e163-117">Value</span><span class="sxs-lookup"><span data-stu-id="4e163-117">Value</span></span></p></th>
<th><p><span data-ttu-id="4e163-118">Significado</span><span class="sxs-lookup"><span data-stu-id="4e163-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e163-119">JET_bitIndexColumnMustBeNull</span><span class="sxs-lookup"><span data-stu-id="4e163-119">JET_bitIndexColumnMustBeNull</span></span></p></td>
<td><p><span data-ttu-id="4e163-120">La columna especificada por el parámetro <em>szColumnName</em> debe ser null para que una entrada de índice de una fila determinada aparezca en este índice.</span><span class="sxs-lookup"><span data-stu-id="4e163-120">The column specified by the <em>szColumnName</em> parameter must be NULL for an index entry for a given row to appear in this index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e163-121">JET_bitIndexColumnMustBeNonNull</span><span class="sxs-lookup"><span data-stu-id="4e163-121">JET_bitIndexColumnMustBeNonNull</span></span></p></td>
<td><p><span data-ttu-id="4e163-122">La columna especificada por el parámetro <em>szColumnName</em> no debe ser null para una entrada de índice para que una fila determinada aparezca en este índice.</span><span class="sxs-lookup"><span data-stu-id="4e163-122">The column specified by the <em>szColumnName</em> parameter must be non-NULL for an index entry in order for a given row to appear in this index.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a><span data-ttu-id="4e163-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e163-123">Remarks</span></span>

<span data-ttu-id="4e163-124">Un índice condicional solo contiene una entrada de índice para las filas que coincidan con la condición especificada.</span><span class="sxs-lookup"><span data-stu-id="4e163-124">A conditional index contains an index entry for only those rows that match the specified condition.</span></span> <span data-ttu-id="4e163-125">Por ejemplo, una columna podría denominarse "marcada" y, cuando se marca una fila, la columna se establece en un valor distinto de NULL.</span><span class="sxs-lookup"><span data-stu-id="4e163-125">For example, a column could be named "Marked", and when a row is marked, the column is set to a non-NULL value.</span></span> <span data-ttu-id="4e163-126">Un JET_bitIndexColumnMustBeNonNull índice condicional en esta columna mostrará todas las filas marcadas y un JET_bitIndexColumnMustBeNull índice condicional mostrará las filas que no están marcadas.</span><span class="sxs-lookup"><span data-stu-id="4e163-126">A JET_bitIndexColumnMustBeNonNull conditional index on this column will show all rows that are marked, and a JET_bitIndexColumnMustBeNull conditional index will show rows that are not marked.</span></span> <span data-ttu-id="4e163-127">Esta es también una manera cómoda de realizar una eliminación de marca y un índice de recolección de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="4e163-127">This is also a convenient way to perform a flag deletion and garbage collecting index.</span></span>

### <a name="requirements"></a><span data-ttu-id="4e163-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e163-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e163-129"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="4e163-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4e163-130">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4e163-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e163-131"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="4e163-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4e163-132">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4e163-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e163-133"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="4e163-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4e163-134">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="4e163-134">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e163-135"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="4e163-135"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="4e163-136">Se implementa como <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) y <strong>JET_CONDITIONALCOLUMN_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="4e163-136">Implemented as <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) and <strong>JET_CONDITIONALCOLUMN_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="4e163-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4e163-137">See Also</span></span>

[<span data-ttu-id="4e163-138">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="4e163-138">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="4e163-139">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="4e163-139">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)
