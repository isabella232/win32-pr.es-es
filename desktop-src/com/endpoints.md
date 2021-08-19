---
title: Puntos de conexión
description: Configura una aplicación COM para usar un número de puerto TCP especificado para las comunicaciones DCOM.
ms.assetid: 2a286a13-24b8-418a-b29b-5543a1c56c45
keywords:
- Valor del Registro de puntos de conexión COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ee2444be55aaf32c028792100e3e6f0ed6989509b7c0af02c5d83bd739fa27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048323"
---
# <a name="endpoints"></a>Puntos de conexión

Configura una aplicación COM para usar un número de puerto TCP especificado para las comunicaciones DCOM.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      Endpoints = ncacn_ip_tcp,0,port
```

## <a name="remarks"></a>Comentarios

Se trata de **un valor REG MULTI \_ \_ SZ.**

El *valor* de puerto es un número entre 1024 y 65535 que especifica el número de puerto TCP que la aplicación COM usará para las comunicaciones DCOM. Si no especifica esta clave del Registro, los números de puerto para las comunicaciones DCOM se asignan dinámicamente. En la mayoría de los escenarios, es posible que prefiera dejar sin definir esta clave del Registro y permitir que DCOM asigne dinámicamente números de puerto.

 

 




