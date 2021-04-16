---
description: 'Más información sobre: enumeración AttachDatabaseGrbit'
title: Enumeración AttachDatabaseGrbit
TOCTitle: AttachDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.attachdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39514410
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.DeleteCorruptIndexes
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.DeleteCorruptIndexes
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81525e97f1b6266ba15baab50168404566bd7bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678509"
---
# <a name="attachdatabasegrbit-enumeration"></a><span data-ttu-id="9f79d-103">Enumeración AttachDatabaseGrbit</span><span class="sxs-lookup"><span data-stu-id="9f79d-103">AttachDatabaseGrbit enumeration</span></span>

<span data-ttu-id="9f79d-104">Opciones de JetAttachDatabase.</span><span class="sxs-lookup"><span data-stu-id="9f79d-104">Options for JetAttachDatabase.</span></span>

<span data-ttu-id="9f79d-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="9f79d-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="9f79d-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9f79d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9f79d-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9f79d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9f79d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f79d-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration AttachDatabaseGrbit
'Usage
Dim instance As AttachDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum AttachDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="9f79d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="9f79d-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="9f79d-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="9f79d-110">Member name</span></span></th>
<th><span data-ttu-id="9f79d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f79d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9f79d-112">None</span><span class="sxs-lookup"><span data-stu-id="9f79d-112">None</span></span></td>
<td><span data-ttu-id="9f79d-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="9f79d-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="9f79d-114">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="9f79d-114">ReadOnly</span></span></td>
<td><span data-ttu-id="9f79d-115">Impide las modificaciones en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="9f79d-115">Prevents modifications to the database.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9f79d-116">DeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="9f79d-116">DeleteCorruptIndexes</span></span></td>
<td><span data-ttu-id="9f79d-117">Si se ha establecido JET_paramEnableIndexChecking, se eliminarán todos los índices sobre los datos Unicode.</span><span class="sxs-lookup"><span data-stu-id="9f79d-117">If JET_paramEnableIndexChecking has been set, all indexes over Unicode data will be deleted.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="9f79d-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f79d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9f79d-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="9f79d-119">Reference</span></span>

[<span data-ttu-id="9f79d-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9f79d-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
