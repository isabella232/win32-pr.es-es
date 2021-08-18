---
title: Nombres de dispositivo
description: Nombres de dispositivo
ms.assetid: 0ba06439-cc33-43e1-a094-09bcc5e2f6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85183a1b23817352ba9e45e8dbb2aaa70493430cd092f357e1eaa8e9bf179d65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497275"
---
# <a name="device-names"></a>Nombres de dispositivo

Para cada tipo de dispositivo, puede haber varios controladores MCI que compartan el conjunto de comandos, pero que funcionen en diferentes formatos de datos. Para identificar de forma única un controlador MCI, MCI usa nombres *de dispositivo*.

Los nombres de dispositivo se identifican en la sección mci del archivo \[ SYSTEM.INI o en la parte adecuada del \] registro. Esta información identifica todos los controladores de MCI que se Windows. Las entradas de la \[ sección mci \] usan el formato siguiente:

*device \_ name driver*  =  *\_ filename.extension*

En el ejemplo siguiente se muestra una \[ sección mci \] típica de SYSTEM.INI:


```C++
[mci]
cdaudio=mcicda.drv 
sequencer=mciseq.drv 
waveaudio=mciwave.drv 
avivideo=mciavi.drv
```



Si un controlador MCI se instala con un nombre de dispositivo que ya existe en SYSTEM.INI o el Registro, el sistema anexa un entero al nombre del dispositivo del nuevo controlador, creando un nombre de dispositivo único. En el ejemplo anterior, a un controlador adicional instalado con el nombre de dispositivo "cdaudio" se le asignaría el nombre del dispositivo "cdaudio1".

 

 




