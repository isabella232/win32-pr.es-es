---
title: Autenticación de usuarios
description: El propio protocolo de autenticación puede autenticar al usuario a través de EAP protegido (PEAP).
ms.assetid: 7e0ff5e3-3274-4b52-8c53-101ad01e3034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10de1d08a0daffe7fb415c3eab4ba939afa9387
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "103785105"
---
# <a name="user-authentication"></a><span data-ttu-id="d7f2f-103">Autenticación de usuarios</span><span class="sxs-lookup"><span data-stu-id="d7f2f-103">User Authentication</span></span>

<span data-ttu-id="d7f2f-104">El propio protocolo de autenticación puede autenticar al usuario a través de EAP protegido (PEAP).</span><span class="sxs-lookup"><span data-stu-id="d7f2f-104">The authentication protocol itself can authenticate the user via Protected EAP (PEAP).</span></span> <span data-ttu-id="d7f2f-105">También hay dos proveedores de autenticación integrados en el sistema operativo: autenticación de dominio de Windows (a la que se tiene acceso a través de los servicios de directorio) y servicio de autenticación remota telefónica de usuario (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="d7f2f-105">There are also two authentication providers built into the operating system: Windows domain authentication (accessed via Directory Services) and Remote Access Dial-In User Service (RADIUS).</span></span>

<span data-ttu-id="d7f2f-106">En el caso de que RADIUS sea el proveedor de autenticación, el complemento EAP se instala en el servidor RADIUS en lugar de en el servidor de punto de acceso inalámbrico (AP), como un servidor RAS.</span><span class="sxs-lookup"><span data-stu-id="d7f2f-106">In the case where RADIUS is the authentication provider, the EAP Plug-in is installed on the RADIUS server rather than on the wireless Access Point (AP) server, such as a RAS server.</span></span> <span data-ttu-id="d7f2f-107">El servidor de AP pasa los paquetes EAP directamente desde el cliente al servicio de autenticación en el servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="d7f2f-107">The AP server passes EAP packets directly from the client to the authentication service on the RADIUS server.</span></span> <span data-ttu-id="d7f2f-108">El servidor de AP no procesa ninguna información de los paquetes EAP, pero debe aceptar las claves de cifrado generadas por PEAP de nivel de servidor y de seguridad completa (256 bits) para crear la conexión segura.</span><span class="sxs-lookup"><span data-stu-id="d7f2f-108">The AP server does not process any of the information in the EAP packets, but it must accept the server-side, full strength (256 bit) PEAP generated encryption keys in order to create the secure connection.</span></span>

 

 




