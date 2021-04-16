---
description: 'Más información acerca de: enumeración JET_DbInfo'
title: Enumeración JET_DbInfo
TOCTitle: JET_DbInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_DbInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfo(v=EXCHG.10)
ms:contentKeyID: 39516181
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 39c6c3175c08e4f7644ad4f0b41137e12e84f71d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705582"
---
# <a name="jet_dbinfo-enumeration"></a><span data-ttu-id="0c423-103">Enumeración JET_DbInfo</span><span class="sxs-lookup"><span data-stu-id="0c423-103">JET_DbInfo enumeration</span></span>

<span data-ttu-id="0c423-104">Niveles de información para recuperar información de base de datos.</span><span class="sxs-lookup"><span data-stu-id="0c423-104">Info levels for retrieving database info.</span></span>

<span data-ttu-id="0c423-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0c423-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0c423-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0c423-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0c423-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c423-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_DbInfo
'Usage
Dim instance As JET_DbInfo
```

``` csharp
public enum JET_DbInfo
```

## <a name="members"></a><span data-ttu-id="0c423-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0c423-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="0c423-109">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="0c423-109">Member name</span></span></th>
<th><span data-ttu-id="0c423-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c423-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0c423-111">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="0c423-111">Filename</span></span></td>
<td><span data-ttu-id="0c423-112">Devuelve la ruta de acceso al archivo de base de datos (cadena).</span><span class="sxs-lookup"><span data-stu-id="0c423-112">Returns the path to the database file (string).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0c423-113">LCID</span><span class="sxs-lookup"><span data-stu-id="0c423-113">LCID</span></span></td>
<td><span data-ttu-id="0c423-114">Devuelve el identificador de configuración regional (LCID) asociado a esta base de datos (Int32).</span><span class="sxs-lookup"><span data-stu-id="0c423-114">Returns the locale identifier (LCID) associated with this database (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0c423-115">Opciones</span><span class="sxs-lookup"><span data-stu-id="0c423-115">Options</span></span></td>
<td><span data-ttu-id="0c423-116">Devuelve un <a href="hh579532(v=exchg.10).md">OpenDatabaseGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="0c423-116">Returns a <a href="hh579532(v=exchg.10).md">OpenDatabaseGrbit</a>.</span></span> <span data-ttu-id="0c423-117">Indica si la base de datos se abre en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="0c423-117">This indicates whether the database is opened in exclusive mode.</span></span> <span data-ttu-id="0c423-118">Si la base de datos está en modo exclusivo, se devolverá <a href="hh579532(v=exchg.10).md">Exclusive</a> , de lo contrario se devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="0c423-118">If the database is in exclusive mode then <a href="hh579532(v=exchg.10).md">Exclusive</a> will be returned, otherwise zero is returned.</span></span> <span data-ttu-id="0c423-119">No se devuelven otras opciones de grbit de la base de datos para JetAttachDatabase y JetOpenDatabase.</span><span class="sxs-lookup"><span data-stu-id="0c423-119">Other database grbit options for JetAttachDatabase and JetOpenDatabase are not returned.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0c423-120">Transacciones</span><span class="sxs-lookup"><span data-stu-id="0c423-120">Transactions</span></span></td>
<td><span data-ttu-id="0c423-121">Devuelve un número uno mayor que el nivel máximo en el que se pueden anidar las transacciones.</span><span class="sxs-lookup"><span data-stu-id="0c423-121">Returns a number one greater than the maximum level to which transactions can be nested.</span></span> <span data-ttu-id="0c423-122">Si se llama a <a href="dn292105(v=exchg.10).md">JetBeginTransaction (JET_SESID)</a> (en un modo de anidamiento, es decir, en la misma sesión, sin commit o rollback) tantas veces como este valor, se devolverá la última llamada a <a href="hh564840(v=exchg.10).md">TransTooDeep</a> (Int32).</span><span class="sxs-lookup"><span data-stu-id="0c423-122">If <a href="dn292105(v=exchg.10).md">JetBeginTransaction(JET_SESID)</a> is called (in a nesting fashion, that is, on the same session, without a commit or rollback) as many times as this value, on the last call <a href="hh564840(v=exchg.10).md">TransTooDeep</a> will be returned (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0c423-123">Versión</span><span class="sxs-lookup"><span data-stu-id="0c423-123">Version</span></span></td>
<td><span data-ttu-id="0c423-124">Devuelve la versión principal del motor de base de datos (Int32).</span><span class="sxs-lookup"><span data-stu-id="0c423-124">Returns the major version of the database engine (Int32).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0c423-125">Filesize</span><span class="sxs-lookup"><span data-stu-id="0c423-125">Filesize</span></span></td>
<td><span data-ttu-id="0c423-126">Devuelve el archivo de la base de datos, en páginas (Int32).</span><span class="sxs-lookup"><span data-stu-id="0c423-126">Returns the filesize of the database, in pages (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0c423-127">SpaceOwned</span><span class="sxs-lookup"><span data-stu-id="0c423-127">SpaceOwned</span></span></td>
<td><span data-ttu-id="0c423-128">Devuelve el espacio de la base de datos, en páginas (Int32).</span><span class="sxs-lookup"><span data-stu-id="0c423-128">Returns the owned space of the database, in pages (Int32).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0c423-129">SpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="0c423-129">SpaceAvailable</span></span></td>
<td><span data-ttu-id="0c423-130">Devuelve el espacio disponible en la base de datos, en páginas (Int32).</span><span class="sxs-lookup"><span data-stu-id="0c423-130">Returns the available space in the database, in pages (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0c423-131">Varios</span><span class="sxs-lookup"><span data-stu-id="0c423-131">Misc</span></span></td>
<td><span data-ttu-id="0c423-132">Devuelve un objeto <a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a> .</span><span class="sxs-lookup"><span data-stu-id="0c423-132">Returns a <a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a> object.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0c423-133">DBInUse</span><span class="sxs-lookup"><span data-stu-id="0c423-133">DBInUse</span></span></td>
<td><span data-ttu-id="0c423-134">Devuelve un valor booleano que indica si la base de datos está adjunta (booleana).</span><span class="sxs-lookup"><span data-stu-id="0c423-134">Returns a boolean indicating whether the database is attached (boolean).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0c423-135">PageSize</span><span class="sxs-lookup"><span data-stu-id="0c423-135">PageSize</span></span></td>
<td><span data-ttu-id="0c423-136">Devuelve el tamaño de página de la base de datos (Int32).</span><span class="sxs-lookup"><span data-stu-id="0c423-136">Returns the page size of the database (Int32).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0c423-137">FileType</span><span class="sxs-lookup"><span data-stu-id="0c423-137">FileType</span></span></td>
<td><span data-ttu-id="0c423-138">Devuelve el tipo de la base de datos (<a href="hh566739(v=exchg.10).md">JET_filetype</a>).</span><span class="sxs-lookup"><span data-stu-id="0c423-138">Returns the type of the database (<a href="hh566739(v=exchg.10).md">JET_filetype</a>).</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="0c423-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c423-139">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0c423-140">Referencia</span><span class="sxs-lookup"><span data-stu-id="0c423-140">Reference</span></span>

[<span data-ttu-id="0c423-141">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0c423-141">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
