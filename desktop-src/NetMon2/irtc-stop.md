---
description: El método Stop detiene la captura actual.
ms.assetid: 64a80ff1-5a48-4be8-835d-a3d304ebb324
title: 'IRTC:: STOP (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: f25bf9d56a6f41acefad9a552dd2f591158bc74e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677646"
---
# <a name="irtcstop-method"></a><span data-ttu-id="246c7-103">IRTC:: STOP (método)</span><span class="sxs-lookup"><span data-stu-id="246c7-103">IRTC::Stop method</span></span>

<span data-ttu-id="246c7-104">El método **Stop** detiene la captura actual.</span><span class="sxs-lookup"><span data-stu-id="246c7-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="246c7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="246c7-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a><span data-ttu-id="246c7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="246c7-106">Parameters</span></span>

<span data-ttu-id="246c7-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="246c7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="246c7-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="246c7-108">Return value</span></span>

<span data-ttu-id="246c7-109">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="246c7-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="246c7-110">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="246c7-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="246c7-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="246c7-111">Return code</span></span>                                                                                          | <span data-ttu-id="246c7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="246c7-112">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="246c7-113"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="246c7-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="246c7-114">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="246c7-114">The NPP is not connected to the network.</span></span> <span data-ttu-id="246c7-115">Llame a [IRTC:: Connect](irtc-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="246c7-115">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="246c7-116"><dt>**NMERR \_ no se \_ captura**</dt></span><span class="sxs-lookup"><span data-stu-id="246c7-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="246c7-117">NPP no está capturando datos.</span><span class="sxs-lookup"><span data-stu-id="246c7-117">The NPP is not capturing data.</span></span> <span data-ttu-id="246c7-118">Llame a [IRTC:: Start](irtc-start.md) para iniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="246c7-118">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="246c7-119"><dt>**NMERR \_ no es en \_ tiempo real**</dt></span><span class="sxs-lookup"><span data-stu-id="246c7-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="246c7-120">NPP está conectado a la red, pero no con el método [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="246c7-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="246c7-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="246c7-121">Remarks</span></span>

<span data-ttu-id="246c7-122">Cuando reinicie la captura después de llamar al método **IRTC:: Stop** , asegúrese de llamar a [IRTC:: configure](irtc-configure.md) cada vez que llame a [IRTC:: Start](irtc-start.md) para reiniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="246c7-122">When you restart the capture after calling the **IRTC::Stop** method, make sure to call [IRTC::Configure](irtc-configure.md) each time you call [IRTC::Start](irtc-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="246c7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="246c7-123">Requirements</span></span>



| <span data-ttu-id="246c7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="246c7-124">Requirement</span></span> | <span data-ttu-id="246c7-125">Value</span><span class="sxs-lookup"><span data-stu-id="246c7-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="246c7-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="246c7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="246c7-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="246c7-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="246c7-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="246c7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="246c7-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="246c7-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="246c7-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="246c7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="246c7-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="246c7-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="246c7-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="246c7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="246c7-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="246c7-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="246c7-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="246c7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="246c7-135">IRTC</span><span class="sxs-lookup"><span data-stu-id="246c7-135">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="246c7-136">IRTC:: Connect</span><span class="sxs-lookup"><span data-stu-id="246c7-136">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="246c7-137">IRTC:: configure</span><span class="sxs-lookup"><span data-stu-id="246c7-137">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="246c7-138">IRTC:: Start</span><span class="sxs-lookup"><span data-stu-id="246c7-138">IRTC::Start</span></span>](irtc-start.md)
</dt> </dl>

 

 




