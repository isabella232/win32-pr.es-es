---
description: Glosario de términos usados en la documentación del SDK de virtualización de Windows.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 365D0295-EA0B-4B40-8272-DFF62B2A6F3D
title: Glosario de Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: badb8fdfd25c4b7e11529778ab2cbd3c8cee5f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278616"
---
# <a name="hyper-v-glossary"></a><span data-ttu-id="6edbc-103">Glosario de Hyper-V</span><span class="sxs-lookup"><span data-stu-id="6edbc-103">Hyper-V glossary</span></span>

<span data-ttu-id="6edbc-104">En este tema se proporciona un glosario de términos que se usan en la documentación del SDK de virtualización de Windows.</span><span class="sxs-lookup"><span data-stu-id="6edbc-104">This topic provides a glossary of terms used in the Windows Virtualization SDK documentation.</span></span>

<dl> <dt>

<span data-ttu-id="6edbc-105"><span id="hyperv.virtualization_glossary_binding"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_BINDING"></span>**enlace**</span><span class="sxs-lookup"><span data-stu-id="6edbc-105"><span id="hyperv.virtualization_glossary_binding"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_BINDING"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-106">Proceso por el que se vinculan los servicios y las capas de software.</span><span class="sxs-lookup"><span data-stu-id="6edbc-106">A process by which software services and layers are linked together.</span></span> <span data-ttu-id="6edbc-107">Cuando se instala un servicio de red, se establecen las relaciones de enlace y las dependencias de los servicios.</span><span class="sxs-lookup"><span data-stu-id="6edbc-107">When a network service is installed, the binding relationships and dependencies for the services are established.</span></span>

</dd> <dt>

<span data-ttu-id="6edbc-108"><span id="hyperv.virtualization_glossary_checkpoint"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_CHECKPOINT"></span>**SnapSure**</span><span class="sxs-lookup"><span data-stu-id="6edbc-108"><span id="hyperv.virtualization_glossary_checkpoint"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_CHECKPOINT"></span>**checkpoint**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-109">Una instantánea de una máquina virtual que permite a un administrador revertir la máquina virtual a su estado en el momento en que se creó el punto de control.</span><span class="sxs-lookup"><span data-stu-id="6edbc-109">A snapshot of a virtual machine that enables an administrator to roll the virtual machine back to its state at the moment the checkpoint was created.</span></span>

</dd> <dt>

<span data-ttu-id="6edbc-110"><span id="hyperv.virtualization_glossary_compact"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_COMPACT"></span>**unidad**</span><span class="sxs-lookup"><span data-stu-id="6edbc-110"><span id="hyperv.virtualization_glossary_compact"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_COMPACT"></span>**compact**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-111">Para reducir el tamaño de un disco duro virtual de expansión dinámica quitando el espacio no utilizado del archivo. VHD.</span><span class="sxs-lookup"><span data-stu-id="6edbc-111">To reduce the size of a dynamically expanding virtual hard disk by removing unused space from the .vhd file.</span></span>

</dd> <dt>

<span data-ttu-id="6edbc-112"><span id="hyperv.virtualization_glossary_dvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DVHD"></span>**disco duro virtual de diferenciación**</span><span class="sxs-lookup"><span data-stu-id="6edbc-112"><span id="hyperv.virtualization_glossary_dvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DVHD"></span>**differencing virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-113">Un disco duro virtual que almacena los cambios en un disco duro virtual principal asociado con el fin de mantener el elemento primario intacto.</span><span class="sxs-lookup"><span data-stu-id="6edbc-113">A virtual hard disk that stores the changes to an associated parent virtual hard disk for the purpose of keeping the parent intact.</span></span> <span data-ttu-id="6edbc-114">El disco de diferenciación es un archivo. vhd independiente que está asociado con el archivo. vhd del disco primario.</span><span class="sxs-lookup"><span data-stu-id="6edbc-114">The differencing disk is a separate .vhd file that is associated with the .vhd file of the parent disk.</span></span> <span data-ttu-id="6edbc-115">Los cambios se siguen acumulando en el disco de diferenciación hasta que se combinan en el disco primario.</span><span class="sxs-lookup"><span data-stu-id="6edbc-115">Changes continue to accumulate in the differencing disk until it is merged to the parent disk.</span></span>

</dd> <dt>

