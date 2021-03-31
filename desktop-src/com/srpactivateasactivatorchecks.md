---
title: SRPActivateAsActivatorChecks
description: Determina si los niveles de confianza de la Directiva de restricción de software (SRP) se usan durante las activaciones de ActivateAsActivator.
ms.assetid: b0d616c3-1cb0-4854-a4f9-6635d61b0698
keywords:
- Valor del registro SRPActivateAsActivatorChecks COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b66ae6b1c7f267f48f24441c04e95eea75e4345
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774970"
---
# <a name="srpactivateasactivatorchecks"></a><span data-ttu-id="94928-104">SRPActivateAsActivatorChecks</span><span class="sxs-lookup"><span data-stu-id="94928-104">SRPActivateAsActivatorChecks</span></span>

<span data-ttu-id="94928-105">Determina si los niveles de confianza de la Directiva de restricción de software (SRP) se usan durante las activaciones de ActivateAsActivator.</span><span class="sxs-lookup"><span data-stu-id="94928-105">Determines whether software restriction policy (SRP) trust levels are used during ActivateAsActivator activations.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="94928-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="94928-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPActivateAsActivatorChecks = value
```

## <a name="remarks"></a><span data-ttu-id="94928-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94928-107">Remarks</span></span>

<span data-ttu-id="94928-108">Este es un valor de **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="94928-108">This is a **REG\_SZ** value.</span></span>

<span data-ttu-id="94928-109">Los valores de cadena de {N, n, NO, no, no} indican que el objeto de servidor se ejecuta con el nivel de confianza de SRP del objeto de cliente, independientemente del nivel de confianza de SRP con el que se configuró.</span><span class="sxs-lookup"><span data-stu-id="94928-109">String values of {N, n, NO, No, no} indicate that the server object runs with the SRP trust level of the client object, regardless of the SRP trust level with which it was configured.</span></span> <span data-ttu-id="94928-110">Si este valor del registro se establece en cualquier otro valor o no existe, el nivel de confianza de SRP configurado para el objeto de servidor se compara con el nivel de confianza de SRP del objeto de cliente y se utiliza el nivel de confianza más riguroso para ejecutar el objeto de servidor.</span><span class="sxs-lookup"><span data-stu-id="94928-110">If this registry value is set to any other value or does not exist, the SRP trust level that is configured for the server object is compared with the SRP trust level of the client object and that the more stringent trust level is used to run the server object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94928-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="94928-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94928-112">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="94928-112">SRPTrustLevel</span></span>](srptrustlevel.md)
</dt> </dl>

 

 




