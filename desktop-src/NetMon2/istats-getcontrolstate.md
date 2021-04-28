---
description: 'Método IStats::GetControlState: el método GetControlState recupera el estado de la captura, lo que indica si la captura se está ejecutando o en pausa.'
ms.assetid: 0faf2300-d9ff-4fe0-9d50-18beafd1daea
title: Método IStats::GetControlState (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 25532293335756a872ef5104d5eef66027fe2ae4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098473"
---
# <a name="istatsgetcontrolstate-method"></a><span data-ttu-id="9ecba-103">IStats::GetControlState (método)</span><span class="sxs-lookup"><span data-stu-id="9ecba-103">IStats::GetControlState method</span></span>

<span data-ttu-id="9ecba-104">El **método GetControlState** recupera el estado de [*la*](c.md)captura , lo que indica si la captura se está ejecutando o en pausa.</span><span class="sxs-lookup"><span data-stu-id="9ecba-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ecba-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ecba-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="9ecba-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ecba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ecba-107">*IsRunnning* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9ecba-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ecba-108">Indicador de que la captura actual se está ejecutando, incluido si la captura está en pausa.</span><span class="sxs-lookup"><span data-stu-id="9ecba-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="9ecba-109">*IsPaused* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9ecba-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ecba-110">Indicador de que la captura actual está en pausa.</span><span class="sxs-lookup"><span data-stu-id="9ecba-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ecba-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ecba-111">Return value</span></span>

<span data-ttu-id="9ecba-112">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="9ecba-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="9ecba-113">Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="9ecba-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="9ecba-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9ecba-114">Return code</span></span>                                                                                            | <span data-ttu-id="9ecba-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="9ecba-115">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9ecba-116"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="9ecba-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="9ecba-117">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="9ecba-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="9ecba-118">Llame [a IStats::Connect](istats-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="9ecba-118">Call [IStats::Connect](istats-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="9ecba-119"><dt>**NMERR \_ NO SOLO \_ \_ ESTADÍSTICAS**</dt></span><span class="sxs-lookup"><span data-stu-id="9ecba-119"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="9ecba-120">El NPP está conectado a la red, pero no con el [método IStats::Connect.](istats-connect.md)</span><span class="sxs-lookup"><span data-stu-id="9ecba-120">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="9ecba-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9ecba-121">Remarks</span></span>

<span data-ttu-id="9ecba-122">Se puede llamar a este método cada vez que el NPP está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="9ecba-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="9ecba-123">Puede usar este método para averiguar si se está ejecutando una captura, si la captura está en pausa o si la captura se ha detenido pero el NPP no está desconectado.</span><span class="sxs-lookup"><span data-stu-id="9ecba-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is not disconnected.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ecba-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ecba-124">Requirements</span></span>



| <span data-ttu-id="9ecba-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ecba-125">Requirement</span></span> | <span data-ttu-id="9ecba-126">Valor</span><span class="sxs-lookup"><span data-stu-id="9ecba-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ecba-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ecba-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9ecba-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9ecba-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="9ecba-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ecba-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9ecba-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9ecba-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="9ecba-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ecba-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ecba-132"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="9ecba-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="9ecba-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9ecba-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ecba-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ecba-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ecba-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9ecba-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ecba-136">IStats</span><span class="sxs-lookup"><span data-stu-id="9ecba-136">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="9ecba-137">IStats::Connect</span><span class="sxs-lookup"><span data-stu-id="9ecba-137">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="9ecba-138">IStats::P ause</span><span class="sxs-lookup"><span data-stu-id="9ecba-138">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="9ecba-139">IStatsC::Start</span><span class="sxs-lookup"><span data-stu-id="9ecba-139">IStatsC::Start</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="9ecba-140">IStatsC::Stop</span><span class="sxs-lookup"><span data-stu-id="9ecba-140">IStatsC::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




