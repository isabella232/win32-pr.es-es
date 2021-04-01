---
description: 'Más información sobre: Windows8Api. JetStopServiceInstance2 (método)'
title: Método Windows8Api. JetStopServiceInstance2 (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetStopServiceInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetStopServiceInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetstopserviceinstance2(v=EXCHG.10)
ms:contentKeyID: 55104460
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetStopServiceInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetStopServiceInstance2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0821a00016eb9cd2c511ee37889e0ddaa0b76edb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082271"
---
# <a name="windows8apijetstopserviceinstance2-method"></a><span data-ttu-id="82d51-103">Windows8Api. JetStopServiceInstance2, método</span><span class="sxs-lookup"><span data-stu-id="82d51-103">Windows8Api.JetStopServiceInstance2 method</span></span>

<span data-ttu-id="82d51-104">Prepara una instancia para la terminación.</span><span class="sxs-lookup"><span data-stu-id="82d51-104">Prepares an instance for termination.</span></span> <span data-ttu-id="82d51-105">También se puede usar para reanudar una inactividad anterior.</span><span class="sxs-lookup"><span data-stu-id="82d51-105">Can also be used to resume a previous quiescing.</span></span>

<span data-ttu-id="82d51-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="82d51-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="82d51-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="82d51-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="82d51-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82d51-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetStopServiceInstance2 ( _
    instance As JET_INSTANCE, _
    grbit As StopServiceGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As StopServiceGrbitWindows8Api.JetStopServiceInstance2(instance, _
    grbit)
```

``` csharp
public static void JetStopServiceInstance2(
    JET_INSTANCE instance,
    StopServiceGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="82d51-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82d51-109">Parameters</span></span>

  - <span data-ttu-id="82d51-110">instance</span><span class="sxs-lookup"><span data-stu-id="82d51-110">instance</span></span>  
    <span data-ttu-id="82d51-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="82d51-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="82d51-112">Instancia de (en ejecución) que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="82d51-112">The (running) instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="82d51-113">grbit</span><span class="sxs-lookup"><span data-stu-id="82d51-113">grbit</span></span>  
    <span data-ttu-id="82d51-114">Tipo: [Microsoft. ISAM. esent. Interop. Windows8. StopServiceGrbit](./stopservicegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="82d51-114">Type: [Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit](./stopservicegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="82d51-115">Opciones para detener o reanudar la instancia.</span><span class="sxs-lookup"><span data-stu-id="82d51-115">The options to stop or resume the instance.</span></span>

## <a name="see-also"></a><span data-ttu-id="82d51-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="82d51-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="82d51-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="82d51-117">Reference</span></span>

[<span data-ttu-id="82d51-118">Clase Windows8Api</span><span class="sxs-lookup"><span data-stu-id="82d51-118">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="82d51-119">Miembros de Windows8Api</span><span class="sxs-lookup"><span data-stu-id="82d51-119">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="82d51-120">Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="82d51-120">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
