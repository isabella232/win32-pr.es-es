---
title: IUniversalOrchestrator::WorkCompleted
description: Llama al orquestador universal para indicar que el trabajo se ha completado
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 8d4a08e7f021811e59a182a8b726397476b78433
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/21/2021
ms.locfileid: "105720779"
---
# <a name="iuniversalorchestratorworkcompleted-method"></a><span data-ttu-id="195f7-103">IUniversalOrchestrator:: WorkCompleted (método)</span><span class="sxs-lookup"><span data-stu-id="195f7-103">IUniversalOrchestrator::WorkCompleted method</span></span>

> [!NOTE] 
> <span data-ttu-id="195f7-104">Esta API pertenece a la API de orquestador universal.</span><span class="sxs-lookup"><span data-stu-id="195f7-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="195f7-105">Permite a los clientes informar a la plataforma universal de que el trabajo programado anteriormente se ha completado y detener las devoluciones de llamada para que funcionen hasta la siguiente llamada de programación de trabajo correcta.</span><span class="sxs-lookup"><span data-stu-id="195f7-105">Allows clients to inform Universal Orchestrator that the previously scheduled work has been completed and stop callbacks to perform work until the next successful ScheduleWork call.</span></span>

## <a name="syntax"></a><span data-ttu-id="195f7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="195f7-106">Syntax</span></span>

```C++
HRESULT WorkCompleted(
  LPCWSTR callerIdentifier,
  BOOL    workCompleted);
```

## <a name="parameters"></a><span data-ttu-id="195f7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="195f7-107">Parameters</span></span>

`callerIdentifier`

<span data-ttu-id="195f7-108">Cadena única que identifica todas las llamadas de este cliente específico.</span><span class="sxs-lookup"><span data-stu-id="195f7-108">A unique string that identifies all calls from this specific client.</span></span>

`workCompleted`

<span data-ttu-id="195f7-109">**True** si el trabajo se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="195f7-109">**TRUE** if the work successfully completed.</span></span> <span data-ttu-id="195f7-110">En caso contrario, **false** si se produjo un error en el intento de trabajo y se debe volver a intentar en el futuro.</span><span class="sxs-lookup"><span data-stu-id="195f7-110">Otherwise, **FALSE** if the work attempt failed and should be retried in the future.</span></span> 

## <a name="return-value"></a><span data-ttu-id="195f7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="195f7-111">Return value</span></span>
<span data-ttu-id="195f7-112">Si este método se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="195f7-112">If this method succeeds, it returns **S_OK**.</span></span>  <span data-ttu-id="195f7-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="195f7-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="195f7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="195f7-114">Requirements</span></span>

| <span data-ttu-id="195f7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="195f7-115">Requirement</span></span> | <span data-ttu-id="195f7-116">Versión</span><span class="sxs-lookup"><span data-stu-id="195f7-116">Version</span></span> |
|---|---|
| <span data-ttu-id="195f7-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="195f7-117">Minimum supported client</span></span> | <span data-ttu-id="195f7-118">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="195f7-118">Windows 10 1903</span></span> |
|   |   |



 

 



