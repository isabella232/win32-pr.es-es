---
description: El método PAUSE detiene temporalmente la captura actual.
ms.assetid: 43176e9e-1502-484c-a8af-4e7bbf5f6474
title: IStas::P método ause (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d9e9f04ce3d25399866c711dad7a853f2c43c2ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678576"
---
# <a name="istatspause-method"></a><span data-ttu-id="8b958-103">IStas::P método ause</span><span class="sxs-lookup"><span data-stu-id="8b958-103">IStats::Pause method</span></span>

<span data-ttu-id="8b958-104">El método **PAUSE** detiene temporalmente la captura actual.</span><span class="sxs-lookup"><span data-stu-id="8b958-104">The **Pause** method temporarily stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b958-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b958-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="8b958-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b958-106">Parameters</span></span>

<span data-ttu-id="8b958-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8b958-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8b958-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b958-108">Return value</span></span>

<span data-ttu-id="8b958-109">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="8b958-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="8b958-110">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="8b958-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="8b958-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8b958-111">Return code</span></span>                                                                                            | <span data-ttu-id="8b958-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b958-112">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8b958-113"><dt>**captura de NMERR en \_ \_ pausa**</dt></span><span class="sxs-lookup"><span data-stu-id="8b958-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl>  | <span data-ttu-id="8b958-114">La captura ya está en pausa.</span><span class="sxs-lookup"><span data-stu-id="8b958-114">The capture is already paused.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="8b958-115"><dt>**NMERR \_ no se \_ captura**</dt></span><span class="sxs-lookup"><span data-stu-id="8b958-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="8b958-116">NPP no está capturando datos.</span><span class="sxs-lookup"><span data-stu-id="8b958-116">The NPP is not capturing data.</span></span> <span data-ttu-id="8b958-117">Llame al método [istas:: Start](istats-start.md) para iniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="8b958-117">Call the [IStats::Start](istats-start.md) method to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="8b958-118"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="8b958-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="8b958-119">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="8b958-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="8b958-120">Llame al método [istas:: Connect](istats-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="8b958-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="8b958-121"><dt>**NMERR \_ no \_ solo estadísticas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8b958-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="8b958-122">NPP está conectado a la red, pero no con el método [istas:: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="8b958-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="8b958-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8b958-123">Remarks</span></span>

<span data-ttu-id="8b958-124">Mientras se pausa la captura, no se capturan nuevos fotogramas hasta que una llamada al método [istas:: resume](istats-resume.md) reinicie la captura.</span><span class="sxs-lookup"><span data-stu-id="8b958-124">While the capture is paused, new frames are not captured until a call to the [IStats::Resume](istats-resume.md) method restarts the capture.</span></span>

<span data-ttu-id="8b958-125">Cuando se usan los **istas::P ause** y **istas:: resume** (métodos) para controlar la captura, monitor de red continúa agregando [*estadísticas de conversación*](c.md) cada vez que se ejecuta la captura.</span><span class="sxs-lookup"><span data-stu-id="8b958-125">When you use the **IStats::Pause** and **IStats::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="8b958-126">Para reiniciar los autores de la llamada de captura [:: resume](istats-resume.md).</span><span class="sxs-lookup"><span data-stu-id="8b958-126">To restart the capture call [IStats::Resume](istats-resume.md).</span></span> <span data-ttu-id="8b958-127">Para detener la captura, llame a [istas:: Stop](istats-stop.md).</span><span class="sxs-lookup"><span data-stu-id="8b958-127">To stop the capture, call [IStats::Stop](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b958-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b958-128">Requirements</span></span>



| <span data-ttu-id="8b958-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b958-129">Requirement</span></span> | <span data-ttu-id="8b958-130">Value</span><span class="sxs-lookup"><span data-stu-id="8b958-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b958-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b958-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8b958-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8b958-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="8b958-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b958-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8b958-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8b958-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="8b958-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b958-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b958-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b958-136"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="8b958-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8b958-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b958-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b958-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b958-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b958-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b958-140">IStas</span><span class="sxs-lookup"><span data-stu-id="8b958-140">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="8b958-141">ISta:: Connect</span><span class="sxs-lookup"><span data-stu-id="8b958-141">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="8b958-142">IStas:: resume</span><span class="sxs-lookup"><span data-stu-id="8b958-142">IStats::Resume</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="8b958-143">ISta:: Start</span><span class="sxs-lookup"><span data-stu-id="8b958-143">IStats::Start</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="8b958-144">IStas:: Stop</span><span class="sxs-lookup"><span data-stu-id="8b958-144">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




