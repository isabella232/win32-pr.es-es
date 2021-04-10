---
description: Enumeración que se usa para la comunicación entre el motor de captura y un host (como Visual Studio Diagnóstico de gráficos).
MS-HAID: vspixengine.CallbackCommandType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeración CallbackCommandType
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 78E0CD6C-5264-4F66-BAB9-20DC9C0C1EC1
api_name:
- CallbackCommandType
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ac33267677ae95f6a3d5f893b84d6566e564cddd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152383"
---
# <a name="span-idvspixenginecallbackcommandtypespancallbackcommandtype-enumeration"></a><span data-ttu-id="3e821-103"><span id="vspixengine.callbackcommandtype"></span>Enumeración CallbackCommandType</span><span class="sxs-lookup"><span data-stu-id="3e821-103"><span id="vspixengine.callbackcommandtype"></span>CallbackCommandType enumeration</span></span>

<span data-ttu-id="3e821-104">Enumeración que se usa para la comunicación entre el motor de captura y un host (como Visual Studio Diagnóstico de gráficos).</span><span class="sxs-lookup"><span data-stu-id="3e821-104">An enum used to communicate between the capture engine and a host (such as Visual Studio Graphics Diagnostics).</span></span>

## <a name="syntax"></a><span data-ttu-id="3e821-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e821-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="3e821-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="3e821-106">Constants</span></span>

<span data-ttu-id="3e821-107"><span id="BeginCommunicationCallback"></span><span id="begincommunicationcallback"></span><span id="BEGINCOMMUNICATIONCALLBACK"></span>**BeginCommunicationCallback**</span><span class="sxs-lookup"><span data-stu-id="3e821-107"><span id="BeginCommunicationCallback"></span><span id="begincommunicationcallback"></span><span id="BEGINCOMMUNICATIONCALLBACK"></span>**BeginCommunicationCallback**</span></span>  
<span data-ttu-id="3e821-108">Resultados de BeginCommunication.</span><span class="sxs-lookup"><span data-stu-id="3e821-108">Results from BeginCommunication.</span></span>

<span data-ttu-id="3e821-109"><span id="ErrorListCallback"></span><span id="errorlistcallback"></span><span id="ERRORLISTCALLBACK"></span>**ErrorListCallback**</span><span class="sxs-lookup"><span data-stu-id="3e821-109"><span id="ErrorListCallback"></span><span id="errorlistcallback"></span><span id="ERRORLISTCALLBACK"></span>**ErrorListCallback**</span></span>  
<span data-ttu-id="3e821-110">Errores.</span><span class="sxs-lookup"><span data-stu-id="3e821-110">Errors.</span></span>

<span data-ttu-id="3e821-111"><span id="WarningListCallback"></span><span id="warninglistcallback"></span><span id="WARNINGLISTCALLBACK"></span>**WarningListCallback**</span><span class="sxs-lookup"><span data-stu-id="3e821-111"><span id="WarningListCallback"></span><span id="warninglistcallback"></span><span id="WARNINGLISTCALLBACK"></span>**WarningListCallback**</span></span>  
<span data-ttu-id="3e821-112">Advertencias.</span><span class="sxs-lookup"><span data-stu-id="3e821-112">Warnings.</span></span>

<span data-ttu-id="3e821-113"><span id="MessagesCallback"></span><span id="messagescallback"></span><span id="MESSAGESCALLBACK"></span>**MessagesCallback**</span><span class="sxs-lookup"><span data-stu-id="3e821-113"><span id="MessagesCallback"></span><span id="messagescallback"></span><span id="MESSAGESCALLBACK"></span>**MessagesCallback**</span></span>  
<span data-ttu-id="3e821-114">Mensajes.</span><span class="sxs-lookup"><span data-stu-id="3e821-114">Messages.</span></span>

<span data-ttu-id="3e821-115"><span id="RunExperimentCallback"></span><span id="runexperimentcallback"></span><span id="RUNEXPERIMENTCALLBACK"></span>**RunExperimentCallback**</span><span class="sxs-lookup"><span data-stu-id="3e821-115"><span id="RunExperimentCallback"></span><span id="runexperimentcallback"></span><span id="RUNEXPERIMENTCALLBACK"></span>**RunExperimentCallback**</span></span>  
<span data-ttu-id="3e821-116">Resultado de RunExperiment.</span><span class="sxs-lookup"><span data-stu-id="3e821-116">Result from RunExperiment.</span></span>

<span data-ttu-id="3e821-117"><span id="RunActionCallback"></span><span id="runactioncallback"></span><span id="RUNACTIONCALLBACK"></span>**RunActionCallback**</span><span class="sxs-lookup"><span data-stu-id="3e821-117"><span id="RunActionCallback"></span><span id="runactioncallback"></span><span id="RUNACTIONCALLBACK"></span>**RunActionCallback**</span></span>  
<span data-ttu-id="3e821-118">Resultado de RunAction.</span><span class="sxs-lookup"><span data-stu-id="3e821-118">Result from RunAction.</span></span>

<span data-ttu-id="3e821-119"><span id="NewFramesCallback"></span><span id="newframescallback"></span><span id="NEWFRAMESCALLBACK"></span>**NewFramesCallback**</span><span class="sxs-lookup"><span data-stu-id="3e821-119"><span id="NewFramesCallback"></span><span id="newframescallback"></span><span id="NEWFRAMESCALLBACK"></span>**NewFramesCallback**</span></span>  
<span data-ttu-id="3e821-120">Valor que indica una devolución de llamada a la que se llamará cuando se hayan capturado fotogramas nuevos y estén listos para mostrarse.</span><span class="sxs-lookup"><span data-stu-id="3e821-120">A value that indicates a callback to be called when new frames have been captured and ready to display.</span></span>

<span data-ttu-id="3e821-121"><span id="BeginCommunicationCallbackLegacy"></span><span id="begincommunicationcallbacklegacy"></span><span id="BEGINCOMMUNICATIONCALLBACKLEGACY"></span>**BeginCommunicationCallbackLegacy**</span><span class="sxs-lookup"><span data-stu-id="3e821-121"><span id="BeginCommunicationCallbackLegacy"></span><span id="begincommunicationcallbacklegacy"></span><span id="BEGINCOMMUNICATIONCALLBACKLEGACY"></span>**BeginCommunicationCallbackLegacy**</span></span>  
<span data-ttu-id="3e821-122">Los resultados de una versión anterior de BeginCommunication se usan en Windows 7 y Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3e821-122">Results from an older version of BeginCommunication used on Windows 7 and Windows 8.</span></span>

<span data-ttu-id="3e821-123"><span id="RunExperimentStatusCallback"></span><span id="runexperimentstatuscallback"></span><span id="RUNEXPERIMENTSTATUSCALLBACK"></span>**RunExperimentStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="3e821-123"><span id="RunExperimentStatusCallback"></span><span id="runexperimentstatuscallback"></span><span id="RUNEXPERIMENTSTATUSCALLBACK"></span>**RunExperimentStatusCallback**</span></span>  
<span data-ttu-id="3e821-124">Resultado de RunExperiementProgress.</span><span class="sxs-lookup"><span data-stu-id="3e821-124">Result from RunExperiementProgress.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e821-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e821-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3e821-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e821-126">Header</span></span></p></td><td><span data-ttu-id="3e821-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="3e821-127">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



