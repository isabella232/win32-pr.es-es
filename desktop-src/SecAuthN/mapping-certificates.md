---
description: Asignación de certificados
ms.assetid: 4139f927-54f4-4968-a9eb-020401bb536d
title: Asignación de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a9ef8822d4f191ae37cdb998166fa54c2b12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816035"
---
# <a name="mapping-certificates"></a><span data-ttu-id="d826f-103">Asignación de certificados</span><span class="sxs-lookup"><span data-stu-id="d826f-103">Mapping Certificates</span></span>

> [!Note]  
> <span data-ttu-id="d826f-104">La información de este tema solo es válida para los servidores que requieren autenticación del cliente.</span><span class="sxs-lookup"><span data-stu-id="d826f-104">The information in this topic is valid only for servers that require client authentication.</span></span>

 

<span data-ttu-id="d826f-105">Si una aplicación de servidor requiere autenticación de cliente, SChannel intenta asignar automáticamente el certificado que el cliente ha suministrado a una cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="d826f-105">When a server application requires client authentication, Schannel automatically attempts to map the certificate supplied by the client to a user account.</span></span>

<span data-ttu-id="d826f-106">Una vez establecido el [*contexto de seguridad*](../secgloss/s-gly.md) , la aplicación de servidor puede usar la función [**QuerySecurityContextToken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) para obtener un [*token de acceso*](../secgloss/a-gly.md) para la cuenta de usuario a la que se asignó el certificado de [*cliente*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d826f-106">After the [*security context*](../secgloss/s-gly.md) has been established, the server application can use the [**QuerySecurityContextToken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) function to obtain an [*access token*](../secgloss/a-gly.md) for the user account to which the [*client certificate*](../secgloss/c-gly.md) was mapped.</span></span> <span data-ttu-id="d826f-107">Además, el servidor puede usar la función [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) para suplantar al cliente.</span><span class="sxs-lookup"><span data-stu-id="d826f-107">Also, the server can use the [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) function to impersonate the client.</span></span>

<span data-ttu-id="d826f-108">Para obtener más información sobre la autenticación, vea [realizar la autenticación con Schannel](performing-authentication-using-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="d826f-108">For more information on authentication, see [Performing Authentication Using Schannel](performing-authentication-using-schannel.md).</span></span>

 

 
