---
description: 'Más información sobre: DurableCommitCallback. ReleaseResource (método)'
title: Método DurableCommitCallback. ReleaseResource (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'ReleaseResource method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.durablecommitcallback.releaseresource(v=EXCHG.10)
ms:contentKeyID: 55104293
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 634dd081513e576c7aabaac17cc5f9d207a8769f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279263"
---
# <a name="durablecommitcallbackreleaseresource-method"></a><span data-ttu-id="0e736-103">DurableCommitCallback. ReleaseResource, método</span><span class="sxs-lookup"><span data-stu-id="0e736-103">DurableCommitCallback.ReleaseResource method</span></span>

<span data-ttu-id="0e736-104">Libera la sesión de confirmación duradera.</span><span class="sxs-lookup"><span data-stu-id="0e736-104">Frees the durable commit session.</span></span>

<span data-ttu-id="0e736-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0e736-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="0e736-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0e736-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0e736-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e736-107">Syntax</span></span>

``` vb
'Declaration
Protected Overrides Sub ReleaseResource
'Usage

Me.ReleaseResource()
```

``` csharp
protected override void ReleaseResource()
```

## <a name="remarks"></a><span data-ttu-id="0e736-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e736-108">Remarks</span></span>

<span data-ttu-id="0e736-109">No intente establecer el parámetro de instancia en null, ya que la devolución de llamada se desecha después de JetTerm y la devolución de llamada no se puede establecer después de JetTerm.</span><span class="sxs-lookup"><span data-stu-id="0e736-109">Do not try to set the instance parameter to null, because the callback is disposed after JetTerm and the callback cannot be set after JetTerm.</span></span>

## <a name="see-also"></a><span data-ttu-id="0e736-110">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e736-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0e736-111">Referencia</span><span class="sxs-lookup"><span data-stu-id="0e736-111">Reference</span></span>

[<span data-ttu-id="0e736-112">Clase DurableCommitCallback</span><span class="sxs-lookup"><span data-stu-id="0e736-112">DurableCommitCallback class</span></span>](./durablecommitcallback-class.md)

[<span data-ttu-id="0e736-113">Miembros de DurableCommitCallback</span><span class="sxs-lookup"><span data-stu-id="0e736-113">DurableCommitCallback members</span></span>](./durablecommitcallback-members.md)

[<span data-ttu-id="0e736-114">Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="0e736-114">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
