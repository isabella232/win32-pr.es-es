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
# <a name="endpoints"></a><span data-ttu-id="74bfa-104">Puntos de conexión</span><span class="sxs-lookup"><span data-stu-id="74bfa-104">Endpoints</span></span>

<span data-ttu-id="74bfa-105">Configura una aplicación COM para que use un número de puerto TCP especificado para las comunicaciones DCOM.</span><span class="sxs-lookup"><span data-stu-id="74bfa-105">Configures a COM application to use a specified TCP port number for DCOM communications.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="74bfa-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="74bfa-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      Endpoints = ncacn_ip_tcp,0,port
```

## <a name="remarks"></a><span data-ttu-id="74bfa-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74bfa-107">Remarks</span></span>

<span data-ttu-id="74bfa-108">Se trata de un valor de **reg \_ multi \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="74bfa-108">This is a **REG\_MULTI\_SZ** value.</span></span>

<span data-ttu-id="74bfa-109">El valor de *Puerto* es un número entre 1024 y 65535 que especifica el número de puerto TCP que utilizará la aplicación com para las comunicaciones DCOM.</span><span class="sxs-lookup"><span data-stu-id="74bfa-109">The *port* value is a number between 1024 and 65535 that specifies the TCP port number that your COM application will use for DCOM communications.</span></span> <span data-ttu-id="74bfa-110">Si no especifica esta clave del registro, los números de puerto para las comunicaciones DCOM se asignan dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="74bfa-110">If you do not specify this registry key, port numbers for DCOM communications are dynamically assigned.</span></span> <span data-ttu-id="74bfa-111">En la mayoría de los escenarios, es posible que prefiera dejar esta clave del registro sin definir y permitir que DCOM asigne números de Puerto dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="74bfa-111">In most scenarios, you might prefer to leave this registry key undefined and allow DCOM to dynamically assign port numbers.</span></span>

 

 




