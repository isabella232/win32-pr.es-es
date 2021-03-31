---
description: 'Más información acerca de: JET_COLUMNID'
title: JET_COLUMNID
TOCTitle: JET_COLUMNID
ms:assetid: d6c74c5c-ba61-4e1c-a1b1-495e925b6b68
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294104(v=EXCHG.10)
ms:contentKeyID: 32765719
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
ms.openlocfilehash: be5b8bb64dc9e0fc42055cf5e4d4f67caa7654bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907647"
---
# <a name="jet_columnid"></a><span data-ttu-id="efc15-103">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="efc15-103">JET_COLUMNID</span></span>


<span data-ttu-id="efc15-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="efc15-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columnid"></a><span data-ttu-id="efc15-105">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="efc15-105">JET_COLUMNID</span></span>

<span data-ttu-id="efc15-106">El tipo de datos **JET_COLUMNID** identifica una columna dentro de una tabla.</span><span class="sxs-lookup"><span data-stu-id="efc15-106">The **JET_COLUMNID** data type identifies a column within a table.</span></span>

```cpp
    typedef unsigned long JET_COLUMNID;
```

### <a name="data-types"></a><span data-ttu-id="efc15-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="efc15-107">Data Types</span></span>

<span data-ttu-id="efc15-108">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="efc15-108">JET_COLUMNID</span></span>

<span data-ttu-id="efc15-109">Identifica una columna dentro de una tabla.</span><span class="sxs-lookup"><span data-stu-id="efc15-109">Identifies a column within a table.</span></span>

### <a name="remarks"></a><span data-ttu-id="efc15-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="efc15-110">Remarks</span></span>

<span data-ttu-id="efc15-111">Los identificadores de columna son únicos en una sola tabla.</span><span class="sxs-lookup"><span data-stu-id="efc15-111">Column IDs are unique within a single table.</span></span> <span data-ttu-id="efc15-112">Una vez que se sabe que una columna tiene un ID. de columna determinado, siempre tendrá ese ID. de columna.</span><span class="sxs-lookup"><span data-stu-id="efc15-112">Once a column is known to have a certain column ID, it will always have that column ID.</span></span> <span data-ttu-id="efc15-113">Restaurar desde copia de seguridad no cambiará el valor de un identificador de columna.</span><span class="sxs-lookup"><span data-stu-id="efc15-113">Restore from backup will not change the value of a column ID.</span></span> <span data-ttu-id="efc15-114">Sin embargo, si se eliminan una o más columnas de la tabla, antes de una columna de tabla específica, una base de datos de Compact puede cambiar el valor de un identificador de columna.</span><span class="sxs-lookup"><span data-stu-id="efc15-114">However, if one or more table columns, prior to a specific table column, are deleted, a compact database can then change the value of a column ID.</span></span>

<span data-ttu-id="efc15-115">En algunos casos, los identificadores de columna son el único medio para identificar columnas.</span><span class="sxs-lookup"><span data-stu-id="efc15-115">In some cases, column IDs are the only means of identifying columns.</span></span> <span data-ttu-id="efc15-116">Cuando se crea una tabla temporal, sus columnas no tienen nombres, pero la función Create devuelve una matriz de identificadores de columna.</span><span class="sxs-lookup"><span data-stu-id="efc15-116">When a temporary table is created, its columns do not have names, but an array of column IDs is returned by the create function.</span></span>

<span data-ttu-id="efc15-117">Las columnas de tablas diferentes pueden tener el mismo ID. de columna.</span><span class="sxs-lookup"><span data-stu-id="efc15-117">Columns in different tables can have the same column ID.</span></span>

### <a name="requirements"></a><span data-ttu-id="efc15-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efc15-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="efc15-119"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="efc15-119"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="efc15-120">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="efc15-120">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efc15-121"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="efc15-121"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="efc15-122">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="efc15-122">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efc15-123"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="efc15-123"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="efc15-124">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="efc15-124">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

