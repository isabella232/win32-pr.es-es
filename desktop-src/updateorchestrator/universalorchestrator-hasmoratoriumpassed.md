---
title: IUniversalOrchestrator::HasMoratoriumPassed
description: Consulta a universal Orchestrator para determinar si se ha superado el período posterior a OOBE.
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 2ed354d365b795a0c959396e6b26d6bc73baad97
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/21/2021
ms.locfileid: "105720776"
---
# <a name="iuniversalorchestratorhasmoratoriumpassed-method"></a><span data-ttu-id="48dd5-103">IUniversalOrchestrator:: HasMoratoriumPassed (método)</span><span class="sxs-lookup"><span data-stu-id="48dd5-103">IUniversalOrchestrator::HasMoratoriumPassed method</span></span>

> [!NOTE] 
> <span data-ttu-id="48dd5-104">Esta API pertenece a la API de orquestador universal.</span><span class="sxs-lookup"><span data-stu-id="48dd5-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="48dd5-105">Permite a los clientes determinar si el orquestador universal funciona inmediatamente después de la nueva experiencia del dispositivo, lo que limita los intentos de trabajo para minimizar la interrupción del usuario.</span><span class="sxs-lookup"><span data-stu-id="48dd5-105">Allows clients to determine if Universal Orchestrator is operating immediately after the new device Out of Box Experience, which limits work attempts to minimize user interruption.</span></span> 

## <a name="syntax"></a><span data-ttu-id="48dd5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48dd5-106">Syntax</span></span>

```C++
HRESULT HasMoratoriumPassed(
  LPCWSTR callerIdentifier,
  BOOL*   moratoriumPassed);
```

## <a name="parameters"></a><span data-ttu-id="48dd5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48dd5-107">Parameters</span></span>

`callerIdentifier`

<span data-ttu-id="48dd5-108">Cadena única que identifica todas las llamadas de este cliente específico.</span><span class="sxs-lookup"><span data-stu-id="48dd5-108">A unique string that identifies all calls from this specific client.</span></span>

`hasMoratoriumPassed`

<span data-ttu-id="48dd5-109">Parámetro de salida que almacena el resultado de la consulta.</span><span class="sxs-lookup"><span data-stu-id="48dd5-109">Output parameter that stores the result of the query.</span></span>

## <a name="return-value"></a><span data-ttu-id="48dd5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48dd5-110">Return value</span></span>
<span data-ttu-id="48dd5-111">Si este método se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="48dd5-111">If this method succeeds, it returns **S_OK**.</span></span>  <span data-ttu-id="48dd5-112">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="48dd5-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="48dd5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48dd5-113">Requirements</span></span>

| <span data-ttu-id="48dd5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="48dd5-114">Requirement</span></span> | <span data-ttu-id="48dd5-115">Versión</span><span class="sxs-lookup"><span data-stu-id="48dd5-115">Version</span></span> |
|---|---|
| <span data-ttu-id="48dd5-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48dd5-116">Minimum supported client</span></span> | <span data-ttu-id="48dd5-117">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="48dd5-117">Windows 10 1903</span></span> |
|   |   |



 

 



