---
description: 'Más información sobre: enumeración UpdateGrbit'
title: Enumeración UpdateGrbit (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: UpdateGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.updategrbit(v=EXCHG.10)
ms:contentKeyID: 39514938
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.CheckESE97Compatibility
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.None
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.CheckESE97Compatibility
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e27809ef16fb00fd538e4c37826d10fefa3b396c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542414"
---
# <a name="updategrbit-enumeration"></a><span data-ttu-id="dc406-103">Enumeración UpdateGrbit</span><span class="sxs-lookup"><span data-stu-id="dc406-103">UpdateGrbit enumeration</span></span>

<span data-ttu-id="dc406-104">Opciones para [JetUpdate2 (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32, UpdateGrbit)](./server2003api.jetupdate2-method.md).</span><span class="sxs-lookup"><span data-stu-id="dc406-104">Options for [JetUpdate2(JET_SESID, JET_TABLEID, \[\], Int32, Int32, UpdateGrbit)](./server2003api.jetupdate2-method.md).</span></span>

<span data-ttu-id="dc406-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="dc406-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="dc406-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dc406-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="dc406-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dc406-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dc406-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc406-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration UpdateGrbit
'Usage
Dim instance As UpdateGrbit
```

``` csharp
[FlagsAttribute]
public enum UpdateGrbit
```

## <a name="members"></a><span data-ttu-id="dc406-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="dc406-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="dc406-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="dc406-110">Member name</span></span></th>
<th><span data-ttu-id="dc406-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc406-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="dc406-112">None</span><span class="sxs-lookup"><span data-stu-id="dc406-112">None</span></span></td>
<td><span data-ttu-id="dc406-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="dc406-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="dc406-114">CheckESE97Compatibility</span><span class="sxs-lookup"><span data-stu-id="dc406-114">CheckESE97Compatibility</span></span></td>
<td><span data-ttu-id="dc406-115"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="dc406-115"><strong>Obsolete.</strong></span></span> <span data-ttu-id="dc406-116">Esta marca hace que la actualización devuelva un error si la actualización no hubiera sido posible en la versión de Windows 2000 de ESE, que aplicó un número máximo menor de instancias de columna multivalor en cada registro que en versiones posteriores de ESE.</span><span class="sxs-lookup"><span data-stu-id="dc406-116">This flag causes the update to return an error if the update would not have been possible in the Windows 2000 version of ESE, which enforced a smaller maximum number of multi-valued column instances in each record than later versions of ESE.</span></span> <span data-ttu-id="dc406-117">Esto solo es importante para las aplicaciones que desean replicar datos entre aplicaciones hospedadas en Windows 2000 y aplicaciones hospedadas en Windows 2003 o versiones posteriores de ESE.</span><span class="sxs-lookup"><span data-stu-id="dc406-117">This is important only for applications that wish to replicate data between applications hosted on Windows 2000 and applications hosted on Windows 2003, or later versions of ESE.</span></span> <span data-ttu-id="dc406-118">No debe ser necesario para la mayoría de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="dc406-118">It should not be necessary for most applications.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="dc406-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc406-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dc406-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="dc406-120">Reference</span></span>

[<span data-ttu-id="dc406-121">Espacio de nombres Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="dc406-121">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
