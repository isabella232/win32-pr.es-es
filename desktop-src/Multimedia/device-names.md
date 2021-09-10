---
title: Nombres de dispositivo
description: Nombres de dispositivo
ms.assetid: 0ba06439-cc33-43e1-a094-09bcc5e2f6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e516f7f8eed338067dc373f8509f46598e198c71
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371612"
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



Si un controlador MCI se instala con un nombre de dispositivo que ya existe en SYSTEM.INI o en el Registro, el sistema anexa un entero al nombre del dispositivo del nuevo controlador, creando un nombre de dispositivo único. En el ejemplo anterior, a un controlador adicional instalado con el nombre de dispositivo "cdaudio" se le asignaría el nombre del dispositivo "cdaudio1".

 

 




