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
# <a name="transport-security"></a><span data-ttu-id="ff4a5-103">Seguridad de transporte</span><span class="sxs-lookup"><span data-stu-id="ff4a5-103">Transport Security</span></span>

<span data-ttu-id="ff4a5-104">Aunque este no es el método preferido, puede usar la configuración de seguridad que ofrece el transporte de canalización con nombre para agregar características de seguridad a la aplicación distribuida.</span><span class="sxs-lookup"><span data-stu-id="ff4a5-104">Although this is not the preferred method, you can use the security settings that the named-pipe transport offers to add security features to your distributed application.</span></span> <span data-ttu-id="ff4a5-105">Esta configuración de seguridad se usa con las funciones de Microsoft RPC que comienzan con los prefijos [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) y [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), y con las funciones [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) y [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).</span><span class="sxs-lookup"><span data-stu-id="ff4a5-105">These security settings are used with the Microsoft RPC functions that start with the prefixes [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) and [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), and the functions [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) and [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).</span></span>

> [!Note]  
> <span data-ttu-id="ff4a5-106">Si está ejecutando una aplicación que es un servicio y usa NTLM para la seguridad, debe agregar una dependencia de servicio explícita para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ff4a5-106">If you are running an application that is a service and you are using NTLM for security, you must add an explicit service dependency for your application.</span></span> <span data-ttu-id="ff4a5-107">El Secur32.dll llamará al administrador de control de servicios (SCM) para comenzar el servicio de paquete de seguridad NTLM.</span><span class="sxs-lookup"><span data-stu-id="ff4a5-107">The Secur32.dll will call the Service Control Manager (SCM) to begin the NTLM security package service.</span></span> <span data-ttu-id="ff4a5-108">Sin embargo, una aplicación RPC que es un servicio y que se ejecuta como sistema, también debe ponerse en contacto con el SC, a menos que se esté conectando a otro servicio en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="ff4a5-108">However, an RPC application that is a service and is running as a system, must also contact the SC unless it is connecting to another service on the same computer.</span></span>

 

 

 




