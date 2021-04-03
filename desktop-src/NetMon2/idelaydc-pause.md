---
description: El método PAUSE pausa la captura actual.
ms.assetid: 9d5e11d1-8c45-4cf5-9fea-10c9e7a6fe86
title: IDelaydC::P método ause (Netmon. h)
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
ms.openlocfilehash: d44ae7792388d9ca637232b45e63d618a37acb6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907663"
---
# <a name="idelaydcpause-method"></a><span data-ttu-id="347ad-103">IDelaydC::P método ause</span><span class="sxs-lookup"><span data-stu-id="347ad-103">IDelaydC::Pause method</span></span>

<span data-ttu-id="347ad-104">El método **PAUSE pausa** la captura actual.</span><span class="sxs-lookup"><span data-stu-id="347ad-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="347ad-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="347ad-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="347ad-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="347ad-106">Parameters</span></span>

<span data-ttu-id="347ad-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="347ad-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="347ad-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="347ad-108">Return value</span></span>

<span data-ttu-id="347ad-109">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="347ad-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="347ad-110">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="347ad-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="347ad-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="347ad-111">Return code</span></span>                                                                                           | <span data-ttu-id="347ad-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="347ad-112">Description</span></span>                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="347ad-113"><dt>**captura de NMERR en \_ \_ pausa**</dt></span><span class="sxs-lookup"><span data-stu-id="347ad-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="347ad-114">La captura ya está en un estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="347ad-114">The capture is already in a paused state.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="347ad-115"><dt>**NMERR \_ no se \_ captura**</dt></span><span class="sxs-lookup"><span data-stu-id="347ad-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="347ad-116">NPP no está capturando datos.</span><span class="sxs-lookup"><span data-stu-id="347ad-116">The NPP is not capturing data.</span></span> <span data-ttu-id="347ad-117">Llame a [IDelaydC:: Start](idelaydc-start.md) para iniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="347ad-117">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="347ad-118"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="347ad-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="347ad-119">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="347ad-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="347ad-120">Llame a [IDelaydC:: Connect](idelaydc-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="347ad-120">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="347ad-121"><dt>**NMERR \_ no \_ retrasado**</dt></span><span class="sxs-lookup"><span data-stu-id="347ad-121"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>    | <span data-ttu-id="347ad-122">NPP está conectado a la red, pero no con el método [IDelaydC:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="347ad-122">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="347ad-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="347ad-123">Remarks</span></span>

<span data-ttu-id="347ad-124">Mientras la captura está en un estado de pausa, los datos nuevos no se agregan al [*archivo de captura*](c.md) actual hasta que se llama al método **IDelaydC:: resume** para reiniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="347ad-124">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until the **IDelaydC::Resume** method is called to restart the capture.</span></span> <span data-ttu-id="347ad-125">Cuando se usan **pausar** y **reanudar** para detener y reiniciar la captura, toda la información capturada se coloca en el mismo archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="347ad-125">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="347ad-126">Al usar **IDelaydC::P ause** y **IDelaydC:: resume** para controlar la captura, monitor de red continúa agregando [*estadísticas de conversación*](c.md) cada vez que se ejecuta la captura.</span><span class="sxs-lookup"><span data-stu-id="347ad-126">When using **IDelaydC::Pause** and **IDelaydC::Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="347ad-127">Para reiniciar la captura, llame a [IDelaydC:: resume](idelaydc-resume.md).</span><span class="sxs-lookup"><span data-stu-id="347ad-127">To restart the capture, call [IDelaydC::Resume](idelaydc-resume.md).</span></span>

<span data-ttu-id="347ad-128">Para detener la captura, llame a [IDelaydC:: Stop](idelaydc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="347ad-128">To stop the capture, call [IDelaydC::Stop](idelaydc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="347ad-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="347ad-129">Requirements</span></span>



| <span data-ttu-id="347ad-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="347ad-130">Requirement</span></span> | <span data-ttu-id="347ad-131">Value</span><span class="sxs-lookup"><span data-stu-id="347ad-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="347ad-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="347ad-132">Minimum supported client</span></span><br/> | <span data-ttu-id="347ad-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="347ad-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="347ad-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="347ad-134">Minimum supported server</span></span><br/> | <span data-ttu-id="347ad-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="347ad-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="347ad-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="347ad-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="347ad-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="347ad-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="347ad-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="347ad-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="347ad-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="347ad-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="347ad-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="347ad-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="347ad-141">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="347ad-141">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="347ad-142">IDelaydC:: Connect</span><span class="sxs-lookup"><span data-stu-id="347ad-142">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="347ad-143">IDelaydC:: resume</span><span class="sxs-lookup"><span data-stu-id="347ad-143">IDelaydC::Resume</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="347ad-144">IDelaydC:: Start</span><span class="sxs-lookup"><span data-stu-id="347ad-144">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="347ad-145">IDelaydC:: Stop</span><span class="sxs-lookup"><span data-stu-id="347ad-145">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




