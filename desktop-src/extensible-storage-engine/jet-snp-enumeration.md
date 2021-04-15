---
description: 'Más información acerca de: enumeración JET_SNP'
title: Enumeración JET_SNP
TOCTitle: JET_SNP enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SNP
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_snp(v=EXCHG.10)
ms:contentKeyID: 39511218
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SNP.Backup
- Microsoft.Isam.Esent.Interop.JET_SNP.Repair
- Microsoft.Isam.Esent.Interop.JET_SNP.Compact
- Microsoft.Isam.Esent.Interop.JET_SNP.Scrub
- Microsoft.Isam.Esent.Interop.JET_SNP
- Microsoft.Isam.Esent.Interop.JET_SNP.Restore
- Microsoft.Isam.Esent.Interop.JET_SNP.UpgradeRecordFormat
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SNP.Scrub
- Microsoft.Isam.Esent.Interop.JET_SNP
- Microsoft.Isam.Esent.Interop.JET_SNP.Backup
- Microsoft.Isam.Esent.Interop.JET_SNP.Restore
- Microsoft.Isam.Esent.Interop.JET_SNP.UpgradeRecordFormat
- Microsoft.Isam.Esent.Interop.JET_SNP.Compact
- Microsoft.Isam.Esent.Interop.JET_SNP.Repair
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10061d0c00d90aa5ca4e0778cba046d2e6f62f4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696226"
---
# <a name="jet_snp-enumeration"></a><span data-ttu-id="88720-103">Enumeración JET_SNP</span><span class="sxs-lookup"><span data-stu-id="88720-103">JET_SNP enumeration</span></span>

<span data-ttu-id="88720-104">El tipo de operación para el que se está informando de progreso.</span><span class="sxs-lookup"><span data-stu-id="88720-104">The type of operation that progress is being reported for.</span></span>

<span data-ttu-id="88720-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="88720-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="88720-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="88720-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="88720-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88720-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_SNP
'Usage
Dim instance As JET_SNP
```

``` csharp
public enum JET_SNP
```

## <a name="members"></a><span data-ttu-id="88720-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="88720-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="88720-109">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="88720-109">Member name</span></span></th>
<th><span data-ttu-id="88720-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="88720-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="88720-111">Reparación</span><span class="sxs-lookup"><span data-stu-id="88720-111">Repair</span></span></td>
<td><span data-ttu-id="88720-112">La devolución de llamada es para una opción de reparación.</span><span class="sxs-lookup"><span data-stu-id="88720-112">Callback is for a repair option.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="88720-113">Compacto</span><span class="sxs-lookup"><span data-stu-id="88720-113">Compact</span></span></td>
<td><span data-ttu-id="88720-114">La devolución de llamada es para desfragmentación de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="88720-114">Callback is for database defragmentation.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="88720-115">Restauración</span><span class="sxs-lookup"><span data-stu-id="88720-115">Restore</span></span></td>
<td><span data-ttu-id="88720-116">La devolución de llamada es para las opciones de restauración.</span><span class="sxs-lookup"><span data-stu-id="88720-116">Callback is for a restore options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="88720-117">Copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="88720-117">Backup</span></span></td>
<td><span data-ttu-id="88720-118">La devolución de llamada es para las opciones de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="88720-118">Callback is for a backup options.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="88720-119">Scrub</span><span class="sxs-lookup"><span data-stu-id="88720-119">Scrub</span></span></td>
<td><span data-ttu-id="88720-120">La devolución de llamada es para el llenado de ceros de base de datos.</span><span class="sxs-lookup"><span data-stu-id="88720-120">Callback is for database zeroing.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="88720-121">UpgradeRecordFormat</span><span class="sxs-lookup"><span data-stu-id="88720-121">UpgradeRecordFormat</span></span></td>
<td><span data-ttu-id="88720-122">La devolución de llamada es para el proceso de actualización del formato de registro de todas las páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="88720-122">Callback is for the process of upgrading the record format of all database pages.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="88720-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="88720-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="88720-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="88720-124">Reference</span></span>

[<span data-ttu-id="88720-125">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="88720-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
