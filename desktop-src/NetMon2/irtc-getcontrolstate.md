---
description: El método GetControlState recupera el estado de la captura, que indica si la captura se está ejecutando o está en pausa.
ms.assetid: ae0cf869-bf5b-4c23-a924-014554053c92
title: 'IRTC:: GetControlState (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d437d9463ed3225cd3a474e78220acf1f07af4bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908702"
---
# <a name="irtcgetcontrolstate-method"></a><span data-ttu-id="d47fa-103">IRTC:: GetControlState (método)</span><span class="sxs-lookup"><span data-stu-id="d47fa-103">IRTC::GetControlState method</span></span>

<span data-ttu-id="d47fa-104">El método **GetControlState** recupera el estado de la [*captura*](c.md), que indica si la captura se está ejecutando o está en pausa.</span><span class="sxs-lookup"><span data-stu-id="d47fa-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="d47fa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d47fa-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="d47fa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d47fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d47fa-107">*IsRunnning* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d47fa-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d47fa-108">Indicador de que la captura actual se está ejecutando, incluido si la captura está en pausa.</span><span class="sxs-lookup"><span data-stu-id="d47fa-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="d47fa-109">*IsPaused* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d47fa-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d47fa-110">Indicador de que la captura actual está en pausa.</span><span class="sxs-lookup"><span data-stu-id="d47fa-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d47fa-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d47fa-111">Return value</span></span>

<span data-ttu-id="d47fa-112">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d47fa-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d47fa-113">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="d47fa-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="d47fa-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d47fa-114">Return code</span></span>                                                                                          | <span data-ttu-id="d47fa-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d47fa-115">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d47fa-116"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="d47fa-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="d47fa-117">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="d47fa-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="d47fa-118">Llame a [IRTC:: Connect](irtc-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="d47fa-118">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="d47fa-119"><dt>**NMERR \_ no es en \_ tiempo real**</dt></span><span class="sxs-lookup"><span data-stu-id="d47fa-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="d47fa-120">NPP está conectado a la red, pero no con el método [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="d47fa-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="d47fa-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d47fa-121">Remarks</span></span>

<span data-ttu-id="d47fa-122">Se puede llamar a este método cada vez que el NPP esté conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="d47fa-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="d47fa-123">Puede usar este método para averiguar si se está ejecutando una captura, si la captura está en pausa, o si se ha detenido la captura pero el NPP todavía está conectado.</span><span class="sxs-lookup"><span data-stu-id="d47fa-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="d47fa-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d47fa-124">Requirements</span></span>



| <span data-ttu-id="d47fa-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d47fa-125">Requirement</span></span> | <span data-ttu-id="d47fa-126">Value</span><span class="sxs-lookup"><span data-stu-id="d47fa-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d47fa-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d47fa-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d47fa-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d47fa-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="d47fa-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d47fa-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d47fa-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d47fa-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="d47fa-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d47fa-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d47fa-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d47fa-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="d47fa-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d47fa-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d47fa-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d47fa-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d47fa-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="d47fa-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d47fa-136">IRTC</span><span class="sxs-lookup"><span data-stu-id="d47fa-136">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="d47fa-137">IRTC:: Connect</span><span class="sxs-lookup"><span data-stu-id="d47fa-137">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="d47fa-138">IRTC::P ause</span><span class="sxs-lookup"><span data-stu-id="d47fa-138">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="d47fa-139">IRTC:: Start</span><span class="sxs-lookup"><span data-stu-id="d47fa-139">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="d47fa-140">IRTC:: Stop</span><span class="sxs-lookup"><span data-stu-id="d47fa-140">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




