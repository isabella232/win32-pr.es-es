---
title: Clase StreamSelectOperation
description: Registra un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por GetMuteAsync y proporciona un método que devuelve los resultados de la operación. | Clase StreamSelectOperation
ms.assetid: 681142B4-AECD-42D0-A2D4-494E69A29025
keywords:
- Clase StreamSelectOperation API de streaming de multimedia
- Clase StreamSelectOperation API de streaming de multimedia, descrita
topic_type:
- apiref
api_name:
- StreamSelectOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a4a19ff2826f0f2ea3e5ef01841ce482d2f293a3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280093"
---
# <a name="streamselectoperation-class"></a><span data-ttu-id="d8b86-106">Clase StreamSelectOperation</span><span class="sxs-lookup"><span data-stu-id="d8b86-106">StreamSelectOperation class</span></span>

<span data-ttu-id="d8b86-107">Registra un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) y proporciona un método que devuelve los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="d8b86-107">Registers an event handler that is invoked when the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) completes, and provides a method that returns the results of the operation.</span></span>

<span data-ttu-id="d8b86-108">**StreamSelectOperation** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d8b86-108">**StreamSelectOperation** has these types of members:</span></span>

-   [<span data-ttu-id="d8b86-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="d8b86-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="d8b86-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d8b86-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d8b86-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="d8b86-111">Methods</span></span>

<span data-ttu-id="d8b86-112">La clase **StreamSelectOperation** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d8b86-112">The **StreamSelectOperation** class has these methods.</span></span>



| <span data-ttu-id="d8b86-113">Método</span><span class="sxs-lookup"><span data-stu-id="d8b86-113">Method</span></span>                                                 | <span data-ttu-id="d8b86-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8b86-114">Description</span></span>                                                                                                                                       |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8b86-115">**GetResults**</span><span class="sxs-lookup"><span data-stu-id="d8b86-115">**GetResults**</span></span>](streamselectoperation-getresults.md) | <span data-ttu-id="d8b86-116">Devuelve los resultados de la operación asincrónica iniciada por [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d8b86-116">Returns the results of the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d8b86-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d8b86-117">Properties</span></span>

<span data-ttu-id="d8b86-118">La clase **StreamSelectOperation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d8b86-118">The **StreamSelectOperation** class has these properties.</span></span>



| <span data-ttu-id="d8b86-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d8b86-119">Property</span></span>                                                        | <span data-ttu-id="d8b86-120">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="d8b86-120">Access type</span></span>           | <span data-ttu-id="d8b86-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8b86-121">Description</span></span>                                                                                                                                                                             |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8b86-122">**Completed**</span><span class="sxs-lookup"><span data-stu-id="d8b86-122">**Completed**</span></span>](streamselectoperation-completed.md)<br/> | <span data-ttu-id="d8b86-123">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d8b86-123">Read/write</span></span><br/> | <span data-ttu-id="d8b86-124">Obtiene o establece un controlador de eventos que se invoca cuando se completa la operación asincrónica iniciada por [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d8b86-124">Gets or sets an event handler that is invoked when the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) is completed.</span></span><br/> |



 

 

