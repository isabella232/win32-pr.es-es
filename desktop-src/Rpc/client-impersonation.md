---
title: Suplantación de cliente (RPC)
description: La suplantación es útil en un entorno informático distribuido cuando los servidores deben pasar solicitudes de cliente a otros procesos de servidor o al sistema operativo.
ms.assetid: 49d833d8-c61c-4746-91cf-c0753847cd3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d03ad3b4d9e2984708e8b274ab9bc57c3235808b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149516"
---
# <a name="client-impersonation"></a>Suplantación de cliente

La suplantación es útil en un entorno informático distribuido cuando los servidores deben pasar solicitudes de cliente a otros procesos de servidor o al sistema operativo. En este caso, un servidor suplanta el contexto de seguridad del cliente. Otros procesos de servidor pueden administrar la solicitud como si el cliente original lo hubiera hecho.

![el servidor suplanta a un cliente que llama cuando realiza llamadas posteriores en nombre del cliente](images/impr.png)

Por ejemplo, un cliente realiza una solicitud al servidor a. Si el servidor a debe consultar al servidor B para completar la solicitud, el servidor A suplanta el contexto de seguridad del cliente y realiza la solicitud al servidor B en nombre del cliente. El servidor B utiliza el contexto de seguridad del cliente original, en lugar de la identidad de seguridad del servidor a, para determinar si se debe completar la tarea.

El servidor llama a [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) para sobrescribir la seguridad del subproceso de servidor con el contexto de seguridad del cliente. Una vez completada la tarea, el servidor llama a [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself) o [**RpcRevertToSelfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoselfex) para restaurar el contexto de seguridad definido para el subproceso de servidor.

Al enlazar, el cliente puede especificar información de calidad de servicio sobre la seguridad que especifica cómo el servidor puede suplantar al cliente. Por ejemplo, una de las opciones permite que el cliente especifique que el servidor no puede suplantarlo. Para obtener más información, consulte [calidad de servicio](quality-of-service.md).

La capacidad de llamar a otros servidores durante la suplantación del cliente original se denomina *delegación*. Cuando se usa la delegación, un servidor que suplanta a un cliente puede llamar a otro servidor y puede realizar llamadas de red con las credenciales del cliente. Es decir, desde la perspectiva del segundo servidor, las solicitudes procedentes del primer servidor no se distinguen de las solicitudes procedentes del cliente. No todos los proveedores de seguridad admiten la delegación. Microsoft envía solo un proveedor de seguridad que admite la delegación: Kerberos.

La delegación puede ser una funcionalidad peligrosa debido a los privilegios que el cliente proporciona al servidor durante una llamada a procedimiento remoto. Este es el motivo por el que Kerberos permite llamadas con el nivel de suplantación de la delegación solo si se solicita la autenticación mutua. Los administradores de dominio pueden limitar los equipos a los que se realizan llamadas con el nivel de suplantación de delegación para evitar que los clientes que no sean suscritos realicen llamadas a servidores que podrían hacer uso abusivo de sus credenciales.

Existe una excepción a la regla de delegación: llama a con [**ncalrpc**](/windows/desktop/Midl/ncalrpc). Cuando se realizan estas llamadas, el servidor obtiene derechos de delegación, incluso si se especifica un nivel de suplantación de suplantación. Es decir, un servidor puede llamar a otros servidores en nombre del cliente. Esto solo funciona para una llamada remota. Por ejemplo, si el cliente A llama al servidor local LB mediante **ncalrpc** local Server lb puede suplantar y llamar a RB del servidor remoto. RB podrá actuar en nombre del cliente A, pero solo en el equipo remoto en el que se ejecuta RB. No puede hacer otra llamada de red al equipo remoto C a menos que LB especifique un nivel de suplantación de delegado cuando se llama RB.

> [!Note]  
> La *suplantación* representa dos significados superpuestos. El primer significado de la suplantación es el proceso general de actuar en nombre de un cliente. El segundo significado es el nivel de suplantación específico denominado suplantación. El contexto del texto generalmente clarifica el significado.

 

 

 