---
description: Autenticación de origen de red
ms.assetid: bffc33ec-0fb0-4bbe-9bac-583b9d4e1153
title: Autenticación de origen de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09c38968fccf501f49ac7666a066b88528b237bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082295"
---
# <a name="network-source-authentication"></a><span data-ttu-id="1ad56-103">Autenticación de origen de red</span><span class="sxs-lookup"><span data-stu-id="1ad56-103">Network Source Authentication</span></span>

<span data-ttu-id="1ad56-104">Algunos hosts multimedia pueden requerir credenciales de usuario de las aplicaciones cliente antes de permitir el acceso a los medios.</span><span class="sxs-lookup"><span data-stu-id="1ad56-104">Certain media hosts may require user credentials from client applications before allowing access to the media.</span></span> <span data-ttu-id="1ad56-105">Las credenciales de usuario incluyen la identificación y la prueba de identificación, como el nombre de usuario y la contraseña, que el servidor multimedia usa para conceder acceso al origen de red que hospeda.</span><span class="sxs-lookup"><span data-stu-id="1ad56-105">User credentials include identification and proof of identification, such as user name and password, which are used by the media server to grant access to the network source it hosts.</span></span> <span data-ttu-id="1ad56-106">El origen de red puede proporcionar autenticación NTLM, implícita o básica.</span><span class="sxs-lookup"><span data-stu-id="1ad56-106">The network source can provide NTLM, Digest, or Basic authentication.</span></span>

<span data-ttu-id="1ad56-107">Las aplicaciones basadas en Media Foundation pueden almacenar las credenciales de usuario para una dirección URL específica en un objeto de *credenciales* que exponga la interfaz [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) .</span><span class="sxs-lookup"><span data-stu-id="1ad56-107">Applications based on Media Foundation can store user credentials for a specific URL in a *credential* object that exposes the [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) interface.</span></span> <span data-ttu-id="1ad56-108">El objeto Credential almacena las credenciales cifradas y proporciona métodos para devolver información como el nombre de usuario, la contraseña y el dominio.</span><span class="sxs-lookup"><span data-stu-id="1ad56-108">The credential object stores encrypted credentials and provides methods to return information such as user name, password, and domain.</span></span>

<span data-ttu-id="1ad56-109">Los objetos de credenciales se crean y mantienen en una memoria caché.</span><span class="sxs-lookup"><span data-stu-id="1ad56-109">The credential objects are created and maintained in a cache.</span></span> <span data-ttu-id="1ad56-110">El objeto de *caché de credenciales* , expuesto por la interfaz [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) , proporciona métodos para recuperar los objetos de credenciales de la memoria caché de credenciales.</span><span class="sxs-lookup"><span data-stu-id="1ad56-110">The *credential cache* object, exposed by the [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) interface provides methods for retrieving the credential objects from the credential cache.</span></span>

<span data-ttu-id="1ad56-111">Una aplicación que admite la autenticación debe implementar la interfaz [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .</span><span class="sxs-lookup"><span data-stu-id="1ad56-111">An application that supports authentication must implement the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span> <span data-ttu-id="1ad56-112">Media Foundation no proporciona una implementación predeterminada de esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="1ad56-112">Media Foundation does not provide a default implementation of this interface.</span></span> <span data-ttu-id="1ad56-113">El administrador de credenciales es responsable de recopilar las credenciales necesarias para una dirección URL de la entrada del usuario o de la lectura desde el almacenamiento persistente.</span><span class="sxs-lookup"><span data-stu-id="1ad56-113">The credential manager is responsible for gathering the required credentials for a URL from user input or reading from persisted storage.</span></span>

<span data-ttu-id="1ad56-114">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="1ad56-114">This section contains the following topics:</span></span>

-   [<span data-ttu-id="1ad56-115">Establecer un administrador de credenciales</span><span class="sxs-lookup"><span data-stu-id="1ad56-115">Setting a Credential Manager</span></span>](setting-a-credential-manager.md)
-   [<span data-ttu-id="1ad56-116">Uso de la caché de credenciales</span><span class="sxs-lookup"><span data-stu-id="1ad56-116">Using the Credential Cache</span></span>](using-the-credential-cache.md)
-   [<span data-ttu-id="1ad56-117">Implementación de IMFNetCredentialManager</span><span class="sxs-lookup"><span data-stu-id="1ad56-117">Implementing IMFNetCredentialManager</span></span>](implementing-imfnetcredentialmanager.md)

## <a name="related-topics"></a><span data-ttu-id="1ad56-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1ad56-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ad56-119">Funciones de red en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1ad56-119">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 



