---
description: El método PAUSE pausa la captura actual.
ms.assetid: efbc8947-b9fe-4dbd-8097-375b5f99845e
title: IESP::P método ause (Netmon. h)
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
ms.openlocfilehash: 0558c5dfe36f26e3aad9f31101364d2e8e5c4967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540182"
---
# <a name="iesppause-method"></a><span data-ttu-id="ae556-103">IESP::P método ause</span><span class="sxs-lookup"><span data-stu-id="ae556-103">IESP::Pause method</span></span>

<span data-ttu-id="ae556-104">El método **PAUSE pausa** la captura actual.</span><span class="sxs-lookup"><span data-stu-id="ae556-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae556-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae556-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause(
   LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="ae556-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae556-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae556-107">*lpStats*</span><span class="sxs-lookup"><span data-stu-id="ae556-107">*lpStats*</span></span> 
</dt> <dd>

<span data-ttu-id="ae556-108">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="ae556-108">Obsolete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae556-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae556-109">Return value</span></span>

<span data-ttu-id="ae556-110">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="ae556-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="ae556-111">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="ae556-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="ae556-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ae556-112">Return code</span></span>                                                                                           | <span data-ttu-id="ae556-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae556-113">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ae556-114"><dt>**captura de NMERR en \_ \_ pausa**</dt></span><span class="sxs-lookup"><span data-stu-id="ae556-114"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="ae556-115">La captura ya está en pausa.</span><span class="sxs-lookup"><span data-stu-id="ae556-115">The capture is already paused.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="ae556-116"><dt>**NMERR \_ no se \_ captura**</dt></span><span class="sxs-lookup"><span data-stu-id="ae556-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="ae556-117">NPP no está capturando datos.</span><span class="sxs-lookup"><span data-stu-id="ae556-117">The NPP is not capturing data.</span></span> <span data-ttu-id="ae556-118">Llame a [iesp:: Start](iesp-start.md) para iniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="ae556-118">Call [IESP::Start](iesp-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="ae556-119"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="ae556-119"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="ae556-120">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="ae556-120">The NPP is not connected to the network.</span></span> <span data-ttu-id="ae556-121">Llame a [iesp:: Connect](iesp-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="ae556-121">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="ae556-122"><dt>**NMERR \_ no \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="ae556-122"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>        | <span data-ttu-id="ae556-123">NPP está conectado a la red, pero no con el método [iesp:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="ae556-123">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="ae556-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ae556-124">Remarks</span></span>

<span data-ttu-id="ae556-125">Mientras la captura está en un estado de pausa, los datos nuevos no se agregan al [*archivo de captura*](c.md) actual hasta que se llama al método [iesp:: resume](iesp-resume.md) para reiniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="ae556-125">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until you call the [IESP::Resume](iesp-resume.md) method to restart the capture.</span></span> <span data-ttu-id="ae556-126">Cuando se usan **pausar** y **reanudar** para detener y reiniciar la captura, toda la información capturada se coloca en el mismo archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="ae556-126">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="ae556-127">Cuando se usan los métodos **iesp::P ause** y **iesp:: resume** para controlar la captura, monitor de red continúa agregando [*estadísticas de conversación*](c.md) cada vez que se ejecuta la captura.</span><span class="sxs-lookup"><span data-stu-id="ae556-127">When you use the **IESP::Pause** and **IESP::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="ae556-128">Para reiniciar la captura, llame a [iesp:: resume](iesp-resume.md).</span><span class="sxs-lookup"><span data-stu-id="ae556-128">To restart the capture, call [IESP::Resume](iesp-resume.md).</span></span> <span data-ttu-id="ae556-129">Para detener la captura, llame a [iesp:: Stop](iesp-stop.md).</span><span class="sxs-lookup"><span data-stu-id="ae556-129">To stop the capture, call [IESP::Stop](iesp-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae556-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae556-130">Requirements</span></span>



| <span data-ttu-id="ae556-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae556-131">Requirement</span></span> | <span data-ttu-id="ae556-132">Value</span><span class="sxs-lookup"><span data-stu-id="ae556-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae556-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae556-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ae556-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ae556-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="ae556-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae556-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ae556-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ae556-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="ae556-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae556-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae556-138"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae556-138"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="ae556-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ae556-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae556-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae556-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae556-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae556-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae556-142">IESP</span><span class="sxs-lookup"><span data-stu-id="ae556-142">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="ae556-143">IESP:: Connect</span><span class="sxs-lookup"><span data-stu-id="ae556-143">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="ae556-144">IESP:: resume</span><span class="sxs-lookup"><span data-stu-id="ae556-144">IESP::Resume</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="ae556-145">IESP:: Start</span><span class="sxs-lookup"><span data-stu-id="ae556-145">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="ae556-146">IESP:: Stop</span><span class="sxs-lookup"><span data-stu-id="ae556-146">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




