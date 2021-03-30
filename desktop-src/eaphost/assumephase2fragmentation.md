---
title: AssumePhase2Fragmentation
description: La clave del registro AssumePhase2Fragmentation determina si el servidor y el cliente suponen una fragmentación de la fase 2.
ms.assetid: 3d6ececf-8871-4038-9706-4da57857d25a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0fa35692ec3ac741e2bd2fdb43607dfe1cb948
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104420029"
---
# <a name="assumephase2fragmentation"></a><span data-ttu-id="a5bfd-103">AssumePhase2Fragmentation</span><span class="sxs-lookup"><span data-stu-id="a5bfd-103">AssumePhase2Fragmentation</span></span>

<span data-ttu-id="a5bfd-104">La clave del registro AssumePhase2Fragmentation determina si el servidor y el cliente suponen una fragmentación de la fase 2.</span><span class="sxs-lookup"><span data-stu-id="a5bfd-104">The AssumePhase2Fragmentation registry key determines if the server and client assume phase 2 fragmentation.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="a5bfd-105">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="a5bfd-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   AssumePhase2Fragmentation = value
```

## <a name="remarks"></a><span data-ttu-id="a5bfd-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5bfd-106">Remarks</span></span>

<span data-ttu-id="a5bfd-107">Se trata de un valor de **Registro \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="a5bfd-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="a5bfd-108">Value</span><span class="sxs-lookup"><span data-stu-id="a5bfd-108">Value</span></span>   | <span data-ttu-id="a5bfd-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5bfd-109">Description</span></span>                                                                                                  |
|---------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5bfd-110">0</span><span class="sxs-lookup"><span data-stu-id="a5bfd-110">0</span></span>       | <span data-ttu-id="a5bfd-111">El servidor y el cliente suponen que la otra parte no es capaz de fragmentar la fase 2 durante la autenticación PEAP.</span><span class="sxs-lookup"><span data-stu-id="a5bfd-111">Server and client assume the other party is not capable of phase 2 fragmentation during PEAP authentication.</span></span> |
| <span data-ttu-id="a5bfd-112">distinto</span><span class="sxs-lookup"><span data-stu-id="a5bfd-112">nonzero</span></span> | <span data-ttu-id="a5bfd-113">El servidor y el cliente suponen que la otra parte es capaz de fragmentar la fase 2 durante la autenticación PEAP.</span><span class="sxs-lookup"><span data-stu-id="a5bfd-113">Server and client assume the other party is capable of phase 2 fragmentation during PEAP authentication.</span></span>     |



 

<span data-ttu-id="a5bfd-114">Si este valor del registro no está presente, el servidor y el cliente suponen que la otra entidad es capaz de fragmentar la fase 2 durante la autenticación PEAP.</span><span class="sxs-lookup"><span data-stu-id="a5bfd-114">If this registry value is not present, the server and client assume the other party is capable of phase 2 fragmentation during PEAP authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5bfd-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a5bfd-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5bfd-116">Configuración del registro de EAPHost</span><span class="sxs-lookup"><span data-stu-id="a5bfd-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




