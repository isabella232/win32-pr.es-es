---
title: Kit de certificación de hardware de Windows
description: Kit de certificación de hardware de Windows
ms.assetid: 99BD2D7D-8F9D-445E-AE04-6A58FFF3DCE6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dba820d62d6766f74549ed23f7a5abdccbca258b
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104078499"
---
# <a name="windows-hardware-certification-kit"></a><span data-ttu-id="6fd3a-103">Kit de certificación de hardware de Windows</span><span class="sxs-lookup"><span data-stu-id="6fd3a-103">Windows Hardware Certification Kit</span></span>

## <a name="platforms"></a><span data-ttu-id="6fd3a-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="6fd3a-104">Platforms</span></span>

 <span data-ttu-id="6fd3a-105">**Clientes** : Windows 7 \| Windows 8</span><span class="sxs-lookup"><span data-stu-id="6fd3a-105">**Clients** - Windows 7 \| Windows 8</span></span>  
<span data-ttu-id="6fd3a-106">**Servidores** : windows Server 2008 R2 \| Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6fd3a-106">**Servers** - Windows Server 2008 R2 \| Windows Server 2012</span></span>  
<span data-ttu-id="6fd3a-107">**Servidor/controlador** : Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6fd3a-107">**Server/Controller** - Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="6fd3a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="6fd3a-108">Description</span></span>

<span data-ttu-id="6fd3a-109">El kit de certificación de hardware de Windows permite a los desarrolladores, ISV, IHV y OEM certificar sus dispositivos de hardware, sistemas y controladores de filtro para los sistemas operativos Windows más recientes.</span><span class="sxs-lookup"><span data-stu-id="6fd3a-109">The Windows Hardware Certification Kit enables developers, ISVs, IHVs, and OEMs to certify their hardware devices, systems, and filter drivers for the latest Windows operating systems.</span></span> <span data-ttu-id="6fd3a-110">Contiene todas las herramientas y documentación que necesita para certificar el hardware y los controladores de filtro para estos sistemas operativos:</span><span class="sxs-lookup"><span data-stu-id="6fd3a-110">It contains all the tools and documentation that you need to certify your hardware and filter drivers for these operating systems:</span></span>

-   <span data-ttu-id="6fd3a-111">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6fd3a-111">Windows 8</span></span>
-   <span data-ttu-id="6fd3a-112">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6fd3a-112">Windows Server 2012</span></span>
-   <span data-ttu-id="6fd3a-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6fd3a-113">Windows 7</span></span>
-   <span data-ttu-id="6fd3a-114">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6fd3a-114">Windows Server 2008 R2</span></span>

<span data-ttu-id="6fd3a-115">El kit de certificación de hardware de Windows sustituye al kit de logotipo de Windows y forma parte del programa de certificación de Windows.</span><span class="sxs-lookup"><span data-stu-id="6fd3a-115">The Windows Hardware Certification Kit replaces the Windows Logo Kit and is a part of the Windows Certification Program.</span></span>

## <a name="usage-or-best-practices"></a><span data-ttu-id="6fd3a-116">Uso o procedimientos recomendados</span><span class="sxs-lookup"><span data-stu-id="6fd3a-116">Usage or best practices</span></span>

<span data-ttu-id="6fd3a-117">Para poder probar cualquier controlador de hardware o de filtro, debe configurar el entorno de prueba adecuado en función del hardware o del controlador de filtro que está certificando.</span><span class="sxs-lookup"><span data-stu-id="6fd3a-117">Before you can test any hardware or filter driver, you must set up the proper test environment based on the hardware or filter driver you are certifying.</span></span> <span data-ttu-id="6fd3a-118">Esto incluye el controlador, el cliente y el hardware potencialmente adicional (por ejemplo, dispositivos multifunción) o software.</span><span class="sxs-lookup"><span data-stu-id="6fd3a-118">This includes the controller, client, and potentially additional hardware (for example, multi-function devices) or software.</span></span> <span data-ttu-id="6fd3a-119">Una vez configurado el entorno, puede probar el hardware con la nueva herramienta de estudio de HCK.</span><span class="sxs-lookup"><span data-stu-id="6fd3a-119">After your environment is set up, you can test your hardware using the new HCK’s Studio tool.</span></span> <span data-ttu-id="6fd3a-120">En estos pasos se describe el proceso de prueba de certificación.</span><span class="sxs-lookup"><span data-stu-id="6fd3a-120">These steps outline the certification test process.</span></span>

1.  <span data-ttu-id="6fd3a-121">Configurar un entorno de prueba.</span><span class="sxs-lookup"><span data-stu-id="6fd3a-121">Set up test environment.</span></span>
2.  <span data-ttu-id="6fd3a-122">Crear un proyecto.</span><span class="sxs-lookup"><span data-stu-id="6fd3a-122">Create a project.</span></span>
3.  <span data-ttu-id="6fd3a-123">Cree uno o varios grupos de máquinas.</span><span class="sxs-lookup"><span data-stu-id="6fd3a-123">Create one or more machine pools.</span></span>
4.  <span data-ttu-id="6fd3a-124">Seleccione las características que desea validar.</span><span class="sxs-lookup"><span data-stu-id="6fd3a-124">Select features to validate.</span></span>
5.  <span data-ttu-id="6fd3a-125">Seleccione y ejecute las pruebas en esas características.</span><span class="sxs-lookup"><span data-stu-id="6fd3a-125">Select and run tests against those features.</span></span>
6.  <span data-ttu-id="6fd3a-126">Ver los resultados de las pruebas.</span><span class="sxs-lookup"><span data-stu-id="6fd3a-126">View test results.</span></span>
7.  <span data-ttu-id="6fd3a-127">Envíe el paquete.</span><span class="sxs-lookup"><span data-stu-id="6fd3a-127">Submit your package.</span></span>

## <a name="resources"></a><span data-ttu-id="6fd3a-128">Recursos</span><span class="sxs-lookup"><span data-stu-id="6fd3a-128">Resources</span></span>

-   [<span data-ttu-id="6fd3a-129">Desarrollo de hardware de Windows</span><span class="sxs-lookup"><span data-stu-id="6fd3a-129">Windows Hardware Development</span></span>](https://msdn.microsoft.com/windows/hardware/)
-   <span data-ttu-id="6fd3a-130">[Programa de certificación de hardware de Windows](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6fd3a-130">[Windows Hardware Certification Program](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))</span></span>
-   <span data-ttu-id="6fd3a-131">[Empezar a desarrollar hardware para Windows](/previous-versions/gg507680(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="6fd3a-131">[Start Developing Hardware for Windows](/previous-versions/gg507680(v=msdn.10))</span></span>

 

 