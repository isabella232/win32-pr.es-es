---
title: Seguridad del cliente durante una llamada asincrónica
description: Seguridad del cliente durante una llamada asincrónica
ms.assetid: 26d1f2c2-cb08-49f1-8beb-b99b029f0d8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bea2f83bf6341704dd0265a37ec2f64b79e9b2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778474"
---
# <a name="client-security-during-an-asynchronous-call"></a><span data-ttu-id="69b6b-103">Seguridad del cliente durante una llamada asincrónica</span><span class="sxs-lookup"><span data-stu-id="69b6b-103">Client Security During an Asynchronous Call</span></span>

<span data-ttu-id="69b6b-104">El administrador proxy creado por MIDL para los objetos que usan el cálculo de referencias estándar implementa la interfaz [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) .</span><span class="sxs-lookup"><span data-stu-id="69b6b-104">The proxy manager created by MIDL for objects that use standard marshaling implements the [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) interface.</span></span> <span data-ttu-id="69b6b-105">Los clientes pueden administrar la seguridad de las llamadas de serialización consultando **IClientSecurity** en el objeto de llamada y obteniendo o cambiando la configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="69b6b-105">Clients can manage the security of marshaled calls by querying for **IClientSecurity** on the call object and obtaining or changing security settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69b6b-106">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="69b6b-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69b6b-107">Realización de una llamada asincrónica</span><span class="sxs-lookup"><span data-stu-id="69b6b-107">Making an Asynchronous Call</span></span>](making-an-asynchronous-call.md)
</dt> </dl>

 

 




