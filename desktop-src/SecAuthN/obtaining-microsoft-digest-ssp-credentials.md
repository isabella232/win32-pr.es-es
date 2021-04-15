---
description: Microsoft Digest requiere credenciales de usuario; tanto el cliente como el servidor deben presentar credenciales válidas para poder establecer un contexto de seguridad para el intercambio de mensajes. Los identificadores de credenciales se usan para obtener y presentar credenciales.
ms.assetid: f97bdaf6-40a8-414e-a561-d3cb953d0bab
title: Obtención de credenciales de Microsoft Digest SSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61895ecc8e49713665af4542689729bc491d9e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497285"
---
# <a name="obtaining-microsoft-digest-ssp-credentials"></a><span data-ttu-id="e0f28-104">Obtención de credenciales de Microsoft Digest SSP</span><span class="sxs-lookup"><span data-stu-id="e0f28-104">Obtaining Microsoft Digest SSP Credentials</span></span>

<span data-ttu-id="e0f28-105">Microsoft Digest requiere [*credenciales*](../secgloss/c-gly.md) de usuario; tanto el cliente como el servidor deben presentar credenciales válidas para poder establecer un [*contexto de seguridad*](../secgloss/s-gly.md) para el intercambio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e0f28-105">User [*credentials*](../secgloss/c-gly.md) are required by Microsoft Digest; both client and server must present valid credentials before they can establish a [*security context*](../secgloss/s-gly.md) for message exchange.</span></span> <span data-ttu-id="e0f28-106">Los identificadores de credenciales se usan para obtener y presentar credenciales.</span><span class="sxs-lookup"><span data-stu-id="e0f28-106">Credentials handles are used to obtain and present credentials.</span></span>

<span data-ttu-id="e0f28-107">Dado que el identificador de credenciales se usa para almacenar información de configuración, no se puede usar el mismo identificador para las operaciones del lado cliente y del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="e0f28-107">Because the credential handle is used to store configuration information, the same handle cannot be used for both client-side and server-side operations.</span></span> <span data-ttu-id="e0f28-108">Esto significa que las aplicaciones que admiten conexiones de cliente y de servidor deben obtener un mínimo de dos identificadores de credenciales.</span><span class="sxs-lookup"><span data-stu-id="e0f28-108">This means that applications that support both client and server connections must obtain a minimum of two credentials handles.</span></span>

<span data-ttu-id="e0f28-109">Para obtener un identificador de las credenciales requeridas por Microsoft Digest, llame a la función [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) .</span><span class="sxs-lookup"><span data-stu-id="e0f28-109">To get a handle to the credentials required by Microsoft Digest, call the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function.</span></span>

<span data-ttu-id="e0f28-110">En los siguientes ejemplos del lenguaje C se muestra cómo obtener las credenciales.</span><span class="sxs-lookup"><span data-stu-id="e0f28-110">The following C language examples demonstrate obtaining credentials.</span></span>

-   [<span data-ttu-id="e0f28-111">Obtención de credenciales de Resumen predeterminadas</span><span class="sxs-lookup"><span data-stu-id="e0f28-111">Obtaining Default Digest Credentials</span></span>](obtaining-default-digest-credentials.md)
-   [<span data-ttu-id="e0f28-112">Obtención de credenciales de Resumen alternativas</span><span class="sxs-lookup"><span data-stu-id="e0f28-112">Obtaining Alternate Digest Credentials</span></span>](obtaining-alternate-digest-credentials.md)

 

 
