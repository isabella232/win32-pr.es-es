---
description: 'Más información acerca de: enumeración JET_IdxInfo'
title: Enumeración JET_IdxInfo
TOCTitle: JET_IdxInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_IdxInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_idxinfo(v=EXCHG.10)
ms:contentKeyID: 39512789
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.VarSegMac
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.KeyMost
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.IndexId
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SysTabCursor
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.OLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Default
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.ResetOLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Langid
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.List
- Microsoft.Isam.Esent.Interop.JET_IdxInfo
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Count
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.IndexId
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_IdxInfo
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.List
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.VarSegMac
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.KeyMost
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.OLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.ResetOLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SysTabCursor
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Count
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Default
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Langid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e1f2cb50537ed492a428c82fd9a6f6541c5fad2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716977"
---
# <a name="jet_idxinfo-enumeration"></a><span data-ttu-id="7afd9-103">Enumeración JET_IdxInfo</span><span class="sxs-lookup"><span data-stu-id="7afd9-103">JET_IdxInfo enumeration</span></span>

<span data-ttu-id="7afd9-104">Niveles de información para recuperar información de índice con JetGetIndexInfo.</span><span class="sxs-lookup"><span data-stu-id="7afd9-104">Info levels for retrieve index information with JetGetIndexInfo.</span></span> <span data-ttu-id="7afd9-105">y JetGetTableIndexInfo.</span><span class="sxs-lookup"><span data-stu-id="7afd9-105">and JetGetTableIndexInfo.</span></span>

<span data-ttu-id="7afd9-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7afd9-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7afd9-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7afd9-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7afd9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7afd9-108">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_IdxInfo
'Usage
Dim instance As JET_IdxInfo
```

``` csharp
public enum JET_IdxInfo
```

## <a name="members"></a><span data-ttu-id="7afd9-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="7afd9-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="7afd9-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="7afd9-110">Member name</span></span></th>
<th><span data-ttu-id="7afd9-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7afd9-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7afd9-112">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7afd9-112">Default</span></span></td>
<td><span data-ttu-id="7afd9-113">Devuelve una estructura de <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> con información sobre el índice.</span><span class="sxs-lookup"><span data-stu-id="7afd9-113">Returns a <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> structure with information about the index.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="7afd9-114">List</span><span class="sxs-lookup"><span data-stu-id="7afd9-114">List</span></span></td>
<td><span data-ttu-id="7afd9-115">Devuelve una estructura de <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> con información sobre el índice.</span><span class="sxs-lookup"><span data-stu-id="7afd9-115">Returns a <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> structure with information about the index.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7afd9-116">SysTabCursor</span><span class="sxs-lookup"><span data-stu-id="7afd9-116">SysTabCursor</span></span></td>
<td><span data-ttu-id="7afd9-117"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="7afd9-117"><strong>Obsolete.</strong></span></span> <span data-ttu-id="7afd9-118">SysTabCursor está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="7afd9-118">SysTabCursor is obsolete.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="7afd9-119">OLC</span><span class="sxs-lookup"><span data-stu-id="7afd9-119">OLC</span></span></td>
<td><span data-ttu-id="7afd9-120"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="7afd9-120"><strong>Obsolete.</strong></span></span> <span data-ttu-id="7afd9-121">OLC está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="7afd9-121">OLC is obsolete.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7afd9-122">ResetOLC</span><span class="sxs-lookup"><span data-stu-id="7afd9-122">ResetOLC</span></span></td>
<td><span data-ttu-id="7afd9-123"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="7afd9-123"><strong>Obsolete.</strong></span></span> <span data-ttu-id="7afd9-124">Restablecer OLC está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="7afd9-124">Reset OLC is obsolete.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="7afd9-125">SpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="7afd9-125">SpaceAlloc</span></span></td>
<td><span data-ttu-id="7afd9-126">Devuelve un entero con el uso de espacio del índice.</span><span class="sxs-lookup"><span data-stu-id="7afd9-126">Returns an integer with the space usage of the index.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7afd9-127">LCID</span><span class="sxs-lookup"><span data-stu-id="7afd9-127">LCID</span></span></td>
<td><span data-ttu-id="7afd9-128">Devuelve un entero con el LCID del índice.</span><span class="sxs-lookup"><span data-stu-id="7afd9-128">Returns an integer with the LCID of the index.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="7afd9-129">Ididioma</span><span class="sxs-lookup"><span data-stu-id="7afd9-129">Langid</span></span></td>
<td><span data-ttu-id="7afd9-130"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="7afd9-130"><strong>Obsolete.</strong></span></span> <span data-ttu-id="7afd9-131">Langid está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="7afd9-131">Langid is obsolete.</span></span> <span data-ttu-id="7afd9-132">En su lugar, use LCID.</span><span class="sxs-lookup"><span data-stu-id="7afd9-132">Use LCID instead.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7afd9-133">Count</span><span class="sxs-lookup"><span data-stu-id="7afd9-133">Count</span></span></td>
<td><span data-ttu-id="7afd9-134">Devuelve un entero con el recuento de índices de la tabla.</span><span class="sxs-lookup"><span data-stu-id="7afd9-134">Returns an integer with the count of indexes in the table.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="7afd9-135">VarSegMac</span><span class="sxs-lookup"><span data-stu-id="7afd9-135">VarSegMac</span></span></td>
<td><span data-ttu-id="7afd9-136">Devuelve un ushort con el valor de cbVarSegMac con el que se creó el índice.</span><span class="sxs-lookup"><span data-stu-id="7afd9-136">Returns a ushort with the value of cbVarSegMac the index was created with.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7afd9-137">IndexId</span><span class="sxs-lookup"><span data-stu-id="7afd9-137">IndexId</span></span></td>
<td><span data-ttu-id="7afd9-138">Devuelve un <a href="hh557060(v=exchg.10).md">JET_INDEXID</a> que identifica el índice.</span><span class="sxs-lookup"><span data-stu-id="7afd9-138">Returns a <a href="hh557060(v=exchg.10).md">JET_INDEXID</a> identifying the index.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="7afd9-139">KeyMost</span><span class="sxs-lookup"><span data-stu-id="7afd9-139">KeyMost</span></span></td>
<td><span data-ttu-id="7afd9-140">Introducido en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7afd9-140">Introduced in Windows Vista.</span></span> <span data-ttu-id="7afd9-141">Devuelve un ushort con el valor de cbKeyMost con el que se creó el índice.</span><span class="sxs-lookup"><span data-stu-id="7afd9-141">Returns a ushort with the value of cbKeyMost the index was created with.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="7afd9-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="7afd9-142">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7afd9-143">Referencia</span><span class="sxs-lookup"><span data-stu-id="7afd9-143">Reference</span></span>

[<span data-ttu-id="7afd9-144">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7afd9-144">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
