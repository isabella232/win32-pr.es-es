---
description: 'Método IDelaydC::GetControlState: el método GetControlState recupera el estado de la captura, lo que indica si la captura se está ejecutando o en pausa.'
ms.assetid: 21b7faaa-591f-4e15-b4e9-453ea690ab4a
title: Método IDelaydC::GetControlState (Netmon.h)
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
ms.openlocfilehash: 825112ec9a33ef176d5a69765837214249e33102
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110773"
---
# <a name="idelaydcgetcontrolstate-method"></a><span data-ttu-id="a5bb7-103">IDelaydC::GetControlState (método)</span><span class="sxs-lookup"><span data-stu-id="a5bb7-103">IDelaydC::GetControlState method</span></span>

<span data-ttu-id="a5bb7-104">El **método GetControlState** recupera el estado de [*la*](c.md)captura , lo que indica si la captura se está ejecutando o en pausa.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5bb7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5bb7-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="a5bb7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5bb7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5bb7-107">*IsRunnning* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a5bb7-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5bb7-108">Indicador de que la captura actual se está ejecutando, incluido si la captura está en pausa.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="a5bb7-109">*IsPaused* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a5bb7-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5bb7-110">Indicador de que la captura actual está en pausa.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5bb7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5bb7-111">Return value</span></span>

<span data-ttu-id="a5bb7-112">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="a5bb7-113">Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="a5bb7-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="a5bb7-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a5bb7-114">Return code</span></span>                                                                                          | <span data-ttu-id="a5bb7-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5bb7-115">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a5bb7-116"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="a5bb7-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="a5bb7-117">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="a5bb7-118">Llame [a IDelaydC::Connect](idelaydc-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-118">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="a5bb7-119"><dt>**NMERR \_ NO \_ RETRASADO**</dt></span><span class="sxs-lookup"><span data-stu-id="a5bb7-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="a5bb7-120">El NPP está conectado a la red, pero no con el [método IDelaydC::Connect.](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="a5bb7-120">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="a5bb7-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a5bb7-121">Remarks</span></span>

<span data-ttu-id="a5bb7-122">Se puede llamar a este método cada vez que el NPP se conecta a la red mediante la [interfaz IDelaydC.](idelaydc.md)</span><span class="sxs-lookup"><span data-stu-id="a5bb7-122">This method can be called any time the NPP is connected to the network by using the [IDelaydC](idelaydc.md) interface.</span></span> <span data-ttu-id="a5bb7-123">Puede usar este método para averiguar si se está ejecutando una captura, si la captura está en pausa o si la captura se ha detenido pero el NPP no está desconectado.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is not disconnected.</span></span>

<span data-ttu-id="a5bb7-124">Los métodos usados para iniciar, pausar y detener la captura se enumeran en la lista Vea también a continuación.</span><span class="sxs-lookup"><span data-stu-id="a5bb7-124">The methods used to start, pause, and, stop the capture are listed in the See Also list below.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5bb7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5bb7-125">Requirements</span></span>



| <span data-ttu-id="a5bb7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5bb7-126">Requirement</span></span> | <span data-ttu-id="a5bb7-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a5bb7-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5bb7-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5bb7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a5bb7-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a5bb7-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="a5bb7-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5bb7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a5bb7-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a5bb7-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="a5bb7-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5bb7-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5bb7-133"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="a5bb7-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="a5bb7-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a5bb7-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5bb7-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5bb7-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5bb7-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a5bb7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5bb7-137">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="a5bb7-137">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="a5bb7-138">IDelaydC::Connect</span><span class="sxs-lookup"><span data-stu-id="a5bb7-138">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="a5bb7-139">IDelaydC::P ause</span><span class="sxs-lookup"><span data-stu-id="a5bb7-139">IDelaydC::Pause</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="a5bb7-140">IDelaydC::Start</span><span class="sxs-lookup"><span data-stu-id="a5bb7-140">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="a5bb7-141">IDelaydC::Stop</span><span class="sxs-lookup"><span data-stu-id="a5bb7-141">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




