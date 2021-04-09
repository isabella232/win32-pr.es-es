---
description: Con un contexto orientado a la conexión, el autor de la llamada de la función es responsable de dar formato a los mensajes. El autor de la llamada se basa en el paquete de seguridad para autenticar las conexiones y garantizar la integridad de determinadas partes del mensaje.
ms.assetid: 82c6b1aa-304c-47f9-8e0f-ad70a89772aa
title: Contextos de Connection-Oriented
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fb9430cbcfd0536d18cd5cbd965c9f4a71742eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155900"
---
# <a name="connection-oriented-contexts"></a><span data-ttu-id="b9b61-104">Contextos de Connection-Oriented</span><span class="sxs-lookup"><span data-stu-id="b9b61-104">Connection-Oriented Contexts</span></span>

<span data-ttu-id="b9b61-105">Con un [*contexto*](/windows/desktop/SecGloss/c-gly)orientado a la conexión, el autor de la llamada de la función es responsable de dar formato a los mensajes.</span><span class="sxs-lookup"><span data-stu-id="b9b61-105">With a connection-oriented [*context*](/windows/desktop/SecGloss/c-gly), the function's caller is responsible for formatting messages.</span></span> <span data-ttu-id="b9b61-106">El autor de la llamada se basa en el [*paquete de seguridad*](/windows/desktop/SecGloss/s-gly) para autenticar las conexiones y garantizar la integridad de determinadas partes del mensaje.</span><span class="sxs-lookup"><span data-stu-id="b9b61-106">The caller relies on the [*security package*](/windows/desktop/SecGloss/s-gly) to authenticate connections and to ensure the integrity of specific parts of the message.</span></span>

<span data-ttu-id="b9b61-107">La mayoría de las opciones de contexto están disponibles para los contextos orientados a la conexión.</span><span class="sxs-lookup"><span data-stu-id="b9b61-107">Most context options are available to connection-oriented contexts.</span></span> <span data-ttu-id="b9b61-108">Estas opciones incluyen la autenticación mutua, la detección de reproducción y la detección de secuencias, tal como se describe en [requisitos de contexto](context-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b9b61-108">These options include mutual authentication, replay detection, and sequence detection, as described in [Context Requirements](context-requirements.md).</span></span>

<span data-ttu-id="b9b61-109">Un paquete de seguridad establece la \_ marca de conexión de la marca SECPKG \_ para indicar que admite la semántica orientada a la conexión.</span><span class="sxs-lookup"><span data-stu-id="b9b61-109">A security package sets the SECPKG\_FLAG\_CONNECTION flag to indicate that it supports connection-oriented semantics.</span></span>

 

 
