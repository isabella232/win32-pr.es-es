---
title: API de scripting de WinRM
description: Administración remota de Windows objetos de scripting se implementan como una capa por encima del Protocolo de WS-Management.
ms.assetid: bd642669-554f-40ab-bd40-235013afa077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7910213487f525b74c3d1a8819a450f95336aba1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704733"
---
# <a name="winrm-scripting-api"></a><span data-ttu-id="ac537-103">API de scripting de WinRM</span><span class="sxs-lookup"><span data-stu-id="ac537-103">WinRM Scripting API</span></span>

<span data-ttu-id="ac537-104">Administración remota de Windows objetos de scripting se implementan como una capa por encima de la [protocolo WS-Management](ws-management-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="ac537-104">Windows Remote Management scripting objects are implemented as a layer above the [WS-Management Protocol](ws-management-protocol.md).</span></span> <span data-ttu-id="ac537-105">Los objetos de scripting le permiten obtener datos o administrar [*recursos*](windows-remote-management-glossary.md) en equipos locales y remotos.</span><span class="sxs-lookup"><span data-stu-id="ac537-105">The scripting objects enable you to obtain data or manage [*resources*](windows-remote-management-glossary.md) on local and remote computers.</span></span>

## <a name="ws-management-objects"></a><span data-ttu-id="ac537-106">Objetos WS-Management</span><span class="sxs-lookup"><span data-stu-id="ac537-106">WS-Management Objects</span></span>

<span data-ttu-id="ac537-107">Cada objeto de scripting tiene una interfaz de C++ correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ac537-107">Each scripting object has a corresponding C++ interface.</span></span> <span data-ttu-id="ac537-108">Para obtener más información, vea [API](winrm-c---api.md) y [scripting de C++ de WinRM en administración remota de Windows](scripting-in-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="ac537-108">For more information, see [WinRM C++ API](winrm-c---api.md) and [Scripting in Windows Remote Management](scripting-in-windows-remote-management.md).</span></span>

<span data-ttu-id="ac537-109">La API de scripting de WinRM proporciona los siguientes objetos.</span><span class="sxs-lookup"><span data-stu-id="ac537-109">The following objects are provided by the WinRM Scripting API.</span></span>

<dl> <dt>

<span data-ttu-id="ac537-110"><span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**ConnectionOptions**](connectionoptions.md)</span><span class="sxs-lookup"><span data-stu-id="ac537-110"><span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**ConnectionOptions**](connectionoptions.md)</span></span>
</dt> <dd>

<span data-ttu-id="ac537-111">Define el nombre de usuario y la contraseña usados para las conexiones remotas.</span><span class="sxs-lookup"><span data-stu-id="ac537-111">Defines the user name and password used for remote connections.</span></span> <span data-ttu-id="ac537-112">El nombre de usuario y la contraseña se pasan cuando se llama al método [**CreateConnectionOptions**](wsman-createconnectionoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="ac537-112">The user name and password are passed when calling the [**CreateConnectionOptions**](wsman-createconnectionoptions.md) method.</span></span> <span data-ttu-id="ac537-113">Para obtener más información, consulte [obtención de datos de un equipo remoto](obtaining-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="ac537-113">For more information, see [Obtaining Data from a Remote Computer](obtaining-data-from-a-remote-computer.md).</span></span> <span data-ttu-id="ac537-114">La interfaz de C++ correspondiente es [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions).</span><span class="sxs-lookup"><span data-stu-id="ac537-114">The corresponding C++ interface is [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions).</span></span>

</dd> <dt>

<span data-ttu-id="ac537-115"><span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**Avanzó**](enumerator.md)</span><span class="sxs-lookup"><span data-stu-id="ac537-115"><span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**Enumerator**](enumerator.md)</span></span>
</dt> <dd>

