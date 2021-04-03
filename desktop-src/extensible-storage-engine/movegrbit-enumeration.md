---
description: 'Más información sobre: enumeración MoveGrbit'
title: Enumeración MoveGrbit
TOCTitle: MoveGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.MoveGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.movegrbit(v=EXCHG.10)
ms:contentKeyID: 39513771
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.MoveGrbit
- Microsoft.Isam.Esent.Interop.MoveGrbit.MoveKeyNE
- Microsoft.Isam.Esent.Interop.MoveGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.MoveGrbit
- Microsoft.Isam.Esent.Interop.MoveGrbit.None
- Microsoft.Isam.Esent.Interop.MoveGrbit.MoveKeyNE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81f047cd69bca668a5eae2b5147d8c0a137011e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082741"
---
# <a name="movegrbit-enumeration"></a><span data-ttu-id="8dc19-103">Enumeración MoveGrbit</span><span class="sxs-lookup"><span data-stu-id="8dc19-103">MoveGrbit enumeration</span></span>

<span data-ttu-id="8dc19-104">Opciones de JetMove.</span><span class="sxs-lookup"><span data-stu-id="8dc19-104">Options for JetMove.</span></span>

<span data-ttu-id="8dc19-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="8dc19-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="8dc19-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8dc19-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8dc19-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8dc19-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8dc19-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8dc19-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration MoveGrbit
'Usage
Dim instance As MoveGrbit
```

``` csharp
[FlagsAttribute]
public enum MoveGrbit
```

## <a name="members"></a><span data-ttu-id="8dc19-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="8dc19-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="8dc19-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="8dc19-110">Member name</span></span></th>
<th><span data-ttu-id="8dc19-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8dc19-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8dc19-112">None</span><span class="sxs-lookup"><span data-stu-id="8dc19-112">None</span></span></td>
<td><span data-ttu-id="8dc19-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="8dc19-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8dc19-114">MoveKeyNE</span><span class="sxs-lookup"><span data-stu-id="8dc19-114">MoveKeyNE</span></span></td>
<td><span data-ttu-id="8dc19-115">Mueve el cursor hacia delante o hacia atrás por el número de entradas de índice necesarias para omitir el número solicitado de valores de clave de índice encontrados en el índice.</span><span class="sxs-lookup"><span data-stu-id="8dc19-115">Moves the cursor forward or backward by the number of index entries required to skip the requested number of index key values encountered in the index.</span></span> <span data-ttu-id="8dc19-116">Esto tiene el efecto de contraer las entradas de índice con valores de clave duplicados en una sola entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="8dc19-116">This has the effect of collapsing index entries with duplicate key values into a single index entry.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="8dc19-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="8dc19-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8dc19-118">Referencia</span><span class="sxs-lookup"><span data-stu-id="8dc19-118">Reference</span></span>

[<span data-ttu-id="8dc19-119">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8dc19-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
