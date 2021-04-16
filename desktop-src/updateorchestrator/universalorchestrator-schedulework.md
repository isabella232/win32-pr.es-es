---
title: IUniversalOrchestrator::ScheduleWork
description: Llama al orquestador universal para programar el trabajo
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 456df8f975114f7bdf750a0449f3bd98efcc3b2e
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/21/2021
ms.locfileid: "105720778"
---
# <a name="iuniversalorchestratorschedulework-method"></a><span data-ttu-id="7e9a7-103">IUniversalOrchestrator:: Scheduled (método)</span><span class="sxs-lookup"><span data-stu-id="7e9a7-103">IUniversalOrchestrator::ScheduleWork method</span></span>

> [!NOTE] 
> <span data-ttu-id="7e9a7-104">Esta API pertenece a la API de orquestador universal.</span><span class="sxs-lookup"><span data-stu-id="7e9a7-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="7e9a7-105">Permite a los clientes informar a universal Orchestrator de que el trabajo está pendiente y proporcionar un archivo binario al que llamará universal Orchestrator para realizar la actualización en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="7e9a7-105">Allows clients to inform Universal Orchestrator that work is pending and provide a binary that will be called by Universal Orchestrator to perform the update work at a later time.</span></span>

<span data-ttu-id="7e9a7-106">El archivo binario de devolución de llamada debe estar firmado con un certificado de Microsoft válido, y el llamador debe invocar la llamada de programación desde el contexto del sistema.</span><span class="sxs-lookup"><span data-stu-id="7e9a7-106">The callback binary must be signed with a valid Microsoft certificate, and the caller must be invoking the ScheduleWork call from SYSTEM context.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e9a7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e9a7-107">Syntax</span></span>

```C++
HRESULT ScheduleWork(
  LPCWSTR callerIdentifier,
  LPCWSTR cmdLine
  LPCWSTR startArg,
  LPCWSTR pauseArg);
```

## <a name="parameters"></a><span data-ttu-id="7e9a7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e9a7-108">Parameters</span></span>

`callerIdentifier`

<span data-ttu-id="7e9a7-109">Cadena única que identifica todas las llamadas de este cliente específico.</span><span class="sxs-lookup"><span data-stu-id="7e9a7-109">A unique string that identifies all calls from this specific client.</span></span>

`cmdLine`

<span data-ttu-id="7e9a7-110">Ruta de acceso completa al archivo binario de devolución de llamada que va a invocar el orquestador universal para realizar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7e9a7-110">The full path to the callback binary that will be invoked by Universal Orchestrator to perform work.</span></span>

`startArg`

<span data-ttu-id="7e9a7-111">Se solicitan los parámetros que se van a pasar al binario de devolución de llamada para indicar que se inicia.</span><span class="sxs-lookup"><span data-stu-id="7e9a7-111">Parameters to pass to the callback binary to indicate Start is requested.</span></span>

`pauseArg`

<span data-ttu-id="7e9a7-112">*(opcional)* Parámetros que se van a pasar al binario de devolución de llamada para indicar que se solicita la pausa.</span><span class="sxs-lookup"><span data-stu-id="7e9a7-112">*(optional)* Parameters to pass to the callback binary to indicate Pause is requested.</span></span>

## <a name="return-value"></a><span data-ttu-id="7e9a7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e9a7-113">Return value</span></span>
<span data-ttu-id="7e9a7-114">Si este método se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="7e9a7-114">If this method succeeds, it returns **S_OK**.</span></span>  <span data-ttu-id="7e9a7-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7e9a7-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e9a7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e9a7-116">Requirements</span></span>

| <span data-ttu-id="7e9a7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e9a7-117">Requirement</span></span> | <span data-ttu-id="7e9a7-118">Versión</span><span class="sxs-lookup"><span data-stu-id="7e9a7-118">Version</span></span> |
|---|---|
| <span data-ttu-id="7e9a7-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e9a7-119">Minimum supported client</span></span> | <span data-ttu-id="7e9a7-120">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="7e9a7-120">Windows 10 1903</span></span> |
|   |   |



 

 



