---
title: Aspectos básicos de seguridad de RPC
description: Para completar cualquier llamada a procedimiento remoto, todas las aplicaciones distribuidas deben crear un enlace entre el cliente y el servidor.
ms.assetid: 7b8adba2-19aa-4179-b6b3-ef27f4383bd4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fdd64352df4bbefc1ec41960b78109b22510c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903785"
---
# <a name="rpc-security-essentials"></a><span data-ttu-id="03845-103">Aspectos básicos de seguridad de RPC</span><span class="sxs-lookup"><span data-stu-id="03845-103">RPC Security Essentials</span></span>

<span data-ttu-id="03845-104">Para completar cualquier llamada a procedimiento remoto, todas las aplicaciones distribuidas deben crear un enlace entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="03845-104">To complete any remote procedure call, all distributed applications must create a binding between the client and the server.</span></span> <span data-ttu-id="03845-105">Para obtener más información sobre los enlaces, vea [enlazar y controlar](binding-and-handles.md).</span><span class="sxs-lookup"><span data-stu-id="03845-105">For more information on bindings, see [Binding and Handles](binding-and-handles.md).</span></span> <span data-ttu-id="03845-106">Para completar una llamada de procedimiento remoto segura, se necesitan pasos adicionales.</span><span class="sxs-lookup"><span data-stu-id="03845-106">To complete a secure remote procedure call, additional steps are necessary.</span></span> <span data-ttu-id="03845-107">En primer lugar, el servidor debe elegir un proveedor de seguridad (servicio de autenticación en la terminología de DCE).</span><span class="sxs-lookup"><span data-stu-id="03845-107">First, the server must choose a security provider (authentication service in DCE terminology).</span></span> <span data-ttu-id="03845-108">Después, debe decidirse por su mecanismo de autenticación.</span><span class="sxs-lookup"><span data-stu-id="03845-108">Then it must decide on its authentication mechanism.</span></span> <span data-ttu-id="03845-109">Después, el cliente obtiene un enlace al servidor y solicita una llamada de procedimiento remoto segura desde el tiempo de ejecución de RPC, y especifica diversas opciones de seguridad, como el proveedor de seguridad, las opciones de QOS de seguridad, etc.</span><span class="sxs-lookup"><span data-stu-id="03845-109">After that, the client obtains a binding to the server, and requests a secure remote procedure call from the RPC run time, and specifies various security options, such as security provider, security QOS options, and so on.</span></span>

<span data-ttu-id="03845-110">En esta sección se explican los conceptos y la información esenciales necesarios para utilizar las funciones de RPC con el fin de crear un cliente y un servidor para una aplicación distribuida autenticada.</span><span class="sxs-lookup"><span data-stu-id="03845-110">This section explains the essential concepts and information required to use the RPC functions to create a client and server for an authenticated distributed application.</span></span> <span data-ttu-id="03845-111">Se organiza en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="03845-111">It is organized into the following topics:</span></span>

-   [<span data-ttu-id="03845-112">Nombres principales</span><span class="sxs-lookup"><span data-stu-id="03845-112">Principal Names</span></span>](principal-names.md)
-   [<span data-ttu-id="03845-113">Niveles de autenticación</span><span class="sxs-lookup"><span data-stu-id="03845-113">Authentication Levels</span></span>](authentication-levels.md)
-   [<span data-ttu-id="03845-114">Servicios de autenticación</span><span class="sxs-lookup"><span data-stu-id="03845-114">Authentication Services</span></span>](authentication-services.md)
-   [<span data-ttu-id="03845-115">Credenciales de autenticación del cliente</span><span class="sxs-lookup"><span data-stu-id="03845-115">Client Authentication Credentials</span></span>](client-authentication-credentials.md)
-   [<span data-ttu-id="03845-116">Servicios de autorización</span><span class="sxs-lookup"><span data-stu-id="03845-116">Authorization Services</span></span>](authorization-services.md)
-   [<span data-ttu-id="03845-117">Calidad de servicio</span><span class="sxs-lookup"><span data-stu-id="03845-117">Quality of Service</span></span>](quality-of-service.md)
-   [<span data-ttu-id="03845-118">Funciones de autorización</span><span class="sxs-lookup"><span data-stu-id="03845-118">Authorization Functions</span></span>](authorization-functions.md)
-   [<span data-ttu-id="03845-119">Funciones de adquisición de claves</span><span class="sxs-lookup"><span data-stu-id="03845-119">Key Acquisition Functions</span></span>](key-acquisition-functions.md)
-   [<span data-ttu-id="03845-120">Suplantación de cliente</span><span class="sxs-lookup"><span data-stu-id="03845-120">Client Impersonation</span></span>](client-impersonation.md)

 

 




