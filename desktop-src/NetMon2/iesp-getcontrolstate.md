---
description: El método GetControlState recupera el estado de la captura, que indica si la captura se está ejecutando o está en pausa.
ms.assetid: 19cc3095-3aa3-4482-95f5-959b19f76cea
title: 'IESP:: GetControlState (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: c791d5dc1f5d5321268fef2fb5cf91e04d9ecff3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686559"
---
# <a name="iespgetcontrolstate-method"></a><span data-ttu-id="ac01b-103">IESP:: GetControlState (método)</span><span class="sxs-lookup"><span data-stu-id="ac01b-103">IESP::GetControlState method</span></span>

<span data-ttu-id="ac01b-104">El método **GetControlState** recupera el estado de la [*captura*](c.md), que indica si la captura se está ejecutando o está en pausa.</span><span class="sxs-lookup"><span data-stu-id="ac01b-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac01b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac01b-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="ac01b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac01b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac01b-107">*IsRunnning* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ac01b-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac01b-108">Indicador de que la captura actual se está ejecutando, incluido si la captura está en pausa.</span><span class="sxs-lookup"><span data-stu-id="ac01b-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="ac01b-109">*IsPaused* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ac01b-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac01b-110">Indicador de que la captura actual está en pausa.</span><span class="sxs-lookup"><span data-stu-id="ac01b-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac01b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac01b-111">Return value</span></span>

<span data-ttu-id="ac01b-112">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="ac01b-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="ac01b-113">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="ac01b-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="ac01b-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ac01b-114">Return code</span></span>                                                                                          | <span data-ttu-id="ac01b-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac01b-115">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ac01b-116"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="ac01b-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="ac01b-117">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="ac01b-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="ac01b-118">Llame a [iesp:: Connect](iesp-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="ac01b-118">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="ac01b-119"><dt>**NMERR \_ no \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="ac01b-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="ac01b-120">NPP está conectado a la red, pero no con el método [iesp:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="ac01b-120">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="ac01b-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac01b-121">Remarks</span></span>

<span data-ttu-id="ac01b-122">Se puede llamar a este método cada vez que el NPP esté conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="ac01b-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="ac01b-123">Puede usar este método para averiguar si se está ejecutando una captura, si la captura está en pausa, o si se ha detenido la captura pero el NPP todavía está conectado.</span><span class="sxs-lookup"><span data-stu-id="ac01b-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac01b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac01b-124">Requirements</span></span>



| <span data-ttu-id="ac01b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac01b-125">Requirement</span></span> | <span data-ttu-id="ac01b-126">Value</span><span class="sxs-lookup"><span data-stu-id="ac01b-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac01b-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac01b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ac01b-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ac01b-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="ac01b-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac01b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ac01b-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ac01b-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="ac01b-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac01b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac01b-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac01b-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="ac01b-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ac01b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac01b-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac01b-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac01b-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac01b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac01b-136">IESP</span><span class="sxs-lookup"><span data-stu-id="ac01b-136">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="ac01b-137">IESP:: Connect</span><span class="sxs-lookup"><span data-stu-id="ac01b-137">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="ac01b-138">IESP::P ause</span><span class="sxs-lookup"><span data-stu-id="ac01b-138">IESP::Pause</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="ac01b-139">IESP:: Start</span><span class="sxs-lookup"><span data-stu-id="ac01b-139">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="ac01b-140">IESP:: Stop</span><span class="sxs-lookup"><span data-stu-id="ac01b-140">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




