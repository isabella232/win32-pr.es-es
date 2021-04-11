---
description: 'Más información sobre: enumeración EndExternalBackupGrbit'
title: Enumeración EndExternalBackupGrbit
TOCTitle: EndExternalBackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.endexternalbackupgrbit(v=EXCHG.10)
ms:contentKeyID: 39516835
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Abort
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Normal
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Abort
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.None
- Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit.Normal
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0bb3fb2f3e959d41c042589f3a280e6466fe4970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279261"
---
# <a name="endexternalbackupgrbit-enumeration"></a><span data-ttu-id="313bb-103">Enumeración EndExternalBackupGrbit</span><span class="sxs-lookup"><span data-stu-id="313bb-103">EndExternalBackupGrbit enumeration</span></span>

<span data-ttu-id="313bb-104">Opciones de [JetEndExternalBackupInstance (JET_INSTANCE)](./api.jetendexternalbackupinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="313bb-104">Options for [JetEndExternalBackupInstance(JET_INSTANCE)](./api.jetendexternalbackupinstance-method.md).</span></span>

<span data-ttu-id="313bb-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="313bb-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="313bb-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="313bb-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="313bb-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="313bb-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="313bb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="313bb-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EndExternalBackupGrbit
'Usage
Dim instance As EndExternalBackupGrbit
```

``` csharp
[FlagsAttribute]
public enum EndExternalBackupGrbit
```

## <a name="members"></a><span data-ttu-id="313bb-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="313bb-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="313bb-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="313bb-110">Member name</span></span></th>
<th><span data-ttu-id="313bb-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="313bb-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="313bb-112">None</span><span class="sxs-lookup"><span data-stu-id="313bb-112">None</span></span></td>
<td><span data-ttu-id="313bb-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="313bb-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="313bb-114">Normal</span><span class="sxs-lookup"><span data-stu-id="313bb-114">Normal</span></span></td>
<td><span data-ttu-id="313bb-115">La aplicación cliente finalizó la copia de seguridad por completo y termina normalmente.</span><span class="sxs-lookup"><span data-stu-id="313bb-115">The client application finished the backup completely, and is ending normally.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="313bb-116">Abort</span><span class="sxs-lookup"><span data-stu-id="313bb-116">Abort</span></span></td>
<td><span data-ttu-id="313bb-117">La aplicación cliente está anulando la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="313bb-117">The client application is aborting the backup.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="313bb-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="313bb-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="313bb-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="313bb-119">Reference</span></span>

[<span data-ttu-id="313bb-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="313bb-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
