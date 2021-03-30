---
title: SRPRunningObjectChecks
description: Determina si los intentos de conexión a objetos en ejecución se filtran para los niveles de confianza de la Directiva de restricción de software (SRP) compatible.
ms.assetid: ab5e74f0-d167-4fb2-af1b-03704039e87c
keywords:
- Valor del registro SRPRunningObjectChecks COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ad307856bcfdd30cfaa6c731551ac6570d2bec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774965"
---
# <a name="srprunningobjectchecks"></a><span data-ttu-id="2f610-104">SRPRunningObjectChecks</span><span class="sxs-lookup"><span data-stu-id="2f610-104">SRPRunningObjectChecks</span></span>

<span data-ttu-id="2f610-105">Determina si los intentos de conexión a objetos en ejecución se filtran para los niveles de confianza de la Directiva de restricción de software (SRP) compatible.</span><span class="sxs-lookup"><span data-stu-id="2f610-105">Determines whether attempts to connect to running objects are screened for compatible software restriction policy (SRP) trust levels.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="2f610-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="2f610-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPRunningObjectChecks = value
```

## <a name="remarks"></a><span data-ttu-id="2f610-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f610-107">Remarks</span></span>

<span data-ttu-id="2f610-108">Este es un valor de **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="2f610-108">This is a **REG\_SZ** value.</span></span>

<span data-ttu-id="2f610-109">Los valores de cadena de {N, n, NO, no, no} indican que los intentos de conexión a objetos en ejecución no se filtran por niveles de confianza de SRP compatibles.</span><span class="sxs-lookup"><span data-stu-id="2f610-109">String values of {N, n, NO, No, no} indicate that attempts to connect to running objects are not screened for compatible SRP trust levels.</span></span> <span data-ttu-id="2f610-110">Si este valor del registro se establece en cualquier otro valor o no existe, el objeto en ejecución no puede tener un nivel de confianza SRP menos estricto que el objeto cliente.</span><span class="sxs-lookup"><span data-stu-id="2f610-110">If this registry value is set to any other value or does not exist, the running object cannot have a less stringent SRP trust level than the client object.</span></span> <span data-ttu-id="2f610-111">Por ejemplo, el objeto en ejecución no puede tener un nivel de confianza no permitido si el objeto de cliente tiene un nivel de confianza no restringido.</span><span class="sxs-lookup"><span data-stu-id="2f610-111">For example, the running object cannot have a Disallowed trust level if the client object has an Unrestricted trust level.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f610-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2f610-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f610-113">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="2f610-113">SRPTrustLevel</span></span>](srptrustlevel.md)
</dt> </dl>

 

 




