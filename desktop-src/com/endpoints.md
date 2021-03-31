---
title: Puntos de conexión
description: Configura una aplicación COM para que use un número de puerto TCP especificado para las comunicaciones DCOM.
ms.assetid: 2a286a13-24b8-418a-b29b-5543a1c56c45
keywords:
- Valor del registro de puntos de conexión COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0addcd6c09b409629bb4a7157241d57476cafe3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418545"
---
# <a name="endpoints"></a>Puntos de conexión

Configura una aplicación COM para que use un número de puerto TCP especificado para las comunicaciones DCOM.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      Endpoints = ncacn_ip_tcp,0,port
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **reg \_ multi \_ SZ** .

El valor de *Puerto* es un número entre 1024 y 65535 que especifica el número de puerto TCP que utilizará la aplicación com para las comunicaciones DCOM. Si no especifica esta clave del registro, los números de puerto para las comunicaciones DCOM se asignan dinámicamente. En la mayoría de los escenarios, es posible que prefiera dejar esta clave del registro sin definir y permitir que DCOM asigne números de Puerto dinámicamente.

 

 




