---
title: Interfaz IUniversalOrchestrator
description: Una interfaz COM que proporciona métodos para permitir que un cliente se comunique con el orquestador universal.
ms.date: 01/14/2021
ms.topic: interface
ms.openlocfilehash: 6fa5dfd9f7853159645fbe3b543c228450f4e1c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/21/2021
ms.locfileid: "105720777"
---
# <a name="iuniversalorchestrator-interface"></a><span data-ttu-id="80110-103">Interfaz IUniversalOrchestrator</span><span class="sxs-lookup"><span data-stu-id="80110-103">IUniversalOrchestrator interface</span></span>

> [!NOTE] 
> <span data-ttu-id="80110-104">Esta API pertenece a la API de orquestador universal.</span><span class="sxs-lookup"><span data-stu-id="80110-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="80110-105">**IUniversalOrchestrator** es una interfaz com que proporciona los métodos siguientes para permitir que un cliente se comunique con el orquestador universal.</span><span class="sxs-lookup"><span data-stu-id="80110-105">**IUniversalOrchestrator** is a COM interface that provides the following methods to allow a client to communicate with the Universal Orchestrator.</span></span>

## <a name="methods"></a><span data-ttu-id="80110-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="80110-106">Methods</span></span>

|<span data-ttu-id="80110-107">Método</span><span class="sxs-lookup"><span data-stu-id="80110-107">Method</span></span> | <span data-ttu-id="80110-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="80110-108">Description</span></span> |
|---|---|
|[<span data-ttu-id="80110-109">:: Programar el programa</span><span class="sxs-lookup"><span data-stu-id="80110-109">::ScheduleWork</span></span>](universalorchestrator-schedulework.md) | <span data-ttu-id="80110-110">Registra el trabajo pendiente con el orquestador universal.</span><span class="sxs-lookup"><span data-stu-id="80110-110">Registers pending work with the Universal Orchestrator.</span></span> |
|[<span data-ttu-id="80110-111">::WorkCompleted</span><span class="sxs-lookup"><span data-stu-id="80110-111">::WorkCompleted</span></span>](universalorchestrator-workcompleted.md) | <span data-ttu-id="80110-112">Informa a la plataforma universal de que se ha completado todo el trabajo.</span><span class="sxs-lookup"><span data-stu-id="80110-112">Informs the Universal Orchestrator that all work is complete.</span></span> |
|[<span data-ttu-id="80110-113">::HasMoratoriumPassed</span><span class="sxs-lookup"><span data-stu-id="80110-113">::HasMoratoriumPassed</span></span>](universalorchestrator-hasmoratoriumpassed.md) | <span data-ttu-id="80110-114">Consulta a universal Orchestrator para determinar si funciona inmediatamente después de la nueva experiencia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="80110-114">Queries Universal Orchestrator to determine if it is operating immediately after the new device Out of Box Experience.</span></span> |


## <a name="requirements"></a><span data-ttu-id="80110-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80110-115">Requirements</span></span>

| <span data-ttu-id="80110-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="80110-116">Requirement</span></span> | <span data-ttu-id="80110-117">Versión</span><span class="sxs-lookup"><span data-stu-id="80110-117">Version</span></span> |
|---|---|
| <span data-ttu-id="80110-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80110-118">Minimum supported client</span></span> | <span data-ttu-id="80110-119">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="80110-119">Windows 10 1903</span></span> |
|   |   |