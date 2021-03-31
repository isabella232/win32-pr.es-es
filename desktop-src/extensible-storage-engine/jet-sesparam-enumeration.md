---
description: 'Más información acerca de: enumeración JET_sesparam'
title: Enumeración JET_sesparam (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: JET_sesparam enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_sesparam(v=EXCHG.10)
ms:contentKeyID: 55104452
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.Base
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitDefault
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitGenericContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.Base
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitGenericContext
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitDefault
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5ddfd613eecf5e9a6d9b6cec9eebcbab04e9b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154012"
---
# <a name="jet_sesparam-enumeration"></a><span data-ttu-id="40930-103">Enumeración JET_sesparam</span><span class="sxs-lookup"><span data-stu-id="40930-103">JET_sesparam enumeration</span></span>

<span data-ttu-id="40930-104">Parámetros de sesión ESENT.</span><span class="sxs-lookup"><span data-stu-id="40930-104">ESENT session parameters.</span></span>

<span data-ttu-id="40930-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="40930-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="40930-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="40930-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="40930-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40930-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_sesparam
'Usage
Dim instance As JET_sesparam
```

``` csharp
public enum JET_sesparam
```

## <a name="members"></a><span data-ttu-id="40930-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="40930-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="40930-109">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="40930-109">Member name</span></span></th>
<th><span data-ttu-id="40930-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="40930-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="40930-111">Base</span><span class="sxs-lookup"><span data-stu-id="40930-111">Base</span></span></td>
<td><span data-ttu-id="40930-112">Este parámetro no está diseñado para usarse.</span><span class="sxs-lookup"><span data-stu-id="40930-112">This parameter is not meant to be used.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="40930-113">CommitDefault</span><span class="sxs-lookup"><span data-stu-id="40930-113">CommitDefault</span></span></td>
<td><span data-ttu-id="40930-114">Este parámetro establece grbits para commit.</span><span class="sxs-lookup"><span data-stu-id="40930-114">This parameter sets the grbits for commit.</span></span> <span data-ttu-id="40930-115">Es funcionalmente igual que el parámetro del sistema JET_param. CommitDefault cuando se usa con una instancia de y un sesid.</span><span class="sxs-lookup"><span data-stu-id="40930-115">It is functionally the same as the system parameter JET_param.CommitDefault when used with an instance and a sesid.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="40930-116">CommitGenericContext</span><span class="sxs-lookup"><span data-stu-id="40930-116">CommitGenericContext</span></span></td>
<td><span data-ttu-id="40930-117">Este parámetro establece un contexto de confirmación específico del usuario que se colocará en el registro de transacciones en la confirmación en el nivel 0.</span><span class="sxs-lookup"><span data-stu-id="40930-117">This parameter sets a user specific commit context that will be placed in the transaction log on commit to level 0.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="40930-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="40930-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="40930-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="40930-119">Reference</span></span>

[<span data-ttu-id="40930-120">Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="40930-120">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
