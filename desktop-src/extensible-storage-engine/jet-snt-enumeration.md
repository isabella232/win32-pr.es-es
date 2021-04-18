---
description: 'Más información acerca de: enumeración JET_SNT'
title: Enumeración JET_SNT
TOCTitle: JET_SNT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SNT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_snt(v=EXCHG.10)
ms:contentKeyID: 39511261
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SNT.Progress
- Microsoft.Isam.Esent.Interop.JET_SNT
- Microsoft.Isam.Esent.Interop.JET_SNT.Begin
- Microsoft.Isam.Esent.Interop.JET_SNT.Complete
- Microsoft.Isam.Esent.Interop.JET_SNT.RecoveryStep
- Microsoft.Isam.Esent.Interop.JET_SNT.Fail
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SNT
- Microsoft.Isam.Esent.Interop.JET_SNT.Complete
- Microsoft.Isam.Esent.Interop.JET_SNT.Begin
- Microsoft.Isam.Esent.Interop.JET_SNT.Progress
- Microsoft.Isam.Esent.Interop.JET_SNT.RecoveryStep
- Microsoft.Isam.Esent.Interop.JET_SNT.Fail
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f6cad661d8265c32d605bbef94d75714ccb1783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714975"
---
# <a name="jet_snt-enumeration"></a><span data-ttu-id="d1f5e-103">Enumeración JET_SNT</span><span class="sxs-lookup"><span data-stu-id="d1f5e-103">JET_SNT enumeration</span></span>

<span data-ttu-id="d1f5e-104">Tipo de progreso en el que se va a informar.</span><span class="sxs-lookup"><span data-stu-id="d1f5e-104">Type of progress being reported.</span></span>

<span data-ttu-id="d1f5e-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d1f5e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d1f5e-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d1f5e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d1f5e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1f5e-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_SNT
'Usage
Dim instance As JET_SNT
```

``` csharp
public enum JET_SNT
```

## <a name="members"></a><span data-ttu-id="d1f5e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1f5e-108">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d1f5e-109">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="d1f5e-109">Member name</span></span></th>
<th><span data-ttu-id="d1f5e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1f5e-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d1f5e-111">Comenzar</span><span class="sxs-lookup"><span data-stu-id="d1f5e-111">Begin</span></span></td>
<td><span data-ttu-id="d1f5e-112">Devolución de llamada para el inicio de una operación.</span><span class="sxs-lookup"><span data-stu-id="d1f5e-112">Callback for the beginning of an operation.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d1f5e-113">Progreso</span><span class="sxs-lookup"><span data-stu-id="d1f5e-113">Progress</span></span></td>
<td><span data-ttu-id="d1f5e-114">Devolución de llamada para el progreso de la operación.</span><span class="sxs-lookup"><span data-stu-id="d1f5e-114">Callback for operation progress.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d1f5e-115">Completo</span><span class="sxs-lookup"><span data-stu-id="d1f5e-115">Complete</span></span></td>
<td><span data-ttu-id="d1f5e-116">Devolución de llamada para la finalización de una operación.</span><span class="sxs-lookup"><span data-stu-id="d1f5e-116">Callback for the completion of an operation.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d1f5e-117">Suspenso</span><span class="sxs-lookup"><span data-stu-id="d1f5e-117">Fail</span></span></td>
<td><span data-ttu-id="d1f5e-118">Devolución de llamada para el error durante la operación.</span><span class="sxs-lookup"><span data-stu-id="d1f5e-118">Callback for failure during the operation.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d1f5e-119">RecoveryStep</span><span class="sxs-lookup"><span data-stu-id="d1f5e-119">RecoveryStep</span></span></td>
<td><span data-ttu-id="d1f5e-120">Devolución de llamada para el control de recuperación.</span><span class="sxs-lookup"><span data-stu-id="d1f5e-120">Callback for recovery control.</span></span>
<p><span data-ttu-id="d1f5e-121">Se usa para el procesamiento interno en versiones del sistema operativo Windows anteriores a Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d1f5e-121">Used for internal processing in versions of the Windows operating system earlier than Windows 8.</span></span> <span data-ttu-id="d1f5e-122">Este valor no es aplicable a las versiones de Windows a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d1f5e-122">This value is not applicable to versions of Windows starting with Windows 8.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="d1f5e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1f5e-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d1f5e-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="d1f5e-124">Reference</span></span>

[<span data-ttu-id="d1f5e-125">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d1f5e-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
