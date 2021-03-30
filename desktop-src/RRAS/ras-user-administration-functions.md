---
title: Funciones de administración de usuarios de RAS
description: Usar las siguientes funciones para administrar usuarios de acceso telefónico
ms.assetid: e58fa4a6-16d3-4953-bf21-887d08e25af7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf8c1e7df962eff2064dac06da256f3a78e8ed17
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488162"
---
# <a name="ras-user-administration-functions"></a><span data-ttu-id="c4e8f-103">Funciones de administración de usuarios de RAS</span><span class="sxs-lookup"><span data-stu-id="c4e8f-103">RAS User Administration Functions</span></span>

<span data-ttu-id="c4e8f-104">Use las siguientes funciones para administrar usuarios de acceso telefónico:</span><span class="sxs-lookup"><span data-stu-id="c4e8f-104">Use the following functions to manage dial-up users:</span></span>

-   [<span data-ttu-id="c4e8f-105">**MprAdminGetPDCServer**</span><span class="sxs-lookup"><span data-stu-id="c4e8f-105">**MprAdminGetPDCServer**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)
-   [<span data-ttu-id="c4e8f-106">**MprAdminSendUserMessage**</span><span class="sxs-lookup"><span data-stu-id="c4e8f-106">**MprAdminSendUserMessage**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)
-   [<span data-ttu-id="c4e8f-107">**MprAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="c4e8f-107">**MprAdminUserGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)
-   [<span data-ttu-id="c4e8f-108">**MprAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="c4e8f-108">**MprAdminUserSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)

<span data-ttu-id="c4e8f-109">Para obtener una lista de los usuarios actuales de un dominio determinado, utilice la función [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) .</span><span class="sxs-lookup"><span data-stu-id="c4e8f-109">To obtain a list of current users on a particular domain, use the [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) function.</span></span> <span data-ttu-id="c4e8f-110">El prototipo de esta función se encuentra en el archivo de encabezado lmaccess. h.</span><span class="sxs-lookup"><span data-stu-id="c4e8f-110">The prototype for this function is in the lmaccess.h header file.</span></span>

 

 