---
description: La interfaz IUpdateService define las siguientes propiedades.
ms.assetid: 33bc28e8-0b83-4d58-a03e-ccf2a97887e6
title: Propiedades de IUpdateService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ff3cf92c89a5ba02b7d95f1a1c99f33de3202d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497602"
---
# <a name="iupdateservice-properties"></a><span data-ttu-id="cb503-103">Propiedades de IUpdateService</span><span class="sxs-lookup"><span data-stu-id="cb503-103">IUpdateService Properties</span></span>

<span data-ttu-id="cb503-104">La interfaz [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) define las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="cb503-104">The [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) interface defines the following properties.</span></span>



| <span data-ttu-id="cb503-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cb503-105">Property</span></span>                                                              | <span data-ttu-id="cb503-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb503-106">Description</span></span>                                                                                     |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb503-107">**CanRegisterWithAU**</span><span class="sxs-lookup"><span data-stu-id="cb503-107">**CanRegisterWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_canregisterwithau)         | <span data-ttu-id="cb503-108">Obtiene un valor booleano que indica si el servicio se puede registrar con Actualizaciones automáticas.</span><span class="sxs-lookup"><span data-stu-id="cb503-108">Gets a Boolean value that indicates whether the service can register with Automatic Updates.</span></span>    |
| [<span data-ttu-id="cb503-109">**ContentValidationCert**</span><span class="sxs-lookup"><span data-stu-id="cb503-109">**ContentValidationCert**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_contentvalidationcert) | <span data-ttu-id="cb503-110">Obtiene un hash SHA-1 del certificado que se utiliza para firmar el contenido del servicio.</span><span class="sxs-lookup"><span data-stu-id="cb503-110">Gets an SHA-1 hash of the certificate that is used to sign the contents of the service.</span></span>         |
| [<span data-ttu-id="cb503-111">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="cb503-111">**ExpirationDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_expirationdate)               | <span data-ttu-id="cb503-112">Obtiene la fecha en la que el archivo. cab de autorización expira.</span><span class="sxs-lookup"><span data-stu-id="cb503-112">Gets the date on which the authorization cabinet file expires.</span></span>                                  |
| [<span data-ttu-id="cb503-113">**IsManaged (**</span><span class="sxs-lookup"><span data-stu-id="cb503-113">**IsManaged**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_ismanaged)                         | <span data-ttu-id="cb503-114">Obtiene un valor booleano que indica si un servicio es un servicio administrado.</span><span class="sxs-lookup"><span data-stu-id="cb503-114">Gets a Boolean value that indicates whether a service is a managed service.</span></span>                     |
| [<span data-ttu-id="cb503-115">**IsRegisteredWithAU**</span><span class="sxs-lookup"><span data-stu-id="cb503-115">**IsRegisteredWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isregisteredwithau)       | <span data-ttu-id="cb503-116">Obtiene un valor booleano que indica si un servicio está registrado con Actualizaciones automáticas.</span><span class="sxs-lookup"><span data-stu-id="cb503-116">Gets a Boolean value that indicates whether a service is registered with Automatic Updates.</span></span>     |
| [<span data-ttu-id="cb503-117">**IsScanPackageService**</span><span class="sxs-lookup"><span data-stu-id="cb503-117">**IsScanPackageService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isscanpackageservice)   | <span data-ttu-id="cb503-118">Obtiene un valor booleano que indica si un servicio se basa en un paquete de examen.</span><span class="sxs-lookup"><span data-stu-id="cb503-118">Gets a Boolean value that indicates whether a service is based on a scan package.</span></span>               |
| [<span data-ttu-id="cb503-119">**IssueDate**</span><span class="sxs-lookup"><span data-stu-id="cb503-119">**IssueDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_issuedate)                         | <span data-ttu-id="cb503-120">Obtiene la fecha en la que se emitió el archivo. cab de autorización.</span><span class="sxs-lookup"><span data-stu-id="cb503-120">Gets the date on which the authorization cabinet file was issued.</span></span>                               |
| [<span data-ttu-id="cb503-121">**Name**</span><span class="sxs-lookup"><span data-stu-id="cb503-121">**Name**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_name)                                   | <span data-ttu-id="cb503-122">Obtiene el nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="cb503-122">Gets the name of the service.</span></span>                                                                   |
| [<span data-ttu-id="cb503-123">**OffersWindowsUpdates**</span><span class="sxs-lookup"><span data-stu-id="cb503-123">**OffersWindowsUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_offerswindowsupdates)   | <span data-ttu-id="cb503-124">Obtiene un valor booleano que indica si el servicio actual ofrece actualizaciones de actualizaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="cb503-124">Gets a Boolean value indicates whether the current service offers updates from Windows Updates.</span></span> |
| [<span data-ttu-id="cb503-125">**RedirectUrls**</span><span class="sxs-lookup"><span data-stu-id="cb503-125">**RedirectUrls**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_redirecturls)                   | <span data-ttu-id="cb503-126">Obtiene la dirección URL del archivo. cab del redirector.</span><span class="sxs-lookup"><span data-stu-id="cb503-126">Gets the URL for the redirector cabinet file.</span></span>                                                   |
| [<span data-ttu-id="cb503-127">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="cb503-127">**ServiceID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceid)                         | <span data-ttu-id="cb503-128">Obtiene el identificador de un servicio.</span><span class="sxs-lookup"><span data-stu-id="cb503-128">Gets the identifier for a service.</span></span>                                                              |
| [<span data-ttu-id="cb503-129">**ServiceUrl**</span><span class="sxs-lookup"><span data-stu-id="cb503-129">**ServiceUrl**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceurl)                       | <span data-ttu-id="cb503-130">Obtiene la dirección URL para el servicio.</span><span class="sxs-lookup"><span data-stu-id="cb503-130">Gets the URL for the service.</span></span>                                                                   |
| [<span data-ttu-id="cb503-131">**SetupPrefix**</span><span class="sxs-lookup"><span data-stu-id="cb503-131">**SetupPrefix**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_setupprefix)                     | <span data-ttu-id="cb503-132">Obtiene el prefijo de los archivos de instalación.</span><span class="sxs-lookup"><span data-stu-id="cb503-132">Gets the prefix for the setup files.</span></span>                                                            |



 

 

 



