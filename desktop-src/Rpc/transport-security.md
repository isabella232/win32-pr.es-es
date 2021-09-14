---
title: Seguridad de transporte
description: Aunque este no es el método preferido, puede usar la configuración de seguridad que ofrece el transporte de canalización con nombre para agregar características de seguridad a la aplicación distribuida.
ms.assetid: faf48049-807c-4155-aa01-1947a0311a71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d129b5a373ed7304c142c66dd0e8b2d4e9035416
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071404"
---
# <a name="transport-security"></a>Seguridad de transporte

Aunque este no es el método preferido, puede usar la configuración de seguridad que ofrece el transporte de canalización con nombre para agregar características de seguridad a la aplicación distribuida. Esta configuración de seguridad se usa con las funciones RPC de Microsoft que comienzan con los prefijos [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) y [**RpcServerUseAllProtseqs,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)y las funciones [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) y [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).

> [!Note]  
> Si ejecuta una aplicación que es un servicio y usa NTLM para la seguridad, debe agregar una dependencia de servicio explícita para la aplicación. El Secur32.dll llamará al Administrador de control de servicios (SCM) para iniciar el servicio de paquetes de seguridad NTLM. Sin embargo, una aplicación RPC que es un servicio y se ejecuta como un sistema, también debe ponerse en contacto con el SC a menos que se conecte a otro servicio en el mismo equipo.

 

 

 




