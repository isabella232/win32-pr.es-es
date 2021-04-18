---
description: 'Más información sobre: enumeración SetCurrentIndexGrbit'
title: Enumeración SetCurrentIndexGrbit
TOCTitle: SetCurrentIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setcurrentindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39515072
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.MoveFirst
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.NoMove
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.None
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.NoMove
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.MoveFirst
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2391715332989bf20aae3d0a666c1cef2ce2e135
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715319"
---
# <a name="setcurrentindexgrbit-enumeration"></a><span data-ttu-id="1341d-103">Enumeración SetCurrentIndexGrbit</span><span class="sxs-lookup"><span data-stu-id="1341d-103">SetCurrentIndexGrbit enumeration</span></span>

<span data-ttu-id="1341d-104">Opciones para [JetSetCurrentIndex2 (JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit)](./api.jetsetcurrentindex2-method.md) y [JetSetCurrentIndex3 (JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit, Int32)](./api.jetsetcurrentindex3-method.md).</span><span class="sxs-lookup"><span data-stu-id="1341d-104">Options for [JetSetCurrentIndex2(JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit)](./api.jetsetcurrentindex2-method.md) and [JetSetCurrentIndex3(JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit, Int32)](./api.jetsetcurrentindex3-method.md).</span></span>

<span data-ttu-id="1341d-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="1341d-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="1341d-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1341d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1341d-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1341d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1341d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1341d-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetCurrentIndexGrbit
'Usage
Dim instance As SetCurrentIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum SetCurrentIndexGrbit
```

## <a name="members"></a><span data-ttu-id="1341d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="1341d-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="1341d-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="1341d-110">Member name</span></span></th>
<th><span data-ttu-id="1341d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="1341d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="1341d-112">None</span><span class="sxs-lookup"><span data-stu-id="1341d-112">None</span></span></td>
<td><span data-ttu-id="1341d-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="1341d-113">Default options.</span></span> <span data-ttu-id="1341d-114">Es lo mismo que MoveFirst.</span><span class="sxs-lookup"><span data-stu-id="1341d-114">This is the same as MoveFirst.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="1341d-115">MoveFirst</span><span class="sxs-lookup"><span data-stu-id="1341d-115">MoveFirst</span></span></td>
<td><span data-ttu-id="1341d-116">Indica que el cursor se debe colocar en la primera entrada del índice especificado.</span><span class="sxs-lookup"><span data-stu-id="1341d-116">Indicates that the cursor should be positioned on the first entry of the specified index.</span></span> <span data-ttu-id="1341d-117">Si se selecciona el índice actual, se omite esta opción.</span><span class="sxs-lookup"><span data-stu-id="1341d-117">If the current index is being selected then this option is ignored.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="1341d-118">Nomove</span><span class="sxs-lookup"><span data-stu-id="1341d-118">NoMove</span></span></td>
<td><span data-ttu-id="1341d-119">Indica que el cursor se debe colocar en la entrada de índice del nuevo índice que corresponde al registro asociado a la entrada de índice en la posición actual del cursor en el índice anterior.</span><span class="sxs-lookup"><span data-stu-id="1341d-119">Indicates that the cursor should be positioned on the index entry of the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="1341d-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="1341d-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1341d-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="1341d-121">Reference</span></span>

[<span data-ttu-id="1341d-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1341d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
