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
# <a name="how-to-assign-a-device-handler-to-a-device"></a>Asignación de un controlador de dispositivo a un dispositivo

Muestra el proceso para agregar un controlador de dispositivo a un dispositivo.

## <a name="instructions"></a>Instrucciones


Para asignar un controlador de dispositivo a un dispositivo, en la subclave **Device Parameters** de la instancia del dispositivo, agregue un valor de tipo **reg \_ SZ** llamado **DeviceHandlers**. La entrada de datos para este valor es el nombre del controlador de dispositivo.

La siguiente es una entrada de ejemplo para un dispositivo ficticio vid \_ 059&PID \_ 0031.

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

Los controladores de dispositivo también se pueden asignar mediante la configuración de [Grupo](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) de dispositivos o de [clase de dispositivo](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) .

 

 



