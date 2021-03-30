---
description: 'Más información sobre: enumeración TermGrbit'
title: Enumeración TermGrbit
TOCTitle: TermGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.TermGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.termgrbit(v=EXCHG.10)
ms:contentKeyID: 39511147
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.TermGrbit
- Microsoft.Isam.Esent.Interop.TermGrbit.Abrupt
- Microsoft.Isam.Esent.Interop.TermGrbit.Complete
- Microsoft.Isam.Esent.Interop.TermGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.TermGrbit.None
- Microsoft.Isam.Esent.Interop.TermGrbit
- Microsoft.Isam.Esent.Interop.TermGrbit.Complete
- Microsoft.Isam.Esent.Interop.TermGrbit.Abrupt
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 49b466b298a78d7bfd6822904aed977e7117b927
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817139"
---
# <a name="termgrbit-enumeration"></a><span data-ttu-id="66dcb-103">Enumeración TermGrbit</span><span class="sxs-lookup"><span data-stu-id="66dcb-103">TermGrbit enumeration</span></span>

<span data-ttu-id="66dcb-104">Opciones de [JetTerm2 (JET_INSTANCE, TermGrbit)](./api.jetterm2-method.md).</span><span class="sxs-lookup"><span data-stu-id="66dcb-104">Options for [JetTerm2(JET_INSTANCE, TermGrbit)](./api.jetterm2-method.md).</span></span>

<span data-ttu-id="66dcb-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="66dcb-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="66dcb-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="66dcb-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="66dcb-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="66dcb-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="66dcb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66dcb-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration TermGrbit
'Usage
Dim instance As TermGrbit
```

``` csharp
[FlagsAttribute]
public enum TermGrbit
```

## <a name="members"></a><span data-ttu-id="66dcb-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="66dcb-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="66dcb-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="66dcb-110">Member name</span></span></th>
<th><span data-ttu-id="66dcb-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="66dcb-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="66dcb-112">None</span><span class="sxs-lookup"><span data-stu-id="66dcb-112">None</span></span></td>
<td><span data-ttu-id="66dcb-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="66dcb-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="66dcb-114">Completo</span><span class="sxs-lookup"><span data-stu-id="66dcb-114">Complete</span></span></td>
<td><span data-ttu-id="66dcb-115">Solicita que la instancia se cierre sin problemas.</span><span class="sxs-lookup"><span data-stu-id="66dcb-115">Requests that the instance be shut down cleanly.</span></span> <span data-ttu-id="66dcb-116">Cualquier trabajo de limpieza opcional que se haría normalmente en segundo plano en tiempo de ejecución se completa inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="66dcb-116">Any optional cleanup work that would ordinarily be done in the background at run time is completed immediately.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="66dcb-117">Abrupta</span><span class="sxs-lookup"><span data-stu-id="66dcb-117">Abrupt</span></span></td>
<td><span data-ttu-id="66dcb-118">Solicita que la instancia se cierre lo más rápido posible.</span><span class="sxs-lookup"><span data-stu-id="66dcb-118">Requests that the instance be shut down as quickly as possible.</span></span> <span data-ttu-id="66dcb-119">Se abandona cualquier trabajo opcional que normalmente se realizaría en segundo plano en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="66dcb-119">Any optional work that would ordinarily be done in the background at run time is abandoned.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="66dcb-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="66dcb-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="66dcb-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="66dcb-121">Reference</span></span>

[<span data-ttu-id="66dcb-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="66dcb-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="66dcb-123">OnDirty</span><span class="sxs-lookup"><span data-stu-id="66dcb-123">Dirty</span></span>](./windows7grbits.dirty-field.md)
