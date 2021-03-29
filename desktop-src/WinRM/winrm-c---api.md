---
title: API de C++ para WinRM
description: Las interfaces de Administración remota de Windows se pueden usar para obtener datos o administrar recursos en un equipo remoto. Esta API está pensada principalmente para uso interno. En su lugar, se recomienda usar la API del shell de cliente de WinRM, siempre que sea posible.
ms.assetid: e50075a1-cb43-4bd6-9bbf-6b715fde6a3a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa7cff2334d9839936d15f7258a70ce03f9751e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994386"
---
# <a name="winrm-c-api"></a><span data-ttu-id="d6e48-105">API de C++ para WinRM</span><span class="sxs-lookup"><span data-stu-id="d6e48-105">WinRM C++ API</span></span>

<span data-ttu-id="d6e48-106">Las interfaces de Administración remota de Windows se pueden usar para obtener datos o administrar [*recursos*](windows-remote-management-glossary.md) en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="d6e48-106">The Windows Remote Management interfaces can be used to obtain data or manage [*resources*](windows-remote-management-glossary.md) on a remote computer.</span></span> <span data-ttu-id="d6e48-107">Esta API está pensada principalmente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="d6e48-107">This API is intended primarily for internal use.</span></span> <span data-ttu-id="d6e48-108">En su lugar, se recomienda usar la [API del shell de cliente de WinRM](client-shell-api.md) , siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="d6e48-108">We recommend using the [WinRM Client Shell API](client-shell-api.md) instead whenever possible.</span></span> <span data-ttu-id="d6e48-109">Las interfaces corresponden estrechamente a la [API de scripting de WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d6e48-109">The interfaces closely correspond to the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

<span data-ttu-id="d6e48-110">Las interfaces de WinRM que heredan directamente de **IDispatch** tienen un objeto de scripting correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d6e48-110">The WinRM interfaces that inherit directly from **IDispatch** each have a corresponding scripting object.</span></span> <span data-ttu-id="d6e48-111">Para obtener más información, consulte la [API de scripting de WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d6e48-111">For more information, see the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

<span data-ttu-id="d6e48-112">En el caso de las aplicaciones multiproceso, WinRM no es compatible con subprocesos independientes que acceden al mismo objeto [**IWSMAN**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) .</span><span class="sxs-lookup"><span data-stu-id="d6e48-112">For multithreaded applications, WinRM does not support separate threads accessing the same [**IWSMAN**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) object.</span></span>

<span data-ttu-id="d6e48-113">WinRM proporciona las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="d6e48-113">The following interfaces are provided by WinRM.</span></span>

<dl> <dt>

<span data-ttu-id="d6e48-114"><span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span><span class="sxs-lookup"><span data-stu-id="d6e48-114"><span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span></span>
</dt> <dd>

<span data-ttu-id="d6e48-115">Proporciona métodos y propiedades que se usan para crear una nueva sesión y administrar una sesión establecida.</span><span class="sxs-lookup"><span data-stu-id="d6e48-115">Provides methods and properties used to create a new session and manage an established session.</span></span> <span data-ttu-id="d6e48-116">[**WSMan**](wsman.md) es el objeto de scripting correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d6e48-116">[**WSMan**](wsman.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="d6e48-117"><span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span><span class="sxs-lookup"><span data-stu-id="d6e48-117"><span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span></span>
</dt> <dd>

<span data-ttu-id="d6e48-118">Proporciona métodos y propiedades que se usan para crear un nuevo [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span><span class="sxs-lookup"><span data-stu-id="d6e48-118">Provides methods and properties used to create a new [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span></span> <span data-ttu-id="d6e48-119">Este método está disponible para el objeto de scripting [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="d6e48-119">This method is available for the [**WSMan**](wsman.md) scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="d6e48-120"><span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)</span><span class="sxs-lookup"><span data-stu-id="d6e48-120"><span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)</span></span>
</dt> <dd>

<span data-ttu-id="d6e48-121">Define el nombre de usuario y la contraseña usados para las conexiones remotas.</span><span class="sxs-lookup"><span data-stu-id="d6e48-121">Defines the user name and password used for remote connections.</span></span> <span data-ttu-id="d6e48-122">[**ConnectionOptions**](connectionoptions.md) es el objeto de scripting correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d6e48-122">[**ConnectionOptions**](connectionoptions.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="d6e48-123"><span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)</span><span class="sxs-lookup"><span data-stu-id="d6e48-123"><span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)</span></span>
</dt> <dd>

<span data-ttu-id="d6e48-124">Define las operaciones de red y las propiedades disponibles para la sesión.</span><span class="sxs-lookup"><span data-stu-id="d6e48-124">Defines the network operations and properties available for the session.</span></span> <span data-ttu-id="d6e48-125">La [**sesión**](session.md) es el objeto de scripting correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d6e48-125">[**Session**](session.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="d6e48-126"><span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)</span><span class="sxs-lookup"><span data-stu-id="d6e48-126"><span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)</span></span>
</dt> <dd>

<span data-ttu-id="d6e48-127">Representa una colección de resultados devueltos al enumerar un recurso.</span><span class="sxs-lookup"><span data-stu-id="d6e48-127">Represents a collection of results returned from enumerating a resource.</span></span> <span data-ttu-id="d6e48-128">El [**enumerador**](enumerator.md) es el objeto de scripting correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d6e48-128">[**Enumerator**](enumerator.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="d6e48-129"><span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)</span><span class="sxs-lookup"><span data-stu-id="d6e48-129"><span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)</span></span>
</dt> <dd>

<span data-ttu-id="d6e48-130">Proporciona la ruta de acceso a un recurso.</span><span class="sxs-lookup"><span data-stu-id="d6e48-130">Supplies the path to a resource.</span></span> <span data-ttu-id="d6e48-131">Puede usar un objeto [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) en lugar de un [*URI de recurso*](windows-remote-management-glossary.md) en operaciones de objeto de [**sesión**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="d6e48-131">You can use an [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) object instead of a [*resource URI*](windows-remote-management-glossary.md) in [**Session**](session.md) object operations.</span></span> <span data-ttu-id="d6e48-132">[**ResourceLocator**](resourcelocator.md) es el objeto de scripting correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d6e48-132">[**ResourceLocator**](resourcelocator.md) is the corresponding scripting object.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="d6e48-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d6e48-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6e48-134">Referencia de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="d6e48-134">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 




