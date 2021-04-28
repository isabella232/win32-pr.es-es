---
description: 'Método IRTC::GetControlState: el método GetControlState recupera el estado de la captura, lo que indica si la captura se está ejecutando o en pausa.'
ms.assetid: ae0cf869-bf5b-4c23-a924-014554053c92
title: Método IRTC::GetControlState (Netmon.h)
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
ms.openlocfilehash: d2e41ad3e4119fffbada26fe3ebebdfe3bf82043
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110713"
---
# <a name="irtcgetcontrolstate-method"></a><span data-ttu-id="4287b-103">IrTC::GetControlState (método)</span><span class="sxs-lookup"><span data-stu-id="4287b-103">IRTC::GetControlState method</span></span>

<span data-ttu-id="4287b-104">El **método GetControlState** recupera el estado de [*la*](c.md)captura , lo que indica si la captura se está ejecutando o en pausa.</span><span class="sxs-lookup"><span data-stu-id="4287b-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="4287b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4287b-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="4287b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4287b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4287b-107">*IsRunnning* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4287b-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4287b-108">Indicador de que la captura actual se está ejecutando, incluido si la captura está en pausa.</span><span class="sxs-lookup"><span data-stu-id="4287b-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="4287b-109">*IsPaused* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4287b-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4287b-110">Indicador de que la captura actual está en pausa.</span><span class="sxs-lookup"><span data-stu-id="4287b-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4287b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4287b-111">Return value</span></span>

<span data-ttu-id="4287b-112">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="4287b-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="4287b-113">Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="4287b-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="4287b-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4287b-114">Return code</span></span>                                                                                          | <span data-ttu-id="4287b-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="4287b-115">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4287b-116"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="4287b-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="4287b-117">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="4287b-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="4287b-118">Llame [a IRTC::Connect](irtc-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="4287b-118">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="4287b-119"><dt>**NMERR \_ NOT \_ REALTIME**</dt></span><span class="sxs-lookup"><span data-stu-id="4287b-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="4287b-120">El NPP está conectado a la red, pero no con el [método IRTC::Connect.](irtc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="4287b-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="4287b-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4287b-121">Remarks</span></span>

<span data-ttu-id="4287b-122">Se puede llamar a este método cada vez que el NPP está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="4287b-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="4287b-123">Puede usar este método para averiguar si se está ejecutando una captura, si la captura está en pausa o si la captura se ha detenido pero el NPP todavía está conectado.</span><span class="sxs-lookup"><span data-stu-id="4287b-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="4287b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4287b-124">Requirements</span></span>



| <span data-ttu-id="4287b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4287b-125">Requirement</span></span> | <span data-ttu-id="4287b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="4287b-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4287b-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4287b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4287b-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4287b-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="4287b-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4287b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4287b-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4287b-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="4287b-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4287b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4287b-132"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="4287b-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="4287b-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4287b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4287b-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4287b-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4287b-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4287b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4287b-136">IRTC</span><span class="sxs-lookup"><span data-stu-id="4287b-136">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="4287b-137">IRTC::Connect</span><span class="sxs-lookup"><span data-stu-id="4287b-137">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="4287b-138">IRTC::P ause</span><span class="sxs-lookup"><span data-stu-id="4287b-138">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="4287b-139">IRTC::Start</span><span class="sxs-lookup"><span data-stu-id="4287b-139">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="4287b-140">IRTC::Stop</span><span class="sxs-lookup"><span data-stu-id="4287b-140">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




