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
# <a name="serial-devices-classes"></a>Clases de dispositivos serie

Los dispositivos serie de una máquina virtual se componen de controladores serie y puertos serie. Cada máquina virtual tiene exactamente un controlador serie y cada controlador serie tiene exactamente dos puertos serie.

La configuración del controlador serie no es configurable. por lo tanto, no hay ninguna instancia de datos de configuración asociada. Además, no puede agregar ni quitar controladores serie o puertos serie de una máquina virtual. Por lo tanto, no hay instancias del grupo de recursos para dispositivos serie.

A continuación se enumeran las clases WMI de virtualización relacionadas con los dispositivos serie.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                      | Descripción                                                                     |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**MSVM \_ SerialController**](msvm-serialcontroller.md)<br/>                         | Representa las capacidades y la administración del controlador serie.<br/> |
| [**MSVM \_ SerialPort**](msvm-serialport.md)<br/>                                     | Representa un puerto serie asociado al controlador serie.<br/>      |
| [**MSVM \_ SerialPortOnSerialController**](msvm-serialportonserialcontroller.md)<br/> | Asocia un puerto serie a un controlador serie.<br/>                   |



 

 

 




