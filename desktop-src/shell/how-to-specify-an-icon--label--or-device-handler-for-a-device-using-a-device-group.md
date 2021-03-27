---
description: Los grupos de dispositivos permiten la especificación de las propiedades Icons, Label o DeviceHandlers de cualquier dispositivo que declare parte de ese grupo.
ms.assetid: 84433068-A869-479D-8ADA-E8221B38CCAE
title: Cómo especificar un icono, etiqueta o controlador de dispositivo para un dispositivo mediante un grupo de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e534aa6fa1bc7dbfe1bae3a2825a14f18096176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001902"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-group"></a>Cómo especificar un icono, etiqueta o controlador de dispositivo para un dispositivo mediante un grupo de dispositivos

Los grupos de dispositivos permiten la especificación de las propiedades Icons, Label o DeviceHandlers de cualquier dispositivo que declare parte de ese grupo. Si el grupo de dispositivos no es un grupo de dispositivos proporcionado por el sistema, se agregará una clave que defina el grupo de dispositivos en la clave **AutoplayHandlers** \\ **DeviceGroups** . No es necesario establecer las tres propiedades de cada grupo; solo puede establecer las propiedades que desea personalizar. Sin embargo, los dispositivos y los controladores de dispositivo siempre deben tener asociados iconos y etiquetas para cumplir los requisitos mínimos de uso.

## <a name="instructions"></a>Instrucciones


En el ejemplo siguiente se usa un sistema con varias unidades Zip conectadas. Sin especificar los valores iconos, etiqueta y DeviceHandlers de cada unidad individualmente, se crea un grupo de dispositivos denominado ZipDrive y se definen los valores que contiene. Cada unidad Zip se declara a continuación como un miembro del grupo ZipDrive.

En primer lugar, defina el grupo de dispositivos agregando la siguiente clave *ZipDrive* y sus valores.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceGroups
                        ZipDrive
                           Icons [REG_MULTI_SZ] = %SystemRoot%\system32\mydll.dll,-103
                           NoMediaIcons [REG_MULTI_SZ] = %SystemRoot%\system32\mydll.dll,-104
                           Label [REG_SZ] = My Custom Device Label
                           DeviceHandlers [REG_SZ] = MyDeviceHandler
```

Cada dispositivo de unidad Zip se declara como parte del grupo ZipDrive, heredando las propiedades de ese grupo. En la clave **DeviceParameters** de la instancia del dispositivo, agregue un valor denominado DeviceGroup como tipo **reg \_ SZ**. La entrada de datos para este valor es el nombre del grupo de dispositivos.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Enum
            USB
               Vid_059b&Pid_0031
                  059B003112010E93
                     Device Parameters
                        DeviceGroup [REG_SZ] = ZipDrive
```

También puede Agregar propiedades de dispositivo personalizadas que no sean iconos, etiqueta y DeviceHandlers en la clave del grupo de dispositivos y, a continuación, aplicarlos a todos los dispositivos que pertenecen a ese grupo de dispositivos.

> [!Note]  
> Las propiedades que se definen en el nivel de instancia de dispositivo tienen prioridad sobre las propiedades definidas en el nivel de grupo de dispositivos, que a su vez tienen prioridad sobre las propiedades definidas en el nivel de clase de dispositivo.

 

 

 



