---
description: El siguiente fragmento de código muestra la publicación de un objeto de usuario en un servidor ILS. Una vez publicado un objeto de usuario, los usuarios remotos pueden utilizar el objeto de usuario para realizar llamadas al usuario especificado.
ms.assetid: 8b68886c-0df5-4005-bcd5-1a18336f5192
title: Agregar un objeto de usuario a un servidor ILS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85b15dcdbca47187cf4155dfbf7535d06718c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809236"
---
# <a name="adding-a-user-object-to-an-ils-server"></a><span data-ttu-id="b5f79-104">Agregar un objeto de usuario a un servidor ILS</span><span class="sxs-lookup"><span data-stu-id="b5f79-104">Adding a User Object to an ILS Server</span></span>

<span data-ttu-id="b5f79-105">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b5f79-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b5f79-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="b5f79-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b5f79-107">El siguiente fragmento de código muestra la publicación de un objeto de usuario en un servidor ILS.</span><span class="sxs-lookup"><span data-stu-id="b5f79-107">The following code fragment illustrates publishing a user object in an ILS server.</span></span> <span data-ttu-id="b5f79-108">Una vez publicado un objeto de usuario, los usuarios remotos pueden utilizar el objeto de usuario para realizar llamadas al usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="b5f79-108">After a user object is published, remote parties can use the user object to make calls to the specified user.</span></span>

<span data-ttu-id="b5f79-109">Este fragmento supone que ya se ha realizado la [conexión a un servidor ILS](connecting-to-an-ils-server.md) .</span><span class="sxs-lookup"><span data-stu-id="b5f79-109">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed.</span></span>


```C++
hr = pDirectory->AddDirectoryObject(pDirectoryObject);
```



## <a name="related-topics"></a><span data-ttu-id="b5f79-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b5f79-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5f79-111">**ITDirectory**</span><span class="sxs-lookup"><span data-stu-id="b5f79-111">**ITDirectory**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[<span data-ttu-id="b5f79-112">**ITDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="b5f79-112">**ITDirectoryObject**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)
</dt> <dt>

[<span data-ttu-id="b5f79-113">**ITDirectoryObjectUser**</span><span class="sxs-lookup"><span data-stu-id="b5f79-113">**ITDirectoryObjectUser**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser)
</dt> </dl>

 

 



