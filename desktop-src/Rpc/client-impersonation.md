---
title: Suplantación de cliente (RPC)
description: La suplantación es útil en un entorno informático distribuido cuando los servidores deben pasar solicitudes de cliente a otros procesos de servidor o al sistema operativo.
ms.assetid: 49d833d8-c61c-4746-91cf-c0753847cd3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73061a35c61a22a4d238e902c3dcb298e3ac0affaf4b0929c83311145a684f1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022834"
---
# <a name="client-impersonation"></a>Suplantación de cliente

La suplantación es útil en un entorno informático distribuido cuando los servidores deben pasar solicitudes de cliente a otros procesos de servidor o al sistema operativo. En este caso, un servidor suplanta el contexto de seguridad del cliente. A continuación, otros procesos de servidor pueden controlar la solicitud como si el cliente original la hubiera realizado.

![el servidor suplanta a un cliente que realiza la llamada al realizar llamadas posteriores en nombre del cliente.](images/impr.png)

Por ejemplo, un cliente realiza una solicitud al servidor A. Si el Servidor A debe consultar el Servidor B para completar la solicitud, el Servidor A suplanta el contexto de seguridad del cliente y realiza la solicitud al servidor B en nombre del cliente. El servidor B usa el contexto de seguridad del cliente original, en lugar de la identidad de seguridad del servidor A, para determinar si se debe completar la tarea.

El servidor llama a [**RpcImpersonateClient para**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) sobrescribir la seguridad del subproceso de servidor con el contexto de seguridad del cliente. Una vez completada la tarea, el servidor llama a [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself) o [**RpcRevertToSelfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoselfex) para restaurar el contexto de seguridad definido para el subproceso del servidor.

Al enlazar, el cliente puede especificar información de calidad de servicio sobre la seguridad, que especifica cómo el servidor puede suplantar al cliente. Por ejemplo, una de las opciones permite al cliente especificar que el servidor no puede suplantarlo. Para obtener más información, vea [Calidad de servicio.](quality-of-service.md)

La capacidad de llamar a otros servidores mientras suplanta el cliente original se denomina *delegación*. Cuando se usa la delegación, un servidor que suplanta a un cliente puede llamar a otro servidor y puede realizar llamadas de red con las credenciales del cliente. Es decir, desde la perspectiva del segundo servidor, las solicitudes procedentes del primer servidor son indistinguibles de las solicitudes procedentes del cliente. No todos los proveedores de seguridad admiten la delegación. Microsoft solo envía un proveedor de seguridad que admite la delegación: Kerberos.

La delegación puede ser una funcionalidad peligrosa debido a los privilegios que el cliente proporciona al servidor durante una llamada a procedimiento remoto. Este es el motivo por el que Kerberos permite llamadas con el nivel de suplantación de delegación solo si se solicita la autenticación mutua. Los administradores de dominio pueden limitar los equipos a los que se realizan llamadas con el nivel de suplantación de delegación para evitar que los clientes nospeccionados puedan realizar llamadas a servidores que podrían utilizar sus credenciales.

Existe una excepción a la regla de delegación: llamadas que [**usan ncalrpc**](/windows/desktop/Midl/ncalrpc). Cuando se realizan estas llamadas, el servidor obtiene derechos de delegación, incluso si se especifica un nivel de suplantación de suplantación. Es decir, un servidor puede llamar a otros servidores en nombre del cliente. Esto solo funciona para una llamada remota. Por ejemplo, si el cliente A llama al servidor local LB mediante **ncalrpc** local server LB puede suplantar y llamar a RB del servidor remoto. RB podrá actuar en nombre del cliente A, pero solo en el equipo remoto en el que se ejecuta RB. No puede realizar otra llamada de red al equipo remoto C a menos que LB especifique un nivel de suplantación de delegado cuando llamó a RB.

> [!Note]  
> El término *suplantación representa* dos significados superpuestos. El primer significado de la suplantación es el proceso general de actuar en nombre de un cliente. El segundo significado es el nivel de suplantación específico denominado suplantación. El contexto del texto suele aclarar el significado.

 

 

 