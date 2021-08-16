---
title: DoNotAddAllApplicationPackagesToRestrictions
description: Determina si RPCSS anexa automáticamente un SID DE TODOS LOS PAQUETES DE APLICACIONES a \_ \_ las restricciones COM de forma predeterminada.
ms.assetid: 4DC1237E-F3EF-40EA-8E64-57320F0C4CC5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1608d49d7e5bebc977ace8e59e4b31c5b13da8ab4f743e89095b9f31632453c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737011"
---
# <a name="donotaddallapplicationpackagestorestrictions"></a>DoNotAddAllApplicationPackagesToRestrictions

Determina si RPCSS anexa automáticamente un SID DE TODOS LOS PAQUETES DE APLICACIONES a \_ \_ las restricciones COM de forma predeterminada.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DoNotAddAllApplicationPackagesToRestrictions = value
```

## <a name="remarks"></a>Comentarios

Se trata de **un valor \_ REG DWORD.**



| Valor | Descripción                                                                               |
|-------|-------------------------------------------------------------------------------------------|
| 0     | Deshabilita las Windows store tras la migración de Windows 7 a Windows 8.                   |
| 1     | No agrega el SID DE \_ TODOS LOS \_ PAQUETES DE APLICACIONES a las restricciones COM. Este es el valor predeterminado. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la seguridad para aplicaciones COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




