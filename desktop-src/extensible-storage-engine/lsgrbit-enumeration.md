---
description: 'Más información sobre: enumeración LsGrbit'
title: Enumeración LsGrbit
TOCTitle: LsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.LsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.lsgrbit(v=EXCHG.10)
ms:contentKeyID: 39514518
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.LsGrbit
- Microsoft.Isam.Esent.Interop.LsGrbit.Cursor
- Microsoft.Isam.Esent.Interop.LsGrbit.None
- Microsoft.Isam.Esent.Interop.LsGrbit.Reset
- Microsoft.Isam.Esent.Interop.LsGrbit.Table
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.LsGrbit
- Microsoft.Isam.Esent.Interop.LsGrbit.Reset
- Microsoft.Isam.Esent.Interop.LsGrbit.None
- Microsoft.Isam.Esent.Interop.LsGrbit.Table
- Microsoft.Isam.Esent.Interop.LsGrbit.Cursor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5fc0a60d039d0eb1307558d42a3e7a3c7e99eb86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082187"
---
# <a name="lsgrbit-enumeration"></a><span data-ttu-id="c1c41-103">Enumeración LsGrbit</span><span class="sxs-lookup"><span data-stu-id="c1c41-103">LsGrbit enumeration</span></span>

<span data-ttu-id="c1c41-104">Opciones para [JetSetLS (JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md) y [JetGetLS (JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetgetls-method.md).</span><span class="sxs-lookup"><span data-stu-id="c1c41-104">Options for [JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md) and [JetGetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetgetls-method.md).</span></span>

<span data-ttu-id="c1c41-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="c1c41-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="c1c41-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c1c41-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c1c41-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c1c41-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c1c41-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1c41-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration LsGrbit
'Usage
Dim instance As LsGrbit
```

``` csharp
[FlagsAttribute]
public enum LsGrbit
```

## <a name="members"></a><span data-ttu-id="c1c41-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c1c41-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="c1c41-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="c1c41-110">Member name</span></span></th>
<th><span data-ttu-id="c1c41-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1c41-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c1c41-112">None</span><span class="sxs-lookup"><span data-stu-id="c1c41-112">None</span></span></td>
<td><span data-ttu-id="c1c41-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="c1c41-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="c1c41-114">Reset</span><span class="sxs-lookup"><span data-stu-id="c1c41-114">Reset</span></span></td>
<td><span data-ttu-id="c1c41-115">El identificador de contexto para el objeto elegido debe restablecerse a JET_LSNil.</span><span class="sxs-lookup"><span data-stu-id="c1c41-115">The context handle for the chosen object should be reset to JET_LSNil.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c1c41-116">Cursor</span><span class="sxs-lookup"><span data-stu-id="c1c41-116">Cursor</span></span></td>
<td><span data-ttu-id="c1c41-117">Especifica que el identificador de contexto debe estar asociado al cursor especificado.</span><span class="sxs-lookup"><span data-stu-id="c1c41-117">Specifies the context handle should be associated with the given cursor.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="c1c41-118">Tabla</span><span class="sxs-lookup"><span data-stu-id="c1c41-118">Table</span></span></td>
<td><span data-ttu-id="c1c41-119">Especifica que el identificador de contexto se debe asociar a la tabla asociada al cursor especificado.</span><span class="sxs-lookup"><span data-stu-id="c1c41-119">Specifies that the context handle should be associated with the table associated with the given cursor.</span></span> <span data-ttu-id="c1c41-120">No se puede usar esta opción con cursor.</span><span class="sxs-lookup"><span data-stu-id="c1c41-120">It is illegal to use this option with Cursor.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="c1c41-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1c41-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c1c41-122">Referencia</span><span class="sxs-lookup"><span data-stu-id="c1c41-122">Reference</span></span>

[<span data-ttu-id="c1c41-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c1c41-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