<span data-ttu-id="6edbc-116"><span id="hyperv.virtualization_glossary_devhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DEVHD"></span>**disco duro virtual de expansión dinámica**</span><span class="sxs-lookup"><span data-stu-id="6edbc-116"><span id="hyperv.virtualization_glossary_devhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DEVHD"></span>**dynamically expanding virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-117">Un disco duro virtual que aumenta de tamaño cada vez que se modifica.</span><span class="sxs-lookup"><span data-stu-id="6edbc-117">A virtual hard disk that grows in size each time it is modified.</span></span> <span data-ttu-id="6edbc-118">Este tipo de disco duro virtual se inicia como un archivo. vhd de 3 KB y puede crecer hasta alcanzar el tamaño máximo especificado cuando se creó el archivo.</span><span class="sxs-lookup"><span data-stu-id="6edbc-118">This type of virtual hard disk starts as a 3 KB .vhd file and can grow as large as the maximum size specified when the file was created.</span></span> <span data-ttu-id="6edbc-119">La única manera de reducir el tamaño del archivo es eliminar los datos eliminados y, a continuación, compactar el disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="6edbc-119">The only way to reduce the file size is to zero out the deleted data and then compact the virtual hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="6edbc-120"><span id="hyperv.virtualization_glossary_fvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_FVHD"></span>**disco duro virtual de tamaño fijo**</span><span class="sxs-lookup"><span data-stu-id="6edbc-120"><span id="hyperv.virtualization_glossary_fvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_FVHD"></span>**fixed-size virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-121">Un disco duro virtual con un tamaño fijo que se determina y para el que se asigna todo el espacio cuando se crea el disco.</span><span class="sxs-lookup"><span data-stu-id="6edbc-121">A virtual hard disk with a fixed size that is determined and for which all space is allocated when the disk is created.</span></span> <span data-ttu-id="6edbc-122">El tamaño del disco no cambia cuando se agregan o eliminan datos.</span><span class="sxs-lookup"><span data-stu-id="6edbc-122">The size of the disk does not change when data is added or deleted.</span></span>

</dd> <dt>

<span data-ttu-id="6edbc-123"><span id="hyperv.virtualization_glossary_gen1vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN1VM"></span>**Máquina virtual de generación 1**</span><span class="sxs-lookup"><span data-stu-id="6edbc-123"><span id="hyperv.virtualization_glossary_gen1vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN1VM"></span>**Generation 1 virtual machine**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-124">Una máquina virtual (VM) que contiene el mismo hardware virtual presente en versiones de Hyper-V anteriores a Windows 8.1 y Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6edbc-124">A virtual machine (VM) that contains the same virtual hardware present in versions of Hyper-V prior to Windows 8.1 and Windows Server 2012 R2</span></span>

</dd> <dt>

<span data-ttu-id="6edbc-125"><span id="hyperv.virtualization_glossary_gen2vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN2VM"></span>**Máquina virtual de generación 2**</span><span class="sxs-lookup"><span data-stu-id="6edbc-125"><span id="hyperv.virtualization_glossary_gen2vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN2VM"></span>**Generation 2 virtual machine**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-126">Una máquina virtual (VM) que contiene un modelo de hardware virtual simplificado y utiliza el firmware UEFI en lugar del BIOS.</span><span class="sxs-lookup"><span data-stu-id="6edbc-126">A virtual machine (VM) that contains a simplified virtual hardware model and uses UEFI firmware instead of BIOS.</span></span> <span data-ttu-id="6edbc-127">En esta máquina virtual, la mayoría de los dispositivos emulados se quitan, lo que reduce la complejidad de la administración y la superficie expuesta a ataques de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6edbc-127">In this VM, most of the emulated devices are removed, which reduces management complexity and security attack surface.</span></span>

</dd> <dt>

<span data-ttu-id="6edbc-128"><span id="hyperv.virtualization_glossary_guestos"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GUESTOS"></span>**sistema operativo invitado**</span><span class="sxs-lookup"><span data-stu-id="6edbc-128"><span id="hyperv.virtualization_glossary_guestos"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GUESTOS"></span>**guest operating system**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-129">Es el sistema operativo que se ejecuta en una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6edbc-129">The operating system running on a virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="6edbc-130"><span id="hyperv.virtualization_glossary_integration_services"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_INTEGRATION_SERVICES"></span>**servicios de integración**</span><span class="sxs-lookup"><span data-stu-id="6edbc-130"><span id="hyperv.virtualization_glossary_integration_services"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_INTEGRATION_SERVICES"></span>**integration services**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-131">Colección de servicios y controladores de software que maximizan el rendimiento y proporcionan una mejor experiencia de usuario en una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6edbc-131">A collection of services and software drivers that maximize performance and provide a better user experience within a virtual machine.</span></span> <span data-ttu-id="6edbc-132">Los servicios de integración solo están disponibles para los sistemas operativos invitados admitidos.</span><span class="sxs-lookup"><span data-stu-id="6edbc-132">Integration services are only available for supported guest operating systems.</span></span>

</dd> <dt>

