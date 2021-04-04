---
description: API de administración de credenciales
ms.assetid: e393041b-f10c-4053-bc6c-65a89f40e74f
title: API de administración de credenciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3cae5054d0a32f42616f2845dcf18ab71ad0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814742"
---
# <a name="credential-management-api"></a><span data-ttu-id="080d3-103">API de administración de credenciales</span><span class="sxs-lookup"><span data-stu-id="080d3-103">Credential Management API</span></span>

<span data-ttu-id="080d3-104">Las funciones de administración de credenciales constituyen el conjunto de funciones que debe implementar un administrador de credenciales.</span><span class="sxs-lookup"><span data-stu-id="080d3-104">The credential management functions constitute the set of functions that a credential manager must implement.</span></span> <span data-ttu-id="080d3-105">Dichos componentes son:</span><span class="sxs-lookup"><span data-stu-id="080d3-105">These are:</span></span>

-   <span data-ttu-id="080d3-106">[**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify), una función de controlador de eventos a la que el MPR llama cuando un usuario inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="080d3-106">[**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify), an event-handler function that the MPR calls when a user logs on.</span></span>
-   <span data-ttu-id="080d3-107">[**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), una función de controlador de eventos a la que el MPR llama cuando se cambia una contraseña de cuenta.</span><span class="sxs-lookup"><span data-stu-id="080d3-107">[**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify), an event-handler function the MPR calls when an account password is changed.</span></span>

<span data-ttu-id="080d3-108">Siempre se llama a las funciones de administración de credenciales en el contexto del sistema (LocalSystem) en lugar de en el contexto del usuario.</span><span class="sxs-lookup"><span data-stu-id="080d3-108">The credential management functions are always called in the system context (LocalSystem) rather than the user context.</span></span>

<span data-ttu-id="080d3-109">Para obtener más información acerca de cómo crear y registrar una aplicación de administrador de credenciales, consulte [implementar un administrador de credenciales](implementing-a-credential-manager.md) y [registrar proveedores de credenciales y administradores de credenciales](registering-network-providers-and-credential-managers.md).</span><span class="sxs-lookup"><span data-stu-id="080d3-109">For more information about how to create and register a credential manager application, see [Implementing a Credential Manager](implementing-a-credential-manager.md) and [Registering Network Providers and Credential Managers](registering-network-providers-and-credential-managers.md).</span></span>

 

 



