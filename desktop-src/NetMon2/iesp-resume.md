---
description: 'Método IESP::Resume: el método Resume reinicia una captura en pausa.'
ms.assetid: 047ea5f8-de3d-40db-ada3-fc0ef4deccef
title: Método IESP::Resume (Netmon.h)
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
ms.openlocfilehash: 498beda4f2f6c61af918d542542c4ed7b789ba1a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084253"
---
# <a name="iespresume-method"></a><span data-ttu-id="598d6-103">IESP::Resume (método)</span><span class="sxs-lookup"><span data-stu-id="598d6-103">IESP::Resume method</span></span>

<span data-ttu-id="598d6-104">El **método Resume** reinicia una captura en pausa.</span><span class="sxs-lookup"><span data-stu-id="598d6-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="598d6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="598d6-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="598d6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="598d6-106">Parameters</span></span>

<span data-ttu-id="598d6-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="598d6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="598d6-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="598d6-108">Return value</span></span>

<span data-ttu-id="598d6-109">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="598d6-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="598d6-110">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="598d6-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="598d6-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="598d6-111">Return code</span></span>                                                                                                | <span data-ttu-id="598d6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="598d6-112">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="598d6-113"><dt>**CAPTURA DE NMERR \_ \_ NO \_ PAUSADA**</dt></span><span class="sxs-lookup"><span data-stu-id="598d6-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="598d6-114">La captura no está en pausa.</span><span class="sxs-lookup"><span data-stu-id="598d6-114">The capture is not paused.</span></span> <span data-ttu-id="598d6-115">Llame [**a IESP::P ause para**](iesp-pause.md) pausar la captura.</span><span class="sxs-lookup"><span data-stu-id="598d6-115">Call [**IESP::Pause**](iesp-pause.md) to pause the capture.</span></span><br/>                        |
| <dl> <span data-ttu-id="598d6-116"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="598d6-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="598d6-117">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="598d6-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="598d6-118">Llame [**a IESP::Connect**](iesp-connect.md) para conectarse a la red.</span><span class="sxs-lookup"><span data-stu-id="598d6-118">Call [**IESP::Connect**](iesp-connect.md) to connect to the network.</span></span><br/> |
| <dl> <span data-ttu-id="598d6-119"><dt>**NMERR \_ NOT \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="598d6-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>             | <span data-ttu-id="598d6-120">El NPP está conectado a la red, pero no con el [**método IESP::Connect.**](iesp-connect.md)</span><span class="sxs-lookup"><span data-stu-id="598d6-120">The NPP is connected to the network, but not with the [**IESP::Connect**](iesp-connect.md) method.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="598d6-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="598d6-121">Remarks</span></span>

<span data-ttu-id="598d6-122">Mientras la captura está en estado en pausa, no [](c.md) se agregan nuevos datos al archivo de captura actual hasta que se llama a **IESP::Resume** para reiniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="598d6-122">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until **IESP::Resume** is called to restart the capture.</span></span> <span data-ttu-id="598d6-123">Cuando **se** usan **Pausar y reanudar** para detener y reiniciar la captura, toda la información capturada se coloca en el mismo archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="598d6-123">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="598d6-124">Al usar **Pausar** **y reanudar** para controlar la captura, Monitor de red sigue agregando [*estadísticas*](c.md) de conversación a las estadísticas existentes para la captura actual.</span><span class="sxs-lookup"><span data-stu-id="598d6-124">When using **Pause** and **Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="598d6-125">Para detener la captura, llame a [**IESP::Stop**](iesp-stop.md).</span><span class="sxs-lookup"><span data-stu-id="598d6-125">To stop the capture, call [**IESP::Stop**](iesp-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="598d6-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="598d6-126">Requirements</span></span>



| <span data-ttu-id="598d6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="598d6-127">Requirement</span></span> | <span data-ttu-id="598d6-128">Valor</span><span class="sxs-lookup"><span data-stu-id="598d6-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="598d6-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="598d6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="598d6-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="598d6-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="598d6-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="598d6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="598d6-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="598d6-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="598d6-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="598d6-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="598d6-134"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="598d6-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="598d6-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="598d6-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="598d6-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="598d6-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="598d6-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="598d6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="598d6-138">IESP</span><span class="sxs-lookup"><span data-stu-id="598d6-138">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="598d6-139">**IESP::Connect**</span><span class="sxs-lookup"><span data-stu-id="598d6-139">**IESP::Connect**</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="598d6-140">**IESP::P ause**</span><span class="sxs-lookup"><span data-stu-id="598d6-140">**IESP::Pause**</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="598d6-141">**IESP::Stop**</span><span class="sxs-lookup"><span data-stu-id="598d6-141">**IESP::Stop**</span></span>](iesp-stop.md)
</dt> </dl>

 

 




