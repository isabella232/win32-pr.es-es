---
title: Puntos de conexión
description: Configura una aplicación COM para usar un número de puerto TCP especificado para las comunicaciones DCOM.
ms.assetid: 2a286a13-24b8-418a-b29b-5543a1c56c45
keywords:
- Valor del Registro de puntos de conexión COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0addcd6c09b409629bb4a7157241d57476cafe3
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369728"
---
# <a name="endpoints"></a>Puntos de conexión

Configura una aplicación COM para usar un número de puerto TCP especificado para las comunicaciones DCOM.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      Endpoints = ncacn_ip_tcp,0,port
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor REG MULTI \_ \_ SZ.**

El *valor* de puerto es un número entre 1024 y 65535 que especifica el número de puerto TCP que la aplicación COM usará para las comunicaciones DCOM. Si no especifica esta clave del Registro, los números de puerto para las comunicaciones DCOM se asignan dinámicamente. En la mayoría de los escenarios, es posible que prefiera dejar sin definir esta clave del Registro y permitir que DCOM asigne dinámicamente números de puerto.

 

 




