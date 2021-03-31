---
title: Referencia de las tiendas en línea de tipo 2
description: Referencia de las tiendas en línea de tipo 2
ms.assetid: b3f580cc-b02d-4312-a7a1-a35778a222bc
keywords:
- Windows Media Player tiendas en línea, referencia
- tiendas en línea, referencia
- tipo 2 tiendas en línea, referencia
- referencia de las tiendas en línea de tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c164ad74481030a52cd31605b29833d3bfbd3f1d
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "103789291"
---
# <a name="reference-for-type-2-online-stores"></a><span data-ttu-id="f8969-107">Referencia de las tiendas en línea de tipo 2</span><span class="sxs-lookup"><span data-stu-id="f8969-107">Reference for Type 2 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="f8969-108">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="f8969-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="f8969-109">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="f8969-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="f8969-110">Windows Media Player 10 o posterior proporciona objetos, interfaces, propiedades y métodos que admiten las tiendas en línea de tipo 2.</span><span class="sxs-lookup"><span data-stu-id="f8969-110">Windows Media Player 10 or later provides objects, interfaces, properties, and methods that support type 2 online stores.</span></span> <span data-ttu-id="f8969-111">En las secciones siguientes se documentan en detalle.</span><span class="sxs-lookup"><span data-stu-id="f8969-111">The following sections document these in detail.</span></span>



| <span data-ttu-id="f8969-112">Sección</span><span class="sxs-lookup"><span data-stu-id="f8969-112">Section</span></span>                                                                                                        | <span data-ttu-id="f8969-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8969-113">Description</span></span>                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8969-114">Interfaz IWMPSubscriptionService</span><span class="sxs-lookup"><span data-stu-id="f8969-114">IWMPSubscriptionService Interface</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)                                               | <span data-ttu-id="f8969-115">Proporciona métodos para aumentar la administración de derechos digitales (DRM) e iniciar procesos en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="f8969-115">Provides methods to augment digital rights management (DRM) and initiate background processes.</span></span>                                                                              |
| [<span data-ttu-id="f8969-116">Interfaz IWMPSubscriptionService2</span><span class="sxs-lookup"><span data-stu-id="f8969-116">IWMPSubscriptionService2 Interface</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)                                             | <span data-ttu-id="f8969-117">Proporciona métodos para iniciar procesos en segundo plano, proporcionar información sobre la actividad de la tienda en línea y proporcionar un puntero a la interfaz principal de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f8969-117">Provides methods to initiate background processes, to provide information about online store activity, and to provide a pointer to the Windows Media Player core interface.</span></span> |
| [<span data-ttu-id="f8969-118">Interfaz IWMPSubscriptionServiceCallback</span><span class="sxs-lookup"><span data-stu-id="f8969-118">IWMPSubscriptionServiceCallback Interface</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback)                               | <span data-ttu-id="f8969-119">Define un método que las tiendas en línea usan para notificar a Windows Media Player cuando se completa un proceso en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="f8969-119">Defines a method that online stores use to notify Windows Media Player when a background process is completed.</span></span>                                                              |
| [<span data-ttu-id="f8969-120">WMPNotifySubscriptionPluginAddRemove</span><span class="sxs-lookup"><span data-stu-id="f8969-120">WMPNotifySubscriptionPluginAddRemove</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-wmpnotifysubscriptionpluginaddremove)                               | <span data-ttu-id="f8969-121">Función que se usa para notificar a Windows Media Player que se ha instalado o desinstalado un complemento.</span><span class="sxs-lookup"><span data-stu-id="f8969-121">A function used to notify Windows Media Player that a plug-in has been installed or uninstalled.</span></span>                                                                            |
| [<span data-ttu-id="f8969-122">Objeto DownloadCollection</span><span class="sxs-lookup"><span data-stu-id="f8969-122">DownloadCollection Object</span></span>](downloadcollection-object.md)                                                     | <span data-ttu-id="f8969-123">Proporciona métodos y propiedades para administrar colecciones de elementos de descarga.</span><span class="sxs-lookup"><span data-stu-id="f8969-123">Provides methods and properties to manage collections of download items.</span></span>                                                                                                    |
| [<span data-ttu-id="f8969-124">Objeto DownloadItem</span><span class="sxs-lookup"><span data-stu-id="f8969-124">DownloadItem Object</span></span>](downloaditem-object.md)                                                                 | <span data-ttu-id="f8969-125">Proporciona métodos y propiedades relacionados con las solicitudes de descarga.</span><span class="sxs-lookup"><span data-stu-id="f8969-125">Provides methods and properties relating to download requests.</span></span>                                                                                                              |
| [<span data-ttu-id="f8969-126">Objeto DownloadManager</span><span class="sxs-lookup"><span data-stu-id="f8969-126">DownloadManager Object</span></span>](downloadmanager-object.md)                                                           | <span data-ttu-id="f8969-127">Proporciona métodos para administrar colecciones de descargas.</span><span class="sxs-lookup"><span data-stu-id="f8969-127">Provides methods to manage download collections.</span></span>                                                                                                                            |
| [<span data-ttu-id="f8969-128">Objeto externo para las tiendas en línea de tipo 2</span><span class="sxs-lookup"><span data-stu-id="f8969-128">External Object for Type 2 Online Stores</span></span>](external-object-for-type-2-online-stores.md)                       | <span data-ttu-id="f8969-129">Proporciona propiedades, métodos y un evento accesible desde páginas web de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="f8969-129">Provides properties, methods, and an event accessible from online store webpages.</span></span>                                                                                           |
| [<span data-ttu-id="f8969-130">Enumeraciones de las tiendas en línea de tipo 2</span><span class="sxs-lookup"><span data-stu-id="f8969-130">Enumerations for Type 2 Online Stores</span></span>](enumerations-for-type-2-online-stores.md)                             | <span data-ttu-id="f8969-131">Describe las enumeraciones usadas por las tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="f8969-131">Describes enumerations used by online stores.</span></span>                                                                                                                               |
| [<span data-ttu-id="f8969-132">Convención de trabajo de Windows Media Player BITS</span><span class="sxs-lookup"><span data-stu-id="f8969-132">Windows Media Player BITS Job Convention</span></span>](windows-media-player-bits-job-convention.md)                       | <span data-ttu-id="f8969-133">Describe una Convención para usar el Servicio de transferencia inteligente en segundo plano (BITS).</span><span class="sxs-lookup"><span data-stu-id="f8969-133">Describes a convention for using the Background Intelligent Transfer Service (BITS).</span></span>                                                                                        |
| [<span data-ttu-id="f8969-134">Claves del registro y entradas para una tienda en línea de tipo 2</span><span class="sxs-lookup"><span data-stu-id="f8969-134">Registry Keys and Entries for a Type 2 Online Store</span></span>](registry-keys-and-entries-for-a-type-2-online-store.md) | <span data-ttu-id="f8969-135">Describe las entradas del registro que una tienda en línea debe crear en el registro del equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="f8969-135">Describes registry entries that an online store must create in the registry on the user's computer.</span></span>                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="f8969-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f8969-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8969-137">**Tipo 2 tiendas en línea**</span><span class="sxs-lookup"><span data-stu-id="f8969-137">**Type 2 Online Stores**</span></span>](type-2-online-stores.md)
</dt> </dl>

 

 




