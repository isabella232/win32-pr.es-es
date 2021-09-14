---
title: Registro de la interfaz
description: El registro de la interfaz que admite un programa de servidor permite enviar llamadas a procedimientos remotos desde programas cliente a la rutina de servidor adecuada.
ms.assetid: 953185a7-00e6-442d-b474-a983f4a91c38
keywords:
- Llamada a procedimiento remoto RPC, tareas, registro de la interfaz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34a12de37b39c719de246ceb79a92d6a51fc361
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361901"
---
# <a name="registering-the-interface"></a>Registro de la interfaz

El registro de la interfaz que admite un programa de servidor permite enviar llamadas a procedimientos remotos desde programas cliente a la rutina de servidor adecuada. Los programas de servidor [**llaman a RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) para registrar sus interfaces. El fragmento de código siguiente muestra su uso:


```C++
RPC_STATUS status;
status = RpcServerRegisterIf(MyInterface_v1_0_s_ifspec, NULL, NULL);
```



El primer parámetro de la [**función RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) es una estructura que el compilador MIDL genera a partir del archivo IDL que define la interfaz (o interfaces) del servidor. El segundo y tercer parámetro son un UUID y un vector de punto de entrada, respectivamente. En este ejemplo, se establecen en **NULL.** En muchos casos, el programa de servidor establecerá estos valores de parámetro en **NULL.** Los programas de servidor usan el segundo y tercer parámetro cuando proporcionan varias implementaciones de los mismos procedimientos en una interfaz. Para obtener más información, vea [Vectores de punto de entrada](registering-interfaces.md).

Los programas de servidor también [**pueden usar RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) para registrar una interfaz. Una ventaja de usar esta función es que proporciona a la aplicación la capacidad de establecer una función de devolución de llamada de seguridad. El uso de funciones de devolución de llamada de seguridad es el enfoque recomendado para proteger una interfaz.

> [!Note]  
> MIDL genera dos estructuras muy similares, una para el cliente y otra para el servidor. La estructura que se pasa a [**la función RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) es la versión del servidor de la estructura producida por MIDL.

 

 

 




