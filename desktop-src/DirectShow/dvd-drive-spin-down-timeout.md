---
description: Tiempo de espera de la desactividad de la unidad de DVD
ms.assetid: 2295253d-0199-41b4-95a8-cda049ca93c7
title: Tiempo de espera de la desactividad de la unidad de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6283f0846ac374ee9f059b6ac712209ceb0a925b904fcb941b5cf14f0e36d96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051885"
---
# <a name="dvd-drive-spin-down-timeout"></a>Tiempo de espera de la desactividad de la unidad de DVD

En equipos portátiles, para conservar la duración de la batería, puede ser conveniente reducir el tiempo que una unidad de DVD seguirá girando después de que el usuario haya pausado la reproducción. De forma predeterminada, el navegador de DVD mantiene el disco girando durante dos minutos. Este valor se puede modificar en el registro Windows bajo esta clave:


```C++
DWORD HKLM\SOFTWARE\Microsoft\DVDNavigator\DriveSpindown 
[Sec]
```



where


```
Sec
```



es el tiempo de giro en segundos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Apéndices](appendixes.md)
</dt> </dl>

 

 



