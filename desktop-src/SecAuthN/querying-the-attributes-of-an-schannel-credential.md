---
description: Proporciona información específica de Schannel sobre una credencial.
ms.assetid: 0c357996-b85a-4231-b258-40b35ab83ae2
title: Consultar los atributos de una credencial Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc63ccc358561dea95cb1273e1367e7fbb39d390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276687"
---
# <a name="querying-the-attributes-of-an-schannel-credential"></a><span data-ttu-id="3b0ba-103">Consultar los atributos de una credencial Schannel</span><span class="sxs-lookup"><span data-stu-id="3b0ba-103">Querying the Attributes of an Schannel Credential</span></span>

<span data-ttu-id="3b0ba-104">La función [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) proporciona información específica de Schannel sobre una credencial.</span><span class="sxs-lookup"><span data-stu-id="3b0ba-104">The [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) function provides Schannel-specific information about a credential.</span></span> <span data-ttu-id="3b0ba-105">Esta información se especifica originalmente cuando se crea la credencial.</span><span class="sxs-lookup"><span data-stu-id="3b0ba-105">This information is originally specified when the credential is created.</span></span> <span data-ttu-id="3b0ba-106">Para obtener más información, consulte [obtención de credenciales de Schannel](obtaining-schannel-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="3b0ba-106">For more information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span> <span data-ttu-id="3b0ba-107">La información que esta función indica es válida para cualquier conexión ([*contextos de seguridad*](../secgloss/s-gly.md)) creada mediante la credencial especificada.</span><span class="sxs-lookup"><span data-stu-id="3b0ba-107">The information reported by this function is valid for any connections ([*security contexts*](../secgloss/s-gly.md)) created by using the specified credential.</span></span>

 

 
