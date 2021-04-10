---
title: Acerca de TBS
description: Servicio del sistema que permite el uso compartido transparente de los recursos de Módulo de plataforma segura (TPM).
ms.assetid: 5ab3f514-dea9-48f7-97d9-abc774e2a273
keywords:
- Servicios base de TPM TBS, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a5d40b1fca688676978f274cb976afedb6e6a56
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104270745"
---
# <a name="about-tbs"></a><span data-ttu-id="e98c5-104">Acerca de TBS</span><span class="sxs-lookup"><span data-stu-id="e98c5-104">About TBS</span></span>

<span data-ttu-id="e98c5-105">La característica servicios base de TPM (TBS) es un servicio del sistema que permite el uso compartido transparente de los recursos de Módulo de plataforma segura (TPM).</span><span class="sxs-lookup"><span data-stu-id="e98c5-105">The TPM Base Services (TBS) feature is a system service that allows transparent sharing of the Trusted Platform Module (TPM) resources.</span></span> <span data-ttu-id="e98c5-106">Comparte simultáneamente los recursos de TPM entre varias aplicaciones en el mismo equipo físico, incluso si esas aplicaciones se ejecutan en máquinas virtuales diferentes.</span><span class="sxs-lookup"><span data-stu-id="e98c5-106">It simultaneously shares the TPM resources among multiple applications on the same physical machine, even if those applications run on different virtual machines.</span></span> <span data-ttu-id="e98c5-107">A partir de Windows 8 y Windows Server 2012, TBS viene preinstalado en todos los sistemas con un TPM.</span><span class="sxs-lookup"><span data-stu-id="e98c5-107">Starting with Windows 8 and Windows Server 2012, TBS comes pre-installed on all systems with a TPM.</span></span>

<span data-ttu-id="e98c5-108">El Trusted Computing Group (TCG) define un Módulo de plataforma segura que proporciona funciones criptográficas diseñadas para proporcionar confianza en la plataforma.</span><span class="sxs-lookup"><span data-stu-id="e98c5-108">The Trusted Computing Group (TCG) defines a Trusted Platform Module that provides cryptographic functions designed to provide trust in the platform.</span></span> <span data-ttu-id="e98c5-109">Dado que el TPM está implementado en hardware, tiene recursos finitos.</span><span class="sxs-lookup"><span data-stu-id="e98c5-109">Because the TPM is implemented in hardware, it has finite resources.</span></span> <span data-ttu-id="e98c5-110">El TCG también define una pila de software que hace uso de estos recursos para proporcionar operaciones de confianza para el software de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e98c5-110">The TCG also defines a software stack that makes use of these resources to provide trusted operations for application software.</span></span> <span data-ttu-id="e98c5-111">Sin embargo, no se realiza ninguna disposición para ejecutar una implementación de TSS en paralelo con el software del sistema operativo que también puede usar recursos de TPM.</span><span class="sxs-lookup"><span data-stu-id="e98c5-111">However, no provision is made for running a TSS implementation side-by-side with operating system software that may also be using TPM resources.</span></span> <span data-ttu-id="e98c5-112">La característica TBS resuelve este problema habilitando cada pila de software que se comunica con TBS para usar la comprobación de recursos de TPM para cualquier otra pila de software que pueda estar ejecutándose en la máquina.</span><span class="sxs-lookup"><span data-stu-id="e98c5-112">The TBS feature solves this problem by enabling each software stack that communicates with TBS to use TPM resources checking for any other software stacks that may be running on the machine.</span></span>

<span data-ttu-id="e98c5-113">La especificación del TPM y la especificación de la pila de software de TCG (TSS) están disponibles en [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/) .</span><span class="sxs-lookup"><span data-stu-id="e98c5-113">The TPM specification and TCG Software Stack (TSS) specification are available at [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/).</span></span>

<span data-ttu-id="e98c5-114">TBS se implementa como un servicio fuera de proceso que acepta comandos que usan un servicio RPC.</span><span class="sxs-lookup"><span data-stu-id="e98c5-114">TBS is implemented as an out-of-process service that accepts commands that use an RPC service.</span></span> <span data-ttu-id="e98c5-115">Una biblioteca vinculada dinámicamente presenta la interfaz del lenguaje C y se comunica con el servicio TBS.</span><span class="sxs-lookup"><span data-stu-id="e98c5-115">A dynamically linked library presents the C language interface and communicates with the TBS service.</span></span>

> [!Note]  
> <span data-ttu-id="e98c5-116">El servicio TBS solo acepta solicitudes RPC del equipo local.</span><span class="sxs-lookup"><span data-stu-id="e98c5-116">The TBS service only accepts RPC requests from the local machine.</span></span>

 

<span data-ttu-id="e98c5-117">Los objetivos principales de TBS son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e98c5-117">The primary goals of the TBS are to:</span></span>

-   <span data-ttu-id="e98c5-118">Proporcionan un uso compartido eficaz de los recursos de TPM limitados, como las ranuras de claves, las ranuras de las sesiones de autorización y las ranuras de transporte.</span><span class="sxs-lookup"><span data-stu-id="e98c5-118">Provide efficient sharing of limited TPM resources, such as key slots, authorization sessions slots, and transport slots.</span></span>
-   <span data-ttu-id="e98c5-119">Proporcionar acceso con prioridad y sincronizado a los recursos de TPM entre varias instancias de pilas de software de TPM.</span><span class="sxs-lookup"><span data-stu-id="e98c5-119">Provide prioritized and synchronized access to TPM resources between multiple instances of TPM software stacks.</span></span>
-   <span data-ttu-id="e98c5-120">Proporcione la administración adecuada de los recursos de TPM a través de los Estados de energía.</span><span class="sxs-lookup"><span data-stu-id="e98c5-120">Provide appropriate management of TPM resources across power states.</span></span>
-   <span data-ttu-id="e98c5-121">Impedir que las pilas de software de TPM tengan acceso a los comandos de TPM que se deben restringir, ya sea debido a limitaciones de plataforma o requisitos administrativos.</span><span class="sxs-lookup"><span data-stu-id="e98c5-121">Prevent TPM software stacks from accessing TPM commands that should be restricted, either because of platform limitations or administrative requirements.</span></span>

<span data-ttu-id="e98c5-122">En la ilustración siguiente se muestra la relación entre TBS y el TPM.</span><span class="sxs-lookup"><span data-stu-id="e98c5-122">The following illustration shows the relationship of the TBS to the TPM.</span></span>

![relación de TBS en modo de usuario con el TPM en modo kernel](images/tbs-block-diagram-as11601.png)

 

 




