---
description: 'Más información acerca de: enumeración JET_prep'
title: Enumeración JET_prep
TOCTitle: JET_prep enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_prep
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_prep(v=EXCHG.10)
ms:contentKeyID: 39510193
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edeaef8144fe6e13674ec6d3dfcb8adf7522e148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697528"
---
# <a name="jet_prep-enumeration"></a><span data-ttu-id="a779a-103">Enumeración JET_prep</span><span class="sxs-lookup"><span data-stu-id="a779a-103">JET_prep enumeration</span></span>

<span data-ttu-id="a779a-104">Tipos de actualización para JetPrepareUpdate.</span><span class="sxs-lookup"><span data-stu-id="a779a-104">Update types for JetPrepareUpdate.</span></span>

<span data-ttu-id="a779a-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a779a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a779a-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a779a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a779a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a779a-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_prep
'Usage
Dim instance As JET_prep
```

``` csharp
public enum JET_prep
```

## <a name="members"></a><span data-ttu-id="a779a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a779a-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="a779a-109">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="a779a-109">Member name</span></span></th>
<th><span data-ttu-id="a779a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a779a-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="a779a-111">Insertar</span><span class="sxs-lookup"><span data-stu-id="a779a-111">Insert</span></span></td>
<td><span data-ttu-id="a779a-112">Esta marca hace que el cursor se prepare para una inserción de un nuevo registro.</span><span class="sxs-lookup"><span data-stu-id="a779a-112">This flag causes the cursor to prepare for an insert of a new record.</span></span> <span data-ttu-id="a779a-113">Todos los datos se inicializan en el estado predeterminado del registro.</span><span class="sxs-lookup"><span data-stu-id="a779a-113">All the data is initialized to the default state for the record.</span></span> <span data-ttu-id="a779a-114">Si la tabla tiene una columna de incremento automático, se asigna un nuevo valor a este registro independientemente de si la actualización se realiza en última instancia, si se produce un error o se cancela.</span><span class="sxs-lookup"><span data-stu-id="a779a-114">If the table has an auto-increment column, then a new value is assigned to this record regardless of whether the update ultimately succeeds, fails or is cancelled.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="a779a-115">Replace</span><span class="sxs-lookup"><span data-stu-id="a779a-115">Replace</span></span></td>
<td><span data-ttu-id="a779a-116">Esta marca hace que el cursor se prepare para un reemplazo del registro actual.</span><span class="sxs-lookup"><span data-stu-id="a779a-116">This flag causes the cursor to prepare for a replace of the current record.</span></span> <span data-ttu-id="a779a-117">Si la tabla tiene una columna de versión, la columna versión se establece en el valor siguiente en su secuencia.</span><span class="sxs-lookup"><span data-stu-id="a779a-117">If the table has a version column, then the version column is set to the next value in its sequence.</span></span> <span data-ttu-id="a779a-118">Si esta actualización no se completa, el valor de versión del registro no se verá afectado.</span><span class="sxs-lookup"><span data-stu-id="a779a-118">If this update does not complete, then the version value in the record will be unaffected.</span></span> <span data-ttu-id="a779a-119">Se realiza un bloqueo de actualización en el registro para evitar que otras sesiones actualicen este registro antes de que se complete esta sesión.</span><span class="sxs-lookup"><span data-stu-id="a779a-119">An update lock is taken on the record to prevent other sessions from updating this record before this session completes.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="a779a-120">Cancelar</span><span class="sxs-lookup"><span data-stu-id="a779a-120">Cancel</span></span></td>
<td><span data-ttu-id="a779a-121">Esta marca hace que JetPrepareUpdate cancele la actualización de este cursor.</span><span class="sxs-lookup"><span data-stu-id="a779a-121">This flag causes JetPrepareUpdate to cancel the update for this cursor.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="a779a-122">ReplaceNoLock</span><span class="sxs-lookup"><span data-stu-id="a779a-122">ReplaceNoLock</span></span></td>
<td><span data-ttu-id="a779a-123">Esta marca es similar a JET_prepReplace, pero no se realiza ningún bloqueo para evitar que otras sesiones actualicen este registro.</span><span class="sxs-lookup"><span data-stu-id="a779a-123">This flag is similar to JET_prepReplace, but no lock is taken to prevent other sessions from updating this record.</span></span> <span data-ttu-id="a779a-124">En su lugar, esta sesión puede recibir JET_errWriteConflict cuando llama a JetUpdate para completar la actualización.</span><span class="sxs-lookup"><span data-stu-id="a779a-124">Instead, this session may receive JET_errWriteConflict when it calls JetUpdate to complete the update.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="a779a-125">InsertCopy</span><span class="sxs-lookup"><span data-stu-id="a779a-125">InsertCopy</span></span></td>
<td><span data-ttu-id="a779a-126">Esta marca hace que el cursor se prepare para una inserción de una copia del registro existente.</span><span class="sxs-lookup"><span data-stu-id="a779a-126">This flag causes the cursor to prepare for an insert of a copy of the existing record.</span></span> <span data-ttu-id="a779a-127">Debe haber un registro actual si se usa esta opción.</span><span class="sxs-lookup"><span data-stu-id="a779a-127">There must be a current record if this option is used.</span></span> <span data-ttu-id="a779a-128">El estado inicial del nuevo registro se copia del registro actual.</span><span class="sxs-lookup"><span data-stu-id="a779a-128">The initial state of the new record is copied from the current record.</span></span> <span data-ttu-id="a779a-129">Los valores Long que se almacenan fuera de registro se copian de manera virtual.</span><span class="sxs-lookup"><span data-stu-id="a779a-129">Long values that are stored off-record are virtually copied.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="a779a-130">InsertCopyDeleteOriginal</span><span class="sxs-lookup"><span data-stu-id="a779a-130">InsertCopyDeleteOriginal</span></span></td>
<td><span data-ttu-id="a779a-131">Esta marca hace que el cursor se prepare para una inserción del mismo registro, y una eliminación o el registro original.</span><span class="sxs-lookup"><span data-stu-id="a779a-131">This flag causes the cursor to prepare for an insert of the same record, and a delete or the original record.</span></span> <span data-ttu-id="a779a-132">Se utiliza en casos en los que la clave principal ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="a779a-132">It is used in cases in which the primary key has changed.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="a779a-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="a779a-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a779a-134">Referencia</span><span class="sxs-lookup"><span data-stu-id="a779a-134">Reference</span></span>

[<span data-ttu-id="a779a-135">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a779a-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
