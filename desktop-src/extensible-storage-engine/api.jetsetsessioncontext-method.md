---
description: 'Más información sobre: API. JetSetSessionContext (método)'
title: Método API. JetSetSessionContext
TOCTitle: 'JetSetSessionContext method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext(Microsoft.Isam.Esent.Interop.JET_SESID,System.IntPtr)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsessioncontext(v=EXCHG.10)
ms:contentKeyID: 55100820
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d73a382a2b8e176e2d1ce6fa13585a6b5fa103e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697590"
---
# <a name="apijetsetsessioncontext-method"></a><span data-ttu-id="a3e68-103">Método API. JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="a3e68-103">Api.JetSetSessionContext method</span></span>

<span data-ttu-id="a3e68-104">Asocia una sesión al subproceso actual utilizando el identificador de contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="a3e68-104">Associates a session with the current thread using the given context handle.</span></span> <span data-ttu-id="a3e68-105">Esta asociación invalida el requisito de motor predeterminado que una transacción para una sesión determinada debe aparecer completamente en el mismo subproceso.</span><span class="sxs-lookup"><span data-stu-id="a3e68-105">This association overrides the default engine requirement that a transaction for a given session must occur entirely on the same thread.</span></span> <span data-ttu-id="a3e68-106">Use [JetResetSessionContext (JET_SESID)](./api.jetresetsessioncontext-method.md) para quitar la asociación.</span><span class="sxs-lookup"><span data-stu-id="a3e68-106">Use [JetResetSessionContext(JET_SESID)](./api.jetresetsessioncontext-method.md) to remove the association.</span></span>

<span data-ttu-id="a3e68-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a3e68-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a3e68-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a3e68-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a3e68-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3e68-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetSessionContext ( _
    sesid As JET_SESID, _
    context As IntPtr _
)
'Usage
Dim sesid As JET_SESID
Dim context As IntPtrApi.JetSetSessionContext(sesid, _
    context)
```

``` csharp
public static void JetSetSessionContext(
    JET_SESID sesid,
    IntPtr context
)
```

#### <a name="parameters"></a><span data-ttu-id="a3e68-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3e68-110">Parameters</span></span>

  - <span data-ttu-id="a3e68-111">sesid</span><span class="sxs-lookup"><span data-stu-id="a3e68-111">sesid</span></span>  
    <span data-ttu-id="a3e68-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a3e68-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a3e68-113">Sesión en la que se va a establecer el contexto.</span><span class="sxs-lookup"><span data-stu-id="a3e68-113">The session to set the context on.</span></span>

<!-- end list -->

  - <span data-ttu-id="a3e68-114">context</span><span class="sxs-lookup"><span data-stu-id="a3e68-114">context</span></span>  
    <span data-ttu-id="a3e68-115">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="a3e68-115">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="a3e68-116">Contexto que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="a3e68-116">The context to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3e68-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3e68-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a3e68-118">Referencia</span><span class="sxs-lookup"><span data-stu-id="a3e68-118">Reference</span></span>

[<span data-ttu-id="a3e68-119">Clase de API</span><span class="sxs-lookup"><span data-stu-id="a3e68-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a3e68-120">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="a3e68-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a3e68-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a3e68-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
