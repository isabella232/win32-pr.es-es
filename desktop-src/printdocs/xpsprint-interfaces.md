---
description: Interfaces de LA API de impresión XPS
ms.assetid: f575109e-e9c4-4db5-945c-7c96b6b5d613
title: Interfaces de LA API de impresión XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47cd01c169c82a9e3210f281ec6c44fa206c40b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105193"
---
# <a name="xps-print-api-interfaces"></a><span data-ttu-id="f4520-103">Interfaces de LA API de impresión XPS</span><span class="sxs-lookup"><span data-stu-id="f4520-103">XPS Print API Interfaces</span></span>

<span data-ttu-id="f4520-104">\[Las interfaces descritas en esta sección están en desuso.</span><span class="sxs-lookup"><span data-stu-id="f4520-104">\[The interfaces described in this section are deprecated.</span></span> <span data-ttu-id="f4520-105">Las aplicaciones cliente deben usar [la API Print Document Package en](./tailored-app-printing-api.md) su lugar.\]</span><span class="sxs-lookup"><span data-stu-id="f4520-105">Client applications should use the [Print Document Package API](./tailored-app-printing-api.md) instead.\]</span></span>

<span data-ttu-id="f4520-106">\[IXpsPrintJob no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="f4520-106">\[IXpsPrintJob is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="f4520-107">\]</span><span class="sxs-lookup"><span data-stu-id="f4520-107">\]</span></span>

<span data-ttu-id="f4520-108">\[IXpsPrintJobStream no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="f4520-108">\[IXpsPrintJobStream is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="f4520-109">\]</span><span class="sxs-lookup"><span data-stu-id="f4520-109">\]</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f4520-110">En esta sección</span><span class="sxs-lookup"><span data-stu-id="f4520-110">In this section</span></span>



| <span data-ttu-id="f4520-111">Interfaz</span><span class="sxs-lookup"><span data-stu-id="f4520-111">Interface</span></span>                                                   | <span data-ttu-id="f4520-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4520-112">Description</span></span>                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4520-113">**IXpsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="f4520-113">**IXpsPrintJob**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjob)<br/>             | <span data-ttu-id="f4520-114">Proporciona acceso a un trabajo de impresión que está actualmente en curso.</span><span class="sxs-lookup"><span data-stu-id="f4520-114">Provides access to a print job that is currently in progress.</span></span><br/>                  |
| [<span data-ttu-id="f4520-115">**IXpsPrintJobStream**</span><span class="sxs-lookup"><span data-stu-id="f4520-115">**IXpsPrintJobStream**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjobstream)<br/> | <span data-ttu-id="f4520-116">Interfaz de secuencia de solo escritura en la que una aplicación escribe datos del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="f4520-116">A write-only stream interface into which an application writes print job data.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="f4520-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f4520-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4520-118">Documentos</span><span class="sxs-lookup"><span data-stu-id="f4520-118">Documents</span></span>](./jobbindalldocuments.md)
</dt> <dt>

[<span data-ttu-id="f4520-119">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="f4520-119">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

