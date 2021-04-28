---
description: 'Método IStats::Resume: el método Resume reinicia una captura en pausa.'
ms.assetid: 128e38c4-7459-4376-a3d7-2c6944fcf535
title: Método IStats::Resume (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ee7818da3d8a02e41488d473d3cf26607d3b84ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114623"
---
# <a name="istatsresume-method"></a><span data-ttu-id="dc1c5-103">IStats::Resume (método)</span><span class="sxs-lookup"><span data-stu-id="dc1c5-103">IStats::Resume method</span></span>

<span data-ttu-id="dc1c5-104">El **método Resume** reinicia una captura en pausa.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc1c5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc1c5-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="dc1c5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc1c5-106">Parameters</span></span>

<span data-ttu-id="dc1c5-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dc1c5-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc1c5-108">Return value</span></span>

<span data-ttu-id="dc1c5-109">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="dc1c5-110">Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="dc1c5-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="dc1c5-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="dc1c5-111">Return code</span></span>                                                                                                | <span data-ttu-id="dc1c5-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc1c5-112">Description</span></span>                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dc1c5-113"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="dc1c5-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="dc1c5-114">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-114">The NPP is not connected to the network.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="dc1c5-115"><dt>**CAPTURA DE NMERR \_ \_ NO EN \_ PAUSA**</dt></span><span class="sxs-lookup"><span data-stu-id="dc1c5-115"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="dc1c5-116">La captura no está en pausa.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-116">The capture is not paused.</span></span> <span data-ttu-id="dc1c5-117">Llame al [método IStats::P ause](istats-pause.md) para detener temporalmente la captura.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-117">Call the [IStats::Pause](istats-pause.md) method to temporarily stop the capture.</span></span><br/>                     |
| <dl> <span data-ttu-id="dc1c5-118"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="dc1c5-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="dc1c5-119">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="dc1c5-120">Llame al [método IStats::Connect](istats-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="dc1c5-121"><dt>**NMERR \_ NO SOLO \_ \_ ESTADÍSTICAS**</dt></span><span class="sxs-lookup"><span data-stu-id="dc1c5-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl>     | <span data-ttu-id="dc1c5-122">El NPP está conectado a la red, pero no con el [método IStats::Connect.](istats-connect.md)</span><span class="sxs-lookup"><span data-stu-id="dc1c5-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="dc1c5-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dc1c5-123">Remarks</span></span>

<span data-ttu-id="dc1c5-124">Mientras la captura está en estado en pausa, no se capturan nuevos datos hasta que se llama al método IStats::Resume para reiniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-124">While the capture is in a paused state, new data is not captured until the IStats::Resume method is called to restart the capture.</span></span>

<span data-ttu-id="dc1c5-125">Al usar los  **métodos Pausar** y Reanudar para controlar la captura, Monitor de red continúa agregando estadísticas de conversación a las [*estadísticas*](c.md) existentes para la captura actual.</span><span class="sxs-lookup"><span data-stu-id="dc1c5-125">When using the **Pause** and **Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="dc1c5-126">Para detener la captura, llame a [IStats::Stop](istats-stop.md).</span><span class="sxs-lookup"><span data-stu-id="dc1c5-126">To stop the capture, call [IStats::Stop](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc1c5-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc1c5-127">Requirements</span></span>



| <span data-ttu-id="dc1c5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc1c5-128">Requirement</span></span> | <span data-ttu-id="dc1c5-129">Valor</span><span class="sxs-lookup"><span data-stu-id="dc1c5-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc1c5-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc1c5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="dc1c5-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dc1c5-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="dc1c5-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc1c5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="dc1c5-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dc1c5-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="dc1c5-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dc1c5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc1c5-135"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="dc1c5-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="dc1c5-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dc1c5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc1c5-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc1c5-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc1c5-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dc1c5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc1c5-139">IStats</span><span class="sxs-lookup"><span data-stu-id="dc1c5-139">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="dc1c5-140">IStats::Connect</span><span class="sxs-lookup"><span data-stu-id="dc1c5-140">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="dc1c5-141">IStats::P ause</span><span class="sxs-lookup"><span data-stu-id="dc1c5-141">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="dc1c5-142">IStats::Stop</span><span class="sxs-lookup"><span data-stu-id="dc1c5-142">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