<span data-ttu-id="6edbc-133"><span id="hyperv.virtualization_glossary_kvp"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_KVP"></span>**par clave-valor**</span><span class="sxs-lookup"><span data-stu-id="6edbc-133"><span id="hyperv.virtualization_glossary_kvp"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_KVP"></span>**key-value pair**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-134">Conjunto de elementos de datos que contiene un identificador único, denominado clave, y un valor que es los datos reales de la clave.</span><span class="sxs-lookup"><span data-stu-id="6edbc-134">A set of data items that contains a unique identifier, called a key, and a value that is the actual data for the key.</span></span>

</dd> <dt>

<span data-ttu-id="6edbc-135"><span id="hyperv.virtualization_glossary_physical_computer"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_PHYSICAL_COMPUTER"></span>**equipo físico**</span><span class="sxs-lookup"><span data-stu-id="6edbc-135"><span id="hyperv.virtualization_glossary_physical_computer"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_PHYSICAL_COMPUTER"></span>**physical computer**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-136">Un equipo basado en hardware, en lugar de una máquina virtual basada en software.</span><span class="sxs-lookup"><span data-stu-id="6edbc-136">A hardware-based computer, as opposed to a software-based virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="6edbc-137"><span id="hyperv.virtualization_glossary_saved_state"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_SAVED_STATE"></span>**estado guardado**</span><span class="sxs-lookup"><span data-stu-id="6edbc-137"><span id="hyperv.virtualization_glossary_saved_state"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_SAVED_STATE"></span>**saved state**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-138">Manera de almacenar una máquina virtual para que se pueda reanudar rápidamente, de forma similar a un equipo portátil en hibernación.</span><span class="sxs-lookup"><span data-stu-id="6edbc-138">A manner of storing a virtual machine so that it can be quickly resumed, similar to a hibernated laptop.</span></span> <span data-ttu-id="6edbc-139">Cuando se coloca una máquina virtual en ejecución en un estado guardado, Virtual Server e Hyper-V detienen la máquina virtual, escriben los datos existentes en la memoria en archivos temporales y detienen el consumo de recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="6edbc-139">When you place a running virtual machine in a saved state, Virtual Server and Hyper-V stop the virtual machine, write the data that exists in memory to temporary files, and stop the consumption of system resources.</span></span> <span data-ttu-id="6edbc-140">Al restaurar una máquina virtual a partir de un estado guardado, se devuelve a la misma condición en que se encontraba cuando se guardó su estado.</span><span class="sxs-lookup"><span data-stu-id="6edbc-140">Restoring a virtual machine from a saved state returns it to the same condition it was in when its state was saved.</span></span>

</dd> <dt>

<span data-ttu-id="6edbc-141"><span id="hyperv.virtualization_glossary_vfd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VFD"></span>**disquete virtual**</span><span class="sxs-lookup"><span data-stu-id="6edbc-141"><span id="hyperv.virtualization_glossary_vfd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VFD"></span>**virtual floppy disk**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-142">Es una versión basada en archivos de un disquete físico.</span><span class="sxs-lookup"><span data-stu-id="6edbc-142">A file-based version of a physical floppy disk.</span></span> <span data-ttu-id="6edbc-143">Un disquete virtual se almacena como un archivo con la extensión de nombre de archivo. VFD.</span><span class="sxs-lookup"><span data-stu-id="6edbc-143">A virtual floppy disk is stored as a file with a .vfd file name extension.</span></span>

</dd> <dt>

<span data-ttu-id="6edbc-144"><span id="hyperv.virtualization_glossary_vhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHD"></span>**disco duro virtual**</span><span class="sxs-lookup"><span data-stu-id="6edbc-144"><span id="hyperv.virtualization_glossary_vhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHD"></span>**virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-145">El medio de almacenamiento de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6edbc-145">The storage medium for a virtual machine.</span></span> <span data-ttu-id="6edbc-146">Puede residir en cualquier topología de almacenamiento a la que el sistema operativo host pueda acceder, incluidos dispositivos externos, redes de área de almacenamiento y almacenamiento conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="6edbc-146">It can reside on any storage topology that the host operating system can access, including external devices, storage area networks, and network-attached storage.</span></span> <span data-ttu-id="6edbc-147">La extensión de nombre de archivo es. VHD.</span><span class="sxs-lookup"><span data-stu-id="6edbc-147">The file name extension is .vhd.</span></span>

</dd> <dt>

