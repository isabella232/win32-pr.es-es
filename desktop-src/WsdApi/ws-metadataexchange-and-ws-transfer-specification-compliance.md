---
description: Antes del 2006 de agosto, WS-MetadataExchange definido su propio método get Metadata Exchange, que se usó en el perfil de dispositivos para servicios web (DPWS).
ms.assetid: 2441beac-ee40-405a-8e98-8b8d65477911
title: Compatibilidad de la especificación de WS-MetadataExchange y WS-Transfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e6ecad5224256f35b2157088ce091e8bd5751c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155801"
---
# <a name="ws-metadataexchange-and-ws-transfer-specification-compliance"></a><span data-ttu-id="3ca72-103">Compatibilidad de la especificación de WS-MetadataExchange y WS-Transfer</span><span class="sxs-lookup"><span data-stu-id="3ca72-103">WS-MetadataExchange and WS-Transfer Specification Compliance</span></span>

<span data-ttu-id="3ca72-104">Antes del 2006 de agosto de [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) , se definió su propio método [Get](get--metadata-exchange--http-request-and-message.md) Metadata Exchange, que se usaba en el [Perfil de dispositivos para servicios web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span><span class="sxs-lookup"><span data-stu-id="3ca72-104">Before August 2006, [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) defined its own [Get](get--metadata-exchange--http-request-and-message.md) metadata exchange method, which was used by [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="3ca72-105">La versión 1,1 de la especificación de WS-MetadataExchange ha reemplazado este método por el método get definido en la especificación de WS-Transfer.</span><span class="sxs-lookup"><span data-stu-id="3ca72-105">The WS-MetadataExchange specification version 1.1 replaced this method with the Get method defined in the WS-Transfer specification.</span></span>

<span data-ttu-id="3ca72-106">En el modelo actual, WS-Transfer proporciona el método [Get](get--metadata-exchange--http-request-and-message.md) y no hace referencia al tipo del cuerpo.</span><span class="sxs-lookup"><span data-stu-id="3ca72-106">In the current model, WS-Transfer provides the [Get](get--metadata-exchange--http-request-and-message.md) method and makes no reference to the type of the body.</span></span> <span data-ttu-id="3ca72-107">WS-MetadataExchange describe el formato del cuerpo y un mecanismo para empaquetar varios fragmentos de metadatos en una sola respuesta, y DPWS describe partes específicas de los metadatos que un servicio debe incluir en una respuesta de metadatos.</span><span class="sxs-lookup"><span data-stu-id="3ca72-107">WS-MetadataExchange describes the format of the body and a mechanism for packaging multiple pieces of metadata in a single response, and DPWS describes specific pieces of metadata that a service should include in a metadata response.</span></span>

<span data-ttu-id="3ca72-108">WSDAPI no es totalmente compatible con la especificación WS-Transfer.</span><span class="sxs-lookup"><span data-stu-id="3ca72-108">WSDAPI does not fully support the WS-Transfer specification.</span></span> <span data-ttu-id="3ca72-109">Dado que solo se requiere el método [Get](get--metadata-exchange--http-request-and-message.md) para los dispositivos, no se han implementado otras partes de WS-Transfer.</span><span class="sxs-lookup"><span data-stu-id="3ca72-109">Because only the [Get](get--metadata-exchange--http-request-and-message.md) method is required for devices, no other portions of WS-Transfer have been implemented.</span></span> <span data-ttu-id="3ca72-110">Además, WSDAPI no implementa el método GetMetadata opcional que se describe en WS-MetadataExchange.</span><span class="sxs-lookup"><span data-stu-id="3ca72-110">Also, WSDAPI does not implement the optional GetMetadata method described in WS-MetadataExchange.</span></span>

 

 



