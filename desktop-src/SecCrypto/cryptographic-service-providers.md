---
description: 'Importante: esta API está en desuso.'
ms.assetid: 4e6eb2df-a917-4533-b9f1-8da39598d0b8
title: Proveedores de servicios criptográficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5431d8ddda1be977e2a33297613633343fc2f9c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423776"
---
# <a name="cryptographic-service-providers"></a><span data-ttu-id="33c0f-103">Proveedores de servicios criptográficos</span><span class="sxs-lookup"><span data-stu-id="33c0f-103">Cryptographic Service Providers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="33c0f-104">Esta API está en desuso.</span><span class="sxs-lookup"><span data-stu-id="33c0f-104">This API is deprecated.</span></span> <span data-ttu-id="33c0f-105">El software nuevo y existente debe empezar a usar las [API de Cryptography Next Generation.](/windows/desktop/SecCNG/cng-portal)</span><span class="sxs-lookup"><span data-stu-id="33c0f-105">New and existing software should start using [Cryptography Next Generation APIs.](/windows/desktop/SecCNG/cng-portal)</span></span> <span data-ttu-id="33c0f-106">Microsoft puede quitar esta API en futuras versiones.</span><span class="sxs-lookup"><span data-stu-id="33c0f-106">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="33c0f-107">Un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) contiene implementaciones de algoritmos y estándares criptográficos.</span><span class="sxs-lookup"><span data-stu-id="33c0f-107">A [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) contains implementations of cryptographic standards and algorithms.</span></span> <span data-ttu-id="33c0f-108">Como mínimo, un CSP consta de una [*biblioteca de vínculos dinámicos*](../secgloss/d-gly.md) (dll) que implementa las funciones de [*CryptoSPI*](../secgloss/c-gly.md) (una [*interfaz de programa del sistema*](../secgloss/s-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="33c0f-108">At a minimum, a CSP consists of a [*dynamic-link library*](../secgloss/d-gly.md) (DLL) that implements the functions in [*CryptoSPI*](../secgloss/c-gly.md) (a [*system program interface*](../secgloss/s-gly.md)).</span></span> <span data-ttu-id="33c0f-109">La mayoría de los CSP contienen la implementación de todas sus propias funciones.</span><span class="sxs-lookup"><span data-stu-id="33c0f-109">Most CSPs contain the implementation of all of their own functions.</span></span> <span data-ttu-id="33c0f-110">Sin embargo, algunos CSP implementan sus funciones principalmente en un programa de servicio basado en Windows administrado por el administrador de control de servicios de Windows.</span><span class="sxs-lookup"><span data-stu-id="33c0f-110">Some CSPs, however, implement their functions mainly in a Windows-based service program managed by the Windows service control manager.</span></span> <span data-ttu-id="33c0f-111">Otros implementan funciones en hardware, como una [*tarjeta inteligente*](../secgloss/s-gly.md) o un coprocesador seguro.</span><span class="sxs-lookup"><span data-stu-id="33c0f-111">Others implement functions in hardware, such as a [*smart card*](../secgloss/s-gly.md) or secure coprocessor.</span></span> <span data-ttu-id="33c0f-112">Si un CSP no implementa sus propias funciones, el archivo DLL actúa como capa de paso a través, lo que facilita la comunicación entre el sistema operativo y la implementación de CSP real.</span><span class="sxs-lookup"><span data-stu-id="33c0f-112">If a CSP does not implement its own functions, the DLL acts as a pass-through layer, facilitating the communication between the operating system and the actual CSP implementation.</span></span>

<span data-ttu-id="33c0f-113">Esta sección incluye los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="33c0f-113">This section includes the following topics.</span></span>



| <span data-ttu-id="33c0f-114">Tema</span><span class="sxs-lookup"><span data-stu-id="33c0f-114">Topic</span></span>                                                                                      | <span data-ttu-id="33c0f-115">Contenido</span><span class="sxs-lookup"><span data-stu-id="33c0f-115">Contents</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33c0f-116">Tipos de proveedor de servicios criptográficos</span><span class="sxs-lookup"><span data-stu-id="33c0f-116">Cryptographic Provider Types</span></span>](cryptographic-provider-types.md)                           | <span data-ttu-id="33c0f-117">Los tipos de proveedor de servicios criptográficos son familias de proveedores de servicios de cifrado que comparten formatos de datos y protocolos criptográficos.</span><span class="sxs-lookup"><span data-stu-id="33c0f-117">Cryptographic provider types are families of cryptographic services providers that share data formats and cryptographic protocols.</span></span> <span data-ttu-id="33c0f-118">Los formatos de datos incluyen esquemas de [*relleno*](../secgloss/p-gly.md) de algoritmos, [*longitudes de clave*](../secgloss/k-gly.md)y modos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="33c0f-118">Data formats include algorithms [*padding*](../secgloss/p-gly.md) schemes, [*key lengths*](../secgloss/k-gly.md), and default modes.</span></span> |
| [<span data-ttu-id="33c0f-119">Proveedores de servicios criptográficos de Microsoft</span><span class="sxs-lookup"><span data-stu-id="33c0f-119">Microsoft Cryptographic Service Providers</span></span>](microsoft-cryptographic-service-providers.md) | <span data-ttu-id="33c0f-120">Información detallada sobre los CSP disponibles actualmente en Microsoft.</span><span class="sxs-lookup"><span data-stu-id="33c0f-120">Detailed information about CSPs currently available from Microsoft.</span></span>                                                                                                                                                                                                                                                                                       |



 

 

 
