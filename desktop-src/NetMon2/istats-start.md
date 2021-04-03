---
description: El método start inicia una captura.
ms.assetid: d4086e30-e5ed-4f29-90f0-d65125d9af6d
title: 'IStas:: Start (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d58821ecc06e0a25d6a260bb2ba9393162dcdca8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908183"
---
# <a name="istatsstart-method"></a><span data-ttu-id="09688-103">IStas:: Start (método)</span><span class="sxs-lookup"><span data-stu-id="09688-103">IStats::Start method</span></span>

<span data-ttu-id="09688-104">El método **Start** inicia una captura.</span><span class="sxs-lookup"><span data-stu-id="09688-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="09688-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09688-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a><span data-ttu-id="09688-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09688-106">Parameters</span></span>

<span data-ttu-id="09688-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="09688-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="09688-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09688-108">Return value</span></span>

<span data-ttu-id="09688-109">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="09688-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="09688-110">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="09688-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="09688-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="09688-111">Return code</span></span>                                                                                            | <span data-ttu-id="09688-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="09688-112">Description</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="09688-113"><dt>**captura de NMERR en \_ \_ pausa**</dt></span><span class="sxs-lookup"><span data-stu-id="09688-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl>  | <span data-ttu-id="09688-114">La captura se ha pausado y debe detenerse antes de que se pueda reiniciar.</span><span class="sxs-lookup"><span data-stu-id="09688-114">The capture has paused and must be stopped before it can be restarted.</span></span> <span data-ttu-id="09688-115">Llame al método [istas:: Stop](istats-stop.md) para detener la captura.</span><span class="sxs-lookup"><span data-stu-id="09688-115">Call the [IStats::Stop](istats-stop.md) method to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="09688-116"><dt>**captura de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="09688-116"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>        | <span data-ttu-id="09688-117">La captura ya se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="09688-117">The capture has already started.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="09688-118"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="09688-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="09688-119">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="09688-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="09688-120">Llame al método [istas:: Connect](istats-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="09688-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/>           |
| <dl> <span data-ttu-id="09688-121"><dt>**NMERR \_ no \_ solo estadísticas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="09688-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="09688-122">NPP está conectado a la red, pero no con el método [istas:: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="09688-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="09688-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09688-123">Remarks</span></span>

<span data-ttu-id="09688-124">Al reiniciar la captura mediante los métodos IStas:: Start y [istas:: Stop](istats-stop.md) , debe llamar al método [istas:: configure](istats-configure.md) para volver a configurar la conexión cada vez que llame a los ISTA:: Start para reiniciar la captura de datos.</span><span class="sxs-lookup"><span data-stu-id="09688-124">When restarting the capture by using the IStats::Start and [IStats::Stop](istats-stop.md) methods, you must call the [IStats::Configure](istats-configure.md) method to reconfigure the connection each time you call IStats::Start to restart the data capture.</span></span>

> [!Note]  
> <span data-ttu-id="09688-125">También puede iniciar y detener la captura mediante los [istas::P ause](istats-pause.md) y [istas:: resume](istats-resume.md) (métodos).</span><span class="sxs-lookup"><span data-stu-id="09688-125">You can also start and stop the capture by using the [IStats::Pause](istats-pause.md) and [IStats::Resume](istats-resume.md) methods.</span></span> <span data-ttu-id="09688-126">Cuando se usan estos métodos, los datos capturados se almacenan en el mismo archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="09688-126">When you use these methods, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="09688-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09688-127">Requirements</span></span>



| <span data-ttu-id="09688-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="09688-128">Requirement</span></span> | <span data-ttu-id="09688-129">Value</span><span class="sxs-lookup"><span data-stu-id="09688-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09688-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09688-130">Minimum supported client</span></span><br/> | <span data-ttu-id="09688-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="09688-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="09688-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09688-132">Minimum supported server</span></span><br/> | <span data-ttu-id="09688-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="09688-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="09688-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09688-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="09688-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="09688-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="09688-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="09688-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09688-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09688-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09688-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="09688-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09688-139">IStas</span><span class="sxs-lookup"><span data-stu-id="09688-139">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="09688-140">ISta:: configurar</span><span class="sxs-lookup"><span data-stu-id="09688-140">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="09688-141">ISta:: Connect</span><span class="sxs-lookup"><span data-stu-id="09688-141">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="09688-142">IStas::P ause</span><span class="sxs-lookup"><span data-stu-id="09688-142">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="09688-143">IStas:: resume</span><span class="sxs-lookup"><span data-stu-id="09688-143">IStats::Resume</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="09688-144">IStas:: Stop</span><span class="sxs-lookup"><span data-stu-id="09688-144">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




