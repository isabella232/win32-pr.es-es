---
title: Funciones del proveedor de transporte de WDS
description: Los proveedores de contenido definidos por el usuario pueden exponer las siguientes funciones de devolución de llamada al servidor de multidifusión.
ms.assetid: 30ec1969-4e90-458e-8a9f-39a7bbf4cd79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2e67747d8ef5738a4bf3bee8ff2ffb3b35cf43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779392"
---
# <a name="wds-transport-provider-functions"></a><span data-ttu-id="22fb6-103">Funciones del proveedor de transporte de WDS</span><span class="sxs-lookup"><span data-stu-id="22fb6-103">WDS Transport Provider Functions</span></span>

<span data-ttu-id="22fb6-104">Los proveedores de contenido definidos por el usuario pueden exponer las siguientes funciones de devolución de llamada al servidor de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="22fb6-104">User-defined content providers can expose the following callback functions to the multicast server.</span></span>



| <span data-ttu-id="22fb6-105">Función</span><span class="sxs-lookup"><span data-stu-id="22fb6-105">Function</span></span>                                                                               | <span data-ttu-id="22fb6-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="22fb6-106">Description</span></span>                                                                                                             |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22fb6-107">*WdsTransportProviderCloseContent*</span><span class="sxs-lookup"><span data-stu-id="22fb6-107">*WdsTransportProviderCloseContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderclosecontent)             | <span data-ttu-id="22fb6-108">Cierra una secuencia de contenido especificada por un identificador.</span><span class="sxs-lookup"><span data-stu-id="22fb6-108">Closes a content stream specified by a handle.</span></span>                                                                          |
| [<span data-ttu-id="22fb6-109">*WdsTransportProviderCloseInstance*</span><span class="sxs-lookup"><span data-stu-id="22fb6-109">*WdsTransportProviderCloseInstance*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercloseinstance)           | <span data-ttu-id="22fb6-110">Cierra una instancia de un proveedor de contenido especificado por un identificador.</span><span class="sxs-lookup"><span data-stu-id="22fb6-110">Closes an instance of a content provider specified by a handle.</span></span>                                                         |
| [<span data-ttu-id="22fb6-111">*WdsTransportProviderCompareContent*</span><span class="sxs-lookup"><span data-stu-id="22fb6-111">*WdsTransportProviderCompareContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercomparecontent)         | <span data-ttu-id="22fb6-112">Compara una instancia y un nombre de contenido especificados con un flujo de contenido abierto para determinar si son iguales.</span><span class="sxs-lookup"><span data-stu-id="22fb6-112">Compares a specified content name and instance to an open content stream to determine if they are the same.</span></span>             |
| [<span data-ttu-id="22fb6-113">*WdsTransportProviderCreateInstance*</span><span class="sxs-lookup"><span data-stu-id="22fb6-113">*WdsTransportProviderCreateInstance*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercreateinstance)         | <span data-ttu-id="22fb6-114">Abre una nueva instancia de un proveedor de contenido.</span><span class="sxs-lookup"><span data-stu-id="22fb6-114">Opens a new instance of a content provider.</span></span>                                                                             |
| [<span data-ttu-id="22fb6-115">*WdsTransportProviderDumpState*</span><span class="sxs-lookup"><span data-stu-id="22fb6-115">*WdsTransportProviderDumpState*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderdumpstate)                   | <span data-ttu-id="22fb6-116">Indica al proveedor de transporte que imprima un resumen de su estado y cualquier otra información relevante en el registro de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="22fb6-116">Instructs the transport provider to print a summary of its state and any other relevant information to the tracing log.</span></span> |
| [<span data-ttu-id="22fb6-117">*WdsTransportProviderGetContentMetadata*</span><span class="sxs-lookup"><span data-stu-id="22fb6-117">*WdsTransportProviderGetContentMetadata*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentmetadata) | <span data-ttu-id="22fb6-118">Recupera los metadatos de una secuencia de contenido abierto.</span><span class="sxs-lookup"><span data-stu-id="22fb6-118">Retrieves metadata for an open content stream.</span></span>                                                                          |
| [<span data-ttu-id="22fb6-119">*WdsTransportProviderGetContentSize*</span><span class="sxs-lookup"><span data-stu-id="22fb6-119">*WdsTransportProviderGetContentSize*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentsize)         | <span data-ttu-id="22fb6-120">Recupera el tamaño de una secuencia de contenido abierto.</span><span class="sxs-lookup"><span data-stu-id="22fb6-120">Retrieves the size of an open content stream.</span></span>                                                                           |
| [<span data-ttu-id="22fb6-121">*WdsTransportProviderInitialize*</span><span class="sxs-lookup"><span data-stu-id="22fb6-121">*WdsTransportProviderInitialize*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize)                 | <span data-ttu-id="22fb6-122">Inicializa un proveedor de contenido.</span><span class="sxs-lookup"><span data-stu-id="22fb6-122">Initializes a content provider.</span></span>                                                                                         |
| [<span data-ttu-id="22fb6-123">*WdsTransportProviderOpenContent*</span><span class="sxs-lookup"><span data-stu-id="22fb6-123">*WdsTransportProviderOpenContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideropencontent)               | <span data-ttu-id="22fb6-124">Abre una nueva vista estática de una secuencia de contenido.</span><span class="sxs-lookup"><span data-stu-id="22fb6-124">Opens a new static view of a content stream.</span></span>                                                                            |
| [<span data-ttu-id="22fb6-125">*WdsTransportProviderReadContent*</span><span class="sxs-lookup"><span data-stu-id="22fb6-125">*WdsTransportProviderReadContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderreadcontent)               | <span data-ttu-id="22fb6-126">Lee el contenido de una secuencia de contenido abierto.</span><span class="sxs-lookup"><span data-stu-id="22fb6-126">Reads content from an open content stream.</span></span>                                                                              |
| [<span data-ttu-id="22fb6-127">*WdsTransportProviderRefreshSettings*</span><span class="sxs-lookup"><span data-stu-id="22fb6-127">*WdsTransportProviderRefreshSettings*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderrefreshsettings)       | <span data-ttu-id="22fb6-128">Indica al proveedor de transporte que debe releer cualquier configuración relevante.</span><span class="sxs-lookup"><span data-stu-id="22fb6-128">Instructs the transport provider to reread any relevant settings.</span></span>                                                       |
| [<span data-ttu-id="22fb6-129">*WdsTransportProviderShutdown*</span><span class="sxs-lookup"><span data-stu-id="22fb6-129">*WdsTransportProviderShutdown*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidershutdown)                     | <span data-ttu-id="22fb6-130">Shutsdown el proveedor de contenido.</span><span class="sxs-lookup"><span data-stu-id="22fb6-130">Shutsdown the content provider.</span></span>                                                                                         |
| [<span data-ttu-id="22fb6-131">*WdsTransportProviderUserAccessCheck*</span><span class="sxs-lookup"><span data-stu-id="22fb6-131">*WdsTransportProviderUserAccessCheck*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideruseraccesscheck)       | <span data-ttu-id="22fb6-132">Especifica el acceso a una secuencia de contenido basándose en el token de un usuario.</span><span class="sxs-lookup"><span data-stu-id="22fb6-132">Specifies access to a content stream based on a user's token.</span></span>                                                           |



 

 

 




