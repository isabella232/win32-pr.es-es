---
description: Los dispositivos serie de una máquina virtual se componen de controladores serie y puertos serie. Cada máquina virtual tiene exactamente un controlador serie y cada controlador serie tiene exactamente dos puertos serie.
ms.assetid: BA24BD74-D80C-4C5C-891F-5F17CDED2EC6
title: Clases de dispositivos serie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ae796b86837372d60bba83e51e0190b9c7d3f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687773"
---
# <a name="serial-devices-classes"></a><span data-ttu-id="f0198-104">Clases de dispositivos serie</span><span class="sxs-lookup"><span data-stu-id="f0198-104">Serial devices classes</span></span>

<span data-ttu-id="f0198-105">Los dispositivos serie de una máquina virtual se componen de controladores serie y puertos serie.</span><span class="sxs-lookup"><span data-stu-id="f0198-105">The serial devices in a virtual machine consist of serial controllers and serial ports.</span></span> <span data-ttu-id="f0198-106">Cada máquina virtual tiene exactamente un controlador serie y cada controlador serie tiene exactamente dos puertos serie.</span><span class="sxs-lookup"><span data-stu-id="f0198-106">Each virtual machine has exactly one serial controller, and each serial controller has exactly two serial ports.</span></span>

<span data-ttu-id="f0198-107">La configuración del controlador serie no es configurable. por lo tanto, no hay ninguna instancia de datos de configuración asociada.</span><span class="sxs-lookup"><span data-stu-id="f0198-107">The settings for the serial controller are not configurable; therefore, there is no setting data instance associated with it.</span></span> <span data-ttu-id="f0198-108">Además, no puede agregar ni quitar controladores serie o puertos serie de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f0198-108">Also, you cannot add or remove serial controllers or serial ports from a virtual machine.</span></span> <span data-ttu-id="f0198-109">Por lo tanto, no hay instancias del grupo de recursos para dispositivos serie.</span><span class="sxs-lookup"><span data-stu-id="f0198-109">Therefore, there are no resource pool instances for serial devices.</span></span>

<span data-ttu-id="f0198-110">A continuación se enumeran las clases WMI de virtualización relacionadas con los dispositivos serie.</span><span class="sxs-lookup"><span data-stu-id="f0198-110">The following are virtualization WMI classes related to serial devices.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f0198-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="f0198-111">In this section</span></span>



| <span data-ttu-id="f0198-112">Tema</span><span class="sxs-lookup"><span data-stu-id="f0198-112">Topic</span></span>                                                                                      | <span data-ttu-id="f0198-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0198-113">Description</span></span>                                                                     |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="f0198-114">**MSVM \_ SerialController**</span><span class="sxs-lookup"><span data-stu-id="f0198-114">**Msvm\_SerialController**</span></span>](msvm-serialcontroller.md)<br/>                         | <span data-ttu-id="f0198-115">Representa las capacidades y la administración del controlador serie.</span><span class="sxs-lookup"><span data-stu-id="f0198-115">Represents the capabilities and management of the serial controller.</span></span><br/> |
| [<span data-ttu-id="f0198-116">**MSVM \_ SerialPort**</span><span class="sxs-lookup"><span data-stu-id="f0198-116">**Msvm\_SerialPort**</span></span>](msvm-serialport.md)<br/>                                     | <span data-ttu-id="f0198-117">Representa un puerto serie asociado al controlador serie.</span><span class="sxs-lookup"><span data-stu-id="f0198-117">Represents a serial port associated with the serial controller.</span></span><br/>      |
| [<span data-ttu-id="f0198-118">**MSVM \_ SerialPortOnSerialController**</span><span class="sxs-lookup"><span data-stu-id="f0198-118">**Msvm\_SerialPortOnSerialController**</span></span>](msvm-serialportonserialcontroller.md)<br/> | <span data-ttu-id="f0198-119">Asocia un puerto serie a un controlador serie.</span><span class="sxs-lookup"><span data-stu-id="f0198-119">Associates a serial port with a serial controller.</span></span><br/>                   |



 

 

 




