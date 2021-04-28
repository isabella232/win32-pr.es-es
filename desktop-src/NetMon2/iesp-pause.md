---
description: 'Método IESP::P ause: el método Pause pausa la captura actual.'
ms.assetid: efbc8947-b9fe-4dbd-8097-375b5f99845e
title: Método IESP::P ause (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 486c7aedc7092e0dd0f9f68cc1ea2ccad08d9438
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084243"
---
# <a name="iesppause-method"></a><span data-ttu-id="edd42-103">IESP::P ause (método)</span><span class="sxs-lookup"><span data-stu-id="edd42-103">IESP::Pause method</span></span>

<span data-ttu-id="edd42-104">El **método Pause** pausa la captura actual.</span><span class="sxs-lookup"><span data-stu-id="edd42-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="edd42-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="edd42-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause(
   LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="edd42-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edd42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edd42-107">*lpStats*</span><span class="sxs-lookup"><span data-stu-id="edd42-107">*lpStats*</span></span> 
</dt> <dd>

<span data-ttu-id="edd42-108">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="edd42-108">Obsolete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edd42-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edd42-109">Return value</span></span>

<span data-ttu-id="edd42-110">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="edd42-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="edd42-111">Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="edd42-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="edd42-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="edd42-112">Return code</span></span>                                                                                           | <span data-ttu-id="edd42-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="edd42-113">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="edd42-114"><dt>**CAPTURA DE NMERR \_ \_ EN PAUSA**</dt></span><span class="sxs-lookup"><span data-stu-id="edd42-114"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="edd42-115">La captura ya está en pausa.</span><span class="sxs-lookup"><span data-stu-id="edd42-115">The capture is already paused.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="edd42-116"><dt>**NMERR \_ NO \_ CAPTURA**</dt></span><span class="sxs-lookup"><span data-stu-id="edd42-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="edd42-117">El NPP no captura datos.</span><span class="sxs-lookup"><span data-stu-id="edd42-117">The NPP is not capturing data.</span></span> <span data-ttu-id="edd42-118">Llame [a IESP::Start](iesp-start.md) para iniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="edd42-118">Call [IESP::Start](iesp-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="edd42-119"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="edd42-119"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="edd42-120">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="edd42-120">The NPP is not connected to the network.</span></span> <span data-ttu-id="edd42-121">Llame [a IESP::Connect](iesp-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="edd42-121">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="edd42-122"><dt>**NMERR \_ NOT \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="edd42-122"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>        | <span data-ttu-id="edd42-123">El NPP está conectado a la red, pero no con el [método IESP::Connect.](iesp-connect.md)</span><span class="sxs-lookup"><span data-stu-id="edd42-123">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="edd42-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="edd42-124">Remarks</span></span>

<span data-ttu-id="edd42-125">Mientras la captura está en estado en pausa, no [](c.md) se agregan nuevos datos al archivo de captura actual hasta que se llama al [método IESP::Resume](iesp-resume.md) para reiniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="edd42-125">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until you call the [IESP::Resume](iesp-resume.md) method to restart the capture.</span></span> <span data-ttu-id="edd42-126">Cuando **se** usan **Pausar y reanudar** para detener y reiniciar la captura, toda la información capturada se coloca en el mismo archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="edd42-126">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="edd42-127">Cuando se usan los métodos **IESP::P ause** e **IESP::Resume** para controlar la captura, Monitor de red continúa agregando [*estadísticas*](c.md) de conversación cada vez que se ejecuta la captura.</span><span class="sxs-lookup"><span data-stu-id="edd42-127">When you use the **IESP::Pause** and **IESP::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="edd42-128">Para reiniciar la captura, llame a [IESP::Resume](iesp-resume.md).</span><span class="sxs-lookup"><span data-stu-id="edd42-128">To restart the capture, call [IESP::Resume](iesp-resume.md).</span></span> <span data-ttu-id="edd42-129">Para detener la captura, llame a [IESP::Stop](iesp-stop.md).</span><span class="sxs-lookup"><span data-stu-id="edd42-129">To stop the capture, call [IESP::Stop](iesp-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="edd42-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edd42-130">Requirements</span></span>



| <span data-ttu-id="edd42-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="edd42-131">Requirement</span></span> | <span data-ttu-id="edd42-132">Valor</span><span class="sxs-lookup"><span data-stu-id="edd42-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edd42-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edd42-133">Minimum supported client</span></span><br/> | <span data-ttu-id="edd42-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="edd42-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="edd42-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edd42-135">Minimum supported server</span></span><br/> | <span data-ttu-id="edd42-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="edd42-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="edd42-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="edd42-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="edd42-138"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="edd42-138"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="edd42-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="edd42-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edd42-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edd42-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edd42-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="edd42-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edd42-142">IESP</span><span class="sxs-lookup"><span data-stu-id="edd42-142">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="edd42-143">IESP::Connect</span><span class="sxs-lookup"><span data-stu-id="edd42-143">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="edd42-144">IESP::Resume</span><span class="sxs-lookup"><span data-stu-id="edd42-144">IESP::Resume</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="edd42-145">IESP::Start</span><span class="sxs-lookup"><span data-stu-id="edd42-145">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="edd42-146">IESP::Stop</span><span class="sxs-lookup"><span data-stu-id="edd42-146">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




