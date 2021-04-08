---
description: El proceso de autenticación de Schannel requiere credenciales. tanto el cliente como el servidor deben obtener credenciales válidas para establecer un contexto de seguridad para el intercambio de mensajes. Para obtener un ejemplo en el que se muestra este procedimiento, vea obtener credenciales.
ms.assetid: ee4a9908-7ba8-4701-84a4-c50b6b989e82
title: Obtención de credenciales de Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e5a5b82b3ed76e905c967009da52d17bff0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813606"
---
# <a name="obtaining-schannel-credentials"></a><span data-ttu-id="24ddd-104">Obtención de credenciales de Schannel</span><span class="sxs-lookup"><span data-stu-id="24ddd-104">Obtaining Schannel Credentials</span></span>

<span data-ttu-id="24ddd-105">El proceso de autenticación de Schannel requiere credenciales. tanto el cliente como el servidor deben obtener credenciales válidas para establecer un [*contexto de seguridad*](../secgloss/s-gly.md) para el intercambio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="24ddd-105">Credentials are required by the Schannel authentication process; both client and server must obtain valid credentials to establish a [*security context*](../secgloss/s-gly.md) for message exchange.</span></span> <span data-ttu-id="24ddd-106">Para obtener un ejemplo en el que se muestra este procedimiento, vea [obtener credenciales](getting-a-certificate-for-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="24ddd-106">For an example that demonstrates this procedure, see [Getting credentials](getting-a-certificate-for-schannel.md).</span></span>

<span data-ttu-id="24ddd-107">La aplicación obtiene las credenciales mediante una llamada a la función [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) , que devuelve un identificador a las credenciales solicitadas.</span><span class="sxs-lookup"><span data-stu-id="24ddd-107">Your application obtains credentials by calling the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function, which returns a handle to the requested credentials.</span></span> <span data-ttu-id="24ddd-108">Dado que los identificadores de credenciales se usan para almacenar información de configuración, no se puede usar el mismo identificador para las operaciones del lado cliente y del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="24ddd-108">Because credentials handles are used to store configuration information, the same handle cannot be used for both client-side and server-side operations.</span></span> <span data-ttu-id="24ddd-109">Esto significa que las aplicaciones que admiten conexiones de cliente y de servidor deben obtener un mínimo de dos identificadores de credenciales.</span><span class="sxs-lookup"><span data-stu-id="24ddd-109">This means that applications that support both client and server connections must obtain a minimum of two credentials handles.</span></span>

<span data-ttu-id="24ddd-110">En Windows XP, una estructura de [**\_ CRED de Schannel**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) especifica lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="24ddd-110">In Windows XP, an [**SCHANNEL\_CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) structure specifies the following:</span></span>

-   <span data-ttu-id="24ddd-111">Un protocolo de seguridad</span><span class="sxs-lookup"><span data-stu-id="24ddd-111">A security protocol</span></span>
-   <span data-ttu-id="24ddd-112">Cifrados permitidos</span><span class="sxs-lookup"><span data-stu-id="24ddd-112">The allowable ciphers</span></span>
-   <span data-ttu-id="24ddd-113">Intensidad mínima y máxima de cifrado</span><span class="sxs-lookup"><span data-stu-id="24ddd-113">Minimum and maximum cipher strengths</span></span>
-   <span data-ttu-id="24ddd-114">Un certificado [*X. 509*](../secgloss/x-gly.md) que se usa para la autenticación, necesario para el servidor, opcional para el cliente a menos que el servidor solicite la autenticación del cliente.</span><span class="sxs-lookup"><span data-stu-id="24ddd-114">An [*X.509*](../secgloss/x-gly.md) certificate used for authentication — Required for server, optional for client unless server requests client authentication.</span></span>

<span data-ttu-id="24ddd-115">Pase la [**estructura \_ CRED de Schannel**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) (a través del parámetro *pAuthData* ) a la función [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) .</span><span class="sxs-lookup"><span data-stu-id="24ddd-115">Pass the [**SCHANNEL\_CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) structure (via the *pAuthData* parameter) to the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function.</span></span> <span data-ttu-id="24ddd-116">Esta función devuelve el identificador de credenciales necesario para establecer un [*contexto de seguridad*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="24ddd-116">This function returns the credentials handle required to establish a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="24ddd-117">Para obtener información detallada sobre cómo establecer los cifrados utilizados con Schannel, consulte [especificar cifrados Schannel y intensidades de cifrado](specifying-schannel-ciphers-and-cipher-strengths.md).</span><span class="sxs-lookup"><span data-stu-id="24ddd-117">For detailed information on setting the ciphers used with Schannel, see [Specifying Schannel Ciphers and Cipher Strengths](specifying-schannel-ciphers-and-cipher-strengths.md).</span></span>

<span data-ttu-id="24ddd-118">Para obtener información acerca de los certificados, consulte [funciones del almacén](../seccrypto/cryptography-functions.md)de certificados y certificados.</span><span class="sxs-lookup"><span data-stu-id="24ddd-118">For information about certificates, see [Certificate and Certificate Store Functions](../seccrypto/cryptography-functions.md).</span></span>

<span data-ttu-id="24ddd-119">Para obtener un ejemplo en el que se muestra la apertura de un [*almacén de certificados*](../secgloss/c-gly.md) y la ubicación de un certificado que se va a usar para la autenticación Schannel, vea [obtener un certificado](getting-a-certificate-for-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="24ddd-119">For an example that demonstrates opening a [*certificate store*](../secgloss/c-gly.md) and locating a certificate to use for Schannel authentication, see [Getting a Certificate](getting-a-certificate-for-schannel.md).</span></span>

 

 
