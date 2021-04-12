---
title: BypassNegotiation
description: La clave del registro BypassNegotiation determina si se produce la negociación de funciones entre el servidor y el cliente, o si se usan los valores preconfigurados.
ms.assetid: 51e21e9c-d6cb-454b-9584-3f48d76a649a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9fdf883249fc5af7a37be83bb153a670295ba1d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104420047"
---
# <a name="bypassnegotiation"></a><span data-ttu-id="6a10f-103">BypassNegotiation</span><span class="sxs-lookup"><span data-stu-id="6a10f-103">BypassNegotiation</span></span>

<span data-ttu-id="6a10f-104">La clave del registro BypassNegotiation determina si se produce la negociación de funciones entre el servidor y el cliente, o si se usan los valores preconfigurados.</span><span class="sxs-lookup"><span data-stu-id="6a10f-104">The BypassNegotiation registry key determines if capabilities negotiation between the server and client occurs or if pre-configured settings are used.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="6a10f-105">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="6a10f-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   BypassNegotiation = value
```

## <a name="remarks"></a><span data-ttu-id="6a10f-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a10f-106">Remarks</span></span>

<span data-ttu-id="6a10f-107">Se trata de un valor de **Registro \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="6a10f-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="6a10f-108">Value</span><span class="sxs-lookup"><span data-stu-id="6a10f-108">Value</span></span>   | <span data-ttu-id="6a10f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a10f-109">Description</span></span>                                                                                                                                                                                          |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a10f-110">0</span><span class="sxs-lookup"><span data-stu-id="6a10f-110">0</span></span>       | <span data-ttu-id="6a10f-111">El servidor y el cliente negocian las capacidades de EAP.</span><span class="sxs-lookup"><span data-stu-id="6a10f-111">Server and client negotiate EAP capabilities.</span></span>                                                                                                                                                        |
| <span data-ttu-id="6a10f-112">distinto</span><span class="sxs-lookup"><span data-stu-id="6a10f-112">nonzero</span></span> | <span data-ttu-id="6a10f-113">El servidor y el cliente no negocian las funcionalidades de EAP.</span><span class="sxs-lookup"><span data-stu-id="6a10f-113">Server and client do not negotiate EAP capabilities.</span></span> <span data-ttu-id="6a10f-114">El servidor y el cliente usan el valor de la clave del registro [AssumePhase2Fragmentation](assumephase2fragmentation.md) para encontrar las capacidades de la otra parte.</span><span class="sxs-lookup"><span data-stu-id="6a10f-114">Server and client use the [AssumePhase2Fragmentation](assumephase2fragmentation.md) registry key value to find the other party's capabilities.</span></span> |



 

<span data-ttu-id="6a10f-115">Si este valor del registro no está presente, el servidor y el cliente negocian las capacidades de EAP.</span><span class="sxs-lookup"><span data-stu-id="6a10f-115">If this registry value is not present, the server and client negotiate EAP capabilities..</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a10f-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6a10f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a10f-117">Configuración del registro de EAPHost</span><span class="sxs-lookup"><span data-stu-id="6a10f-117">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




