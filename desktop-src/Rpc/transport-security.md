---
title: Seguridad de transporte
description: Aunque este no es el método preferido, puede usar la configuración de seguridad que ofrece el transporte de canalización con nombre para agregar características de seguridad a la aplicación distribuida.
ms.assetid: faf48049-807c-4155-aa01-1947a0311a71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d129b5a373ed7304c142c66dd0e8b2d4e9035416
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357472"
---
# <a name="transport-security"></a>Seguridad de transporte

Aunque este no es el método preferido, puede usar la configuración de seguridad que ofrece el transporte de canalización con nombre para agregar características de seguridad a la aplicación distribuida. Esta configuración de seguridad se usa con las funciones de Microsoft RPC que comienzan con los prefijos [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) y [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), y con las funciones [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) y [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).

> [!Note]  
> Si está ejecutando una aplicación que es un servicio y usa NTLM para la seguridad, debe agregar una dependencia de servicio explícita para la aplicación. El Secur32.dll llamará al administrador de control de servicios (SCM) para comenzar el servicio de paquete de seguridad NTLM. Sin embargo, una aplicación RPC que es un servicio y que se ejecuta como sistema, también debe ponerse en contacto con el SC, a menos que se esté conectando a otro servicio en el mismo equipo.

 

 

 




