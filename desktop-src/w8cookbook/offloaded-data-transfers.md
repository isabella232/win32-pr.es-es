---
title: Transferencias de datos descargados
description: Transferencias de datos descargados
ms.assetid: 91EBE6D6-2DA7-48DA-AEB7-3FAFCA8341F5
keywords:
- ODX
- descarga de copia
- reduce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1057ed27347fefc7ebc6a171eb7273da4341b024
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "105714487"
---
# <a name="offloaded-data-transfers"></a><span data-ttu-id="4a269-106">Transferencias de datos descargados</span><span class="sxs-lookup"><span data-stu-id="4a269-106">Offloaded data transfers</span></span>

## <a name="platforms"></a><span data-ttu-id="4a269-107">Plataformas</span><span class="sxs-lookup"><span data-stu-id="4a269-107">Platforms</span></span>

<span data-ttu-id="4a269-108">**Clientes** : Windows 8</span><span class="sxs-lookup"><span data-stu-id="4a269-108">**Clients** – Windows 8</span></span>  
<span data-ttu-id="4a269-109">**Servidores** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4a269-109">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="4a269-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a269-110">Description</span></span>

<span data-ttu-id="4a269-111">Para hacer avanzar el movimiento de datos de almacenamiento, Microsoft ha desarrollado una nueva tecnología de transferencia de datos: transferencia de datos descargados (ODX).</span><span class="sxs-lookup"><span data-stu-id="4a269-111">To advance the storage data movement, Microsoft has developed a new data transfer technology – offloaded data transfer (ODX).</span></span> <span data-ttu-id="4a269-112">En lugar de usar operaciones de lectura y escritura almacenadas en búfer, Windows ODX inicia la operación de copia con una descarga leída y recupera un token que representa los datos del dispositivo de almacenamiento y, a continuación, usa un comando de carga de descarga con el token para solicitar el movimiento de datos del disco de origen al disco de destino.</span><span class="sxs-lookup"><span data-stu-id="4a269-112">Instead of using buffered read and buffered write operations, Windows ODX starts the copy operation with an offload read and retrieves a token representing the data from the storage device, then uses an offload write command with the token to request data movement from the source disk to the destination disk.</span></span> <span data-ttu-id="4a269-113">El administrador de copia de los dispositivos de almacenamiento realiza el movimiento de datos según el token.</span><span class="sxs-lookup"><span data-stu-id="4a269-113">The copy manager of the storage devices performs the data movement according to the token.</span></span> <span data-ttu-id="4a269-114">En Windows 8, el administrador de ti y el administrador de almacenamiento pueden usar la característica ODX de Windows para interactuar con el dispositivo de almacenamiento con el fin de trasladar archivos o datos de gran tamaño a través de la red de almacenamiento de alta velocidad.</span><span class="sxs-lookup"><span data-stu-id="4a269-114">In the Windows 8, the IT manager and storage administrator are able to use the Windows ODX feature to interact with the storage device to move large files or data through the high-speed storage network.</span></span> <span data-ttu-id="4a269-115">Windows ODX reducirá notablemente el tráfico de red de cliente-servidor y el uso de tiempo de CPU durante las transferencias de datos grandes porque todo el movimiento de datos se encuentra en la red de almacenamiento de back-end.</span><span class="sxs-lookup"><span data-stu-id="4a269-115">Windows ODX will significantly reduce client-server network traffic and CPU time usage during large data transfers because all the data movement is at the backend storage network.</span></span> <span data-ttu-id="4a269-116">ODX se puede usar en la implementación de máquinas virtuales, la migración de datos masiva y la compatibilidad con dispositivos de almacenamiento en capas, y puede reducir el costo de la implementación de hardware físico a través de las características de almacenamiento ODX y de aprovisionamiento fino.</span><span class="sxs-lookup"><span data-stu-id="4a269-116">ODX can be used in virtual machine deployment, massive data migration, and tiered storage device support, and can lower the cost of physical hardware deployment through the ODX and thin provisioning storage features.</span></span>

> [!Note]  
> <span data-ttu-id="4a269-117">Esta característica solo funcionará en dispositivos de almacenamiento con la implementación de la especificación de SPC4 y SBC3.</span><span class="sxs-lookup"><span data-stu-id="4a269-117">This feature will only work on storage devices with SPC4 and SBC3 specification implementation.</span></span>

 

## <a name="functional-details"></a><span data-ttu-id="4a269-118">Detalles funcionales</span><span class="sxs-lookup"><span data-stu-id="4a269-118">Functional details</span></span>

-   <span data-ttu-id="4a269-119">La característica ODX de Windows se incrusta en el motor de copia del sistema operativo Windows. durante la enumeración de almacenamiento, Windows consultará la funcionalidad ODX del dispositivo de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="4a269-119">The Windows ODX feature is embedded in the copy engine of the Windows operating system; during storage enumeration, Windows will query the ODX capability of the storage device</span></span>
-   <span data-ttu-id="4a269-120">Copiar el dispositivo de almacenamiento de origen y el dispositivo de almacenamiento de destino de copia deben administrarse en el mismo administrador de copias para admitir la descarga de copia</span><span class="sxs-lookup"><span data-stu-id="4a269-120">Copy source storage device and copy destination storage device should be managed under the same copy manager for copy offload support</span></span>
-   <span data-ttu-id="4a269-121">Si se produce un error en una operación de descarga de copia, el administrador de copias del dispositivo de almacenamiento debe devolver los datos de detección adicionales adecuados para el control de errores de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="4a269-121">If a copy offload operation fails, the storage device’s copy manager must return the proper additional sense data for the apps’ error handling</span></span>
-   <span data-ttu-id="4a269-122">El motor de copia de Windows revertirá a la operación de copia tradicional si se produce un error en la operación de descarga de copia</span><span class="sxs-lookup"><span data-stu-id="4a269-122">The Windows copy engine will fall back to the traditional copy operation if the copy offload operation fails</span></span>

