---
title: Llamada a procedimiento remoto
description: La llamada a procedimiento remoto (RPC) de Microsoft define una tecnología eficaz para crear programas cliente/servidor distribuidos.
ms.assetid: 27c7c352-5fc1-47cf-99b1-fdf3eca986bc
keywords:
- RPC
- RPC, (consulte llamada a procedimiento remoto)
- RPC llamada a procedimiento remoto, página de inicio
- RPC de llamada a procedimiento remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3461116468bf1d686d1a5695924e5fe66007b35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421229"
---
# <a name="remote-procedure-call"></a><span data-ttu-id="bb86c-107">Llamada a procedimiento remoto</span><span class="sxs-lookup"><span data-stu-id="bb86c-107">Remote Procedure Call</span></span>

## <a name="purpose"></a><span data-ttu-id="bb86c-108">Propósito</span><span class="sxs-lookup"><span data-stu-id="bb86c-108">Purpose</span></span>

<span data-ttu-id="bb86c-109">La llamada a procedimiento remoto (RPC) de Microsoft define una tecnología eficaz para crear programas cliente/servidor distribuidos.</span><span class="sxs-lookup"><span data-stu-id="bb86c-109">Microsoft Remote Procedure Call (RPC) defines a powerful technology for creating distributed client/server programs.</span></span> <span data-ttu-id="bb86c-110">Las bibliotecas y los códigos auxiliares en tiempo de ejecución de RPC administran la mayoría de los procesos relacionados con los protocolos de red y la comunicación.</span><span class="sxs-lookup"><span data-stu-id="bb86c-110">The RPC run-time stubs and libraries manage most of the processes relating to network protocols and communication.</span></span> <span data-ttu-id="bb86c-111">Esto le permite centrarse en los detalles de la aplicación en lugar de los detalles de la red.</span><span class="sxs-lookup"><span data-stu-id="bb86c-111">This enables you to focus on the details of the application rather than the details of the network.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="bb86c-112">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="bb86c-112">Where applicable</span></span>

<span data-ttu-id="bb86c-113">RPC puede usarse en todas las aplicaciones cliente/servidor basadas en los sistemas operativos Windows.</span><span class="sxs-lookup"><span data-stu-id="bb86c-113">RPC can be used in all client/server applications based on Windows operating systems.</span></span> <span data-ttu-id="bb86c-114">También se puede usar para crear programas de cliente y servidor para entornos de red heterogéneos que incluyen sistemas operativos como UNIX y Apple.</span><span class="sxs-lookup"><span data-stu-id="bb86c-114">It can also be used to create client and server programs for heterogeneous network environments that include such operating systems as Unix and Apple.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="bb86c-115">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="bb86c-115">Developer audience</span></span>

<span data-ttu-id="bb86c-116">RPC está diseñado para que lo usen los programadores de C/C++.</span><span class="sxs-lookup"><span data-stu-id="bb86c-116">RPC is designed to be used by C/C++ programmers.</span></span> <span data-ttu-id="bb86c-117">Es necesario estar familiarizado con el Lenguaje de definición de interfaz de Microsoft (MIDL) y el compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="bb86c-117">Familiarity with the Microsoft Interface Definition Language (MIDL) and the MIDL compiler are required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="bb86c-118">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="bb86c-118">Run-time requirements</span></span>

<span data-ttu-id="bb86c-119">Las bibliotecas en tiempo de ejecución de RPC se incluyen con Windows.</span><span class="sxs-lookup"><span data-stu-id="bb86c-119">The RPC run-time libraries are included with Windows.</span></span> <span data-ttu-id="bb86c-120">Los componentes del entorno de desarrollo de RPC se instalan al instalar el kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bb86c-120">The components of the RPC development environment are installed when you install the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bb86c-121">Para obtener más información, vea [instalar el entorno de programación de RPC](installing-the-rpc-programming-environment.md).</span><span class="sxs-lookup"><span data-stu-id="bb86c-121">For details, see [Installing the RPC Programming Environment](installing-the-rpc-programming-environment.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bb86c-122">En esta sección</span><span class="sxs-lookup"><span data-stu-id="bb86c-122">In this section</span></span>



| <span data-ttu-id="bb86c-123">Tema</span><span class="sxs-lookup"><span data-stu-id="bb86c-123">Topic</span></span>                                                                           | <span data-ttu-id="bb86c-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb86c-124">Description</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb86c-125">Mejores prácticas de programación de RPC</span><span class="sxs-lookup"><span data-stu-id="bb86c-125">Best RPC Programming Practices</span></span>](best-rpc-programming-practices.md)<br/> | <span data-ttu-id="bb86c-126">Instrucciones sobre las prácticas de programación RPC que ayudan a crear las mejores aplicaciones RPC posibles.</span><span class="sxs-lookup"><span data-stu-id="bb86c-126">Guidance on RPC programming practices that help create the best possible RPC applications.</span></span><br/>                            |
| [<span data-ttu-id="bb86c-127">Información general</span><span class="sxs-lookup"><span data-stu-id="bb86c-127">Overview</span></span>](overviews.md)<br/>                                            | <span data-ttu-id="bb86c-128">Información general acerca de la incorporación de RPC a las aplicaciones cliente/servidor.</span><span class="sxs-lookup"><span data-stu-id="bb86c-128">General information about incorporating RPC into your client/server applications.</span></span><br/>                                     |
| [<span data-ttu-id="bb86c-129">Referencia</span><span class="sxs-lookup"><span data-stu-id="bb86c-129">Reference</span></span>](reference.md)<br/>                                           | <span data-ttu-id="bb86c-130">Documentación de tipos, funciones y constantes de RPC.</span><span class="sxs-lookup"><span data-stu-id="bb86c-130">Documentation of RPC types, functions, and constants.</span></span><br/>                                                                 |
| [<span data-ttu-id="bb86c-131">Motor NDR de RPC</span><span class="sxs-lookup"><span data-stu-id="bb86c-131">RPC NDR Engine</span></span>](rpc-ndr-engine.md)<br/>                                 | <span data-ttu-id="bb86c-132">Documentación del motor de cálculo de referencias para componentes de RPC y DCOM, el motor de representación de datos de red (NDR) de RPC.</span><span class="sxs-lookup"><span data-stu-id="bb86c-132">Documentation of the marshaling engine for RPC and DCOM components, the RPC Network Data Representation (NDR) Engine.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="bb86c-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bb86c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb86c-134">Lenguaje de definición de interfaz de Microsoft (MIDL)</span><span class="sxs-lookup"><span data-stu-id="bb86c-134">Microsoft Interface Definition Language (MIDL)</span></span>](/windows/desktop/Midl/midl-start-page)
</dt> </dl>

 

