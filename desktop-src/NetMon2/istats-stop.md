---
description: 'Método IStats::Stop: el método Stop detiene la captura actual.'
ms.assetid: 3aeeb29e-e174-46a2-82bb-44c466b8db98
title: Método IStats::Stop (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ef51aff870a3193963b3802332112c51f1024826
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114613"
---
# <a name="istatsstop-method"></a><span data-ttu-id="68df9-103">IStats::Stop (método)</span><span class="sxs-lookup"><span data-stu-id="68df9-103">IStats::Stop method</span></span>

<span data-ttu-id="68df9-104">El **método Stop** detiene la captura actual.</span><span class="sxs-lookup"><span data-stu-id="68df9-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="68df9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68df9-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a><span data-ttu-id="68df9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68df9-106">Parameters</span></span>

<span data-ttu-id="68df9-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="68df9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="68df9-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68df9-108">Return value</span></span>

<span data-ttu-id="68df9-109">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="68df9-109">If the method is successful the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="68df9-110">Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="68df9-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="68df9-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="68df9-111">Return code</span></span>                                                                                            | <span data-ttu-id="68df9-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="68df9-112">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="68df9-113"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="68df9-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="68df9-114">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="68df9-114">The NPP is not connected to the network.</span></span> <span data-ttu-id="68df9-115">Llame al [método IStats::Connect](istats-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="68df9-115">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="68df9-116"><dt>**NMERR \_ NO \_ CAPTURA**</dt></span><span class="sxs-lookup"><span data-stu-id="68df9-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="68df9-117">El NPP no captura datos.</span><span class="sxs-lookup"><span data-stu-id="68df9-117">The NPP is not capturing data.</span></span> <span data-ttu-id="68df9-118">Llame al [método IStats::Start](istats-start.md) para iniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="68df9-118">Call the [IStats::Start](istats-start.md) method to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="68df9-119"><dt>**NMERR \_ NO SOLO \_ \_ ESTADÍSTICAS**</dt></span><span class="sxs-lookup"><span data-stu-id="68df9-119"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="68df9-120">El NPP está conectado a la red, pero no con el [método IStats::Connect.](istats-connect.md)</span><span class="sxs-lookup"><span data-stu-id="68df9-120">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="68df9-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="68df9-121">Remarks</span></span>

<span data-ttu-id="68df9-122">Al reiniciar la captura después de llamar a **IStats::Stop,** asegúrese de llamar al método [IStats::Configure](istats-configure.md) cada vez que llame a [IStats::Start](istats-start.md) para reiniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="68df9-122">When restarting the capture after **IStats::Stop** has been called, make sure you call the [IStats::Configure](istats-configure.md) method each time you call [IStats::Start](istats-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="68df9-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68df9-123">Requirements</span></span>



| <span data-ttu-id="68df9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="68df9-124">Requirement</span></span> | <span data-ttu-id="68df9-125">Valor</span><span class="sxs-lookup"><span data-stu-id="68df9-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68df9-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68df9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="68df9-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="68df9-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="68df9-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68df9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="68df9-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="68df9-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="68df9-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68df9-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="68df9-131"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="68df9-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="68df9-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68df9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68df9-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68df9-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68df9-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="68df9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68df9-135">IStats</span><span class="sxs-lookup"><span data-stu-id="68df9-135">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="68df9-136">IStats::Connect</span><span class="sxs-lookup"><span data-stu-id="68df9-136">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="68df9-137">IStats::Configure</span><span class="sxs-lookup"><span data-stu-id="68df9-137">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="68df9-138">IStats::Start</span><span class="sxs-lookup"><span data-stu-id="68df9-138">IStats::Start</span></span>](istats-start.md)
</dt> </dl>

 

 




