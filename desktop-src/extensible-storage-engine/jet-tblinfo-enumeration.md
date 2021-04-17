---
description: 'Más información acerca de: enumeración JET_TblInfo'
title: Enumeración JET_TblInfo
TOCTitle: JET_TblInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_TblInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tblinfo(v=EXCHG.10)
ms:contentKeyID: 39512198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad43dcecf65fdc9fb8dd53bdf686a077e6bdfa8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697243"
---
# <a name="jet_tblinfo-enumeration"></a><span data-ttu-id="83a01-103">Enumeración JET_TblInfo</span><span class="sxs-lookup"><span data-stu-id="83a01-103">JET_TblInfo enumeration</span></span>

<span data-ttu-id="83a01-104">Niveles de información para recuperar la información de la tabla con JetGetTableInfo.</span><span class="sxs-lookup"><span data-stu-id="83a01-104">Info levels for retrieving table info with JetGetTableInfo.</span></span>

<span data-ttu-id="83a01-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="83a01-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="83a01-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="83a01-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="83a01-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83a01-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_TblInfo
'Usage
Dim instance As JET_TblInfo
```

``` csharp
public enum JET_TblInfo
```

## <a name="members"></a><span data-ttu-id="83a01-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="83a01-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="83a01-109">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="83a01-109">Member name</span></span></th>
<th><span data-ttu-id="83a01-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="83a01-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="83a01-111">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="83a01-111">Default</span></span></td>
<td><span data-ttu-id="83a01-112">Opciones predeterminadas</span><span class="sxs-lookup"><span data-stu-id="83a01-112">Default option.</span></span> <span data-ttu-id="83a01-113">Recupera un <a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a> que contiene información sobre la tabla.</span><span class="sxs-lookup"><span data-stu-id="83a01-113">Retrieves a <a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a> containing information about the table.</span></span> <span data-ttu-id="83a01-114">Use esta opción con <a href="dn292198(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="83a01-114">Use this option with <a href="dn292198(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="83a01-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="83a01-115">Name</span></span></td>
<td><span data-ttu-id="83a01-116">Recupera el nombre de la tabla.</span><span class="sxs-lookup"><span data-stu-id="83a01-116">Retrieves the name of the table.</span></span> <span data-ttu-id="83a01-117">Use esta opción con <a href="dn292204(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, cadena JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="83a01-117">Use this option with <a href="dn292204(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="83a01-118">Dbid</span><span class="sxs-lookup"><span data-stu-id="83a01-118">Dbid</span></span></td>
<td><span data-ttu-id="83a01-119">Recupera el <a href="hh596176(v=exchg.10).md">JET_DBID</a> de la base de datos que contiene la tabla.</span><span class="sxs-lookup"><span data-stu-id="83a01-119">Retrieves the <a href="hh596176(v=exchg.10).md">JET_DBID</a> of the database containing the table.</span></span> <span data-ttu-id="83a01-120">Use esta opción con <a href="dn292197(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="83a01-120">Use this option with <a href="dn292197(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="83a01-121">SpaceUsage</span><span class="sxs-lookup"><span data-stu-id="83a01-121">SpaceUsage</span></span></td>
<td><span data-ttu-id="83a01-122">El comportamiento del método depende del tamaño de la matriz que se pasa al método.</span><span class="sxs-lookup"><span data-stu-id="83a01-122">The behavior of the method depends on how large the array that is passed to the method is.</span></span> <span data-ttu-id="83a01-123">La matriz debe tener al menos dos entradas.</span><span class="sxs-lookup"><span data-stu-id="83a01-123">The array must have at least two entries.</span></span> <span data-ttu-id="83a01-124">La primera entrada contendrá el número de extensiones de propiedad de la tabla.</span><span class="sxs-lookup"><span data-stu-id="83a01-124">The first entry will contain the number of Owned Extents in the table.</span></span> <span data-ttu-id="83a01-125">La segunda entrada contendrá el número de extensiones disponibles en la tabla.</span><span class="sxs-lookup"><span data-stu-id="83a01-125">The second entry will contain the number of Available Extents in the table.</span></span> <span data-ttu-id="83a01-126">Si la matriz tiene más de dos entradas, los bytes restantes del búfer estarán compuestos de una matriz de estructuras que representan una lista de extensiones.</span><span class="sxs-lookup"><span data-stu-id="83a01-126">If the array has more than two entries then the remaining bytes of the buffer will consist of an array of structures that represent a list of extents.</span></span> <span data-ttu-id="83a01-127">Esta estructura contiene dos miembros: el último número de página en la extensión y el número de páginas en la extensión.</span><span class="sxs-lookup"><span data-stu-id="83a01-127">This structure contains two members: the last page number in the extent and the number of pages in the extent.</span></span> <span data-ttu-id="83a01-128">Use esta opción con <a href="dn292202(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="83a01-128">Use this option with <a href="dn292202(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="83a01-129">SpaceAlloc</span><span class="sxs-lookup"><span data-stu-id="83a01-129">SpaceAlloc</span></span></td>
<td><span data-ttu-id="83a01-130">La matriz pasada a JetGetTableInfo debe tener dos entradas.</span><span class="sxs-lookup"><span data-stu-id="83a01-130">The array passed to JetGetTableInfo must have two entries.</span></span> <span data-ttu-id="83a01-131">La primera entrada se establecerá en el número de páginas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="83a01-131">The first entry will be set to the number of pages in the table.</span></span> <span data-ttu-id="83a01-132">La segunda entrada se establecerá en la densidad de destino de las páginas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="83a01-132">The second entry will be set to the target density of pages for the table.</span></span> <span data-ttu-id="83a01-133">Use esta opción con <a href="dn292202(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="83a01-133">Use this option with <a href="dn292202(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="83a01-134">SpaceOwned</span><span class="sxs-lookup"><span data-stu-id="83a01-134">SpaceOwned</span></span></td>
<td><span data-ttu-id="83a01-135">Obtiene el número de páginas de propiedad de la tabla.</span><span class="sxs-lookup"><span data-stu-id="83a01-135">Gets the number of owned pages in the table.</span></span> <span data-ttu-id="83a01-136">Use esta opción con <a href="dn292201(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, Int32 JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="83a01-136">Use this option with <a href="dn292201(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="83a01-137">SpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="83a01-137">SpaceAvailable</span></span></td>
<td><span data-ttu-id="83a01-138">Obtiene el número de páginas disponibles en la tabla.</span><span class="sxs-lookup"><span data-stu-id="83a01-138">Gets the number of available pages in the table.</span></span> <span data-ttu-id="83a01-139">Use esta opción con <a href="dn292201(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, Int32 JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="83a01-139">Use this option with <a href="dn292201(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="83a01-140">TemplateTableName</span><span class="sxs-lookup"><span data-stu-id="83a01-140">TemplateTableName</span></span></td>
<td><span data-ttu-id="83a01-141">Si la tabla es una tabla derivada, el resultado se rellenará con el nombre de la tabla de la que la tabla derivada heredó su DDL.</span><span class="sxs-lookup"><span data-stu-id="83a01-141">If the table is a derived table, the result will be filled in with the name of the table from which the derived table inherited its DDL.</span></span> <span data-ttu-id="83a01-142">Si la tabla no es una tabla derivada, el búfer será una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="83a01-142">If the table is not a derived table, the buffer will an empty string.</span></span> <span data-ttu-id="83a01-143">Use esta opción con <a href="dn292204(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, cadena JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="83a01-143">Use this option with <a href="dn292204(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="83a01-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="83a01-144">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="83a01-145">Referencia</span><span class="sxs-lookup"><span data-stu-id="83a01-145">Reference</span></span>

[<span data-ttu-id="83a01-146">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="83a01-146">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
