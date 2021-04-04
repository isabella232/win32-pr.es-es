---
title: Publicar con el servicio de nombres de RPC
description: Los servicios RPC pueden publicar sus identificadores en un espacio de nombres mediante las API del servicio de nombres de RPC (RpcNs).
ms.assetid: 0c8e1207-daeb-4dc8-b83a-a54cd59a46a7
ms.tgt_platform: multiple
keywords:
- Publicar con el servicio de nombres de RPC AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b672eec6308d709fe2f4cbc64ad22ecf0d6edd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077504"
---
# <a name="publishing-with-the-rpc-name-service"></a><span data-ttu-id="6d63a-104">Publicar con el servicio de nombres de RPC</span><span class="sxs-lookup"><span data-stu-id="6d63a-104">Publishing with the RPC Name Service</span></span>

<span data-ttu-id="6d63a-105">Los servicios RPC pueden publicar sus identificadores en un espacio de nombres mediante las API del servicio de nombres de RPC (RpcNs).</span><span class="sxs-lookup"><span data-stu-id="6d63a-105">RPC services can publish their identifiers in a namespace using the RPC name service (RpcNs) APIs.</span></span> <span data-ttu-id="6d63a-106">Las API de RpcNs en Windows 2000 publican las entradas RPC en Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="6d63a-106">The RpcNs APIs in Windows 2000 publish the RPC entries in Active Directory Domain Services.</span></span> <span data-ttu-id="6d63a-107">Los servicios crean enlaces RPC y los publican en el espacio de nombres según las entradas de servidor RPC con atributos, incluido el identificador de interfaz único, un GUID que los clientes reconocen.</span><span class="sxs-lookup"><span data-stu-id="6d63a-107">Services create RPC bindings and publish them in the namespace as named RPC Server entries with attributes including the unique interface ID, a GUID that is recognized by clients.</span></span> <span data-ttu-id="6d63a-108">Después, un cliente puede buscar los servidores RPC que ofrecen la interfaz deseada, importar el enlace y conectarse al servidor.</span><span class="sxs-lookup"><span data-stu-id="6d63a-108">A client can then search for RPC Servers offering the desired interface, import the binding, and connect to the server.</span></span>

<span data-ttu-id="6d63a-109">Para obtener más información acerca de cómo publicar un servicio RPC, consulte [enlace del lado servidor](/windows/desktop/Rpc/server-side-binding).</span><span class="sxs-lookup"><span data-stu-id="6d63a-109">For more information about publishing an RPC service, see [Server-side Binding](/windows/desktop/Rpc/server-side-binding).</span></span>

 

 