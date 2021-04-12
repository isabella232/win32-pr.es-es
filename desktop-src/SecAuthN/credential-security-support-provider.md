---
description: El protocolo de proveedor de compatibilidad para seguridad de credenciales (CredSSP) es un proveedor de compatibilidad de seguridad que se implementa mediante la interfaz del proveedor de compatibilidad para seguridad (SSPI).
ms.assetid: b3006b89-d9fc-4444-a3c8-ad2698de501c
title: Proveedor de compatibilidad con seguridad de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9aa961f37043d84dc21280ea7d5ecb9c27c075
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275797"
---
# <a name="credential-security-support-provider"></a><span data-ttu-id="a495d-103">Proveedor de compatibilidad con seguridad de credenciales</span><span class="sxs-lookup"><span data-stu-id="a495d-103">Credential Security Support Provider</span></span>

<span data-ttu-id="a495d-104">El protocolo de proveedor de compatibilidad para seguridad de credenciales (CredSSP) es un proveedor de compatibilidad de seguridad que se implementa mediante la interfaz del proveedor de compatibilidad para seguridad ([SSPI](sspi.md)).</span><span class="sxs-lookup"><span data-stu-id="a495d-104">The Credential Security Support Provider protocol (CredSSP) is a Security Support Provider that is implemented by using the Security Support Provider Interface ([SSPI](sspi.md)).</span></span> <span data-ttu-id="a495d-105">CredSSP permite a una aplicación delegar las credenciales del usuario desde el cliente al servidor de destino para la autenticación remota.</span><span class="sxs-lookup"><span data-stu-id="a495d-105">CredSSP lets an application delegate the user's credentials from the client to the target server for remote authentication.</span></span> <span data-ttu-id="a495d-106">CredSSP proporciona un canal de [Protocolo de seguridad de capa de transporte](transport-layer-security-protocol.md) cifrado.</span><span class="sxs-lookup"><span data-stu-id="a495d-106">CredSSP provides an encrypted [Transport Layer Security Protocol](transport-layer-security-protocol.md) channel.</span></span> <span data-ttu-id="a495d-107">El cliente se autentica a través del canal cifrado mediante el Protocolo simple y protegido Negotiate (SPNEGO) con [Microsoft Kerberos](microsoft-kerberos.md) o [Microsoft NTLM](microsoft-ntlm.md).</span><span class="sxs-lookup"><span data-stu-id="a495d-107">The client is authenticated over the encrypted channel by using the Simple and Protected Negotiate (SPNEGO) protocol with either [Microsoft Kerberos](microsoft-kerberos.md) or [Microsoft NTLM](microsoft-ntlm.md).</span></span>

> [!Caution]  
> <span data-ttu-id="a495d-108">Esta no es una delegación restringida.</span><span class="sxs-lookup"><span data-stu-id="a495d-108">This is not constrained delegation.</span></span> <span data-ttu-id="a495d-109">CredSSP pasa las credenciales completas del usuario al servidor sin ninguna restricción.</span><span class="sxs-lookup"><span data-stu-id="a495d-109">CredSSP passes the user's full credentials to the server without any constraint.</span></span>

 

<span data-ttu-id="a495d-110">Para obtener información sobre SPNEGO, consulte [Microsoft Negotiate](microsoft-negotiate.md).</span><span class="sxs-lookup"><span data-stu-id="a495d-110">For information about SPNEGO, see [Microsoft Negotiate](microsoft-negotiate.md).</span></span>

<span data-ttu-id="a495d-111">Una vez autenticado el cliente y el servidor, el cliente pasa las credenciales del usuario al servidor.</span><span class="sxs-lookup"><span data-stu-id="a495d-111">After the client and server are authenticated, the client passes the user's credentials to the server.</span></span> <span data-ttu-id="a495d-112">Las credenciales se cifran doble bajo las claves de sesión SPNEGO y TLS.</span><span class="sxs-lookup"><span data-stu-id="a495d-112">The credentials are doubly encrypted under the SPNEGO and TLS session keys.</span></span> <span data-ttu-id="a495d-113">CredSSP admite el inicio de sesión basado en contraseña, así como el inicio de sesión de tarjeta inteligente basado en [*X. 509*](/windows/desktop/SecGloss/x-gly) y PKINIT.</span><span class="sxs-lookup"><span data-stu-id="a495d-113">CredSSP supports password-based logon as well as smart card logon based on both [*X.509*](/windows/desktop/SecGloss/x-gly) and PKINIT.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a495d-114">CredSSP no es compatible con los clientes de WOW64.</span><span class="sxs-lookup"><span data-stu-id="a495d-114">CredSSP does not support Wow64 clients.</span></span>

 

<span data-ttu-id="a495d-115">Para obtener más información acerca de CredSSP, vea los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="a495d-115">For more information about CredSSP, see the following topics.</span></span>



| <span data-ttu-id="a495d-116">Tema</span><span class="sxs-lookup"><span data-stu-id="a495d-116">Topic</span></span>                                                                         | <span data-ttu-id="a495d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a495d-117">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a495d-118">Configuración de directiva de grupo CredSSP</span><span class="sxs-lookup"><span data-stu-id="a495d-118">CredSSP Group Policy Settings</span></span>](credssp-group-policy-settings.md)<br/> | <span data-ttu-id="a495d-119">La delegación de credenciales por CredSSP se puede controlar mediante la configuración de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="a495d-119">Delegation of credentials by CredSSP can be controlled by using group policy settings.</span></span><br/> |



 

 