## <a name="using-odx"></a><span data-ttu-id="4a269-123">Usar ODX</span><span class="sxs-lookup"><span data-stu-id="4a269-123">Using ODX</span></span>

-   <span data-ttu-id="4a269-124">La aplicación de transferencia de datos debe asegurarse de que tanto el LUN de origen de copia como el LUN de destino de copia son compatibles con ODX antes de llamar a las rutinas de la API ODX</span><span class="sxs-lookup"><span data-stu-id="4a269-124">The data transfer app must ensure both copy source LUN and copy destination LUN are ODX capable before calling the ODX API routines</span></span>
-   <span data-ttu-id="4a269-125">En el explorador de Windows, los usuarios pueden usar "arrastrar" o "copiar y pegar" para realizar la descarga de copia</span><span class="sxs-lookup"><span data-stu-id="4a269-125">In Windows explorer, users could use “drag” or “copy and paste” to perform copy offload</span></span>
-   <span data-ttu-id="4a269-126">Cuando el LUN de origen y el LUN de destino se montan con el sistema de archivos, la aplicación solo debe llamar a la descarga \_ \_ de fsctl y la \_ \_ escritura de descarga de fsctl para realizar la transferencia de datos desde el LUN de origen al LUN de destino.</span><span class="sxs-lookup"><span data-stu-id="4a269-126">When the source LUN and destination LUN are mounted with the file system, the app must only call FSCTL\_Offload\_Read and FSCTL\_Offload\_Write to perform data transfer from the source LUN to the destination LUN</span></span>
-   <span data-ttu-id="4a269-127">Si se produce un error en una operación de descarga de copia, el administrador de copias del dispositivo de almacenamiento debe devolver los datos de detección adicionales adecuados para el control de errores de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="4a269-127">If a copy offload operation fails, the storage device’s copy manager must return the proper additional sense data for apps’ error handling</span></span>
-   <span data-ttu-id="4a269-128">Cuando el LUN de origen o el LUN de destino no están montados con el sistema de archivos y están bloqueados, la aplicación debe llamar al almacenamiento de IOCTL \_ \_ administrar \_ \_ \_ los atributos del conjunto de datos con la \_ acción DeviceDsmAction OffloadRead o DeviceDsmAction \_ OffloadWrite para realizar la descarga de la copia.</span><span class="sxs-lookup"><span data-stu-id="4a269-128">When the source LUN or destination LUN is not mounted with the file system and locked, the app must call IOCTL\_STORAGE\_MANAGE\_DATA\_SET\_ATTRIBUTES with DeviceDsmAction\_OffloadRead or DeviceDsmAction\_OffloadWrite action to perform copy offload</span></span>
-   <span data-ttu-id="4a269-129">Las aplicaciones de administración de almacenamiento pueden usar la \_ \_ API de paso a través de SCSI para realizar transferencias de datos descargados si los LUN de origen y de destino no se montan con ningún sistema de archivos y están bloqueados.</span><span class="sxs-lookup"><span data-stu-id="4a269-129">Storage management apps may use SCSI\_PASS\_THROUGH API to perform offloaded data transfers when both source and destination LUNs are not mounted with any file system and locked</span></span>

## <a name="tests"></a><span data-ttu-id="4a269-130">Pruebas</span><span class="sxs-lookup"><span data-stu-id="4a269-130">Tests</span></span>

-   <span data-ttu-id="4a269-131">Para garantizar una experiencia de usuario sólida, Compruebe la certificación de Windows ODX de la matriz de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="4a269-131">To ensure a robust user experience, verify the Windows ODX certification of the storage array</span></span>
-   <span data-ttu-id="4a269-132">El dispositivo de almacenamiento debe cumplir los requisitos de certificación de las transferencias de datos descargados de Windows (que se usan como logotipo) para admitir la característica ODX</span><span class="sxs-lookup"><span data-stu-id="4a269-132">The storage device must comply with Windows Offloaded Data Transfers certification (used to be Logo) requirements to support ODX feature</span></span>
-   <span data-ttu-id="4a269-133">Use el kit de certificación de hardware de transferencias de datos descargados de Windows para comprobar la compatibilidad de las características de ODX con los dispositivos de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="4a269-133">Use the Windows Offloaded Data Transfers Hardware Certification Kit to verify the ODX feature support of the storage devices</span></span>

## <a name="resources"></a><span data-ttu-id="4a269-134">Recursos</span><span class="sxs-lookup"><span data-stu-id="4a269-134">Resources</span></span>

-   <span data-ttu-id="4a269-135">Especificación de la XCOPY XCOPY Lite (11-059r8)</span><span class="sxs-lookup"><span data-stu-id="4a269-135">T10 XCOPY Lite Spec (11-059r8)</span></span>
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf)
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf)
-   [<span data-ttu-id="4a269-136">Servicios del panel de hardware</span><span class="sxs-lookup"><span data-stu-id="4a269-136">Hardware Dashboard Services</span></span>](/windows-hardware/drivers/dashboard/)
-   [<span data-ttu-id="4a269-137">\_Estructura de paso \_ a través de SCSI</span><span class="sxs-lookup"><span data-stu-id="4a269-137">SCSI\_PASS\_THROUGH Structure</span></span>](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_scsi_pass_through)

 

 