---
title: Aprovisionamiento fino de unidades lógicas
description: Aprovisionamiento fino de unidades lógicas
ms.assetid: D64ECA7B-62AC-4C14-BE4B-84DA2E20C16B
keywords:
- LUN
- LBA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4abb6fa3cec112737b23e3cd658a48984cb0fcd1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104078507"
---
# <a name="thin-provisioning-of-logical-units"></a><span data-ttu-id="fb49f-105">Aprovisionamiento fino de unidades lógicas</span><span class="sxs-lookup"><span data-stu-id="fb49f-105">Thin provisioning of logical units</span></span>

## <a name="platforms"></a><span data-ttu-id="fb49f-106">Plataformas</span><span class="sxs-lookup"><span data-stu-id="fb49f-106">Platforms</span></span>

<span data-ttu-id="fb49f-107">**Clientes** : Windows 8</span><span class="sxs-lookup"><span data-stu-id="fb49f-107">**Clients** – Windows 8</span></span>  
<span data-ttu-id="fb49f-108">**Servidores** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fb49f-108">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="fb49f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb49f-109">Description</span></span>

<span data-ttu-id="fb49f-110">El aprovisionamiento fino de Windows es una interfaz para la solución de aprovisionamiento de almacenamiento de un extremo a otro.</span><span class="sxs-lookup"><span data-stu-id="fb49f-110">Windows Thin Provisioning is an interface to the end-to-end storage provisioning solution.</span></span> <span data-ttu-id="fb49f-111">Para ofrecer un servicio de aprovisionamiento de almacenamiento de alta disponibilidad, escalable y fácil de usar, se necesitan implementaciones sólidas desde el host del servidor al dispositivo de destino de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="fb49f-111">To deliver a highly available, scalable and user-friendly storage provisioning service requires robust implementations from the server host to the storage target device.</span></span> <span data-ttu-id="fb49f-112">La característica de aprovisionamiento fino de Windows proporciona una vista sincrónica de los dispositivos de almacenamiento de aprovisionamiento fino al administrador del sistema, el administrador de ti y el administrador de almacenamiento a través de la identificación de la unidad lógica (LUN) de aprovisionamiento fino, la notificación de umbrales, el control de agotamiento de recursos, la recuperación de espacio y la recuperación de estado del direccionamiento de bloque lógico (LBA)</span><span class="sxs-lookup"><span data-stu-id="fb49f-112">The Windows thin provisioning feature provides a synchronous view of the thin provisioning storage devices to the system administrator, IT manager, and storage administrator through the thinly provisioned logical unit’s (LUN’s) identification, threshold notification, resource exhaustion handling, space reclamation, and logical block addressing (LBA) state retrieval.</span></span> <span data-ttu-id="fb49f-113">La característica de aprovisionamiento fino de Windows presenta un sólido modelo de servicio de aprovisionamiento de almacenamiento que se puede aplicar a los sistemas de almacenamiento cliente-servidor, almacenamiento de virtualización y servicios de almacenamiento en la nube.</span><span class="sxs-lookup"><span data-stu-id="fb49f-113">The Windows thin provisioning feature presents a robust storage provisioning service model that can be applied to client-server storage systems, virtualization storage, and cloud storage services.</span></span> <span data-ttu-id="fb49f-114">Microsoft garantizará la alta calidad de la característica de aprovisionamiento fino aplicando los requisitos del kit de certificación de hardware de aprovisionamiento fino de Windows para los productos de la matriz de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="fb49f-114">Microsoft will ensure the high quality of the thin provisioning feature by enforcing the Windows Thin Provisioning Hardware Certification Kit requirements for storage array products.</span></span>

<span data-ttu-id="fb49f-115">La solución de almacenamiento de aprovisionamiento fino de Windows:</span><span class="sxs-lookup"><span data-stu-id="fb49f-115">The Windows Thin Provisioning storage solution:</span></span>

-   <span data-ttu-id="fb49f-116">Permite a los administradores de almacenamiento crear un LUN mayor con menos recursos de disco físico.</span><span class="sxs-lookup"><span data-stu-id="fb49f-116">Allows storage administrators to create a larger LUN with fewer physical disk resources</span></span>
-   <span data-ttu-id="fb49f-117">Agrega o quita un recurso de disco físico sin interrumpir el servicio de aprovisionamiento de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="fb49f-117">Adds or removes physical disk resource without interrupting the storage provisioning service</span></span>
-   <span data-ttu-id="fb49f-118">Alerta a los usuarios del uso del volumen de almacenamiento a través de la configuración de umbral</span><span class="sxs-lookup"><span data-stu-id="fb49f-118">Alerts users to the storage volume usage through the threshold setting</span></span>
-   <span data-ttu-id="fb49f-119">Admite el aprovisionamiento de almacenamiento a través de la configuración del grupo de almacenamiento compartido</span><span class="sxs-lookup"><span data-stu-id="fb49f-119">Supports storage provisioning through the shared storage pool configuration</span></span>
-   <span data-ttu-id="fb49f-120">Aumenta o disminuye el tamaño del grupo de almacenamiento en función de la demanda y el uso del espacio de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="fb49f-120">Increases or decreases the size of the storage pool according to the demand and usage of storage space</span></span>

<span data-ttu-id="fb49f-121">Resumen de las características de aprovisionamiento fino de Windows:</span><span class="sxs-lookup"><span data-stu-id="fb49f-121">Summary of the Windows Thin Provisioning features:</span></span>