<span data-ttu-id="ac537-116">Representa una colección de resultados devueltos al enumerar un recurso.</span><span class="sxs-lookup"><span data-stu-id="ac537-116">Represents a collection of results returned from enumerating a resource.</span></span> <span data-ttu-id="ac537-117">Para obtener más información, consulte [enumeración o enumeración de todas las instancias de un recurso](enumerating-or-listing-all-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="ac537-117">For more information, see [Enumerating or Listing All the Instances of a Resource](enumerating-or-listing-all-instances-of-a-resource.md).</span></span> <span data-ttu-id="ac537-118">La interfaz de C++ correspondiente es [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span><span class="sxs-lookup"><span data-stu-id="ac537-118">The corresponding C++ interface is [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span></span>

</dd> <dt>

<span data-ttu-id="ac537-119"><span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)</span><span class="sxs-lookup"><span data-stu-id="ac537-119"><span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)</span></span>
</dt> <dd>

<span data-ttu-id="ac537-120">Proporciona la ruta de acceso a un recurso.</span><span class="sxs-lookup"><span data-stu-id="ac537-120">Supplies the path to a resource.</span></span> <span data-ttu-id="ac537-121">Puede usar un objeto [**ResourceLocator**](resourcelocator.md) en lugar de un [*URI de recurso*](windows-remote-management-glossary.md) en operaciones de objetos de [**sesión**](session.md) , como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)o [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="ac537-121">You can use a [**ResourceLocator**](resourcelocator.md) object instead of a [*resource URI*](windows-remote-management-glossary.md) in [**Session**](session.md) object operations, such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="ac537-122">La interfaz de C++ correspondiente es [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span><span class="sxs-lookup"><span data-stu-id="ac537-122">The corresponding C++ interface is [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span></span>

</dd> <dt>

<span data-ttu-id="ac537-123"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**Sesión**](session.md)</span><span class="sxs-lookup"><span data-stu-id="ac537-123"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**Session**](session.md)</span></span>
</dt> <dd>

<span data-ttu-id="ac537-124">Define las operaciones de red y las propiedades disponibles para la sesión, como [**Session. Get**](session-get.md), [**Session. Enumerate**](session-enumerate.md), [**Session. Invoke**](session-invoke.md).</span><span class="sxs-lookup"><span data-stu-id="ac537-124">Defines the network operations and properties available for the session, such as [**Session.Get**](session-get.md), [**Session.Enumerate**](session-enumerate.md), [**Session.Invoke**](session-invoke.md).</span></span> <span data-ttu-id="ac537-125">Para obtener más información, consulte [obtener datos del equipo local](obtaining-data-from-the-local-computer.md).</span><span class="sxs-lookup"><span data-stu-id="ac537-125">For more information, see [Obtaining Data from the Local Computer](obtaining-data-from-the-local-computer.md).</span></span> <span data-ttu-id="ac537-126">La interfaz de C++ correspondiente es [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession).</span><span class="sxs-lookup"><span data-stu-id="ac537-126">The corresponding C++ interface is [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession).</span></span>

</dd> <dt>

<span data-ttu-id="ac537-127"><span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**WSMan**](wsman.md)</span><span class="sxs-lookup"><span data-stu-id="ac537-127"><span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**WSMan**](wsman.md)</span></span>
</dt> <dd>

<span data-ttu-id="ac537-128">Proporciona métodos y propiedades que se usan para crear una nueva sesión o administrar una sesión establecida.</span><span class="sxs-lookup"><span data-stu-id="ac537-128">Provides methods and properties used to create a new session or manage an established session.</span></span> <span data-ttu-id="ac537-129">Para obtener más información, vea [uso de administración remota de Windows](using-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="ac537-129">For more information see, [Using Windows Remote Management](using-windows-remote-management.md).</span></span> <span data-ttu-id="ac537-130">Las interfaces de C++ correspondientes son [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) y [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex).</span><span class="sxs-lookup"><span data-stu-id="ac537-130">The corresponding C++ interfaces are [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) and [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="ac537-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ac537-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac537-132">Acerca de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="ac537-132">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="ac537-133">Usar Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="ac537-133">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="ac537-134">Scripting en Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="ac537-134">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="ac537-135">Referencia de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="ac537-135">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 




