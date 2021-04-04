---
description: 'Más información sobre: enumeración ObjectInfoFlags'
title: Enumeración ObjectInfoFlags
TOCTitle: ObjectInfoFlags enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ObjectInfoFlags
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.objectinfoflags(v=EXCHG.10)
ms:contentKeyID: 39515824
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.None
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.System
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableDerived
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableTemplate
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableFixedDDL
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableNoFixedVarColumnsInDerivedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.System
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableDerived
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.None
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableFixedDDL
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableNoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableTemplate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b3f301f1e786d126dbd57c071fe89356e0acc891
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910241"
---
# <a name="objectinfoflags-enumeration"></a><span data-ttu-id="db5de-103">Enumeración ObjectInfoFlags</span><span class="sxs-lookup"><span data-stu-id="db5de-103">ObjectInfoFlags enumeration</span></span>

<span data-ttu-id="db5de-104">Marcas para objetos ESENT (tablas).</span><span class="sxs-lookup"><span data-stu-id="db5de-104">Flags for ESENT objects (tables).</span></span> <span data-ttu-id="db5de-105">Se usa en [JET_OBJECTINFO](./jet-objectinfo-class.md).</span><span class="sxs-lookup"><span data-stu-id="db5de-105">Used in [JET_OBJECTINFO](./jet-objectinfo-class.md).</span></span>

<span data-ttu-id="db5de-106">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="db5de-106">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="db5de-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="db5de-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="db5de-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="db5de-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="db5de-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db5de-109">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ObjectInfoFlags
'Usage
Dim instance As ObjectInfoFlags
```

``` csharp
[FlagsAttribute]
public enum ObjectInfoFlags
```

## <a name="members"></a><span data-ttu-id="db5de-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="db5de-110">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="db5de-111">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="db5de-111">Member name</span></span></th>
<th><span data-ttu-id="db5de-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="db5de-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="db5de-113">None</span><span class="sxs-lookup"><span data-stu-id="db5de-113">None</span></span></td>
<td><span data-ttu-id="db5de-114">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="db5de-114">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="db5de-115">System</span><span class="sxs-lookup"><span data-stu-id="db5de-115">System</span></span></td>
<td><span data-ttu-id="db5de-116">El objeto solo es para uso interno.</span><span class="sxs-lookup"><span data-stu-id="db5de-116">Object is for internal use only.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="db5de-117">TableFixedDDL</span><span class="sxs-lookup"><span data-stu-id="db5de-117">TableFixedDDL</span></span></td>
<td><span data-ttu-id="db5de-118">El DDL de la tabla es fijo.</span><span class="sxs-lookup"><span data-stu-id="db5de-118">Table's DDL is fixed.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="db5de-119">TableTemplate</span><span class="sxs-lookup"><span data-stu-id="db5de-119">TableTemplate</span></span></td>
<td><span data-ttu-id="db5de-120">El DDL de la tabla es heredable.</span><span class="sxs-lookup"><span data-stu-id="db5de-120">Table's DDL is inheritable.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="db5de-121">TableDerived</span><span class="sxs-lookup"><span data-stu-id="db5de-121">TableDerived</span></span></td>
<td><span data-ttu-id="db5de-122">El DDL de la tabla se hereda de una tabla de plantillas.</span><span class="sxs-lookup"><span data-stu-id="db5de-122">Table's DDL is inherited from a template table.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="db5de-123">TableNoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="db5de-123">TableNoFixedVarColumnsInDerivedTables</span></span></td>
<td><span data-ttu-id="db5de-124">Columnas fijas o variables en las tablas derivadas (de modo que se puedan agregar columnas fijas o de variables a la plantilla en el futuro).</span><span class="sxs-lookup"><span data-stu-id="db5de-124">Fixed or variable columns in derived tables (so that fixed or variable columns can be added to the template in the future).</span></span> <span data-ttu-id="db5de-125">Se usa junto con TableTemplate.</span><span class="sxs-lookup"><span data-stu-id="db5de-125">Used in conjunction with TableTemplate.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="db5de-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="db5de-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="db5de-127">Referencia</span><span class="sxs-lookup"><span data-stu-id="db5de-127">Reference</span></span>

[<span data-ttu-id="db5de-128">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="db5de-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
