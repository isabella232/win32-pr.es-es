---
description: 'Más información sobre: enumeración RollbackTransactionGrbit'
title: Enumeración RollbackTransactionGrbit
TOCTitle: RollbackTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.rollbacktransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39513584
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.RollbackAll
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.RollbackAll
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf2635d94070fc47bebbd6cdd0e53deddeb4c5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687674"
---
# <a name="rollbacktransactiongrbit-enumeration"></a><span data-ttu-id="96a40-103">Enumeración RollbackTransactionGrbit</span><span class="sxs-lookup"><span data-stu-id="96a40-103">RollbackTransactionGrbit enumeration</span></span>

<span data-ttu-id="96a40-104">Opciones de JetRollbackTransaction.</span><span class="sxs-lookup"><span data-stu-id="96a40-104">Options for JetRollbackTransaction.</span></span>

<span data-ttu-id="96a40-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="96a40-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="96a40-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="96a40-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="96a40-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="96a40-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="96a40-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96a40-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration RollbackTransactionGrbit
'Usage
Dim instance As RollbackTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum RollbackTransactionGrbit
```

## <a name="members"></a><span data-ttu-id="96a40-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="96a40-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="96a40-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="96a40-110">Member name</span></span></th>
<th><span data-ttu-id="96a40-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="96a40-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="96a40-112">None</span><span class="sxs-lookup"><span data-stu-id="96a40-112">None</span></span></td>
<td><span data-ttu-id="96a40-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="96a40-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="96a40-114">RollbackAll</span><span class="sxs-lookup"><span data-stu-id="96a40-114">RollbackAll</span></span></td>
<td><span data-ttu-id="96a40-115">Esta opción solicita que se deshagan todos los cambios realizados en el estado de la base de datos durante todos los puntos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="96a40-115">This option requests that all changes made to the state of the database during all save points be undone.</span></span> <span data-ttu-id="96a40-116">Como resultado, la sesión finalizará la transacción.</span><span class="sxs-lookup"><span data-stu-id="96a40-116">As a result, the session will exit the transaction.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="96a40-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="96a40-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="96a40-118">Referencia</span><span class="sxs-lookup"><span data-stu-id="96a40-118">Reference</span></span>

[<span data-ttu-id="96a40-119">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="96a40-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
