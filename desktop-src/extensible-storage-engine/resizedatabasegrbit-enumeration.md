---
description: 'Más información sobre: enumeración ResizeDatabaseGrbit'
title: Enumeración ResizeDatabaseGrbit (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: ResizeDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.resizedatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 55104329
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.OnlyGrow
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit
- Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit.OnlyGrow
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51d703f96882136e2b88f1a2df37609573c725e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687677"
---
# <a name="resizedatabasegrbit-enumeration"></a><span data-ttu-id="b0a8f-103">Enumeración ResizeDatabaseGrbit</span><span class="sxs-lookup"><span data-stu-id="b0a8f-103">ResizeDatabaseGrbit enumeration</span></span>

<span data-ttu-id="b0a8f-104">Opciones para [JetResizeDatabase (JET_SESID, JET_DBID, Int32, Int32, ResizeDatabaseGrbit)](./windows8api.jetresizedatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="b0a8f-104">Options for [JetResizeDatabase(JET_SESID, JET_DBID, Int32, Int32, ResizeDatabaseGrbit)](./windows8api.jetresizedatabase-method.md).</span></span>

<span data-ttu-id="b0a8f-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="b0a8f-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="b0a8f-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b0a8f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="b0a8f-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b0a8f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b0a8f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0a8f-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ResizeDatabaseGrbit
'Usage
Dim instance As ResizeDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum ResizeDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="b0a8f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="b0a8f-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="b0a8f-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="b0a8f-110">Member name</span></span></th>
<th><span data-ttu-id="b0a8f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0a8f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b0a8f-112">None</span><span class="sxs-lookup"><span data-stu-id="b0a8f-112">None</span></span></td>
<td><span data-ttu-id="b0a8f-113">No hay opciones.</span><span class="sxs-lookup"><span data-stu-id="b0a8f-113">No option.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="b0a8f-114">OnlyGrow</span><span class="sxs-lookup"><span data-stu-id="b0a8f-114">OnlyGrow</span></span></td>
<td><span data-ttu-id="b0a8f-115">Crezca solo la base de datos.</span><span class="sxs-lookup"><span data-stu-id="b0a8f-115">Only grow the database.</span></span> <span data-ttu-id="b0a8f-116">Si la llamada de cambiar tamaño reduciría la base de datos, no haga nada.</span><span class="sxs-lookup"><span data-stu-id="b0a8f-116">If the resize call would shrink the database, do nothing.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="b0a8f-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0a8f-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b0a8f-118">Referencia</span><span class="sxs-lookup"><span data-stu-id="b0a8f-118">Reference</span></span>

[<span data-ttu-id="b0a8f-119">Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="b0a8f-119">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
