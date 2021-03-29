---
title: Marco biométrico de Windows
description: Puede usar la API de Plataforma de biometría de Windows para crear aplicaciones cliente que capturen, guarden y comparen de forma segura la información biométrica del usuario final.
ms.assetid: d9ac9ec1-bb34-402d-a590-73d5070b97ba
keywords:
- API Plataforma de biometría de Windows API de Plataforma de biometría de Windows
- API de API Plataforma de biometría de Windows de Plataforma de biometría de Windows, Página principal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4341f09f3141e1be77bcdf0987ee1273ffddcf6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778978"
---
# <a name="windows-biometric-framework"></a><span data-ttu-id="4c574-105">Marco biométrico de Windows</span><span class="sxs-lookup"><span data-stu-id="4c574-105">Windows Biometric Framework</span></span>

## <a name="purpose"></a><span data-ttu-id="4c574-106">Propósito</span><span class="sxs-lookup"><span data-stu-id="4c574-106">Purpose</span></span>

<span data-ttu-id="4c574-107">Puede usar la API de Plataforma de biometría de Windows para crear aplicaciones cliente que capturen, guarden y comparen de forma segura la información biométrica del usuario final.</span><span class="sxs-lookup"><span data-stu-id="4c574-107">You can use the Windows Biometric Framework API to create client applications that securely capture, save, and compare end-user biometric information.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="4c574-108">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="4c574-108">Developer audience</span></span>

<span data-ttu-id="4c574-109">Los desarrolladores que usen esta API deben estar familiarizados con los lenguajes de programación C y C++ y con el entorno de programación basado en Windows.</span><span class="sxs-lookup"><span data-stu-id="4c574-109">Developers who use this API should be familiar with the C and C++ programming languages and the Windows-based programming environment.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="4c574-110">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="4c574-110">Run-time requirements</span></span>

<span data-ttu-id="4c574-111">La API de Plataforma de biometría de Windows se admite a partir de Windows Server 2008 R2 y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4c574-111">The Windows Biometric Framework API is supported beginning with Windows Server 2008 R2 and Windows 7.</span></span> <span data-ttu-id="4c574-112">Para obtener información sobre los requisitos de tiempo de ejecución para un elemento de programación determinado, vea la sección de requisitos de la página de referencia de ese elemento.</span><span class="sxs-lookup"><span data-stu-id="4c574-112">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4c574-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="4c574-113">In this section</span></span>



| <span data-ttu-id="4c574-114">Tema</span><span class="sxs-lookup"><span data-stu-id="4c574-114">Topic</span></span>                                                                                       | <span data-ttu-id="4c574-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c574-115">Description</span></span>                                                                                                                                              |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c574-116">Información general sobre el marco biométrico</span><span class="sxs-lookup"><span data-stu-id="4c574-116">Biometric Framework overview</span></span>](biometric-framework-overview.md)<br/>                 | <span data-ttu-id="4c574-117">Describe la compatibilidad nativa con biometría en Windows.</span><span class="sxs-lookup"><span data-stu-id="4c574-117">Describes the native support for biometrics in Windows.</span></span><br/>                                                                                       |
| [<span data-ttu-id="4c574-118">Creación de aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="4c574-118">Creating client applications</span></span>](creating-client-applications.md)<br/>                 | <span data-ttu-id="4c574-119">Puede usar la API de cliente para capturar y usar la información biométrica en sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="4c574-119">You can use the client API to capture and use biometric information in your applications.</span></span><br/>                                                     |
| [<span data-ttu-id="4c574-120">Crear complementos de adaptador</span><span class="sxs-lookup"><span data-stu-id="4c574-120">Creating Adapter Plug-ins</span></span>](creating-adapter-plug-ins.md)<br/>                       | <span data-ttu-id="4c574-121">Puede crear adaptadores de motor, adaptadores de sensor y adaptadores de almacenamiento mediante los temas de esta sección.</span><span class="sxs-lookup"><span data-stu-id="4c574-121">You can create engine adapters, sensor adapters, and storage adapters using the topics in this section.</span></span><br/>                                       |
| [<span data-ttu-id="4c574-122">Creación de un grupo de sensores privados</span><span class="sxs-lookup"><span data-stu-id="4c574-122">Creating a Private Sensor Pool</span></span>](creating-a-private-sensor-pool.md)<br/>             | <span data-ttu-id="4c574-123">Hay dos tipos de grupos de sensores: privado y sistema.</span><span class="sxs-lookup"><span data-stu-id="4c574-123">There are two types of sensor pools: private and system.</span></span> <span data-ttu-id="4c574-124">En esta sección se describe cada una de ellas y se explica cómo crear un grupo de sensores privados.</span><span class="sxs-lookup"><span data-stu-id="4c574-124">This section describes each and explains how to create a private sensor pool.</span></span> <br/>       |
| [<span data-ttu-id="4c574-125">Referencia de API de Plataforma de biometría de Windows</span><span class="sxs-lookup"><span data-stu-id="4c574-125">Windows Biometric Framework API Reference</span></span>](biometric-service-api-reference.md)<br/> | <span data-ttu-id="4c574-126">Descripciones detalladas de las funciones, estructuras y otros elementos de programación que se pueden usar para crear aplicaciones cliente y complementos.</span><span class="sxs-lookup"><span data-stu-id="4c574-126">Detailed descriptions of functions, structures, and other programming elements that can be used to create a client applications and plug-ins.</span></span><br/> |



 

 

 





