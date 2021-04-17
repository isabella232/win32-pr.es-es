---
description: Monitor de red captura el tráfico de red para la visualización y el análisis. Permite realizar tareas como el análisis de datos capturados anteriormente en métodos definidos por el usuario y extraer datos de analizadores de protocolos definidos.
ms.assetid: a70b6e22-e744-4760-b878-9ee35428fed5
title: Monitor de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51a57dd2373d7a10fedd68a72dbc4021efdb921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546350"
---
# <a name="network-monitor"></a><span data-ttu-id="9b6e7-104">Monitor de red</span><span class="sxs-lookup"><span data-stu-id="9b6e7-104">Network Monitor</span></span>

## <a name="purpose"></a><span data-ttu-id="9b6e7-105">Propósito</span><span class="sxs-lookup"><span data-stu-id="9b6e7-105">Purpose</span></span>

<span data-ttu-id="9b6e7-106">Monitor de red captura el tráfico de red para la visualización y el análisis.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-106">Network Monitor captures network traffic for display and analysis.</span></span> <span data-ttu-id="9b6e7-107">Permite realizar tareas como el análisis de datos capturados anteriormente en métodos definidos por el usuario y extraer datos de analizadores de protocolos definidos.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-107">It enables you to perform tasks such as analyzing previously captured data in user-defined methods and extract data from defined protocol parsers.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="9b6e7-108">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="9b6e7-108">Developer audience</span></span>

<span data-ttu-id="9b6e7-109">Se puede tener acceso a todos los conjuntos de API proporcionados por Monitor de red con C/C++.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-109">All API sets provided by Network Monitor can be accessed using C/C++.</span></span> <span data-ttu-id="9b6e7-110">Los desarrolladores que también trabajan con [*proveedores de paquetes de red*](n.md) también deben estar familiarizados con com.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-110">Those developers also working with [*network packet providers*](n.md) must also be familiar with COM.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="9b6e7-111">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="9b6e7-111">Run-time requirements</span></span>

<span data-ttu-id="9b6e7-112">Para llamar a desde la API de Monitor de red, debe ejecutar en Windows NT Server 4,0, Windows 2000 Server o Windows Server 2003, o tener instalado Microsoft Systems Management Server.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-112">To call from the Network Monitor API, you must be running on Windows NT Server 4.0, Windows 2000 Server, or Windows Server 2003, or have Microsoft Systems Management Server installed.</span></span>

<span data-ttu-id="9b6e7-113">El controlador NPP y las características admitidas incluyen todas las versiones de Windows NT 4,0 y Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-113">The NPP driver and supported features include all versions of Windows NT 4.0 and Windows 2000 Server.</span></span>

> [!Note]  
> <span data-ttu-id="9b6e7-114">Monitor de red 2,1 y versiones anteriores no se admiten en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-114">Network Monitor 2.1 and earlier are not supported on Windows Vista and later.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="9b6e7-115">En esta sección</span><span class="sxs-lookup"><span data-stu-id="9b6e7-115">In this section</span></span>



| <span data-ttu-id="9b6e7-116">Tema</span><span class="sxs-lookup"><span data-stu-id="9b6e7-116">Topic</span></span>                                                                 | <span data-ttu-id="9b6e7-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b6e7-117">Description</span></span>                                                                                           |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b6e7-118">SDK de Monitor de red</span><span class="sxs-lookup"><span data-stu-id="9b6e7-118">The Network Monitor SDK</span></span>](the-network-monitor-sdk.md)<br/>     | <span data-ttu-id="9b6e7-119">Introducción al SDK de Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-119">Introduction to the Network Monitor SDK.</span></span><br/>                                                   |
| [<span data-ttu-id="9b6e7-120">Acerca de Monitor de red 2,1</span><span class="sxs-lookup"><span data-stu-id="9b6e7-120">About Network Monitor 2.1</span></span>](about-network-monitor-2-1.md)<br/> | <span data-ttu-id="9b6e7-121">Monitor de red conceptos y servicios.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-121">Network Monitor concepts and services.</span></span><br/>                                                     |
| [<span data-ttu-id="9b6e7-122">Uso de Monitor de red 2,1</span><span class="sxs-lookup"><span data-stu-id="9b6e7-122">Using Network Monitor 2.1</span></span>](using-network-monitor-2-1.md)<br/> | <span data-ttu-id="9b6e7-123">Temas relacionados con tareas que describen cómo usar funciones de Monitor de red y componentes COM.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-123">Task-related topics that describe how to use Network Monitor functions and COM components.</span></span><br/> |
| [<span data-ttu-id="9b6e7-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="9b6e7-124">Reference</span></span>](reference.md)<br/>                                 | <span data-ttu-id="9b6e7-125">Temas de referencia para Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-125">Reference topics for Network Monitor.</span></span><br/>                                                      |
| [<span data-ttu-id="9b6e7-126">Glosario</span><span class="sxs-lookup"><span data-stu-id="9b6e7-126">Glossary</span></span>](glossary.md)<br/>                                   | <span data-ttu-id="9b6e7-127">Definiciones y terminología para Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="9b6e7-127">Definitions and terminology for Network Monitor.</span></span><br/>                                           |



 

 

 




