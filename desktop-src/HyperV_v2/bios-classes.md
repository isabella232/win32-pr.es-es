---
description: El BIOS virtual es una imagen de software que se carga en la RAM para configurar algunos de los aspectos básicos de y arrancar un equipo. Hay un elemento BIOS por sistema y ese elemento no se puede reemplazar ni quitar.
ms.assetid: EC691401-947F-4B56-A8A7-F0ECBF01677B
title: Clases de BIOS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e725910bbeb1032f876b5e4fcf08da4a6ea60bc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104002018"
---
# <a name="bios-classes"></a><span data-ttu-id="4cbda-104">Clases de BIOS</span><span class="sxs-lookup"><span data-stu-id="4cbda-104">BIOS classes</span></span>

<span data-ttu-id="4cbda-105">El BIOS virtual es una imagen de software que se carga en la RAM para configurar algunos de los aspectos básicos de y arrancar un equipo.</span><span class="sxs-lookup"><span data-stu-id="4cbda-105">The virtual BIOS is a software image that is loaded into RAM to configure some of the basic aspects of and boot a computer system.</span></span> <span data-ttu-id="4cbda-106">Hay un elemento BIOS por sistema y ese elemento no se puede reemplazar ni quitar.</span><span class="sxs-lookup"><span data-stu-id="4cbda-106">There is one BIOS element per computer system and that element cannot be replaced or removed.</span></span> <span data-ttu-id="4cbda-107">Por lo tanto, no hay ningún grupo de recursos para agregar nuevos elementos BIOS a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4cbda-107">Thus, there is no resource pool for adding new BIOS elements to the virtual machine.</span></span> <span data-ttu-id="4cbda-108">El elemento BIOS tampoco tiene su propia clase SettingData para describir la configuración del BIOS.</span><span class="sxs-lookup"><span data-stu-id="4cbda-108">The BIOS element also does not have its own SettingData class to describe the settings for the BIOS.</span></span> <span data-ttu-id="4cbda-109">La configuración del BIOS, como los números de serie, el orden de arranque y el estado de Bloq Num, se encuentra en la clase [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="4cbda-109">Settings for the BIOS, such as serial numbers, boot order, and num lock state, are found in the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class.</span></span>

<span data-ttu-id="4cbda-110">A continuación se enumeran las clases WMI de virtualización relacionadas con el BIOS.</span><span class="sxs-lookup"><span data-stu-id="4cbda-110">The following are virtualization WMI classes related to the BIOS.</span></span> <span data-ttu-id="4cbda-111">Estas clases se encuentran en \\ \\ . \\ \\Espacio de nombres de virtualización de raíz.</span><span class="sxs-lookup"><span data-stu-id="4cbda-111">These classes are in the \\\\.\\Root\\Virtualization namespace.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4cbda-112">En esta sección</span><span class="sxs-lookup"><span data-stu-id="4cbda-112">In this section</span></span>



| <span data-ttu-id="4cbda-113">Tema</span><span class="sxs-lookup"><span data-stu-id="4cbda-113">Topic</span></span>                                                    | <span data-ttu-id="4cbda-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4cbda-114">Description</span></span>                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4cbda-115">**MSVM \_ BIOSElement**</span><span class="sxs-lookup"><span data-stu-id="4cbda-115">**Msvm\_BIOSElement**</span></span>](msvm-bioselement.md)<br/> | <span data-ttu-id="4cbda-116">Representa el software de bajo nivel que se carga en la RAM para configurar e iniciar el sistema.</span><span class="sxs-lookup"><span data-stu-id="4cbda-116">Represents the low-level software that is loaded into RAM to configure and start the system.</span></span><br/> |
| [<span data-ttu-id="4cbda-117">**MSVM \_ SystemBIOS**</span><span class="sxs-lookup"><span data-stu-id="4cbda-117">**Msvm\_SystemBIOS**</span></span>](msvm-systembios.md)<br/>   | <span data-ttu-id="4cbda-118">Se usa para asociar una máquina virtual a su BIOS.</span><span class="sxs-lookup"><span data-stu-id="4cbda-118">Used to associate a virtual machine with its BIOS.</span></span><br/>                                           |



 

 

 