-   <span data-ttu-id="fb49f-122">Identificación de LUN de aprovisionamiento fino</span><span class="sxs-lookup"><span data-stu-id="fb49f-122">Thin Provisioning LUN identification</span></span>
-   <span data-ttu-id="fb49f-123">Identificadores para la notificación de umbrales, el agotamiento de recursos temporal y el agotamiento de recursos permanente</span><span class="sxs-lookup"><span data-stu-id="fb49f-123">Handles for threshold notification, temporary resource exhaustion, and permanent resource exhaustion</span></span>
-   <span data-ttu-id="fb49f-124">Recuperación del espacio de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="fb49f-124">Storage space reclamation</span></span>
-   <span data-ttu-id="fb49f-125">Asignación de consultas de estado de bloques lógicos</span><span class="sxs-lookup"><span data-stu-id="fb49f-125">Mapping state queries of logical blocks</span></span>

## <a name="manifestation"></a><span data-ttu-id="fb49f-126">Manifestación</span><span class="sxs-lookup"><span data-stu-id="fb49f-126">Manifestation</span></span>

<span data-ttu-id="fb49f-127">Sin la comprensión adecuada de los identificadores de Windows para el LUN de aprovisionamiento fino, la aplicación podría generar un error inesperado o una causa desconocida.</span><span class="sxs-lookup"><span data-stu-id="fb49f-127">Without the proper understanding of the Windows handles for thin provisioning LUN, the app could fail with unexpected behavior or for an unknown cause.</span></span>

## <a name="using-thin-provisioning-luns"></a><span data-ttu-id="fb49f-128">Uso de LUN de aprovisionamiento fino</span><span class="sxs-lookup"><span data-stu-id="fb49f-128">Using thin provisioning LUNs</span></span>

<span data-ttu-id="fb49f-129">Para usar LUN con aprovisionamiento fino en Windows 8 o Windows Server 2012, los administradores de sistemas y almacenamiento deben tener en cuenta estos aspectos:</span><span class="sxs-lookup"><span data-stu-id="fb49f-129">To use thinly provisioned LUNs in Windows 8 or Windows Server 2012, system and storage administrators should be aware of these matters:</span></span>

-   <span data-ttu-id="fb49f-130">Identificación de LUN de aprovisionamiento fino; los administradores del sistema o los usuarios finales pueden usar Defrag y la utilidad del optimizador de almacenamiento para identificar el tipo de medio del dispositivo de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="fb49f-130">Thin provisioning LUN identification; system administrators or end users can use Defrag and the Storage Optimizer utility to identify the media type of the storage device</span></span>
-   <span data-ttu-id="fb49f-131">Cuando se alcanza un umbral o un evento de agotamiento de recursos permanente, Windows registra un evento del sistema para alertar al administrador del sistema</span><span class="sxs-lookup"><span data-stu-id="fb49f-131">When a threshold or a permanent resource exhaustion event is hit, Windows will log a system event to alert the system administrator</span></span>
-   <span data-ttu-id="fb49f-132">La recuperación de espacio de almacenamiento se puede realizar manual o automáticamente mediante la notificación de eliminación de archivo o el programador del optimizador de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="fb49f-132">Storage space reclamation can be performed manually or automatically by file delete notification or the scheduler of the storage optimizer</span></span>
-   <span data-ttu-id="fb49f-133">El administrador de almacenamiento debe implementar la notificación de umbral para alertar al administrador del sistema o al usuario final y evitar cualquier interrupción del servicio de almacenamiento inesperada.</span><span class="sxs-lookup"><span data-stu-id="fb49f-133">Storage administrator should implement the threshold notification to alert system administrator or end user and avoid any unexpected storage service interruption</span></span>

## <a name="tests"></a><span data-ttu-id="fb49f-134">Pruebas</span><span class="sxs-lookup"><span data-stu-id="fb49f-134">Tests</span></span>

-   <span data-ttu-id="fb49f-135">La matriz de almacenamiento debe recibir el certificado de aprovisionamiento fino de Windows 8 para admitir las características de aprovisionamiento fino de Windows</span><span class="sxs-lookup"><span data-stu-id="fb49f-135">Storage array must receive Windows 8 Thin Provisioning certificate to support Windows Thin Provisioning features</span></span>
-   <span data-ttu-id="fb49f-136">El kit de certificación de hardware de aprovisionamiento fino de Windows para la matriz de almacenamiento será una herramienta de prueba útil para comprobar la capacidad de la matriz de almacenamiento para la compatibilidad con las características de aprovisionamiento fino de Windows</span><span class="sxs-lookup"><span data-stu-id="fb49f-136">Windows Thin Provisioning Hardware Certification Kit for storage array will be a useful test tool to verify storage array’s capability for Windows Thin Provisioning feature support</span></span>
-   <span data-ttu-id="fb49f-137">Windows espera que el LUN de aprovisionamiento fino y el LUN de aprovisionamiento completo funcionen en el mismo sistema sin ningún problema</span><span class="sxs-lookup"><span data-stu-id="fb49f-137">Windows expects the Thin Provisioning LUN and Full Provisioning LUN to work in the same system without any issue</span></span>

## <a name="resources"></a><span data-ttu-id="fb49f-138">Recursos</span><span class="sxs-lookup"><span data-stu-id="fb49f-138">Resources</span></span>

-   [<span data-ttu-id="fb49f-139">Especificación del comando de bloque SCSI de T10 (SBC3r27)</span><span class="sxs-lookup"><span data-stu-id="fb49f-139">T10 SCSI Block Command Spec (SBC3r27)</span></span>](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r27.pdf)
-   [<span data-ttu-id="fb49f-140">Servicios del panel de hardware</span><span class="sxs-lookup"><span data-stu-id="fb49f-140">Hardware Dashboard Services</span></span>](/windows-hardware/drivers/dashboard/)

 

 