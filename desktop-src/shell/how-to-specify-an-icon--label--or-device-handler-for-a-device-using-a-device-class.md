---
description: Las clases de dispositivo permiten especificar las propiedades Icons, Label y DeviceHandlers para cualquier dispositivo de esa clase.
ms.assetid: E32C1BA6-B520-4809-A9E9-48813C7EBAA4
title: Cómo especificar un icono, una etiqueta o un controlador de dispositivos para un dispositivo mediante una clase de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f81ee6fa469a6bec13abbc1d8a088f5fb334ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468191"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-class"></a>Cómo especificar un icono, una etiqueta o un controlador de dispositivos para un dispositivo mediante una clase de dispositivo

Las clases de dispositivo permiten especificar las propiedades Icons, Label y DeviceHandlers para cualquier dispositivo de esa clase. Esto es similar al uso de grupos de dispositivos, pero las clases de dispositivo y sus pertenencias están determinadas por el hardware en lugar de crearse o asignarse. Cada nombre de clave de clase, que es Plug and Play GUID de interfaz de dispositivo, se encuentra en la **clave DeviceClasses.** En la clave de clase individual, asigne los valores para Iconos, Etiqueta y DeviceHandlers.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Paso 1:

En el ejemplo siguiente se muestran los valores de clave de clase y DeviceHandlers para la interfaz de volumen.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceClasses
                        {53f5630d-b6bf-11d0-94f2-00a0c91efb8b}
                           DeviceHandlers [REG_SZ] = GenericVolumeHandler
```

También puede agregar propiedades de dispositivo personalizadas en la clave de clase de dispositivo. A continuación, las propiedades de dispositivo personalizadas se aplican a todos los dispositivos de esa clase. Los dispositivos y controladores de dispositivos siempre deben tener asociados iconos y etiquetas para cumplir los requisitos mínimos de facilidad de uso.

> [!Note]  
> Las propiedades que se definen en el nivel de instancia de dispositivo tienen prioridad sobre las propiedades definidas en el nivel de grupo de dispositivos, que a su vez tienen prioridad sobre las propiedades definidas en el nivel de clase de dispositivo.

 

 

 



