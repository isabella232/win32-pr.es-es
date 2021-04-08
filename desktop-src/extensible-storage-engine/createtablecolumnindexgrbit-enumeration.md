---
description: 'Más información sobre: enumeración CreateTableColumnIndexGrbit'
title: Enumeración CreateTableColumnIndexGrbit
TOCTitle: CreateTableColumnIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createtablecolumnindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39516657
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.FixedDDL
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.NoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.TemplateTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.TemplateTable
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.NoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.FixedDDL
- Microsoft.Isam.Esent.Interop.CreateTableColumnIndexGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72f91c5d41b8262e3b2804159914b0a9ccaaaa7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002999"
---
# <a name="createtablecolumnindexgrbit-enumeration"></a><span data-ttu-id="55ac1-103">Enumeración CreateTableColumnIndexGrbit</span><span class="sxs-lookup"><span data-stu-id="55ac1-103">CreateTableColumnIndexGrbit enumeration</span></span>

<span data-ttu-id="55ac1-104">Opciones de JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="55ac1-104">Options for JetCreateTableColumnIndex.</span></span>

<span data-ttu-id="55ac1-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="55ac1-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="55ac1-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="55ac1-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="55ac1-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="55ac1-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="55ac1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55ac1-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateTableColumnIndexGrbit
'Usage
Dim instance As CreateTableColumnIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateTableColumnIndexGrbit
```

## <a name="members"></a><span data-ttu-id="55ac1-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="55ac1-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="55ac1-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="55ac1-110">Member name</span></span></th>
<th><span data-ttu-id="55ac1-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="55ac1-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="55ac1-112">None</span><span class="sxs-lookup"><span data-stu-id="55ac1-112">None</span></span></td>
<td><span data-ttu-id="55ac1-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="55ac1-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="55ac1-114">FixedDDL</span><span class="sxs-lookup"><span data-stu-id="55ac1-114">FixedDDL</span></span></td>
<td><span data-ttu-id="55ac1-115">El DDL es fijo.</span><span class="sxs-lookup"><span data-stu-id="55ac1-115">The DDL is fixed.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="55ac1-116">TemplateTable</span><span class="sxs-lookup"><span data-stu-id="55ac1-116">TemplateTable</span></span></td>
<td><span data-ttu-id="55ac1-117">El DDL es heredable.</span><span class="sxs-lookup"><span data-stu-id="55ac1-117">The DDL is inheritable.</span></span> <span data-ttu-id="55ac1-118">Implica FixedDDL.</span><span class="sxs-lookup"><span data-stu-id="55ac1-118">Implies FixedDDL.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="55ac1-119">NoFixedVarColumnsInDerivedTables</span><span class="sxs-lookup"><span data-stu-id="55ac1-119">NoFixedVarColumnsInDerivedTables</span></span></td>
<td><span data-ttu-id="55ac1-120">Se usa junto con TemplateTable.</span><span class="sxs-lookup"><span data-stu-id="55ac1-120">Used in conjunction with TemplateTable.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="55ac1-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="55ac1-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="55ac1-122">Referencia</span><span class="sxs-lookup"><span data-stu-id="55ac1-122">Reference</span></span>

[<span data-ttu-id="55ac1-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="55ac1-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
