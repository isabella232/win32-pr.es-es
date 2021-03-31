---
description: El método resume reinicia una captura en pausa.
ms.assetid: 128e38c4-7459-4376-a3d7-2c6944fcf535
title: 'IStas:: resume (método) (Netmon. h)'
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
ms.openlocfilehash: db84f51d2a2a2c2d15e3b4164fe1fac09e72bf20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911638"
---
# <a name="istatsresume-method"></a><span data-ttu-id="28c10-103">IStas:: resume (método)</span><span class="sxs-lookup"><span data-stu-id="28c10-103">IStats::Resume method</span></span>

<span data-ttu-id="28c10-104">El método **resume** reinicia una captura en pausa.</span><span class="sxs-lookup"><span data-stu-id="28c10-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="28c10-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28c10-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="28c10-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28c10-106">Parameters</span></span>

<span data-ttu-id="28c10-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="28c10-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28c10-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28c10-108">Return value</span></span>

<span data-ttu-id="28c10-109">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="28c10-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="28c10-110">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="28c10-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="28c10-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="28c10-111">Return code</span></span>                                                                                                | <span data-ttu-id="28c10-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="28c10-112">Description</span></span>                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="28c10-113"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="28c10-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="28c10-114">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="28c10-114">The NPP is not connected to the network.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="28c10-115"><dt>**la captura de NMERR no está en \_ \_ \_ pausa**</dt></span><span class="sxs-lookup"><span data-stu-id="28c10-115"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="28c10-116">La captura no está en pausa.</span><span class="sxs-lookup"><span data-stu-id="28c10-116">The capture is not paused.</span></span> <span data-ttu-id="28c10-117">Llame al método [istas::P ause](istats-pause.md) para detener temporalmente la captura.</span><span class="sxs-lookup"><span data-stu-id="28c10-117">Call the [IStats::Pause](istats-pause.md) method to temporarily stop the capture.</span></span><br/>                     |
| <dl> <span data-ttu-id="28c10-118"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="28c10-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="28c10-119">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="28c10-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="28c10-120">Llame al método [istas:: Connect](istats-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="28c10-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="28c10-121"><dt>**NMERR \_ no \_ solo estadísticas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="28c10-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl>     | <span data-ttu-id="28c10-122">NPP está conectado a la red, pero no con el método [istas:: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="28c10-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="28c10-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28c10-123">Remarks</span></span>

<span data-ttu-id="28c10-124">Mientras la captura está en un estado de pausa, los nuevos datos no se capturan hasta que se llama al método IStas:: resume para reiniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="28c10-124">While the capture is in a paused state, new data is not captured until the IStats::Resume method is called to restart the capture.</span></span>

<span data-ttu-id="28c10-125">Al usar los métodos **pausar** y **reanudar** para controlar la captura, monitor de red continúa agregando [*estadísticas de conversación*](c.md) a las estadísticas existentes para la captura actual.</span><span class="sxs-lookup"><span data-stu-id="28c10-125">When using the **Pause** and **Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="28c10-126">Para detener la captura, llame a [istas:: Stop](istats-stop.md).</span><span class="sxs-lookup"><span data-stu-id="28c10-126">To stop the capture, call [IStats::Stop](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="28c10-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28c10-127">Requirements</span></span>



| <span data-ttu-id="28c10-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="28c10-128">Requirement</span></span> | <span data-ttu-id="28c10-129">Value</span><span class="sxs-lookup"><span data-stu-id="28c10-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28c10-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28c10-130">Minimum supported client</span></span><br/> | <span data-ttu-id="28c10-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="28c10-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="28c10-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28c10-132">Minimum supported server</span></span><br/> | <span data-ttu-id="28c10-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="28c10-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="28c10-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28c10-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="28c10-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="28c10-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="28c10-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="28c10-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28c10-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28c10-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28c10-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="28c10-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28c10-139">IStas</span><span class="sxs-lookup"><span data-stu-id="28c10-139">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="28c10-140">ISta:: Connect</span><span class="sxs-lookup"><span data-stu-id="28c10-140">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="28c10-141">IStas::P ause</span><span class="sxs-lookup"><span data-stu-id="28c10-141">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="28c10-142">IStas:: Stop</span><span class="sxs-lookup"><span data-stu-id="28c10-142">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




