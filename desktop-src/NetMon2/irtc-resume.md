---
description: El método resume reinicia una captura en pausa.
ms.assetid: 685dfdee-3bd0-44b3-ac4f-c9960cf77c5c
title: 'IRTC:: resume (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 991f70944b44ce13641318219788d9d6122b15c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677645"
---
# <a name="irtcresume-method"></a><span data-ttu-id="ef1d2-103">IRTC:: resume (método)</span><span class="sxs-lookup"><span data-stu-id="ef1d2-103">IRTC::Resume method</span></span>

<span data-ttu-id="ef1d2-104">El método **resume** reinicia una captura en pausa.</span><span class="sxs-lookup"><span data-stu-id="ef1d2-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef1d2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef1d2-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="ef1d2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef1d2-106">Parameters</span></span>

<span data-ttu-id="ef1d2-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ef1d2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ef1d2-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef1d2-108">Return value</span></span>

<span data-ttu-id="ef1d2-109">Si el método se ejecuta correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="ef1d2-109">If the method is successful the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="ef1d2-110">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="ef1d2-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="ef1d2-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ef1d2-111">Return code</span></span>                                                                                                | <span data-ttu-id="ef1d2-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef1d2-112">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef1d2-113"><dt>**la captura de NMERR no está en \_ \_ \_ pausa**</dt></span><span class="sxs-lookup"><span data-stu-id="ef1d2-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="ef1d2-114">La captura no está en pausa.</span><span class="sxs-lookup"><span data-stu-id="ef1d2-114">The capture is not paused.</span></span> <span data-ttu-id="ef1d2-115">Llame a [IRTC::P ause](irtc-pause.md) para pausar la captura.</span><span class="sxs-lookup"><span data-stu-id="ef1d2-115">Call [IRTC::Pause](irtc-pause.md) to pause the capture.</span></span><br/>                                |
| <dl> <span data-ttu-id="ef1d2-116"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="ef1d2-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="ef1d2-117">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="ef1d2-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="ef1d2-118">Llame a [IRTC:: Connect](irtc-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="ef1d2-118">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="ef1d2-119"><dt>**NMERR \_ no es en \_ tiempo real**</dt></span><span class="sxs-lookup"><span data-stu-id="ef1d2-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>        | <span data-ttu-id="ef1d2-120">NPP está conectado a la red, pero no con el método [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="ef1d2-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="ef1d2-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef1d2-121">Remarks</span></span>

<span data-ttu-id="ef1d2-122">Mientras la captura está en un estado de pausa, los nuevos datos no se capturan hasta que una llamada al método [IRTC:: resume](idelaydc-resume.md) reinicie la captura.</span><span class="sxs-lookup"><span data-stu-id="ef1d2-122">While the capture is in a paused state, new data is not captured until a call to the [IRTC::Resume](idelaydc-resume.md) method restarts the capture.</span></span>

<span data-ttu-id="ef1d2-123">Al usar los métodos **pausar** y **reanudar** para controlar la captura, monitor de red continúa agregando [*estadísticas de conversación*](c.md) a las estadísticas existentes para la captura actual.</span><span class="sxs-lookup"><span data-stu-id="ef1d2-123">When using the **Pause** and **Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="ef1d2-124">Para detener la captura, llame al método [IRTC:: Stop](irtc-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="ef1d2-124">To stop the capture, call the [IRTC::Stop](irtc-stop.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef1d2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef1d2-125">Requirements</span></span>



| <span data-ttu-id="ef1d2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef1d2-126">Requirement</span></span> | <span data-ttu-id="ef1d2-127">Value</span><span class="sxs-lookup"><span data-stu-id="ef1d2-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef1d2-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef1d2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ef1d2-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ef1d2-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="ef1d2-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef1d2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ef1d2-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ef1d2-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="ef1d2-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef1d2-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef1d2-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef1d2-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="ef1d2-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ef1d2-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef1d2-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef1d2-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef1d2-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef1d2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef1d2-137">IRTC</span><span class="sxs-lookup"><span data-stu-id="ef1d2-137">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="ef1d2-138">IRTC:: Connect</span><span class="sxs-lookup"><span data-stu-id="ef1d2-138">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="ef1d2-139">IRTC::P ause</span><span class="sxs-lookup"><span data-stu-id="ef1d2-139">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="ef1d2-140">IRTC:: Stop</span><span class="sxs-lookup"><span data-stu-id="ef1d2-140">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




