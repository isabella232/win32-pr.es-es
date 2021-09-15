---
description: Los grupos de dispositivos permiten especificar las propiedades Iconos, Etiqueta o DeviceHandlers para cualquier dispositivo que se declare como parte de ese grupo.
ms.assetid: 84433068-A869-479D-8ADA-E8221B38CCAE
title: Cómo especificar un icono, una etiqueta o un controlador de dispositivos para un dispositivo mediante un grupo de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e534aa6fa1bc7dbfe1bae3a2825a14f18096176
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468189"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-group"></a>Cómo especificar un icono, una etiqueta o un controlador de dispositivos para un dispositivo mediante un grupo de dispositivos

Los grupos de dispositivos permiten especificar las propiedades Iconos, Etiqueta o DeviceHandlers para cualquier dispositivo que se declare como parte de ese grupo. Si el grupo de dispositivos no es un grupo de dispositivos proporcionado por el sistema, se agregará una clave que defina el grupo de dispositivos en la clave **DeviceGroups de AutoplayHandlers.** \\  No es necesario establecer las tres propiedades para cada grupo; solo puede establecer las propiedades que desea personalizar. Sin embargo, los dispositivos y los controladores de dispositivos siempre deben tener asociados iconos y etiquetas para cumplir los requisitos mínimos de facilidad de uso.

## <a name="instructions"></a>Instructions


En el ejemplo siguiente se usa un sistema con varias unidades Zip conectadas. Sin especificar los valores icons, Label y DeviceHandlers para cada unidad individualmente, se crea un grupo de dispositivos denominado ZipDrive y se definen esos valores dentro de él. A continuación, cada unidad ZIP se declara como miembro del grupo ZipDrive.

En primer lugar, defina el grupo de dispositivos agregando la siguiente *clave zipDrive* y sus valores.

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

A continuación, cada dispositivo de unidad ZIP se declara como parte del grupo ZipDrive, heredando las propiedades de ese grupo. En la **clave DeviceParameters** de la instancia del dispositivo, agregue un valor denominado DeviceGroup como tipo **REG \_ SZ**. La entrada de datos de este valor es el nombre del grupo de dispositivos.

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

También puede agregar propiedades de dispositivo personalizadas que no son Iconos, Etiqueta y DeviceHandlers en la clave del grupo de dispositivos y, a continuación, aplicarlas a todos los dispositivos que pertenecen a ese grupo de dispositivos.

> [!Note]  
> Las propiedades que se definen en el nivel de instancia de dispositivo tienen prioridad sobre las propiedades definidas en el nivel de grupo de dispositivos, que a su vez tienen prioridad sobre las propiedades definidas en el nivel de clase de dispositivo.

 

 

 



