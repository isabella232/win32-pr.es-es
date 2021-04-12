---
title: Configuración de autenticación dinámica
description: Las aplicaciones pueden cambiar las configuraciones de autenticación en un grupo de direcciones URL o una sesión de servidor en cualquier momento.
ms.assetid: 8a5cc119-0427-487d-a155-74c14e2104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84c68daf04d870d4aa50596397f4f021ac1729af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356827"
---
# <a name="dynamic-authentication-configuration"></a><span data-ttu-id="ab71a-103">Configuración de autenticación dinámica</span><span class="sxs-lookup"><span data-stu-id="ab71a-103">Dynamic Authentication Configuration</span></span>

<span data-ttu-id="ab71a-104">De forma predeterminada, la API del servidor HTTP no realiza la autenticación a menos que la aplicación la habilite específicamente.</span><span class="sxs-lookup"><span data-stu-id="ab71a-104">By default, the HTTP Server API does not perform authentication unless the application specifically enables it.</span></span> <span data-ttu-id="ab71a-105">Las aplicaciones pueden cambiar las configuraciones de autenticación en un grupo de direcciones URL o una sesión de servidor en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="ab71a-105">Applications can change authentication configurations on a URL Group or server session at any time.</span></span> <span data-ttu-id="ab71a-106">Los cambios en la configuración de autenticación no afectan a las solicitudes que ya se han autenticado o se envían a la aplicación</span><span class="sxs-lookup"><span data-stu-id="ab71a-106">Changes to the authentication configuration do not affect requests that are already authenticated or being dispatched to the application</span></span>

<span data-ttu-id="ab71a-107">En el caso de los esquemas de autenticación en los que se requieren varios redondeos de protocolo de enlace, la API del servidor HTTP quita el protocolo de enlace de autenticación si ya no se admite el esquema actual debido a los cambios de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ab71a-107">For authentication schemes where multiple rounds of handshake are required, the HTTP Server API drops the authentication handshake if the current scheme is no longer supported due to configuration changes from the application.</span></span> <span data-ttu-id="ab71a-108">Por ejemplo, si la aplicación habilita Negotiate y deshabilita NTLM, y la API del servidor HTTP está en el protocolo de enlace de autenticación intermedia para NTLM, el protocolo de enlace para NTLM se descarta y la solicitud se pasa a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ab71a-108">For example, if the application enables Negotiate and disables NTLM, and the HTTP Server API is in the intermediate authentication handshake for NTLM, the handshake for NTLM is discarded and the request is passed to the application.</span></span> <span data-ttu-id="ab71a-109">La aplicación envía un desafío de autenticación 401 con los nuevos tipos de autenticación especificados en el encabezado WWW-Authenticate.</span><span class="sxs-lookup"><span data-stu-id="ab71a-109">The application sends a 401 authentication challenge with the new authentication types specified in the WWW-Authenticate header.</span></span>

 

 




