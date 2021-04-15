---
title: Versiones de sistema operativo
description: Este tipo de datos DWORD debe contener el tipo de sistema operativo en la palabra de orden superior y el número de versión del sistema operativo en la palabra de orden inferior. En la tabla siguiente se muestran los valores posibles para el sistema operativo.
ms.assetid: 318e277b-a797-45a5-87c5-25b91fdf278d
keywords:
- Versiones de sistema operativo almacenamiento estructurado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5de916d354a721834b9a10651c36d3bf389e28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665833"
---
# <a name="operating-system-versions"></a>Versiones de sistema operativo

Este tipo de datos **DWORD** debe contener el tipo de sistema operativo en la palabra de orden superior y el número de versión del sistema operativo en la palabra de orden inferior. En la tabla siguiente se muestran los valores posibles para el sistema operativo.



| Sistema operativo       | Value  |
|------------------------|--------|
| Windows de 32 bits (Win32) | 0x0002 |
| Macintosh              | 0x0001 |
| Windows de 16 bits (Win16) | 0x0000 |



 

En el caso de los sistemas operativos Microsoft Windows, la versión del sistema operativo es la palabra de orden inferior devuelta por la función [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion) . En el caso de Microsoft Windows, el código de ejemplo siguiente establece correctamente la versión del sistema operativo de origen.

``` syntax
#ifdef WIN32 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 2 ) ; 
#else 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 0 ) ; 
#endif
```

 

 