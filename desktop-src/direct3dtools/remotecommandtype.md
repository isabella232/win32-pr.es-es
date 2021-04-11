---
description: Enumeración que se usa para la comunicación entre el motor de captura y un host (como Visual Studio Diagnóstico de gráficos).
MS-HAID: vspixengine.RemoteCommandType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeración RemoteCommandType
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B517F70C-2BFB-42E7-8597-AC5915AB2DE0
api_name:
- RemoteCommandType
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 63b94ace0818e2057a87c0f3962bb3967843bcfc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104080044"
---
# <a name="span-idvspixengineremotecommandtypespanremotecommandtype-enumeration"></a><span data-ttu-id="fb3ce-103"><span id="vspixengine.remotecommandtype"></span>Enumeración RemoteCommandType</span><span class="sxs-lookup"><span data-stu-id="fb3ce-103"><span id="vspixengine.remotecommandtype"></span>RemoteCommandType enumeration</span></span>

<span data-ttu-id="fb3ce-104">Enumeración que se usa para la comunicación entre el motor de captura y un host (como Visual Studio Diagnóstico de gráficos).</span><span class="sxs-lookup"><span data-stu-id="fb3ce-104">An enum used to communicate between the capture engine and a host (such as Visual Studio Graphics Diagnostics).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb3ce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb3ce-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="fb3ce-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="fb3ce-106">Constants</span></span>

<span data-ttu-id="fb3ce-107"><span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**BeginCommunication**</span><span class="sxs-lookup"><span data-stu-id="fb3ce-107"><span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**BeginCommunication**</span></span>  
<span data-ttu-id="fb3ce-108">Inicia la comunicación.</span><span class="sxs-lookup"><span data-stu-id="fb3ce-108">Starts communication.</span></span>

<span data-ttu-id="fb3ce-109"><span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**RunExperiment**</span><span class="sxs-lookup"><span data-stu-id="fb3ce-109"><span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**RunExperiment**</span></span>  
<span data-ttu-id="fb3ce-110">Inicia una sesión de captura de Diagnóstico de gráficos (un experimento).</span><span class="sxs-lookup"><span data-stu-id="fb3ce-110">Starts a Graphics Diagnostics capture session (an experiment).</span></span>

<span data-ttu-id="fb3ce-111"><span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**RunAction**</span><span class="sxs-lookup"><span data-stu-id="fb3ce-111"><span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**RunAction**</span></span>  
<span data-ttu-id="fb3ce-112">Inicia una captura (igual que al pulsar Impr Pant).</span><span class="sxs-lookup"><span data-stu-id="fb3ce-112">Starts a capture (same as hitting print screen).</span></span> <span data-ttu-id="fb3ce-113">Lo envía un host al capturar un fotograma.</span><span class="sxs-lookup"><span data-stu-id="fb3ce-113">Sent by a host when capturing a frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb3ce-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb3ce-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fb3ce-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb3ce-115">Header</span></span></p></td><td><span data-ttu-id="fb3ce-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="fb3ce-116">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



