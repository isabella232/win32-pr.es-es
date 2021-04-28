---
description: 'Método IRTC::P ause: el método Pause pausa la captura actual.'
ms.assetid: 8c7b310e-de04-4bd8-9c96-3c5948e610be
title: Método IRTC::P ause (Netmon.h)
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
ms.openlocfilehash: d42af1912365a4237889e4e46d0fb3343377c772
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110683"
---
# <a name="irtcpause-method"></a><span data-ttu-id="416b2-103">IRTC::P ause (método)</span><span class="sxs-lookup"><span data-stu-id="416b2-103">IRTC::Pause method</span></span>

<span data-ttu-id="416b2-104">El **método Pause** pausa la captura actual.</span><span class="sxs-lookup"><span data-stu-id="416b2-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="416b2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="416b2-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="416b2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="416b2-106">Parameters</span></span>

<span data-ttu-id="416b2-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="416b2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="416b2-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="416b2-108">Return value</span></span>

<span data-ttu-id="416b2-109">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="416b2-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="416b2-110">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="416b2-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="416b2-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="416b2-111">Return code</span></span>                                                                                           | <span data-ttu-id="416b2-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="416b2-112">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="416b2-113"><dt>**CAPTURA DE NMERR \_ \_ EN PAUSA**</dt></span><span class="sxs-lookup"><span data-stu-id="416b2-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="416b2-114">La captura ya está en pausa.</span><span class="sxs-lookup"><span data-stu-id="416b2-114">The capture is already paused.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="416b2-115"><dt>**NMERR \_ NO \_ CAPTURA**</dt></span><span class="sxs-lookup"><span data-stu-id="416b2-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="416b2-116">El NPP no captura datos.</span><span class="sxs-lookup"><span data-stu-id="416b2-116">The NPP is not capturing data.</span></span> <span data-ttu-id="416b2-117">Llame [a IRTC::Start](irtc-start.md) para iniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="416b2-117">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="416b2-118"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="416b2-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="416b2-119">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="416b2-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="416b2-120">Llame [a IRTC::Connect](irtc-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="416b2-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="416b2-121"><dt>**NMERR \_ NOT \_ REALTIME**</dt></span><span class="sxs-lookup"><span data-stu-id="416b2-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>   | <span data-ttu-id="416b2-122">El NPP está conectado a la red, pero no con el [método IRTC::Connect.](irtc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="416b2-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="416b2-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="416b2-123">Remarks</span></span>

<span data-ttu-id="416b2-124">Mientras la captura está en estado en pausa, no se capturan nuevos fotogramas hasta que se llama al método [IRTC::Resume](irtc-resume.md) para reiniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="416b2-124">While the capture is in a paused state, new frames are not captured until the [IRTC::Resume](irtc-resume.md) method is called to restart the capture.</span></span>

<span data-ttu-id="416b2-125">Cuando se usan los métodos **IRTC::P ause** e **IRTC::Resume** para controlar la captura, Monitor de red continúa agregando [*estadísticas*](c.md) de conversación cada vez que se ejecuta la captura.</span><span class="sxs-lookup"><span data-stu-id="416b2-125">When you use the **IRTC::Pause** and **IRTC::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="416b2-126">Para reiniciar la llamada de [captura, llame a IRTC::Resume.](irtc-resume.md)</span><span class="sxs-lookup"><span data-stu-id="416b2-126">To restart the capture call [IRTC::Resume](irtc-resume.md).</span></span> <span data-ttu-id="416b2-127">Para detener la captura, llame [a IRTC::Stop](irtc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="416b2-127">To stop the capture, call [IRTC::Stop](irtc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="416b2-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="416b2-128">Requirements</span></span>



| <span data-ttu-id="416b2-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="416b2-129">Requirement</span></span> | <span data-ttu-id="416b2-130">Valor</span><span class="sxs-lookup"><span data-stu-id="416b2-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="416b2-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="416b2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="416b2-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="416b2-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="416b2-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="416b2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="416b2-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="416b2-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="416b2-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="416b2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="416b2-136"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="416b2-136"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="416b2-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="416b2-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="416b2-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="416b2-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="416b2-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="416b2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="416b2-140">IRTC</span><span class="sxs-lookup"><span data-stu-id="416b2-140">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="416b2-141">IRTC::Connect</span><span class="sxs-lookup"><span data-stu-id="416b2-141">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="416b2-142">IRTC::Resume</span><span class="sxs-lookup"><span data-stu-id="416b2-142">IRTC::Resume</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="416b2-143">IRTC::Start</span><span class="sxs-lookup"><span data-stu-id="416b2-143">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="416b2-144">IRTC::Stop</span><span class="sxs-lookup"><span data-stu-id="416b2-144">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




