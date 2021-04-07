---
description: 'Más información sobre: enumeración EscrowUpdateGrbit'
title: Enumeración EscrowUpdateGrbit
TOCTitle: EscrowUpdateGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.escrowupdategrbit(v=EXCHG.10)
ms:contentKeyID: 39514160
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.None
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.NoRollback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.None
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.NoRollback
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d301ef801a5685057a9e33beb794f3b6cf13e646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002997"
---
# <a name="escrowupdategrbit-enumeration"></a><span data-ttu-id="d9bf7-103">Enumeración EscrowUpdateGrbit</span><span class="sxs-lookup"><span data-stu-id="d9bf7-103">EscrowUpdateGrbit enumeration</span></span>

<span data-ttu-id="d9bf7-104">Opciones de JetEscrowUpdate.</span><span class="sxs-lookup"><span data-stu-id="d9bf7-104">Options for JetEscrowUpdate.</span></span>

<span data-ttu-id="d9bf7-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="d9bf7-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="d9bf7-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d9bf7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d9bf7-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d9bf7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d9bf7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9bf7-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EscrowUpdateGrbit
'Usage
Dim instance As EscrowUpdateGrbit
```

``` csharp
[FlagsAttribute]
public enum EscrowUpdateGrbit
```

## <a name="members"></a><span data-ttu-id="d9bf7-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="d9bf7-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d9bf7-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="d9bf7-110">Member name</span></span></th>
<th><span data-ttu-id="d9bf7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9bf7-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d9bf7-112">None</span><span class="sxs-lookup"><span data-stu-id="d9bf7-112">None</span></span></td>
<td><span data-ttu-id="d9bf7-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="d9bf7-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d9bf7-114">Norollback</span><span class="sxs-lookup"><span data-stu-id="d9bf7-114">NoRollback</span></span></td>
<td><span data-ttu-id="d9bf7-115">Incluso si la sesión que realiza la actualización de custodia tiene la reversión de la transacción, esta actualización no se deshará.</span><span class="sxs-lookup"><span data-stu-id="d9bf7-115">Even if the session performing the escrow update has its transaction rollback this update will not be undone.</span></span> <span data-ttu-id="d9bf7-116">Dado que es posible que las entradas de registro no se vacíen en el disco, es posible que se pierdan actualizaciones recientes de custodia realizadas con esta marca si se produce un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="d9bf7-116">As the log records may not be flushed to disk, recent escrow updates done with this flag may be lost if there is a crash.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="d9bf7-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9bf7-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d9bf7-118">Referencia</span><span class="sxs-lookup"><span data-stu-id="d9bf7-118">Reference</span></span>

[<span data-ttu-id="d9bf7-119">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d9bf7-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
