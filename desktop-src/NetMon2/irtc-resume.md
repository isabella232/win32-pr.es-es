---
description: 'Método IRTC::Resume: el método Resume reinicia una captura en pausa.'
ms.assetid: 685dfdee-3bd0-44b3-ac4f-c9960cf77c5c
title: Método IRTC::Resume (Netmon.h)
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
ms.openlocfilehash: 55e5cb66eecbee96df9573e9347d1f32e3508d2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110573"
---
# <a name="irtcresume-method"></a><span data-ttu-id="4692e-103">IrTC::Resume (método)</span><span class="sxs-lookup"><span data-stu-id="4692e-103">IRTC::Resume method</span></span>

<span data-ttu-id="4692e-104">El **método Resume** reinicia una captura en pausa.</span><span class="sxs-lookup"><span data-stu-id="4692e-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="4692e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4692e-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="4692e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4692e-106">Parameters</span></span>

<span data-ttu-id="4692e-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="4692e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4692e-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4692e-108">Return value</span></span>

<span data-ttu-id="4692e-109">Si el método se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="4692e-109">If the method is successful the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="4692e-110">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="4692e-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="4692e-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4692e-111">Return code</span></span>                                                                                                | <span data-ttu-id="4692e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4692e-112">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4692e-113"><dt>**CAPTURA DE NMERR \_ \_ NO \_ PAUSADA**</dt></span><span class="sxs-lookup"><span data-stu-id="4692e-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="4692e-114">La captura no está en pausa.</span><span class="sxs-lookup"><span data-stu-id="4692e-114">The capture is not paused.</span></span> <span data-ttu-id="4692e-115">Llame [a IRTC::P ause para](irtc-pause.md) pausar la captura.</span><span class="sxs-lookup"><span data-stu-id="4692e-115">Call [IRTC::Pause](irtc-pause.md) to pause the capture.</span></span><br/>                                |
| <dl> <span data-ttu-id="4692e-116"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="4692e-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="4692e-117">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="4692e-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="4692e-118">Llame [a IRTC::Connect](irtc-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="4692e-118">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="4692e-119"><dt>**NMERR \_ NOT \_ REALTIME**</dt></span><span class="sxs-lookup"><span data-stu-id="4692e-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>        | <span data-ttu-id="4692e-120">El NPP está conectado a la red, pero no con el [método IRTC::Connect.](irtc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="4692e-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="4692e-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4692e-121">Remarks</span></span>

<span data-ttu-id="4692e-122">Mientras la captura está en estado en pausa, los nuevos datos no se capturan hasta que una llamada al método [IRTC::Resume](idelaydc-resume.md) reinicia la captura.</span><span class="sxs-lookup"><span data-stu-id="4692e-122">While the capture is in a paused state, new data is not captured until a call to the [IRTC::Resume](idelaydc-resume.md) method restarts the capture.</span></span>

<span data-ttu-id="4692e-123">Al usar los  **métodos Pausar** y Reanudar para controlar la captura, Monitor de red sigue agregando estadísticas de conversación a las [*estadísticas*](c.md) existentes para la captura actual.</span><span class="sxs-lookup"><span data-stu-id="4692e-123">When using the **Pause** and **Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="4692e-124">Para detener la captura, llame al [método IRTC::Stop.](irtc-stop.md)</span><span class="sxs-lookup"><span data-stu-id="4692e-124">To stop the capture, call the [IRTC::Stop](irtc-stop.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4692e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4692e-125">Requirements</span></span>



| <span data-ttu-id="4692e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4692e-126">Requirement</span></span> | <span data-ttu-id="4692e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="4692e-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4692e-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4692e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4692e-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4692e-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="4692e-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4692e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4692e-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4692e-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="4692e-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4692e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4692e-133"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="4692e-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="4692e-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4692e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4692e-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4692e-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4692e-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4692e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4692e-137">IRTC</span><span class="sxs-lookup"><span data-stu-id="4692e-137">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="4692e-138">IRTC::Connect</span><span class="sxs-lookup"><span data-stu-id="4692e-138">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="4692e-139">IRTC::P ause</span><span class="sxs-lookup"><span data-stu-id="4692e-139">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="4692e-140">IRTC::Stop</span><span class="sxs-lookup"><span data-stu-id="4692e-140">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




