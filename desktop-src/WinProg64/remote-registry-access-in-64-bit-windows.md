---
title: Acceso remoto al registro en Windows de 64 bits
description: El redirector del registro proporciona acceso remoto al registro en Windows de 64 bits a través de la función RegConnectRegistry.
ms.assetid: 7873c1e2-53fb-4c93-bf4c-251a13cd8db7
keywords:
- acceso al registro remoto de 64 bits programación de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a139198ca08e0fdb9d7bcb070dcabf89dfa5403
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695608"
---
# <a name="remote-registry-access-in-64-bit-windows"></a><span data-ttu-id="d1904-104">Acceso remoto al registro en Windows de 64 bits</span><span class="sxs-lookup"><span data-stu-id="d1904-104">Remote Registry Access in 64-bit Windows</span></span>

<span data-ttu-id="d1904-105">El redirector del registro proporciona acceso remoto al registro en Windows de 64 bits a través de la función [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) .</span><span class="sxs-lookup"><span data-stu-id="d1904-105">The registry redirector provides remote access to the registry on 64-bit Windows through the [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) function.</span></span>

<span data-ttu-id="d1904-106">Si el cliente es una aplicación de 32 bits, tiene acceso a la vista del registro de 32 bits predeterminada del servidor.</span><span class="sxs-lookup"><span data-stu-id="d1904-106">If the client is a 32-bit application, it accesses the server's default 32-bit registry view.</span></span> <span data-ttu-id="d1904-107">Si el cliente es una aplicación de 64 bits, tiene acceso a la vista del registro de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d1904-107">If the client is a 64-bit application, it accesses the 64-bit registry view.</span></span>

<span data-ttu-id="d1904-108">**Windows Server 2003:** Todos los clientes acceden a la vista del registro de 64 bits a menos que la aplicación use la marca de clave \_ WOW64 \_ 32KEY.</span><span class="sxs-lookup"><span data-stu-id="d1904-108">**Windows Server 2003:** All clients access the 64-bit registry view unless the application uses the KEY\_WOW64\_32KEY flag.</span></span> <span data-ttu-id="d1904-109">Este comportamiento cambió con Windows Server 2003 con Service Pack 1 (SP1) y Windows XP Professional x64 Edition, siempre que tanto el cliente como el servidor ejecuten estas versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="d1904-109">This behavior changed with Windows Server 2003 with Service Pack 1 (SP1) and Windows XP Professional x64 Edition, provided that both the client and the server are running these versions of Windows.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1904-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d1904-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1904-111">Redirector del registro</span><span class="sxs-lookup"><span data-stu-id="d1904-111">Registry Redirector</span></span>](registry-redirector.md)
</dt> <dt>

[<span data-ttu-id="d1904-112">Reflexión del registro</span><span class="sxs-lookup"><span data-stu-id="d1904-112">Registry Reflection</span></span>](registry-reflection.md)
</dt> </dl>

 

 