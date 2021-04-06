---
description: El método GetControlState recupera el estado de la captura, que indica si la captura se está ejecutando o está en pausa.
ms.assetid: 21b7faaa-591f-4e15-b4e9-453ea690ab4a
title: 'IDelaydC:: GetControlState (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 8f5c3f084db788844f061ba2005d9c3ca38acef0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000919"
---
# <a name="idelaydcgetcontrolstate-method"></a><span data-ttu-id="6c0bc-103">IDelaydC:: GetControlState (método)</span><span class="sxs-lookup"><span data-stu-id="6c0bc-103">IDelaydC::GetControlState method</span></span>

<span data-ttu-id="6c0bc-104">El método **GetControlState** recupera el estado de la [*captura*](c.md), que indica si la captura se está ejecutando o está en pausa.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c0bc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c0bc-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="6c0bc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c0bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c0bc-107">*IsRunnning* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6c0bc-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c0bc-108">Indicador de que la captura actual se está ejecutando, incluido si la captura está en pausa.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="6c0bc-109">*IsPaused* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6c0bc-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c0bc-110">Indicador de que la captura actual está en pausa.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c0bc-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c0bc-111">Return value</span></span>

<span data-ttu-id="6c0bc-112">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6c0bc-113">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="6c0bc-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="6c0bc-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6c0bc-114">Return code</span></span>                                                                                          | <span data-ttu-id="6c0bc-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c0bc-115">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c0bc-116"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="6c0bc-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="6c0bc-117">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="6c0bc-118">Llame a [IDelaydC:: Connect](idelaydc-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-118">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="6c0bc-119"><dt>**NMERR \_ no \_ retrasado**</dt></span><span class="sxs-lookup"><span data-stu-id="6c0bc-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="6c0bc-120">NPP está conectado a la red, pero no con el método [IDelaydC:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="6c0bc-120">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="6c0bc-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c0bc-121">Remarks</span></span>

<span data-ttu-id="6c0bc-122">Se puede llamar a este método cada vez que el NPP esté conectado a la red mediante la interfaz [IDelaydC](idelaydc.md) .</span><span class="sxs-lookup"><span data-stu-id="6c0bc-122">This method can be called any time the NPP is connected to the network by using the [IDelaydC](idelaydc.md) interface.</span></span> <span data-ttu-id="6c0bc-123">Puede usar este método para averiguar si se está ejecutando una captura, si la captura está en pausa, o si se ha detenido la captura pero el NPP no está desconectado.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is not disconnected.</span></span>

<span data-ttu-id="6c0bc-124">Los métodos que se usan para iniciar, pausar y detener la captura se muestran en la lista vea también.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-124">The methods used to start, pause, and, stop the capture are listed in the See Also list below.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c0bc-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c0bc-125">Requirements</span></span>



| <span data-ttu-id="6c0bc-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c0bc-126">Requirement</span></span> | <span data-ttu-id="6c0bc-127">Value</span><span class="sxs-lookup"><span data-stu-id="6c0bc-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c0bc-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c0bc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6c0bc-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6c0bc-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="6c0bc-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c0bc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6c0bc-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6c0bc-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="6c0bc-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c0bc-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c0bc-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c0bc-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="6c0bc-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6c0bc-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c0bc-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c0bc-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c0bc-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c0bc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c0bc-137">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="6c0bc-137">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="6c0bc-138">IDelaydC:: Connect</span><span class="sxs-lookup"><span data-stu-id="6c0bc-138">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="6c0bc-139">IDelaydC::P ause</span><span class="sxs-lookup"><span data-stu-id="6c0bc-139">IDelaydC::Pause</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="6c0bc-140">IDelaydC:: Start</span><span class="sxs-lookup"><span data-stu-id="6c0bc-140">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="6c0bc-141">IDelaydC:: Stop</span><span class="sxs-lookup"><span data-stu-id="6c0bc-141">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




