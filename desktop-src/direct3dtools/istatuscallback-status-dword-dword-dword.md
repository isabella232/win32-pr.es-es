---
description: Función de devolución de llamada que se usa para notificar el progreso del host de los motores. Esto también sirve como una manera para que el host determine que el motor todavía se está ejecutando.
title: 'IStatusCallback:: status (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4DC2A05F-506C-4AB4-98E1-58827056700D
api_name:
- IStatusCallback.Status
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09fba28486bd6f1c43e4b0c4fb0dfcf495e0722b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714747"
---
# <a name="span-idvspixengineistatuscallback_status_dword_dword_dwordspanistatuscallbackstatus-method"></a><span data-ttu-id="afdb9-104"><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>IStatusCallback:: status (método)</span><span class="sxs-lookup"><span data-stu-id="afdb9-104"><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>IStatusCallback::Status method</span></span>

<span data-ttu-id="afdb9-105">Función de devolución de llamada que se usa para notificar al host el progreso del motor.</span><span class="sxs-lookup"><span data-stu-id="afdb9-105">A callback function used to notify the host of the engine's progress.</span></span> <span data-ttu-id="afdb9-106">Esto también sirve como una manera para que el host determine que el motor todavía se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="afdb9-106">This also serves as a way for the host to determine that the engine is still running.</span></span>

## <a name="syntax"></a><span data-ttu-id="afdb9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="afdb9-107">Syntax</span></span>


```C++
HRESULT Status(
   DWORD dwMillisecondsElapsed,
   DWORD dwFramesCaptured,
   DWORD dwFramesElapsed
);
```

## <a name="parameters"></a><span data-ttu-id="afdb9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="afdb9-108">Parameters</span></span>

<span data-ttu-id="afdb9-109">*dwMillisecondsElapsed* </span><span class="sxs-lookup"><span data-stu-id="afdb9-109">*dwMillisecondsElapsed* </span></span>  
<span data-ttu-id="afdb9-110">Tiempo transcurrido desde la última llamada al estado, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="afdb9-110">The time elapsed since the last call to Status, in milliseconds.</span></span>

<span data-ttu-id="afdb9-111">*dwFramesCaptured* </span><span class="sxs-lookup"><span data-stu-id="afdb9-111">*dwFramesCaptured* </span></span>  
<span data-ttu-id="afdb9-112">Número de fotogramas que se han capturado desde la última llamada al estado.</span><span class="sxs-lookup"><span data-stu-id="afdb9-112">The number of frames that have been captures since the last call to Status.</span></span>

<span data-ttu-id="afdb9-113">*dwFramesElapsed* </span><span class="sxs-lookup"><span data-stu-id="afdb9-113">*dwFramesElapsed* </span></span>  
<span data-ttu-id="afdb9-114">Número de fotogramas transcurridos desde la última llamada al estado.</span><span class="sxs-lookup"><span data-stu-id="afdb9-114">The number of frames elapsed since the last call to Status.</span></span>

## <a name="return-value"></a><span data-ttu-id="afdb9-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="afdb9-115">Return value</span></span>

<span data-ttu-id="afdb9-116">Si este método se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="afdb9-116">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="afdb9-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="afdb9-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="afdb9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afdb9-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="afdb9-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="afdb9-119">Header</span></span></p></td><td><span data-ttu-id="afdb9-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="afdb9-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="afdb9-121"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="afdb9-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="afdb9-122">**IStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="afdb9-122">**IStatusCallback**</span></span>](/windows/desktop/direct3dtools/istatuscallback)

 

 
