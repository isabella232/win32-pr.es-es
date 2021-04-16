---
description: El método resume reinicia una captura en pausa.
ms.assetid: 047ea5f8-de3d-40db-ada3-fc0ef4deccef
title: 'IESP:: resume (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 01bbb748fc91bcc5a78b281ec9ebdd2a6d479888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686557"
---
# <a name="iespresume-method"></a><span data-ttu-id="1921d-103">IESP:: resume (método)</span><span class="sxs-lookup"><span data-stu-id="1921d-103">IESP::Resume method</span></span>

<span data-ttu-id="1921d-104">El método **resume** reinicia una captura en pausa.</span><span class="sxs-lookup"><span data-stu-id="1921d-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="1921d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1921d-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="1921d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1921d-106">Parameters</span></span>

<span data-ttu-id="1921d-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1921d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1921d-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1921d-108">Return value</span></span>

<span data-ttu-id="1921d-109">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1921d-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1921d-110">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="1921d-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="1921d-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1921d-111">Return code</span></span>                                                                                                | <span data-ttu-id="1921d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1921d-112">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1921d-113"><dt>**la captura de NMERR no está en \_ \_ \_ pausa**</dt></span><span class="sxs-lookup"><span data-stu-id="1921d-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="1921d-114">La captura no está en pausa.</span><span class="sxs-lookup"><span data-stu-id="1921d-114">The capture is not paused.</span></span> <span data-ttu-id="1921d-115">Llame a [**iesp::P ause**](iesp-pause.md) para pausar la captura.</span><span class="sxs-lookup"><span data-stu-id="1921d-115">Call [**IESP::Pause**](iesp-pause.md) to pause the capture.</span></span><br/>                        |
| <dl> <span data-ttu-id="1921d-116"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="1921d-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="1921d-117">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="1921d-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="1921d-118">Llame a [**iesp:: Connect**](iesp-connect.md) para conectarse a la red.</span><span class="sxs-lookup"><span data-stu-id="1921d-118">Call [**IESP::Connect**](iesp-connect.md) to connect to the network.</span></span><br/> |
| <dl> <span data-ttu-id="1921d-119"><dt>**NMERR \_ no \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="1921d-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>             | <span data-ttu-id="1921d-120">NPP está conectado a la red, pero no con el método [**iesp:: Connect**](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="1921d-120">The NPP is connected to the network, but not with the [**IESP::Connect**](iesp-connect.md) method.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="1921d-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1921d-121">Remarks</span></span>

<span data-ttu-id="1921d-122">Mientras la captura está en un estado de pausa, los datos nuevos no se agregan al [*archivo de captura*](c.md) actual hasta que se llama a **iesp:: resume** para reiniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="1921d-122">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until **IESP::Resume** is called to restart the capture.</span></span> <span data-ttu-id="1921d-123">Cuando se usan **pausar** y **reanudar** para detener y reiniciar la captura, toda la información capturada se coloca en el mismo archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="1921d-123">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="1921d-124">Al usar **pausar** y **reanudar** para controlar la captura, monitor de red continúa agregando [*estadísticas de conversación*](c.md) a las estadísticas existentes para la captura actual.</span><span class="sxs-lookup"><span data-stu-id="1921d-124">When using **Pause** and **Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="1921d-125">Para detener la captura, llame a [**iesp:: Stop**](iesp-stop.md).</span><span class="sxs-lookup"><span data-stu-id="1921d-125">To stop the capture, call [**IESP::Stop**](iesp-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1921d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1921d-126">Requirements</span></span>



| <span data-ttu-id="1921d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1921d-127">Requirement</span></span> | <span data-ttu-id="1921d-128">Value</span><span class="sxs-lookup"><span data-stu-id="1921d-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1921d-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1921d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1921d-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1921d-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="1921d-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1921d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1921d-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1921d-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="1921d-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1921d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1921d-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1921d-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="1921d-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1921d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1921d-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1921d-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1921d-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="1921d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1921d-138">IESP</span><span class="sxs-lookup"><span data-stu-id="1921d-138">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="1921d-139">**IESP:: Connect**</span><span class="sxs-lookup"><span data-stu-id="1921d-139">**IESP::Connect**</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="1921d-140">**IESP::P ause**</span><span class="sxs-lookup"><span data-stu-id="1921d-140">**IESP::Pause**</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="1921d-141">**IESP:: Stop**</span><span class="sxs-lookup"><span data-stu-id="1921d-141">**IESP::Stop**</span></span>](iesp-stop.md)
</dt> </dl>

 

 




