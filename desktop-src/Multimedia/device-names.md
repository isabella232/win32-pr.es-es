---
title: Nombres de dispositivo
description: Nombres de dispositivo
ms.assetid: 0ba06439-cc33-43e1-a094-09bcc5e2f6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e516f7f8eed338067dc373f8509f46598e198c71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487046"
---
# <a name="device-names"></a>Nombres de dispositivo

Para cada tipo de dispositivo, puede haber varios controladores MCI que compartan el conjunto de comandos pero operen en formatos de datos diferentes. Para identificar de forma única un controlador MCI, MCI usa *nombres de dispositivo*.

Los nombres de los dispositivos se identifican en la \[ \] sección MCI del archivo SYSTEM.INI o en la parte adecuada del registro. Esta información identifica todos los controladores MCI en Windows. Las entradas de la \[ \] sección MCI usan el formato siguiente:

*nombre del dispositivo \_ nombre* de  =  *\_ archivo. extensión*

En el ejemplo siguiente se muestra \[ una \] sección típica de mci de SYSTEM.INI:


```C++
[mci]
cdaudio=mcicda.drv 
sequencer=mciseq.drv 
waveaudio=mciwave.drv 
avivideo=mciavi.drv
```



Si se instala un controlador MCI con un nombre de dispositivo que ya existe en SYSTEM.INI o en el registro, el sistema anexa un entero al nombre de dispositivo del nuevo controlador y crea un nombre de dispositivo único. En el ejemplo anterior, se asignaría el nombre de dispositivo "cdaudio1" a un controlador adicional instalado con el nombre de dispositivo "cdaudio".

 

 




