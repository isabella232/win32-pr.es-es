---
description: Muestra el proceso para agregar un controlador de dispositivos a un dispositivo.
title: Asignación de un controlador de dispositivos a un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de091a7206e8fe2d9ea2781e2c5b3475cb71446bae2effa9e017795ced8b9bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092979"
---
# <a name="how-to-assign-a-device-handler-to-a-device"></a>Asignación de un controlador de dispositivos a un dispositivo

Muestra el proceso para agregar un controlador de dispositivos a un dispositivo.

## <a name="instructions"></a>Instructions


Para asignar un controlador de dispositivos a un dispositivo, en la subclave **Parámetros** del dispositivo de la instancia del dispositivo, agregue un valor de tipo **REG \_ SZ** denominado **DeviceHandlers**. La entrada de datos de este valor es el nombre del controlador de dispositivos.

A continuación se muestra una entrada de ejemplo para un dispositivo Vid \_ 059&Pid \_ 0031 ficticio.

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

Los controladores de dispositivos también se pueden asignar mediante la configuración del grupo [de dispositivos](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) [o la clase de](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) dispositivo.

 

 



