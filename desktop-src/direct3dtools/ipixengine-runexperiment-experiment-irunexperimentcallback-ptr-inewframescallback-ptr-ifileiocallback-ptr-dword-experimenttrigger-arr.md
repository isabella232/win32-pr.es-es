---
description: Ejecuta un experimento.
MS-HAID: vspixengine.IPixEngine\_RunExperiment\_Experiment\_IRunExperimentCallback\_ptr\_INewFramesCallback\_ptr\_IFileIOCallback\_ptr\_DWORD\_ExperimentTrigger\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine:: RunExperiment (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A2EEC278-C074-44B3-94DC-E2D9DC770576
api_name:
- IPixEngine.RunExperiment
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c656d57dda496b6c1d8c128dc5e832ec40ef13f7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152273"
---
# <a name="span-idvspixengineipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arrspanipixenginerunexperiment-method"></a><span data-ttu-id="9d40b-103"><span id="vspixengine.ipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arr"></span>IPixEngine:: RunExperiment (método)</span><span class="sxs-lookup"><span data-stu-id="9d40b-103"><span id="vspixengine.ipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arr"></span>IPixEngine::RunExperiment method</span></span>

<span data-ttu-id="9d40b-104">Ejecuta un experimento.</span><span class="sxs-lookup"><span data-stu-id="9d40b-104">Runs an experiment.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d40b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d40b-105">Syntax</span></span>


```C++
HRESULT RunExperiment(
   Experiment               experiment,
   IRunExperimentCallback * pRequestCallback,
   INewFramesCallback*      callbacks,
   IFileIOCallback*         pFileIOCallback,
   DWORD                    triggersCount,
   ExperimentTrigger []     count4_triggersBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="9d40b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d40b-106">Parameters</span></span>

<span data-ttu-id="9d40b-107">*pruebas* </span><span class="sxs-lookup"><span data-stu-id="9d40b-107">*experiment* </span></span>  
<span data-ttu-id="9d40b-108">Describe el experimento que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="9d40b-108">Describes the experiment to be run.</span></span>

<span data-ttu-id="9d40b-109">*pRequestCallback* </span><span class="sxs-lookup"><span data-stu-id="9d40b-109">*pRequestCallback* </span></span>  
<span data-ttu-id="9d40b-110">La dirección de una función que se usa para notificar al host que el motor ha iniciado el experimento.</span><span class="sxs-lookup"><span data-stu-id="9d40b-110">The address of a function used to notify the host that engine has started the experiment.</span></span>

<span data-ttu-id="9d40b-111">*devoluciones* </span><span class="sxs-lookup"><span data-stu-id="9d40b-111">*callbacks* </span></span>  
<span data-ttu-id="9d40b-112">La dirección de una función que se usa para notificar al host que se han capturado nuevos fotogramas.</span><span class="sxs-lookup"><span data-stu-id="9d40b-112">The address of a function used to notify the host that new frames have been captured.</span></span>

<span data-ttu-id="9d40b-113">*pFileIOCallback* </span><span class="sxs-lookup"><span data-stu-id="9d40b-113">*pFileIOCallback* </span></span>  
<span data-ttu-id="9d40b-114">La dirección de una función que se usa para notificar al host de errores de e/s de archivo durante el análisis.</span><span class="sxs-lookup"><span data-stu-id="9d40b-114">The address of a function used to notify the host of file IO errors during parsing.</span></span>

<span data-ttu-id="9d40b-115">*triggersCount* </span><span class="sxs-lookup"><span data-stu-id="9d40b-115">*triggersCount* </span></span>  
<span data-ttu-id="9d40b-116">Número de desencadenadores del experimento.</span><span class="sxs-lookup"><span data-stu-id="9d40b-116">The number of triggers in the experiment.</span></span>

<span data-ttu-id="9d40b-117">*count4 \_ triggersBuffer* </span><span class="sxs-lookup"><span data-stu-id="9d40b-117">*count4\_triggersBuffer* </span></span>  
<span data-ttu-id="9d40b-118">Desencadenadores de captura.</span><span class="sxs-lookup"><span data-stu-id="9d40b-118">Capture triggers.</span></span>

## <a name="return-value"></a><span data-ttu-id="9d40b-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d40b-119">Return value</span></span>

<span data-ttu-id="9d40b-120">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9d40b-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9d40b-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9d40b-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d40b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d40b-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9d40b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d40b-123">Header</span></span></p></td><td><span data-ttu-id="9d40b-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="9d40b-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="9d40b-125"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="9d40b-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="9d40b-126">**IPixEngine**</span><span class="sxs-lookup"><span data-stu-id="9d40b-126">**IPixEngine**</span></span>](/windows/desktop/direct3dtools/ipixengine)

 

 
