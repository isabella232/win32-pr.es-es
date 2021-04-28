---
description: 'IDelaydC::P ause: el método Pause pausa la captura actual.'
ms.assetid: 9d5e11d1-8c45-4cf5-9fea-10c9e7a6fe86
title: Método IDelaydC::P ause (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 21b4cd7b6cb921f7bd71b8670a37da12b2239b92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098503"
---
# <a name="idelaydcpause-method"></a><span data-ttu-id="0cc9b-103">IDelaydC::P ause (método)</span><span class="sxs-lookup"><span data-stu-id="0cc9b-103">IDelaydC::Pause method</span></span>

<span data-ttu-id="0cc9b-104">El **método Pause** pausa la captura actual.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cc9b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0cc9b-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="0cc9b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0cc9b-106">Parameters</span></span>

<span data-ttu-id="0cc9b-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0cc9b-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0cc9b-108">Return value</span></span>

<span data-ttu-id="0cc9b-109">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0cc9b-110">Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="0cc9b-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="0cc9b-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0cc9b-111">Return code</span></span>                                                                                           | <span data-ttu-id="0cc9b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="0cc9b-112">Description</span></span>                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0cc9b-113"><dt>**CAPTURA DE NMERR \_ \_ EN PAUSA**</dt></span><span class="sxs-lookup"><span data-stu-id="0cc9b-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="0cc9b-114">La captura ya está en estado en pausa.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-114">The capture is already in a paused state.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="0cc9b-115"><dt>**NMERR \_ NO \_ CAPTURA**</dt></span><span class="sxs-lookup"><span data-stu-id="0cc9b-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="0cc9b-116">El NPP no captura datos.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-116">The NPP is not capturing data.</span></span> <span data-ttu-id="0cc9b-117">Llame [a IDelaydC::Start para](idelaydc-start.md) iniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-117">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="0cc9b-118"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="0cc9b-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="0cc9b-119">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="0cc9b-120">Llame [a IDelaydC::Connect](idelaydc-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-120">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="0cc9b-121"><dt>**NMERR \_ NO \_ RETRASADO**</dt></span><span class="sxs-lookup"><span data-stu-id="0cc9b-121"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>    | <span data-ttu-id="0cc9b-122">El NPP está conectado a la red, pero no con el [método IDelaydC::Connect.](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="0cc9b-122">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="0cc9b-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0cc9b-123">Remarks</span></span>

<span data-ttu-id="0cc9b-124">Mientras la captura está en estado en pausa, no [](c.md) se agregan nuevos datos al archivo de captura actual hasta que se llama al método **IDelaydC::Resume** para reiniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-124">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until the **IDelaydC::Resume** method is called to restart the capture.</span></span> <span data-ttu-id="0cc9b-125">Cuando **se** usan **Pausar y reanudar** para detener y reiniciar la captura, toda la información capturada se coloca en el mismo archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-125">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="0cc9b-126">Al usar **IDelaydC::P ause** e **IDelaydC::Resume** para controlar la captura, Monitor de red continúa agregando [*estadísticas*](c.md) de conversación cada vez que se ejecuta la captura.</span><span class="sxs-lookup"><span data-stu-id="0cc9b-126">When using **IDelaydC::Pause** and **IDelaydC::Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="0cc9b-127">Para reiniciar la captura, llame a [IDelaydC::Resume](idelaydc-resume.md).</span><span class="sxs-lookup"><span data-stu-id="0cc9b-127">To restart the capture, call [IDelaydC::Resume](idelaydc-resume.md).</span></span>

<span data-ttu-id="0cc9b-128">Para detener la captura, llame [a IDelaydC::Stop](idelaydc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="0cc9b-128">To stop the capture, call [IDelaydC::Stop](idelaydc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0cc9b-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cc9b-129">Requirements</span></span>



| <span data-ttu-id="0cc9b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cc9b-130">Requirement</span></span> | <span data-ttu-id="0cc9b-131">Valor</span><span class="sxs-lookup"><span data-stu-id="0cc9b-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cc9b-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cc9b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0cc9b-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0cc9b-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="0cc9b-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0cc9b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0cc9b-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0cc9b-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="0cc9b-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0cc9b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cc9b-137"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="0cc9b-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="0cc9b-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0cc9b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cc9b-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cc9b-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cc9b-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0cc9b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cc9b-141">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="0cc9b-141">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="0cc9b-142">IDelaydC::Connect</span><span class="sxs-lookup"><span data-stu-id="0cc9b-142">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="0cc9b-143">IDelaydC::Resume</span><span class="sxs-lookup"><span data-stu-id="0cc9b-143">IDelaydC::Resume</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="0cc9b-144">IDelaydC::Start</span><span class="sxs-lookup"><span data-stu-id="0cc9b-144">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="0cc9b-145">IDelaydC::Stop</span><span class="sxs-lookup"><span data-stu-id="0cc9b-145">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




