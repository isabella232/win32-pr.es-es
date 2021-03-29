---
description: Tiempo de espera de la unidad de DVD
ms.assetid: 2295253d-0199-41b4-95a8-cda049ca93c7
title: Tiempo de espera de la unidad de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acda6853830ee7289e529d029c78fe4e56e4a0e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906761"
---
# <a name="dvd-drive-spin-down-timeout"></a>Tiempo de espera de la unidad de DVD

En equipos portátiles, para conservar la duración de la batería, puede ser deseable reducir el tiempo que una unidad de DVD seguirá girando después de que el usuario haya pausado la reproducción. De forma predeterminada, el navegador de DVD mantiene el disco girando durante dos minutos. Este valor se puede modificar en el registro de Windows con esta clave:


```C++
DWORD HKLM\SOFTWARE\Microsoft\DVDNavigator\DriveSpindown 
[Sec]
```



where


```
Sec
```



es el tiempo de espera en segundos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Apéndices](appendixes.md)
</dt> </dl>

 

 



