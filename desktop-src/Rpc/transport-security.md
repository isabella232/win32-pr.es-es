---
title: Seguridad de transporte
description: Aunque este no es el método preferido, puede usar la configuración de seguridad que ofrece el transporte de canalización con nombre para agregar características de seguridad a la aplicación distribuida.
ms.assetid: faf48049-807c-4155-aa01-1947a0311a71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3d92a0c9f0b31392d265c1c60bd201d088af8e8ff0b10ac4e09e274da92d2a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011213"
---
# <a name="transport-security"></a>Seguridad de transporte

Aunque este no es el método preferido, puede usar la configuración de seguridad que ofrece el transporte de canalización con nombre para agregar características de seguridad a la aplicación distribuida. Esta configuración de seguridad se usa con las funciones RPC de Microsoft que comienzan con los prefijos [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) y [**RpcServerUseAllProtseqs,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs)y las funciones [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) y [**RpcRevertToSelf.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself)

> [!Note]  
> Si ejecuta una aplicación que es un servicio y usa NTLM para la seguridad, debe agregar una dependencia de servicio explícita para la aplicación. El Secur32.dll llamará al Administrador de control de servicios (SCM) para iniciar el servicio de paquete de seguridad NTLM. Sin embargo, una aplicación RPC que es un servicio y se ejecuta como un sistema, también debe ponerse en contacto con el SC a menos que se conecte a otro servicio en el mismo equipo.

 

 

 




