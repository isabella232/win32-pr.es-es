---
description: 'Más información sobre: API. JetResetSessionContext (método)'
title: Método API. JetResetSessionContext
TOCTitle: 'JetResetSessionContext method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetResetSessionContext(Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetresetsessioncontext(v=EXCHG.10)
ms:contentKeyID: 55100785
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetResetSessionContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetResetSessionContext
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a34a6c2922c0041f0720b498855b15c4aed23f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697719"
---
# <a name="apijetresetsessioncontext-method"></a><span data-ttu-id="e5d5b-103">Método API. JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="e5d5b-103">Api.JetResetSessionContext method</span></span>

<span data-ttu-id="e5d5b-104">Desasocia una sesión del subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="e5d5b-104">Disassociates a session from the current thread.</span></span> <span data-ttu-id="e5d5b-105">Debe usarse junto con [JetSetSessionContext (JET_SESID, IntPtr)](./api.jetsetsessioncontext-method.md).</span><span class="sxs-lookup"><span data-stu-id="e5d5b-105">This should be used in conjunction with [JetSetSessionContext(JET_SESID, IntPtr)](./api.jetsetsessioncontext-method.md).</span></span>

<span data-ttu-id="e5d5b-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e5d5b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e5d5b-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e5d5b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e5d5b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e5d5b-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetResetSessionContext ( _
    sesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESIDApi.JetResetSessionContext(sesid)
```

``` csharp
public static void JetResetSessionContext(
    JET_SESID sesid
)
```

#### <a name="parameters"></a><span data-ttu-id="e5d5b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e5d5b-109">Parameters</span></span>

  - <span data-ttu-id="e5d5b-110">sesid</span><span class="sxs-lookup"><span data-stu-id="e5d5b-110">sesid</span></span>  
    <span data-ttu-id="e5d5b-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e5d5b-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e5d5b-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="e5d5b-112">The session to use.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5d5b-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5d5b-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e5d5b-114">Referencia</span><span class="sxs-lookup"><span data-stu-id="e5d5b-114">Reference</span></span>

[<span data-ttu-id="e5d5b-115">Clase de API</span><span class="sxs-lookup"><span data-stu-id="e5d5b-115">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e5d5b-116">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="e5d5b-116">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e5d5b-117">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e5d5b-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