<span data-ttu-id="6edbc-148"><span id="hyperv.virtualization_glossary_vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM"></span>**máquina virtual**</span><span class="sxs-lookup"><span data-stu-id="6edbc-148"><span id="hyperv.virtualization_glossary_vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM"></span>**virtual machine**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-149">Un equipo dentro de un equipo, implementado en el software.</span><span class="sxs-lookup"><span data-stu-id="6edbc-149">A computer within a computer, implemented in software.</span></span> <span data-ttu-id="6edbc-150">Una máquina virtual emula un sistema de hardware completo, desde el procesador a la tarjeta de red, en un entorno de software independiente y aislado que permite el funcionamiento simultáneo de sistemas operativos que serían incompatibles de otro modo.</span><span class="sxs-lookup"><span data-stu-id="6edbc-150">A virtual machine emulates a complete hardware system, from processor to network card, in a self-contained, isolated software environment, enabling the simultaneous operation of otherwise incompatible operating systems.</span></span> <span data-ttu-id="6edbc-151">Cada sistema operativo secundario se ejecuta en su propia máquina virtual de software aislado.</span><span class="sxs-lookup"><span data-stu-id="6edbc-151">Each child operating system runs in its own isolated software virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="6edbc-152"><span id="hyperv.virtualization_glossary_vm_config"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM_CONFIG"></span>**configuración de la máquina virtual**</span><span class="sxs-lookup"><span data-stu-id="6edbc-152"><span id="hyperv.virtualization_glossary_vm_config"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM_CONFIG"></span>**virtual machine configuration**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-153">La configuración de los recursos asignados a una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6edbc-153">The configuration of the resources assigned to a virtual machine.</span></span> <span data-ttu-id="6edbc-154">Algunos ejemplos son los dispositivos como los discos y los adaptadores de red, así como la memoria y los procesadores.</span><span class="sxs-lookup"><span data-stu-id="6edbc-154">Examples include devices such as disks and network adapters, as well as memory and processors.</span></span>

</dd> <dt>

<span data-ttu-id="6edbc-155"><span id="hyperv.virtualization_glossary_vmms"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMMS"></span>**Servicio de administración de máquinas virtuales**</span><span class="sxs-lookup"><span data-stu-id="6edbc-155"><span id="hyperv.virtualization_glossary_vmms"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMMS"></span>**Virtual Machine Management Service**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-156">El servicio de Hyper-V que proporciona acceso de administración a las máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="6edbc-156">The Hyper-V service that provides management access to virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="6edbc-157"><span id="hyperv.virtualization_glossary_vmss"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMSS"></span>**instantánea de máquina virtual**</span><span class="sxs-lookup"><span data-stu-id="6edbc-157"><span id="hyperv.virtualization_glossary_vmss"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMSS"></span>**virtual machine snapshot**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-158">Una instantánea basada en archivos del estado, los datos de disco y la configuración de una máquina virtual en un momento específico.</span><span class="sxs-lookup"><span data-stu-id="6edbc-158">A file-based snapshot of the state, disk data, and configuration of a virtual machine at a specific point in time.</span></span>

</dd> <dt>

<span data-ttu-id="6edbc-159"><span id="hyperv.virtualization_glossary_virtual_network"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_NETWORK"></span>**red virtual**</span><span class="sxs-lookup"><span data-stu-id="6edbc-159"><span id="hyperv.virtualization_glossary_virtual_network"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_NETWORK"></span>**virtual network**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-160">Una versión virtual de un conmutador de red físico.</span><span class="sxs-lookup"><span data-stu-id="6edbc-160">A virtual version of a physical network switch.</span></span> <span data-ttu-id="6edbc-161">Una red virtual se puede configurar para proporcionar acceso a recursos de red locales o externos para una o más máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="6edbc-161">A virtual network can be configured to provide access to local or external network resources for one or more virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="6edbc-162"><span id="hyperv.virtualization_glossary_vnm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VNM"></span>**Administrador de redes virtuales**</span><span class="sxs-lookup"><span data-stu-id="6edbc-162"><span id="hyperv.virtualization_glossary_vnm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VNM"></span>**Virtual Network Manager**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-163">Servicio de Hyper-V que se usa para crear y administrar redes virtuales.</span><span class="sxs-lookup"><span data-stu-id="6edbc-163">A Hyper-V service used to create and manage virtual networks.</span></span>

</dd> <dt>

<span data-ttu-id="6edbc-164"><span id="hyperv.virtualization_glossary_virtual_switch"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_SWITCH"></span>**conmutador virtual**</span><span class="sxs-lookup"><span data-stu-id="6edbc-164"><span id="hyperv.virtualization_glossary_virtual_switch"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_SWITCH"></span>**virtual switch**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-165">Vea Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="6edbc-165">See virtual network.</span></span>

</dd> <dt>

<span data-ttu-id="6edbc-166"><span id="hyperv.virtualization_glossary_vhdx_resize"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHDX_RESIZE"></span>**Cambiar el tamaño de VHDX**</span><span class="sxs-lookup"><span data-stu-id="6edbc-166"><span id="hyperv.virtualization_glossary_vhdx_resize"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHDX_RESIZE"></span>**VHDX resize**</span></span>
</dt> <dd>

<span data-ttu-id="6edbc-167">Operación que reduce o expande un disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="6edbc-167">The operation that shrinks or expands a virtual hard disk.</span></span>

</dd> </dl>

 

 



