---
description: 'Más información acerca de: constructor DurableCommitCallback'
title: Constructor DurableCommitCallback (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'DurableCommitCallback constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.#ctor(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.durablecommitcallback.durablecommitcallback(v=EXCHG.10)
ms:contentKeyID: 55104290
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.DurableCommitCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ade1952615b98d9ea41a7a1b83d0bf1a3c6fc8d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817574"
---
# <a name="durablecommitcallback-constructor"></a><span data-ttu-id="41208-103">Constructor de DurableCommitCallback</span><span class="sxs-lookup"><span data-stu-id="41208-103">DurableCommitCallback constructor</span></span>

<span data-ttu-id="41208-104">Inicializa una nueva instancia de la clase [DurableCommitCallback](./durablecommitcallback-class.md) .</span><span class="sxs-lookup"><span data-stu-id="41208-104">Initializes a new instance of the [DurableCommitCallback](./durablecommitcallback-class.md) class.</span></span>

<span data-ttu-id="41208-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="41208-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="41208-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="41208-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="41208-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41208-107">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    instance As JET_INSTANCE, _
    wrappedCallback As JET_PFNDURABLECOMMITCALLBACK _
)
'Usage
Dim instance As JET_INSTANCE
Dim wrappedCallback As JET_PFNDURABLECOMMITCALLBACK

Dim instance As New DurableCommitCallback(instance, _
    wrappedCallback)
```

``` csharp
public DurableCommitCallback(
    JET_INSTANCE instance,
    JET_PFNDURABLECOMMITCALLBACK wrappedCallback
)
```

#### <a name="parameters"></a><span data-ttu-id="41208-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="41208-108">Parameters</span></span>

  - <span data-ttu-id="41208-109">instance</span><span class="sxs-lookup"><span data-stu-id="41208-109">instance</span></span>  
    <span data-ttu-id="41208-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="41208-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="41208-111">Instancia de con la que se va a asociar la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="41208-111">The instance with which to associate the callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="41208-112">wrappedCallback</span><span class="sxs-lookup"><span data-stu-id="41208-112">wrappedCallback</span></span>  
    <span data-ttu-id="41208-113">Tipo: [Microsoft.ISAM.esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK](./jet-pfndurablecommitcallback-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="41208-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK](./jet-pfndurablecommitcallback-delegate.md)</span></span>  
    
    <span data-ttu-id="41208-114">Devolución de llamada de código administrado que se va a llamar.</span><span class="sxs-lookup"><span data-stu-id="41208-114">The managed code callback to call.</span></span>

## <a name="see-also"></a><span data-ttu-id="41208-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="41208-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="41208-116">Referencia</span><span class="sxs-lookup"><span data-stu-id="41208-116">Reference</span></span>

[<span data-ttu-id="41208-117">Clase DurableCommitCallback</span><span class="sxs-lookup"><span data-stu-id="41208-117">DurableCommitCallback class</span></span>](./durablecommitcallback-class.md)

[<span data-ttu-id="41208-118">Miembros de DurableCommitCallback</span><span class="sxs-lookup"><span data-stu-id="41208-118">DurableCommitCallback members</span></span>](./durablecommitcallback-members.md)

[<span data-ttu-id="41208-119">Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="41208-119">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
