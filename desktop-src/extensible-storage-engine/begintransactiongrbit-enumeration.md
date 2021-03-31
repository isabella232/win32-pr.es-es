---
description: 'Más información sobre: enumeración BeginTransactionGrbit'
title: Enumeración BeginTransactionGrbit
TOCTitle: BeginTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.begintransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39515115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit
- Microsoft.Isam.Esent.Interop.BeginTransactionGrbit.ReadOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5f407c54b7b6e76ab63dcfb97d1307458ba15277
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816982"
---
# <a name="begintransactiongrbit-enumeration"></a><span data-ttu-id="06092-103">Enumeración BeginTransactionGrbit</span><span class="sxs-lookup"><span data-stu-id="06092-103">BeginTransactionGrbit enumeration</span></span>

<span data-ttu-id="06092-104">Opciones de [JetBeginTransaction2 (JET_SESID, BeginTransactionGrbit)](./api.jetbegintransaction2-method.md).</span><span class="sxs-lookup"><span data-stu-id="06092-104">Options for [JetBeginTransaction2(JET_SESID, BeginTransactionGrbit)](./api.jetbegintransaction2-method.md).</span></span>

<span data-ttu-id="06092-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="06092-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="06092-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="06092-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="06092-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="06092-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="06092-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06092-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BeginTransactionGrbit
'Usage
Dim instance As BeginTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum BeginTransactionGrbit
```

## <a name="members"></a><span data-ttu-id="06092-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="06092-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="06092-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="06092-110">Member name</span></span></th>
<th><span data-ttu-id="06092-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="06092-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="06092-112">None</span><span class="sxs-lookup"><span data-stu-id="06092-112">None</span></span></td>
<td><span data-ttu-id="06092-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="06092-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="06092-114">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="06092-114">ReadOnly</span></span></td>
<td><span data-ttu-id="06092-115">La transacción no modificará la base de datos.</span><span class="sxs-lookup"><span data-stu-id="06092-115">The transaction will not modify the database.</span></span> <span data-ttu-id="06092-116">Si se intenta realizar una actualización, se producirá un error en la operación con <a href="hh564840(v=exchg.10).md">TransReadOnly</a>.</span><span class="sxs-lookup"><span data-stu-id="06092-116">If an update is attempted, that operation will fail with <a href="hh564840(v=exchg.10).md">TransReadOnly</a>.</span></span> <span data-ttu-id="06092-117">Se omite esta opción a menos que se solicite cuando la sesión especificada no está ya en una transacción.</span><span class="sxs-lookup"><span data-stu-id="06092-117">This option is ignored unless it is requested when the given session is not already in a transaction.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="06092-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="06092-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="06092-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="06092-119">Reference</span></span>

[<span data-ttu-id="06092-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="06092-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
