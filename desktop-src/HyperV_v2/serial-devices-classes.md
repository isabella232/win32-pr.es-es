---
description: Los dispositivos serie de una máquina virtual constan de controladores serie y puertos serie. Cada máquina virtual tiene exactamente un controlador serie y cada controlador serie tiene exactamente dos puertos serie.
ms.assetid: BA24BD74-D80C-4C5C-891F-5F17CDED2EC6
title: Clases de dispositivos serie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b1b95a2baaf4bc3dacfddf0e18f6acd88379f958e49fc1ccbd5d6ee5cf49a11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746115"
---
# <a name="serial-devices-classes"></a>Clases de dispositivos serie

Los dispositivos serie de una máquina virtual constan de controladores serie y puertos serie. Cada máquina virtual tiene exactamente un controlador serie y cada controlador serie tiene exactamente dos puertos serie.

La configuración del controlador serie no es configurable; por lo tanto, no hay ninguna instancia de datos de configuración asociada a ella. Además, no puede agregar ni quitar controladores serie ni puertos serie de una máquina virtual. Por lo tanto, no hay instancias de grupo de recursos para dispositivos serie.

Las siguientes son clases WMI de virtualización relacionadas con dispositivos serie.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                      | Descripción                                                                     |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**Msvm \_ SerialController**](msvm-serialcontroller.md)<br/>                         | Representa las funcionalidades y la administración del controlador serie.<br/> |
| [**Msvm \_ SerialPort**](msvm-serialport.md)<br/>                                     | Representa un puerto serie asociado al controlador serie.<br/>      |
| [**Msvm \_ SerialPortOnSerialController**](msvm-serialportonserialcontroller.md)<br/> | Asocia un puerto serie a un controlador serie.<br/>                   |



 

 

 




