---
description: Muestra el proceso para agregar un controlador de dispositivos a un dispositivo.
title: Asignación de un controlador de dispositivos a un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16db6a39406e3d8ba7cd8b497e12883685b80d93
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360373"
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

Los controladores de dispositivos también se pueden asignar mediante la configuración del grupo [de dispositivos](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md) o [la clase de](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md) dispositivo.

 

 



