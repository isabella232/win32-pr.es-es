---
description: El método PAUSE pausa la captura actual.
ms.assetid: 8c7b310e-de04-4bd8-9c96-3c5948e610be
title: IRTC::P método ause (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d2593c380d0fea52d030586da2f473a3f3fa9446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276277"
---
# <a name="irtcpause-method"></a><span data-ttu-id="beea3-103">IRTC::P método ause</span><span class="sxs-lookup"><span data-stu-id="beea3-103">IRTC::Pause method</span></span>

<span data-ttu-id="beea3-104">El método **PAUSE pausa** la captura actual.</span><span class="sxs-lookup"><span data-stu-id="beea3-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="beea3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="beea3-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="beea3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="beea3-106">Parameters</span></span>

<span data-ttu-id="beea3-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="beea3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="beea3-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="beea3-108">Return value</span></span>

<span data-ttu-id="beea3-109">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="beea3-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="beea3-110">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="beea3-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="beea3-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="beea3-111">Return code</span></span>                                                                                           | <span data-ttu-id="beea3-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="beea3-112">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="beea3-113"><dt>**captura de NMERR en \_ \_ pausa**</dt></span><span class="sxs-lookup"><span data-stu-id="beea3-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="beea3-114">La captura ya está en pausa.</span><span class="sxs-lookup"><span data-stu-id="beea3-114">The capture is already paused.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="beea3-115"><dt>**NMERR \_ no se \_ captura**</dt></span><span class="sxs-lookup"><span data-stu-id="beea3-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="beea3-116">NPP no está capturando datos.</span><span class="sxs-lookup"><span data-stu-id="beea3-116">The NPP is not capturing data.</span></span> <span data-ttu-id="beea3-117">Llame a [IRTC:: Start](irtc-start.md) para iniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="beea3-117">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="beea3-118"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="beea3-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="beea3-119">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="beea3-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="beea3-120">Llame a [IRTC:: Connect](irtc-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="beea3-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="beea3-121"><dt>**NMERR \_ no es en \_ tiempo real**</dt></span><span class="sxs-lookup"><span data-stu-id="beea3-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>   | <span data-ttu-id="beea3-122">NPP está conectado a la red, pero no con el método [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="beea3-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="beea3-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="beea3-123">Remarks</span></span>

<span data-ttu-id="beea3-124">Mientras la captura está en un estado de pausa, no se capturan nuevos fotogramas hasta que se llama al método [IRTC:: resume](irtc-resume.md) para reiniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="beea3-124">While the capture is in a paused state, new frames are not captured until the [IRTC::Resume](irtc-resume.md) method is called to restart the capture.</span></span>

<span data-ttu-id="beea3-125">Cuando se usan los métodos **IRTC::P ause** y **IRTC:: resume** para controlar la captura, monitor de red continúa agregando [*estadísticas de conversación*](c.md) cada vez que se ejecuta la captura.</span><span class="sxs-lookup"><span data-stu-id="beea3-125">When you use the **IRTC::Pause** and **IRTC::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="beea3-126">Para reiniciar la llamada de captura [IRTC:: resume](irtc-resume.md).</span><span class="sxs-lookup"><span data-stu-id="beea3-126">To restart the capture call [IRTC::Resume](irtc-resume.md).</span></span> <span data-ttu-id="beea3-127">Para detener la captura, llame a [IRTC:: Stop](irtc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="beea3-127">To stop the capture, call [IRTC::Stop](irtc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="beea3-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="beea3-128">Requirements</span></span>



| <span data-ttu-id="beea3-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="beea3-129">Requirement</span></span> | <span data-ttu-id="beea3-130">Value</span><span class="sxs-lookup"><span data-stu-id="beea3-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="beea3-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="beea3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="beea3-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="beea3-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="beea3-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="beea3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="beea3-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="beea3-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="beea3-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="beea3-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="beea3-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="beea3-136"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="beea3-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="beea3-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="beea3-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="beea3-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beea3-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="beea3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beea3-140">IRTC</span><span class="sxs-lookup"><span data-stu-id="beea3-140">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="beea3-141">IRTC:: Connect</span><span class="sxs-lookup"><span data-stu-id="beea3-141">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="beea3-142">IRTC:: resume</span><span class="sxs-lookup"><span data-stu-id="beea3-142">IRTC::Resume</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="beea3-143">IRTC:: Start</span><span class="sxs-lookup"><span data-stu-id="beea3-143">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="beea3-144">IRTC:: Stop</span><span class="sxs-lookup"><span data-stu-id="beea3-144">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




