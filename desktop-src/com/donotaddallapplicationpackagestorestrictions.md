---
title: DoNotAddAllApplicationPackagesToRestrictions
description: Determina si RPCSS anexa automáticamente un \_ \_ SID de todos los paquetes de aplicación a las restricciones de com de forma predeterminada.
ms.assetid: 4DC1237E-F3EF-40EA-8E64-57320F0C4CC5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800077c61e01cf0b3f76d5a92f8282c7ecca12e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418428"
---
# <a name="donotaddallapplicationpackagestorestrictions"></a>DoNotAddAllApplicationPackagesToRestrictions

Determina si RPCSS anexa automáticamente un \_ \_ SID de todos los paquetes de aplicación a las restricciones de com de forma predeterminada.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DoNotAddAllApplicationPackagesToRestrictions = value
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **Registro \_ DWORD** .



| Value | Descripción                                                                               |
|-------|-------------------------------------------------------------------------------------------|
| 0     | Deshabilita las aplicaciones de la tienda Windows tras la migración de Windows 7 a Windows 8.                   |
| 1     | No agrega el SID todos \_ los \_ paquetes de aplicación a las restricciones com. Este es el valor predeterminado. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer la seguridad de las aplicaciones COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




