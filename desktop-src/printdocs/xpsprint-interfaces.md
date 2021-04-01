---
description: .
ms.assetid: f575109e-e9c4-4db5-945c-7c96b6b5d613
title: Interfaces de la API de impresión XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 828e999417354678d77ad1de8c29beb5956f7762
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812560"
---
# <a name="xps-print-api-interfaces"></a><span data-ttu-id="ef5ec-103">Interfaces de la API de impresión XPS</span><span class="sxs-lookup"><span data-stu-id="ef5ec-103">XPS Print API Interfaces</span></span>

<span data-ttu-id="ef5ec-104">\[Las interfaces descritas en esta sección están desusadas.</span><span class="sxs-lookup"><span data-stu-id="ef5ec-104">\[The interfaces described in this section are deprecated.</span></span> <span data-ttu-id="ef5ec-105">En su lugar, las aplicaciones cliente deben usar la [API Print Document Package](./tailored-app-printing-api.md) .\]</span><span class="sxs-lookup"><span data-stu-id="ef5ec-105">Client applications should use the [Print Document Package API](./tailored-app-printing-api.md) instead.\]</span></span>

<span data-ttu-id="ef5ec-106">\[IXpsPrintJob no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="ef5ec-106">\[IXpsPrintJob is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="ef5ec-107">\]</span><span class="sxs-lookup"><span data-stu-id="ef5ec-107">\]</span></span>

<span data-ttu-id="ef5ec-108">\[IXpsPrintJobStream no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="ef5ec-108">\[IXpsPrintJobStream is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="ef5ec-109">\]</span><span class="sxs-lookup"><span data-stu-id="ef5ec-109">\]</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ef5ec-110">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ef5ec-110">In this section</span></span>



| <span data-ttu-id="ef5ec-111">Interfaz</span><span class="sxs-lookup"><span data-stu-id="ef5ec-111">Interface</span></span>                                                   | <span data-ttu-id="ef5ec-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef5ec-112">Description</span></span>                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef5ec-113">**IXpsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="ef5ec-113">**IXpsPrintJob**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjob)<br/>             | <span data-ttu-id="ef5ec-114">Proporciona acceso a un trabajo de impresión que está actualmente en curso.</span><span class="sxs-lookup"><span data-stu-id="ef5ec-114">Provides access to a print job that is currently in progress.</span></span><br/>                  |
| [<span data-ttu-id="ef5ec-115">**IXpsPrintJobStream**</span><span class="sxs-lookup"><span data-stu-id="ef5ec-115">**IXpsPrintJobStream**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjobstream)<br/> | <span data-ttu-id="ef5ec-116">Una interfaz de secuencia de solo escritura en la que una aplicación escribe datos del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="ef5ec-116">A write-only stream interface into which an application writes print job data.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="ef5ec-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ef5ec-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef5ec-118">Documentos</span><span class="sxs-lookup"><span data-stu-id="ef5ec-118">Documents</span></span>](./jobbindalldocuments.md)
</dt> <dt>

[<span data-ttu-id="ef5ec-119">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="ef5ec-119">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

