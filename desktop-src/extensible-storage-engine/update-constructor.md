---
description: 'Más información acerca de: constructor de actualizaciones'
title: Actualizar constructor
TOCTitle: 'Update constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_prep)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.update(v=EXCHG.10)
ms:contentKeyID: 55104189
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Update.Update
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Update..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 841403523e0cae7c71fb8fa0861c1d400a26a726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652969"
---
# <a name="update-constructor"></a><span data-ttu-id="da0cb-103">Actualizar constructor</span><span class="sxs-lookup"><span data-stu-id="da0cb-103">Update constructor</span></span>

<span data-ttu-id="da0cb-104">Inicializa una nueva instancia de la clase Update.</span><span class="sxs-lookup"><span data-stu-id="da0cb-104">Initializes a new instance of the Update class.</span></span> <span data-ttu-id="da0cb-105">Esto inicia automáticamente una actualización.</span><span class="sxs-lookup"><span data-stu-id="da0cb-105">This automatically begins an update.</span></span> <span data-ttu-id="da0cb-106">La actualización se cancelará si no se guarda explícitamente.</span><span class="sxs-lookup"><span data-stu-id="da0cb-106">The update will be cancelled if not explicitly saved.</span></span>

<span data-ttu-id="da0cb-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="da0cb-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="da0cb-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="da0cb-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="da0cb-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da0cb-109">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    prep As JET_prep _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim prep As JET_prep

Dim instance As New Update(sesid, tableid, _
    prep)
```

``` csharp
public Update(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_prep prep
)
```

#### <a name="parameters"></a><span data-ttu-id="da0cb-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da0cb-110">Parameters</span></span>

  - <span data-ttu-id="da0cb-111">sesid</span><span class="sxs-lookup"><span data-stu-id="da0cb-111">sesid</span></span>  
    <span data-ttu-id="da0cb-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="da0cb-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="da0cb-113">Sesión para la que se va a iniciar la transacción.</span><span class="sxs-lookup"><span data-stu-id="da0cb-113">The session to start the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="da0cb-114">TABLEID</span><span class="sxs-lookup"><span data-stu-id="da0cb-114">tableid</span></span>  
    <span data-ttu-id="da0cb-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="da0cb-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="da0cb-116">TABLEID para el que se va a preparar la actualización.</span><span class="sxs-lookup"><span data-stu-id="da0cb-116">The tableid to prepare the update for.</span></span>

<!-- end list -->

  - <span data-ttu-id="da0cb-117">porcentaje</span><span class="sxs-lookup"><span data-stu-id="da0cb-117">prep</span></span>  
    <span data-ttu-id="da0cb-118">Tipo: [Microsoft.ISAM.esent.Interop.JET_prep](./jet-prep-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="da0cb-118">Type: [Microsoft.Isam.Esent.Interop.JET_prep](./jet-prep-enumeration.md)</span></span>  
    
    <span data-ttu-id="da0cb-119">Tipo de actualización.</span><span class="sxs-lookup"><span data-stu-id="da0cb-119">The type of update.</span></span>

## <a name="see-also"></a><span data-ttu-id="da0cb-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="da0cb-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="da0cb-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="da0cb-121">Reference</span></span>

[<span data-ttu-id="da0cb-122">Update (clase)</span><span class="sxs-lookup"><span data-stu-id="da0cb-122">Update class</span></span>](./update-class.md)

[<span data-ttu-id="da0cb-123">Actualizar miembros</span><span class="sxs-lookup"><span data-stu-id="da0cb-123">Update members</span></span>](./update-members.md)

[<span data-ttu-id="da0cb-124">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="da0cb-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
