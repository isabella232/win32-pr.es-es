---
description: Interfaces de API de firma digital XPS
ms.assetid: 44244035-f7d5-47f1-b4d8-b895562be855
title: Interfaces de API de firma digital XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160fc532ed90cb41e4d0cb524daba87f72edefd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688388"
---
# <a name="xps-digital-signature-api-interfaces"></a><span data-ttu-id="7c7bd-103">Interfaces de API de firma digital XPS</span><span class="sxs-lookup"><span data-stu-id="7c7bd-103">XPS Digital Signature API Interfaces</span></span>

## <a name="contents"></a><span data-ttu-id="7c7bd-104">Contenido</span><span class="sxs-lookup"><span data-stu-id="7c7bd-104">Contents</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7c7bd-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="7c7bd-105">In this section</span></span>



| <span data-ttu-id="7c7bd-106">Interfaz</span><span class="sxs-lookup"><span data-stu-id="7c7bd-106">Interface</span></span>                                                                           | <span data-ttu-id="7c7bd-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c7bd-107">Description</span></span>                                                                                         |
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c7bd-108">**IXpsSignature**</span><span class="sxs-lookup"><span data-stu-id="7c7bd-108">**IXpsSignature**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature)<br/>                                   | <span data-ttu-id="7c7bd-109">Representa una firma digital única.</span><span class="sxs-lookup"><span data-stu-id="7c7bd-109">Represents a single digital signature.</span></span><br/>                                                   |
| [<span data-ttu-id="7c7bd-110">**IXpsSignatureBlock**</span><span class="sxs-lookup"><span data-stu-id="7c7bd-110">**IXpsSignatureBlock**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock)<br/>                         | <span data-ttu-id="7c7bd-111">Representa un bloque de solicitudes de firma que se almacenan en un elemento SignatureDefinitions.</span><span class="sxs-lookup"><span data-stu-id="7c7bd-111">Represents a block of signature requests that are stored in a SignatureDefinitions part.</span></span><br/> |
| [<span data-ttu-id="7c7bd-112">**IXpsSignatureBlockCollection**</span><span class="sxs-lookup"><span data-stu-id="7c7bd-112">**IXpsSignatureBlockCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)<br/>     | <span data-ttu-id="7c7bd-113">Colección de interfaces [**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) .</span><span class="sxs-lookup"><span data-stu-id="7c7bd-113">A collection of [**IXpsSignatureBlock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock) interfaces.</span></span><br/>             |
| [<span data-ttu-id="7c7bd-114">**IXpsSignatureCollection**</span><span class="sxs-lookup"><span data-stu-id="7c7bd-114">**IXpsSignatureCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)<br/>               | <span data-ttu-id="7c7bd-115">Colección de punteros de interfaz [**IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) .</span><span class="sxs-lookup"><span data-stu-id="7c7bd-115">A collection of [**IXpsSignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature) interface pointers.</span></span><br/>               |
| [<span data-ttu-id="7c7bd-116">**IXpsSignatureManager**</span><span class="sxs-lookup"><span data-stu-id="7c7bd-116">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)<br/>                     | <span data-ttu-id="7c7bd-117">Administra las firmas digitales y las solicitudes de firma digital de un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="7c7bd-117">Manages the digital signatures and digital signature requests of an XPS document.</span></span><br/>        |
| [<span data-ttu-id="7c7bd-118">**IXpsSignatureRequest**</span><span class="sxs-lookup"><span data-stu-id="7c7bd-118">**IXpsSignatureRequest**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest)<br/>                     | <span data-ttu-id="7c7bd-119">Obtiene acceso a los componentes de una solicitud de firma.</span><span class="sxs-lookup"><span data-stu-id="7c7bd-119">Accesses the components of a signature request.</span></span><br/>                                          |
| [<span data-ttu-id="7c7bd-120">**IXpsSignatureRequestCollection**</span><span class="sxs-lookup"><span data-stu-id="7c7bd-120">**IXpsSignatureRequestCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)<br/> | <span data-ttu-id="7c7bd-121">Colección de interfaces [**IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) .</span><span class="sxs-lookup"><span data-stu-id="7c7bd-121">A collection of [**IXpsSignatureRequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest) interfaces.</span></span><br/>         |
| [<span data-ttu-id="7c7bd-122">**IXpsSigningOptions**</span><span class="sxs-lookup"><span data-stu-id="7c7bd-122">**IXpsSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)<br/>                         | <span data-ttu-id="7c7bd-123">Proporciona acceso a las opciones de firma individuales que utilizan las nuevas firmas.</span><span class="sxs-lookup"><span data-stu-id="7c7bd-123">Provides access to the individual signing options that are used by new signatures.</span></span><br/>       |



 

 

 




