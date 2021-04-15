---
title: NTLMSSP
description: NTLMSSP
ms.assetid: ae434165-4429-4ef0-b083-60abdfc50de0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706c788f103d3d616b5a3087522b5f06b417e972
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105695770"
---
# <a name="ntlmssp"></a><span data-ttu-id="58a05-103">NTLMSSP</span><span class="sxs-lookup"><span data-stu-id="58a05-103">NTLMSSP</span></span>

<span data-ttu-id="58a05-104">NTLMSSP, cuyo identificador de servicio de autenticación es RPC \_ C \_ authn \_ WinNT, es un proveedor de compatibilidad para seguridad que está disponible en todas las versiones de DCOM.</span><span class="sxs-lookup"><span data-stu-id="58a05-104">NTLMSSP, whose authentication service identifier is RPC\_C\_AUTHN\_WINNT, is a security support provider that is available on all versions of DCOM.</span></span> <span data-ttu-id="58a05-105">Usa el protocolo NTLM para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="58a05-105">It uses the NTLM protocol for authentication.</span></span> <span data-ttu-id="58a05-106">NTLM nunca transmite realmente la contraseña del usuario al servidor durante la autenticación.</span><span class="sxs-lookup"><span data-stu-id="58a05-106">NTLM never actually transmits the user's password to the server during authentication.</span></span> <span data-ttu-id="58a05-107">Por lo tanto, el servidor no puede usar la contraseña durante la suplantación para tener acceso a los recursos de red a los que el usuario tendría acceso.</span><span class="sxs-lookup"><span data-stu-id="58a05-107">Therefore, the server cannot use the password during impersonation to access network resources that the user would have access to.</span></span> <span data-ttu-id="58a05-108">Solo se puede tener acceso a los recursos locales.</span><span class="sxs-lookup"><span data-stu-id="58a05-108">Only local resources can be accessed.</span></span>

<span data-ttu-id="58a05-109">NTLM funciona tanto de forma local como entre equipos.</span><span class="sxs-lookup"><span data-stu-id="58a05-109">NTLM works both locally and across computers.</span></span> <span data-ttu-id="58a05-110">Es decir, si el cliente y el servidor se encuentran en equipos diferentes, NTLM todavía puede asegurarse de que el cliente es quien dice ser.</span><span class="sxs-lookup"><span data-stu-id="58a05-110">That is, if the client and server are on different computers, NTLM can still make sure the client is who it claims to be.</span></span>

<span data-ttu-id="58a05-111">Con NTLM, la identidad del cliente se representa mediante un nombre de dominio, un nombre de usuario y una contraseña o un token.</span><span class="sxs-lookup"><span data-stu-id="58a05-111">With NTLM, the client's identity is represented by a domain name, user name, and a password or token.</span></span> <span data-ttu-id="58a05-112">Cuando un servidor llama a [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), se devuelven el nombre de dominio y el nombre de usuario del cliente.</span><span class="sxs-lookup"><span data-stu-id="58a05-112">When a server calls [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), the client's domain name and user name are returned.</span></span> <span data-ttu-id="58a05-113">Sin embargo, cuando un servidor llama a [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), se devuelve el token del cliente.</span><span class="sxs-lookup"><span data-stu-id="58a05-113">However, when a server calls [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), the client's token is returned.</span></span> <span data-ttu-id="58a05-114">Si no hay ninguna relación de confianza entre el cliente y el servidor, y si el servidor tiene una cuenta local con el mismo nombre y la misma contraseña que el cliente, esa cuenta se usará para representar al cliente.</span><span class="sxs-lookup"><span data-stu-id="58a05-114">If there is no trust relationship between client and server and if the server has a local account with the same name and password as the client, that account will be used to represent the client.</span></span>

<span data-ttu-id="58a05-115">NTLM admite la autenticación mutua entre subprocesos y procesos cruzados (solo localmente).</span><span class="sxs-lookup"><span data-stu-id="58a05-115">NTLM supports mutual authentication cross-thread and cross-process (locally only).</span></span> <span data-ttu-id="58a05-116">Si el cliente especifica el nombre principal del servidor con el formato usuario del dominio \\ en una llamada a [**IClientSecurity:: SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket), la identidad del servidor debe coincidir con el nombre de la entidad de seguridad o se producirá un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="58a05-116">If the client specifies the principal name of the server in the form domain\\user in a call to [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket), the server's identity must match that principal name or the call will fail.</span></span> <span data-ttu-id="58a05-117">Si el cliente especifica **null**, no se comprobará la identidad del servidor.</span><span class="sxs-lookup"><span data-stu-id="58a05-117">If the client specifies **NULL**, the server's identity will not be checked.</span></span>

<span data-ttu-id="58a05-118">NTLM también admite el nivel de suplantación de delegado entre subprocesos y procesos cruzados (solo localmente).</span><span class="sxs-lookup"><span data-stu-id="58a05-118">NTLM additionally supports the delegate impersonation level cross-thread and cross-process (locally only).</span></span>

## <a name="related-topics"></a><span data-ttu-id="58a05-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="58a05-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58a05-120">COM y paquetes de seguridad</span><span class="sxs-lookup"><span data-stu-id="58a05-120">COM and Security Packages</span></span>](com-and-security-packages.md)
</dt> </dl>

 

 