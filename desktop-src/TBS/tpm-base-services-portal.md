---
title: Servicios base de TPM
description: El software TPM proporciona servicios como una API expuesta a través de la llamada a procedimiento remoto. Use TPM para crear un módulo de TPM.
ms.assetid: ae6e7fe9-585d-467a-8456-e008b8ea89a0
keywords:
- Servicios base de TPM TBS
- Servicios base de TPM TBS, Página principal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d2cbdfc1f85d6917f2e9a7a5b8e7a0fc25ebdc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421079"
---
# <a name="tpm-base-services"></a><span data-ttu-id="7477e-106">Servicios base de TPM</span><span class="sxs-lookup"><span data-stu-id="7477e-106">TPM Base Services</span></span>

## <a name="purpose"></a><span data-ttu-id="7477e-107">Propósito</span><span class="sxs-lookup"><span data-stu-id="7477e-107">Purpose</span></span>

<span data-ttu-id="7477e-108">La característica de servicios base de Módulo de plataforma segura (TBS) centraliza el acceso de TPM entre las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="7477e-108">The Trusted Platform Module (TPM) Base Services (TBS) feature centralizes TPM access across applications.</span></span>

<span data-ttu-id="7477e-109">La característica TBS se ejecuta como un servicio de sistema en Windows Server 2008, Windows Vista o sistemas operativos más recientes.</span><span class="sxs-lookup"><span data-stu-id="7477e-109">The TBS feature runs as a system service in Windows Server 2008, Windows Vista, or newer operating systems.</span></span> <span data-ttu-id="7477e-110">Proporciona servicios como una API expuesta a través de llamadas a procedimiento remoto (RPC).</span><span class="sxs-lookup"><span data-stu-id="7477e-110">It provides services as an API exposed through remote procedure calls (RPC).</span></span> <span data-ttu-id="7477e-111">La característica TBS usa las prioridades especificadas al llamar a las aplicaciones para programar el acceso de TPM de forma cooperativa.</span><span class="sxs-lookup"><span data-stu-id="7477e-111">The TBS feature uses priorities specified by calling applications to cooperatively schedule TPM access.</span></span>

> [!Note]
>
> <span data-ttu-id="7477e-112">El TPM se puede usar para las operaciones de almacenamiento de claves.</span><span class="sxs-lookup"><span data-stu-id="7477e-112">The TPM can be used for key storage operations.</span></span> <span data-ttu-id="7477e-113">Sin embargo, se recomienda que los desarrolladores usen las [API de almacenamiento de claves](/windows/desktop/SecCNG/key-storage-and-retrieval) para estos escenarios en su lugar.</span><span class="sxs-lookup"><span data-stu-id="7477e-113">However, developers are encouraged to use the [Key Storage APIs](/windows/desktop/SecCNG/key-storage-and-retrieval) for these scenarios instead.</span></span> <span data-ttu-id="7477e-114">Las API de almacenamiento de claves proporcionan la funcionalidad para crear, firmar o cifrar con y conservar claves criptográficas, y son de mayor nivel y más fáciles de usar que los TBS para estos escenarios de destino.</span><span class="sxs-lookup"><span data-stu-id="7477e-114">The Key Storage APIs provide the functionality to create, sign or encrypt with, and persist cryptographic keys, and they are higher-level and easier to use than the TBS for these targeted scenarios.</span></span>

 

## <a name="developer-audience"></a><span data-ttu-id="7477e-115">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="7477e-115">Developer audience</span></span>

<span data-ttu-id="7477e-116">TBS está pensado para que lo usen los desarrolladores de aplicaciones basadas en los sistemas operativos Windows.</span><span class="sxs-lookup"><span data-stu-id="7477e-116">TBS is intended for use by developers of applications based on the Windows operating systems.</span></span> <span data-ttu-id="7477e-117">Los desarrolladores deben estar familiarizados con los lenguajes de programación C y C++ y el entorno de programación de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7477e-117">Developers should be familiar with the C and C++ programming languages and the Microsoft Windows programming environment.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="7477e-118">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="7477e-118">Run-time requirements</span></span>

<span data-ttu-id="7477e-119">La característica TBS requiere como mínimo el sistema operativo Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7477e-119">The TBS feature requires at least Windows Server 2008 or Windows Vista operating system.</span></span> <span data-ttu-id="7477e-120">Para obtener información sobre los requisitos de tiempo de ejecución para un elemento de programación determinado, vea la sección de requisitos de la página de referencia de ese elemento.</span><span class="sxs-lookup"><span data-stu-id="7477e-120">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7477e-121">En esta sección</span><span class="sxs-lookup"><span data-stu-id="7477e-121">In this section</span></span>



| <span data-ttu-id="7477e-122">Tema</span><span class="sxs-lookup"><span data-stu-id="7477e-122">Topic</span></span>                                         | <span data-ttu-id="7477e-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="7477e-123">Description</span></span>                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="7477e-124">Acerca de TBS</span><span class="sxs-lookup"><span data-stu-id="7477e-124">About TBS</span></span>](about-tbs.md)<br/>         | <span data-ttu-id="7477e-125">Conceptos clave y una vista de alto nivel de la característica de TBS.</span><span class="sxs-lookup"><span data-stu-id="7477e-125">Key concepts and a high-level view of the TBS feature.</span></span><br/>               |
| [<span data-ttu-id="7477e-126">Uso de TBS</span><span class="sxs-lookup"><span data-stu-id="7477e-126">Using TBS</span></span>](using-tbs.md)<br/>         | <span data-ttu-id="7477e-127">Procesos y procedimientos de TBS para usar la API de TBS.</span><span class="sxs-lookup"><span data-stu-id="7477e-127">TBS processes and procedures for using the TBS API.</span></span><br/>                  |
| [<span data-ttu-id="7477e-128">Referencia de TBS</span><span class="sxs-lookup"><span data-stu-id="7477e-128">TBS Reference</span></span>](tbs-reference.md)<br/> | <span data-ttu-id="7477e-129">Documentación acerca de las funciones, estructuras y códigos de retorno de TBS.</span><span class="sxs-lookup"><span data-stu-id="7477e-129">Documentation about the TBS functions, structures, and return codes.</span></span><br/> |



 

 

