---
title: Acerca de las extensiones de NPS
description: En esta sección se describe cómo implementar archivos DLL para ampliar la funcionalidad de NPS. Describe la interacción entre NPS y los archivos dll, y presenta algunas consideraciones de diseño relacionadas con los archivos dll.
ms.assetid: 3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05878a5243774046c1ca052052d59be9378483d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665858"
---
# <a name="about-nps-extensions"></a><span data-ttu-id="209fa-104">Acerca de las extensiones de NPS</span><span class="sxs-lookup"><span data-stu-id="209fa-104">About NPS Extensions</span></span>

> [!Note]  
> <span data-ttu-id="209fa-105">Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="209fa-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="209fa-106">El contenido de este tema se aplica a IAS y NPS.</span><span class="sxs-lookup"><span data-stu-id="209fa-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="209fa-107">En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.</span><span class="sxs-lookup"><span data-stu-id="209fa-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="209fa-108">En esta sección se describe cómo implementar archivos DLL para ampliar la funcionalidad de NPS.</span><span class="sxs-lookup"><span data-stu-id="209fa-108">This section describes how to implement DLLs to extend the functionality of NPS.</span></span> <span data-ttu-id="209fa-109">Describe la interacción entre NPS y los archivos dll, y presenta algunas consideraciones de diseño relacionadas con los archivos dll.</span><span class="sxs-lookup"><span data-stu-id="209fa-109">It describes the interaction between NPS and the DLLs, and presents some design considerations regarding the DLLs.</span></span>

<span data-ttu-id="209fa-110">NPS proporciona dos puntos de extensión, uno para la autenticación y el otro para la autorización.</span><span class="sxs-lookup"><span data-stu-id="209fa-110">NPS provides two extension points, one for authentication and the other for authorization.</span></span> <span data-ttu-id="209fa-111">La autenticación se refiere a la comprobación de la identidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="209fa-111">Authentication refers to verifying the identity of the user.</span></span> <span data-ttu-id="209fa-112">La autorización se refiere a determinar qué servicios debe proporcionar la red al usuario.</span><span class="sxs-lookup"><span data-stu-id="209fa-112">Authorization refers to determining what services the network should provide to the user.</span></span> <span data-ttu-id="209fa-113">Los dos puntos de extensión corresponden a los archivos dll de extensión de autenticación y dll de extensión de autorización.</span><span class="sxs-lookup"><span data-stu-id="209fa-113">The two extension points correspond to Authentication Extension DLLs and Authorization Extension DLLs.</span></span> <span data-ttu-id="209fa-114">Cada punto de extensión puede admitir varios archivos dll.</span><span class="sxs-lookup"><span data-stu-id="209fa-114">Each extension point can support multiple DLLs.</span></span>

<span data-ttu-id="209fa-115">NPS proporciona servicios de autenticación y autorización.</span><span class="sxs-lookup"><span data-stu-id="209fa-115">NPS provides both authentication and authorization services.</span></span> <span data-ttu-id="209fa-116">NPS llama a los archivos dll de extensión de autenticación antes de la autenticación y autorización de NPS integrada.</span><span class="sxs-lookup"><span data-stu-id="209fa-116">Authentication Extension DLLs are called by NPS prior to the built-in NPS authentication and authorization.</span></span> <span data-ttu-id="209fa-117">Se llama a los archivos dll de extensión de autorización después de la autenticación y autorización de NPS.</span><span class="sxs-lookup"><span data-stu-id="209fa-117">Authorization Extension DLLs are called after NPS authentication and authorization.</span></span>

<span data-ttu-id="209fa-118">En el diagrama siguiente se ilustra el flujo de paquetes a través de un servidor RADIUS NPS que se expande mediante el uso de archivos dll de extensión.</span><span class="sxs-lookup"><span data-stu-id="209fa-118">The following diagram illustrates the flow of packets through an NPS RADIUS server that is expanded using Extension DLLs.</span></span>

![proceso de autenticación y autorización de NPS](images/ias03.png)

<span data-ttu-id="209fa-120">Si un archivo DLL de extensión de autenticación devuelve ACCEPT, el paquete omite la autenticación NPS y va directamente a la autorización NPS.</span><span class="sxs-lookup"><span data-stu-id="209fa-120">If an Authentication Extension DLL returns ACCEPT, the packet skips the NPS authentication and goes directly to NPS authorization.</span></span>

> [!Note]  
> <span data-ttu-id="209fa-121">Cuando hay varios archivos dll de extensión de autenticación, es posible que también se omita el resto de los archivos dll de extensión.</span><span class="sxs-lookup"><span data-stu-id="209fa-121">When multiple Authentication Extension DLLs are present, the rest of the Extension DLLs might be skipped as well.</span></span> <span data-ttu-id="209fa-122">Para obtener más información, consulte [configuración de los archivos dll de extensión](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls) .</span><span class="sxs-lookup"><span data-stu-id="209fa-122">See [Setting Up the Extension DLLs](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls) for more information.</span></span>

 

<span data-ttu-id="209fa-123">Si un archivo DLL de extensión de autenticación devuelve CONTINUE, el paquete va a la autenticación NPS y, a continuación, a la autorización NPS.</span><span class="sxs-lookup"><span data-stu-id="209fa-123">If an Authentication Extension DLL returns CONTINUE, the packet goes to NPS authentication, and then to NPS authorization.</span></span>

> [!Note]  
> <span data-ttu-id="209fa-124">Cuando hay varios archivos dll de extensión de autenticación, el resto de los archivos dll de extensión de autenticación se invocan antes de la autenticación NPS.</span><span class="sxs-lookup"><span data-stu-id="209fa-124">When multiple Authentication Extension DLLs are present, the rest of the Authentication Extension DLLs are invoked before NPS authentication.</span></span>

 

<span data-ttu-id="209fa-125">En los temas siguientes se describen con más detalle los archivos dll de extensión:</span><span class="sxs-lookup"><span data-stu-id="209fa-125">The following topics describe the Extension DLLs in more detail:</span></span>

-   [<span data-ttu-id="209fa-126">Configuración de los archivos dll de extensión</span><span class="sxs-lookup"><span data-stu-id="209fa-126">Setting Up the Extension DLLs</span></span>](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
-   [<span data-ttu-id="209fa-127">Invocar los archivos dll de extensión</span><span class="sxs-lookup"><span data-stu-id="209fa-127">Invoking the Extension DLLs</span></span>](/windows/desktop/Nps/ias-authentication-and-authorization-process)
-   [<span data-ttu-id="209fa-128">Atributos de identificación de usuario</span><span class="sxs-lookup"><span data-stu-id="209fa-128">User Identification Attributes</span></span>](/windows/desktop/Nps/ias-user-identification-attributes)

 

 