---
description: Muestra el proceso para agregar un controlador de dispositivo a un dispositivo.
title: Asignación de un controlador de dispositivo a un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16db6a39406e3d8ba7cd8b497e12883685b80d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985467"
---
# <a name="how-to-assign-a-device-handler-to-a-device"></a><span data-ttu-id="18e8e-103">Asignación de un controlador de dispositivo a un dispositivo</span><span class="sxs-lookup"><span data-stu-id="18e8e-103">How to Assign a Device Handler to a Device</span></span>

<span data-ttu-id="18e8e-104">Muestra el proceso para agregar un controlador de dispositivo a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18e8e-104">Illustrates the process for adding a device handler to a device.</span></span>

## <a name="instructions"></a><span data-ttu-id="18e8e-105">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="18e8e-105">Instructions</span></span>


<span data-ttu-id="18e8e-106">Para asignar un controlador de dispositivo a un dispositivo, en la subclave **Device Parameters** de la instancia del dispositivo, agregue un valor de tipo **reg \_ SZ** llamado **DeviceHandlers**.</span><span class="sxs-lookup"><span data-stu-id="18e8e-106">To assign a device handler to a device, under the **Device Parameters** subkey of the device instance, add a value of type **REG\_SZ** named **DeviceHandlers**.</span></span> <span data-ttu-id="18e8e-107">La entrada de datos para este valor es el nombre del controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18e8e-107">The data entry for this value is the name of the device handler.</span></span>

<span data-ttu-id="18e8e-108">La siguiente es una entrada de ejemplo para un dispositivo ficticio vid \_ 059&PID \_ 0031.</span><span class="sxs-lookup"><span data-stu-id="18e8e-108">The following is an example entry for a fictitious Vid\_059&Pid\_0031 device.</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Enum
            USB
               Vid_059b&Pid_0031
                  059B003112010E93
                     Device Parameters
                        DeviceHandlers = MyDeviceHandler
```

<span data-ttu-id="18e8e-109">Los controladores de dispositivo también se pueden asignar mediante la configuración de [Grupo](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) de dispositivos o de [clase de dispositivo](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) .</span><span class="sxs-lookup"><span data-stu-id="18e8e-109">Device handlers can also be assigned by using [device group](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) or [device class](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) settings.</span></span>

 

 



