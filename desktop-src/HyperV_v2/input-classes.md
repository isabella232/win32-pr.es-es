---
description: Estas clases representan los dispositivos de entrada de usuario. Una máquina virtual siempre tiene una instancia de cada clase asociada.
ms.assetid: FFCA890D-6102-47BB-B499-4B9D77D75E9B
title: Clases de entrada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2955cadfb00dcc39fed490a9c706b12bb1a8993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687196"
---
# <a name="input-classes"></a><span data-ttu-id="43b74-104">Clases de entrada</span><span class="sxs-lookup"><span data-stu-id="43b74-104">Input classes</span></span>

<span data-ttu-id="43b74-105">Estas clases representan los dispositivos de entrada de usuario.</span><span class="sxs-lookup"><span data-stu-id="43b74-105">The user input devices are represented by these classes.</span></span> <span data-ttu-id="43b74-106">Una máquina virtual siempre tiene una instancia de cada clase asociada.</span><span class="sxs-lookup"><span data-stu-id="43b74-106">A virtual machine always has one instance of each class associated with it.</span></span> <span data-ttu-id="43b74-107">Es posible que estos dispositivos no se agreguen o quiten de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="43b74-107">These devices may not be added or removed from the virtual machine.</span></span> <span data-ttu-id="43b74-108">Por lo tanto, no hay instancias del grupo de recursos para dispositivos de teclado o de mouse.</span><span class="sxs-lookup"><span data-stu-id="43b74-108">Therefore, there are no resource pool instances for keyboard or mouse devices.</span></span>

<span data-ttu-id="43b74-109">Los dispositivos de teclado y mouse están vinculados a la máquina virtual a través de la Asociación [**MSVM \_ SystemDevice**](msvm-systemdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="43b74-109">The keyboard and mouse devices are linked to the virtual machine through the [**Msvm\_SystemDevice**](msvm-systemdevice.md) association.</span></span> <span data-ttu-id="43b74-110">Una máquina virtual contiene un dispositivo de mouse PS2 y uno sintético.</span><span class="sxs-lookup"><span data-stu-id="43b74-110">A virtual machine contains both a PS2 and a synthetic mouse device.</span></span> <span data-ttu-id="43b74-111">Solo hay un dispositivo señalador activo a la vez.</span><span class="sxs-lookup"><span data-stu-id="43b74-111">Only one pointing device is active at a time.</span></span>

<span data-ttu-id="43b74-112">A continuación se enumeran las clases WMI de virtualización relacionadas con la entrada.</span><span class="sxs-lookup"><span data-stu-id="43b74-112">The following are virtualization WMI classes related to input.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="43b74-113">En esta sección</span><span class="sxs-lookup"><span data-stu-id="43b74-113">In this section</span></span>



| <span data-ttu-id="43b74-114">Tema</span><span class="sxs-lookup"><span data-stu-id="43b74-114">Topic</span></span>                                                          | <span data-ttu-id="43b74-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="43b74-115">Description</span></span>                                     |
|----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="43b74-116">**\_Teclado MSVM**</span><span class="sxs-lookup"><span data-stu-id="43b74-116">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)<br/>             | <span data-ttu-id="43b74-117">Representa un dispositivo de teclado.</span><span class="sxs-lookup"><span data-stu-id="43b74-117">Represents a keyboard device.</span></span><br/>        |
| [<span data-ttu-id="43b74-118">**MSVM \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="43b74-118">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)<br/>             | <span data-ttu-id="43b74-119">Representa un dispositivo de mouse PS2.</span><span class="sxs-lookup"><span data-stu-id="43b74-119">Represents a PS2 mouse device.</span></span><br/>       |
| [<span data-ttu-id="43b74-120">**MSVM \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="43b74-120">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)<br/> | <span data-ttu-id="43b74-121">Representa un dispositivo de mouse sintético.</span><span class="sxs-lookup"><span data-stu-id="43b74-121">Represents a synthetic mouse device.</span></span><br/> |



 

 

 




