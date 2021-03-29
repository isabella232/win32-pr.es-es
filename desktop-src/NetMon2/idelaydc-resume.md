---
description: El método resume reinicia una captura en pausa.
ms.assetid: 4fa47220-d323-407b-9dae-704969f66bdd
title: 'IDelaydC:: resume (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ba0deef666c2e9829cb5a71d91e73da9c1b7d780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808695"
---
# <a name="idelaydcresume-method"></a><span data-ttu-id="bc0bf-103">IDelaydC:: resume (método)</span><span class="sxs-lookup"><span data-stu-id="bc0bf-103">IDelaydC::Resume method</span></span>

<span data-ttu-id="bc0bf-104">El método **resume** reinicia una captura en pausa.</span><span class="sxs-lookup"><span data-stu-id="bc0bf-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc0bf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc0bf-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="bc0bf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc0bf-106">Parameters</span></span>

<span data-ttu-id="bc0bf-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="bc0bf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bc0bf-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc0bf-108">Return value</span></span>

<span data-ttu-id="bc0bf-109">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="bc0bf-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="bc0bf-110">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="bc0bf-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="bc0bf-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bc0bf-111">Return code</span></span>                                                                                                | <span data-ttu-id="bc0bf-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc0bf-112">Description</span></span>                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bc0bf-113"><dt>**la captura de NMERR no está en \_ \_ \_ pausa**</dt></span><span class="sxs-lookup"><span data-stu-id="bc0bf-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="bc0bf-114">La captura no está en pausa.</span><span class="sxs-lookup"><span data-stu-id="bc0bf-114">The capture is not paused.</span></span> <span data-ttu-id="bc0bf-115">Llame a [**IDelaydC::P ause**](idelaydc-pause.md) para pausar la captura.</span><span class="sxs-lookup"><span data-stu-id="bc0bf-115">Call [**IDelaydC::Pause**](idelaydc-pause.md) to pause the capture.</span></span><br/>                                |
| <dl> <span data-ttu-id="bc0bf-116"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="bc0bf-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="bc0bf-117">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="bc0bf-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="bc0bf-118">Llame a [**IDelaydC:: Connect**](idelaydc-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="bc0bf-118">Call [**IDelaydC::Connect**](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="bc0bf-119"><dt>**NMERR \_ no \_ retrasado**</dt></span><span class="sxs-lookup"><span data-stu-id="bc0bf-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>         | <span data-ttu-id="bc0bf-120">NPP está conectado a la red, pero no con el método [**IDelaydC:: Connect**](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="bc0bf-120">The NPP is connected to the network but not with the [**IDelaydC::Connect**](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="bc0bf-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc0bf-121">Remarks</span></span>

<span data-ttu-id="bc0bf-122">Mientras se pausa la captura, los nuevos datos no se agregan al [*archivo de captura*](c.md) actual hasta que se llama al método **IDelaydC:: resume** para reiniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="bc0bf-122">While the capture is paused, new data is not added to the current [*capture file*](c.md) until the **IDelaydC::Resume** method is called to restart the capture.</span></span> <span data-ttu-id="bc0bf-123">Cuando se usan [**pausar**](idelaydc-pause.md) y **reanudar** para detener y reiniciar la captura, toda la información capturada se coloca en el mismo archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="bc0bf-123">When [**Pause**](idelaydc-pause.md) and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="bc0bf-124">Al usar [**pausar**](idelaydc-pause.md) y **reanudar** para controlar la captura, monitor de red continúa agregando [*estadísticas de conversación*](c.md) a las estadísticas existentes para la captura actual.</span><span class="sxs-lookup"><span data-stu-id="bc0bf-124">When using [**Pause**](idelaydc-pause.md) and **Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="bc0bf-125">Para detener la captura, llame a [**IDelaydC:: Stop**](idelaydc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="bc0bf-125">To stop the capture, call [**IDelaydC::Stop**](idelaydc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc0bf-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc0bf-126">Requirements</span></span>



| <span data-ttu-id="bc0bf-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc0bf-127">Requirement</span></span> | <span data-ttu-id="bc0bf-128">Value</span><span class="sxs-lookup"><span data-stu-id="bc0bf-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc0bf-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc0bf-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bc0bf-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bc0bf-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="bc0bf-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc0bf-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bc0bf-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bc0bf-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="bc0bf-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc0bf-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc0bf-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc0bf-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="bc0bf-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bc0bf-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc0bf-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc0bf-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc0bf-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc0bf-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc0bf-138">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="bc0bf-138">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="bc0bf-139">**IDelaydC:: Connect**</span><span class="sxs-lookup"><span data-stu-id="bc0bf-139">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="bc0bf-140">**IDelaydC::P ause**</span><span class="sxs-lookup"><span data-stu-id="bc0bf-140">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="bc0bf-141">**IDelaydC:: Stop**</span><span class="sxs-lookup"><span data-stu-id="bc0bf-141">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




