---
description: 'Método IStats::Start: el método Start inicia una captura.'
ms.assetid: d4086e30-e5ed-4f29-90f0-d65125d9af6d
title: Método IStats::Start (Netmon.h)
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
ms.openlocfilehash: 64f02529ba10d98092eb30a1bcc350d5c72049fc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094553"
---
# <a name="istatsstart-method"></a><span data-ttu-id="cad81-103">IStats::Start (método)</span><span class="sxs-lookup"><span data-stu-id="cad81-103">IStats::Start method</span></span>

<span data-ttu-id="cad81-104">El **método Start** inicia una captura.</span><span class="sxs-lookup"><span data-stu-id="cad81-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="cad81-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cad81-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a><span data-ttu-id="cad81-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cad81-106">Parameters</span></span>

<span data-ttu-id="cad81-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cad81-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cad81-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cad81-108">Return value</span></span>

<span data-ttu-id="cad81-109">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="cad81-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="cad81-110">Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="cad81-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="cad81-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="cad81-111">Return code</span></span>                                                                                            | <span data-ttu-id="cad81-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="cad81-112">Description</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cad81-113"><dt>**CAPTURA DE NMERR \_ \_ EN PAUSA**</dt></span><span class="sxs-lookup"><span data-stu-id="cad81-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl>  | <span data-ttu-id="cad81-114">La captura se ha detenido y debe detenerse antes de poder reiniciarse.</span><span class="sxs-lookup"><span data-stu-id="cad81-114">The capture has paused and must be stopped before it can be restarted.</span></span> <span data-ttu-id="cad81-115">Llame al [método IStats::Stop](istats-stop.md) para detener la captura.</span><span class="sxs-lookup"><span data-stu-id="cad81-115">Call the [IStats::Stop](istats-stop.md) method to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="cad81-116"><dt>**CAPTURA DE \_ NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="cad81-116"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>        | <span data-ttu-id="cad81-117">La captura ya se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="cad81-117">The capture has already started.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="cad81-118"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="cad81-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="cad81-119">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="cad81-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="cad81-120">Llame al [método IStats::Connect](istats-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="cad81-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/>           |
| <dl> <span data-ttu-id="cad81-121"><dt>**NMERR \_ NO SOLO \_ \_ ESTADÍSTICAS**</dt></span><span class="sxs-lookup"><span data-stu-id="cad81-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="cad81-122">El NPP está conectado a la red, pero no con el [método IStats::Connect.](istats-connect.md)</span><span class="sxs-lookup"><span data-stu-id="cad81-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="cad81-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cad81-123">Remarks</span></span>

<span data-ttu-id="cad81-124">Al reiniciar la captura mediante los métodos IStats::Start e [IStats::Stop,](istats-stop.md) debe llamar al método [IStats::Configure](istats-configure.md) para volver a configurar la conexión cada vez que llame a IStats::Start para reiniciar la captura de datos.</span><span class="sxs-lookup"><span data-stu-id="cad81-124">When restarting the capture by using the IStats::Start and [IStats::Stop](istats-stop.md) methods, you must call the [IStats::Configure](istats-configure.md) method to reconfigure the connection each time you call IStats::Start to restart the data capture.</span></span>

> [!Note]  
> <span data-ttu-id="cad81-125">También puede iniciar y detener la captura mediante los [métodos IStats::P ause](istats-pause.md) [e IStats::Resume.](istats-resume.md)</span><span class="sxs-lookup"><span data-stu-id="cad81-125">You can also start and stop the capture by using the [IStats::Pause](istats-pause.md) and [IStats::Resume](istats-resume.md) methods.</span></span> <span data-ttu-id="cad81-126">Cuando se usan estos métodos, los datos capturados se almacenan en el mismo archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="cad81-126">When you use these methods, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cad81-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cad81-127">Requirements</span></span>



| <span data-ttu-id="cad81-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="cad81-128">Requirement</span></span> | <span data-ttu-id="cad81-129">Valor</span><span class="sxs-lookup"><span data-stu-id="cad81-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cad81-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cad81-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cad81-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cad81-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="cad81-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cad81-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cad81-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cad81-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="cad81-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cad81-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="cad81-135"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="cad81-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="cad81-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cad81-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cad81-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cad81-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cad81-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cad81-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cad81-139">IStats</span><span class="sxs-lookup"><span data-stu-id="cad81-139">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="cad81-140">IStats::Configure</span><span class="sxs-lookup"><span data-stu-id="cad81-140">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="cad81-141">IStats::Connect</span><span class="sxs-lookup"><span data-stu-id="cad81-141">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="cad81-142">IStats::P ause</span><span class="sxs-lookup"><span data-stu-id="cad81-142">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="cad81-143">IStats::Resume</span><span class="sxs-lookup"><span data-stu-id="cad81-143">IStats::Resume</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="cad81-144">IStats::Stop</span><span class="sxs-lookup"><span data-stu-id="cad81-144">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




