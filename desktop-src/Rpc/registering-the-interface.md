---
title: Registro de la interfaz
description: El registro de la interfaz que admite un programa de servidor permite que las llamadas a procedimientos remotos de los programas cliente se envíen a la rutina de servidor adecuada.
ms.assetid: 953185a7-00e6-442d-b474-a983f4a91c38
keywords:
- Procedimiento remoto Llamar a RPC , tareas, registrar la interfaz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c444a82d30848f4f01643c08f17f484d027bc7b8c8efe3f10e7f3c194aac26a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926883"
---
# <a name="registering-the-interface"></a>Registro de la interfaz

El registro de la interfaz que admite un programa de servidor permite que las llamadas a procedimientos remotos de los programas cliente se envíen a la rutina de servidor adecuada. Los programas de servidor [**llaman a RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) para registrar sus interfaces. El fragmento de código siguiente muestra su uso:


```C++
RPC_STATUS status;
status = RpcServerRegisterIf(MyInterface_v1_0_s_ifspec, NULL, NULL);
```



El primer parámetro de la [**función RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) es una estructura que el compilador MIDL genera a partir del archivo IDL que define la interfaz (o interfaces) del servidor. El segundo y tercer parámetro son un UUID y un vector de punto de entrada, respectivamente. Se establecen en **NULL en** este ejemplo. En muchos casos, el programa de servidor establecerá estos valores de parámetro en **NULL.** Los programas de servidor usan el segundo y tercer parámetro cuando proporcionan varias implementaciones de los mismos procedimientos en una interfaz. Para obtener más información, vea [Vectores de punto de entrada](registering-interfaces.md).

Los programas de servidor también [**pueden usar RpcServerRegisterIfEx para**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) registrar una interfaz. Una ventaja de usar esta función es que proporciona a la aplicación la capacidad de establecer una función de devolución de llamada de seguridad. El uso de funciones de devolución de llamada de seguridad es el enfoque recomendado para proteger una interfaz.

> [!Note]  
> MIDL genera dos estructuras muy similares, una para el cliente y otra para el servidor. La estructura que se pasa a [**la función RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) es la versión de servidor de la estructura producida por MIDL.

 

 

 




