---
description: 'Más información sobre: enumeración OpenDatabaseGrbit'
title: Enumeración OpenDatabaseGrbit
TOCTitle: OpenDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.opendatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39514563
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.Exclusive
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.Exclusive
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d14fb779ec02137f6a4fce1cfdd92f46dedcb832
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277098"
---
# <a name="opendatabasegrbit-enumeration"></a><span data-ttu-id="f2704-103">Enumeración OpenDatabaseGrbit</span><span class="sxs-lookup"><span data-stu-id="f2704-103">OpenDatabaseGrbit enumeration</span></span>

<span data-ttu-id="f2704-104">Opciones para [JetOpenDatabase (JET_SESID, cadena, cadena, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="f2704-104">Options for [JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span></span>

<span data-ttu-id="f2704-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="f2704-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="f2704-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f2704-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f2704-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f2704-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f2704-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2704-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration OpenDatabaseGrbit
'Usage
Dim instance As OpenDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum OpenDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="f2704-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="f2704-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f2704-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="f2704-110">Member name</span></span></th>
<th><span data-ttu-id="f2704-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2704-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f2704-112">None</span><span class="sxs-lookup"><span data-stu-id="f2704-112">None</span></span></td>
<td><span data-ttu-id="f2704-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="f2704-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f2704-114">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="f2704-114">ReadOnly</span></span></td>
<td><span data-ttu-id="f2704-115">Impide las modificaciones en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f2704-115">Prevents modifications to the database.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f2704-116">Exclusivo</span><span class="sxs-lookup"><span data-stu-id="f2704-116">Exclusive</span></span></td>
<td><span data-ttu-id="f2704-117">Permite que una sola sesión adjunte una base de datos.</span><span class="sxs-lookup"><span data-stu-id="f2704-117">Allows only a single session to attach a database.</span></span> <span data-ttu-id="f2704-118">Normalmente, varias sesiones pueden abrir una base de datos.</span><span class="sxs-lookup"><span data-stu-id="f2704-118">Normally, several sessions can open a database.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="f2704-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2704-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f2704-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="f2704-120">Reference</span></span>

[<span data-ttu-id="f2704-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f2704-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
