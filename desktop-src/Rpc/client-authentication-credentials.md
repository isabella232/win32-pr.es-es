---
title: Credenciales de autenticación del cliente
description: Cada cliente autenticado debe proporcionar las credenciales de autenticación al servidor.
ms.assetid: d567e944-8d68-4d95-be6a-840e30f57ba9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3704663411fc33340a462d8e3b356041b6061468
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076299"
---
# <a name="client-authentication-credentials"></a><span data-ttu-id="28e99-103">Credenciales de autenticación del cliente</span><span class="sxs-lookup"><span data-stu-id="28e99-103">Client Authentication Credentials</span></span>

<span data-ttu-id="28e99-104">Cada cliente autenticado debe proporcionar las credenciales de autenticación al servidor.</span><span class="sxs-lookup"><span data-stu-id="28e99-104">Each authenticated client must provide authentication credentials to the server.</span></span> <span data-ttu-id="28e99-105">En RPC, el cliente almacena sus credenciales de autenticación en el enlace entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="28e99-105">Under RPC, the client stores its authentication credentials in the binding between the client and the server.</span></span> <span data-ttu-id="28e99-106">Para ello, el cliente llama a [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) o [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa).</span><span class="sxs-lookup"><span data-stu-id="28e99-106">To do this, the client calls [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) or [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa).</span></span>

<span data-ttu-id="28e99-107">Hay dos tipos de credenciales: implícitas y explícitas:</span><span class="sxs-lookup"><span data-stu-id="28e99-107">There are two types of credentials—implicit and explicit:</span></span>

-   <span data-ttu-id="28e99-108">Las credenciales explícitas existen cuando el cliente suministra el nombre de usuario, la contraseña y el dominio.</span><span class="sxs-lookup"><span data-stu-id="28e99-108">Explicit credentials exist when the client supplies username, password, and domain.</span></span>
-   <span data-ttu-id="28e99-109">Las credenciales implícitas existen cuando el cliente usa las credenciales del subproceso o el token de proceso que llama a las funciones **RpcBindingSetAuthInfo** o **RpcBindingSetAuthInfoEx** .</span><span class="sxs-lookup"><span data-stu-id="28e99-109">Implicit credentials exist when the client uses credentials from the thread or process token calling the **RpcBindingSetAuthInfo** or **RpcBindingSetAuthInfoEx** functions.</span></span>

<span data-ttu-id="28e99-110">Los clientes deben abstenerse de proporcionar credenciales explícitas porque almacenar, manipular y recuperar una contraseña de usuario puede introducir una vulnerabilidad de seguridad en un sistema distribuido si se usan credenciales explícitas.</span><span class="sxs-lookup"><span data-stu-id="28e99-110">Clients should refrain from supplying explicit credentials because storing, manipulating, and retrieving a user password can introduce a security vulnerability into a distributed system if explicit credentials are used.</span></span>

<span data-ttu-id="28e99-111">Para usar credenciales IMPLÍCITAS, el cliente llama a **RpcBindingSetAuthInfo**(*ex*).</span><span class="sxs-lookup"><span data-stu-id="28e99-111">To use implicit credentials, the client calls **RpcBindingSetAuthInfo**(*Ex*).</span></span> <span data-ttu-id="28e99-112">El sistema de seguridad y RPC obtienen credenciales del subproceso o el token del proceso para su uso en la sesión de autenticación.</span><span class="sxs-lookup"><span data-stu-id="28e99-112">The security system and RPC obtain credentials from the thread or process token for use in the authentication session.</span></span>

<span data-ttu-id="28e99-113">Si el cliente usa credenciales explícitas, el quinto parámetro de estas dos funciones es del tipo [**identificador de identidad de autenticación de RPC \_ \_ \_**](rpc-auth-identity-handle.md).</span><span class="sxs-lookup"><span data-stu-id="28e99-113">If the client uses explicit credentials, the fifth parameter of these two functions is of type [**RPC\_AUTH\_IDENTITY\_HANDLE**](rpc-auth-identity-handle.md).</span></span> <span data-ttu-id="28e99-114">Se trata de un tipo flexible que es un puntero a una estructura de datos.</span><span class="sxs-lookup"><span data-stu-id="28e99-114">This is a flexible type that is a pointer to a data structure.</span></span> <span data-ttu-id="28e99-115">El contenido de la estructura de datos puede diferir con cada servicio de autenticación.</span><span class="sxs-lookup"><span data-stu-id="28e99-115">The contents of the data structure can differ with each authentication service.</span></span> <span data-ttu-id="28e99-116">Actualmente, el SSP que admite RPC requiere que la aplicación establezca **el \_ \_ \_ identificador de identidad de autenticación de RPC** para que apunte a una estructura de [**\_ \_ \_ identidad de autenticación de WinNT**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) .</span><span class="sxs-lookup"><span data-stu-id="28e99-116">Currently, the SSPs that RPC supports require that your application set **RPC\_AUTH\_IDENTITY\_HANDLE** to point to a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) structure.</span></span> <span data-ttu-id="28e99-117">La estructura de **\_ identidad de \_ autenticación \_ de WinNT** de la SEC contiene campos para un nombre de usuario, dominio y contraseña.</span><span class="sxs-lookup"><span data-stu-id="28e99-117">The **SEC\_WINNT\_AUTH\_IDENTITY** structure contains fields for a user name, domain, and password.</span></span>

 

 




