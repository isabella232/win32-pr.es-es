---
description: El método start inicia la captura.
ms.assetid: 1f676e19-18ff-4c34-a83f-2723ff356be2
title: 'IRTC:: Start (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 3ee30112baf7813c983230fb90cd15ea7f52e2bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908698"
---
# <a name="irtcstart-method"></a><span data-ttu-id="805db-103">IRTC:: Start (método)</span><span class="sxs-lookup"><span data-stu-id="805db-103">IRTC::Start method</span></span>

<span data-ttu-id="805db-104">El método **Start** inicia la captura.</span><span class="sxs-lookup"><span data-stu-id="805db-104">The **Start** method starts the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="805db-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="805db-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a><span data-ttu-id="805db-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="805db-106">Parameters</span></span>

<span data-ttu-id="805db-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="805db-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="805db-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="805db-108">Return value</span></span>

<span data-ttu-id="805db-109">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="805db-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="805db-110">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="805db-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="805db-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="805db-111">Return code</span></span>                                                                                           | <span data-ttu-id="805db-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="805db-112">Description</span></span>                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="805db-113"><dt>**captura de NMERR en \_ \_ pausa**</dt></span><span class="sxs-lookup"><span data-stu-id="805db-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="805db-114">La captura está en un estado de pausa y debe detenerse antes de que se pueda reiniciar.</span><span class="sxs-lookup"><span data-stu-id="805db-114">The capture is in a paused state and must be stopped before it can be restarted.</span></span> <span data-ttu-id="805db-115">Llame a [IRTC:: Stop](idelaydc-stop.md) para detener la captura.</span><span class="sxs-lookup"><span data-stu-id="805db-115">Call [IRTC::Stop](idelaydc-stop.md) to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="805db-116"><dt>**captura de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="805db-116"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="805db-117">La captura ya se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="805db-117">The capture is already started.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="805db-118"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="805db-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="805db-119">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="805db-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="805db-120">Llame a [IRTC:: Connect](irtc-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="805db-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/>                         |
| <dl> <span data-ttu-id="805db-121"><dt>**NMERR \_ no es en \_ tiempo real**</dt></span><span class="sxs-lookup"><span data-stu-id="805db-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>   | <span data-ttu-id="805db-122">NPP está conectado a la red, pero no con el método [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="805db-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="805db-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="805db-123">Remarks</span></span>

<span data-ttu-id="805db-124">Cuando reinicie la captura mediante los métodos IRTC:: Start y [IRTC:: Stop](irtc-stop.md) , debe llamar al método [IRTC:: configure](irtc-configure.md) para volver a configurar la conexión cada vez que llame a IRTC:: Start para reiniciar la captura de datos.</span><span class="sxs-lookup"><span data-stu-id="805db-124">When you restart the capture by using the IRTC::Start and [IRTC::Stop](irtc-stop.md) methods, you must call the [IRTC::Configure](irtc-configure.md) method to reconfigure the connection each time you call IRTC::Start to restart the data capture.</span></span>

> [!Note]  
> <span data-ttu-id="805db-125">También puede iniciar y detener la captura mediante los métodos [IRTC::P ause](irtc-pause.md) y [IRTC:: resume](irtc-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="805db-125">You can also start and stop the capture by using the [IRTC::Pause](irtc-pause.md) and [IRTC::Resume](irtc-resume.md) methods.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="805db-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="805db-126">Requirements</span></span>



| <span data-ttu-id="805db-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="805db-127">Requirement</span></span> | <span data-ttu-id="805db-128">Value</span><span class="sxs-lookup"><span data-stu-id="805db-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="805db-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="805db-129">Minimum supported client</span></span><br/> | <span data-ttu-id="805db-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="805db-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="805db-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="805db-131">Minimum supported server</span></span><br/> | <span data-ttu-id="805db-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="805db-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="805db-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="805db-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="805db-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="805db-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="805db-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="805db-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="805db-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="805db-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="805db-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="805db-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="805db-138">IRTC</span><span class="sxs-lookup"><span data-stu-id="805db-138">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="805db-139">IRTC:: configure</span><span class="sxs-lookup"><span data-stu-id="805db-139">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="805db-140">IRTC:: Connect</span><span class="sxs-lookup"><span data-stu-id="805db-140">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="805db-141">IRTC::P ause</span><span class="sxs-lookup"><span data-stu-id="805db-141">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="805db-142">IRTC:: resume</span><span class="sxs-lookup"><span data-stu-id="805db-142">IRTC::Resume</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="805db-143">IRTC:: Stop</span><span class="sxs-lookup"><span data-stu-id="805db-143">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




