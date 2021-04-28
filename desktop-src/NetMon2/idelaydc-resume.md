---
description: 'Método IDelaydC::Resume: el método Resume reinicia una captura en pausa.'
ms.assetid: 4fa47220-d323-407b-9dae-704969f66bdd
title: Método IDelaydC::Resume (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 9c8c3b505e0e9fb306a444111cce22c8c580d015
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109193"
---
# <a name="idelaydcresume-method"></a><span data-ttu-id="e68bf-103">IDelaydC::Resume (método)</span><span class="sxs-lookup"><span data-stu-id="e68bf-103">IDelaydC::Resume method</span></span>

<span data-ttu-id="e68bf-104">El **método Resume** reinicia una captura en pausa.</span><span class="sxs-lookup"><span data-stu-id="e68bf-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="e68bf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e68bf-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="e68bf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e68bf-106">Parameters</span></span>

<span data-ttu-id="e68bf-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e68bf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e68bf-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e68bf-108">Return value</span></span>

<span data-ttu-id="e68bf-109">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="e68bf-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e68bf-110">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="e68bf-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="e68bf-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e68bf-111">Return code</span></span>                                                                                                | <span data-ttu-id="e68bf-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e68bf-112">Description</span></span>                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e68bf-113"><dt>**CAPTURA DE NMERR \_ \_ NO \_ PAUSADA**</dt></span><span class="sxs-lookup"><span data-stu-id="e68bf-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="e68bf-114">La captura no está en pausa.</span><span class="sxs-lookup"><span data-stu-id="e68bf-114">The capture is not paused.</span></span> <span data-ttu-id="e68bf-115">Llame [**a IDelaydC::P ause para**](idelaydc-pause.md) pausar la captura.</span><span class="sxs-lookup"><span data-stu-id="e68bf-115">Call [**IDelaydC::Pause**](idelaydc-pause.md) to pause the capture.</span></span><br/>                                |
| <dl> <span data-ttu-id="e68bf-116"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="e68bf-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="e68bf-117">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="e68bf-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="e68bf-118">Llame [**a IDelaydC::Connect**](idelaydc-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="e68bf-118">Call [**IDelaydC::Connect**](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="e68bf-119"><dt>**NMERR \_ NO \_ RETRASADA**</dt></span><span class="sxs-lookup"><span data-stu-id="e68bf-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>         | <span data-ttu-id="e68bf-120">El NPP está conectado a la red, pero no con [**el método IDelaydC::Connect.**](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="e68bf-120">The NPP is connected to the network but not with the [**IDelaydC::Connect**](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="e68bf-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e68bf-121">Remarks</span></span>

<span data-ttu-id="e68bf-122">Mientras la captura está en pausa, no se [](c.md) agregan nuevos datos al archivo de captura actual hasta que se llama al método **IDelaydC::Resume** para reiniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="e68bf-122">While the capture is paused, new data is not added to the current [*capture file*](c.md) until the **IDelaydC::Resume** method is called to restart the capture.</span></span> <span data-ttu-id="e68bf-123">Cuando [**se**](idelaydc-pause.md) usan **Pausar y reanudar** para detener y reiniciar la captura, toda la información capturada se coloca en el mismo archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="e68bf-123">When [**Pause**](idelaydc-pause.md) and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="e68bf-124">Al usar [**Pausar**](idelaydc-pause.md) **y reanudar** para controlar la captura, Monitor de red sigue agregando [*estadísticas*](c.md) de conversación a las estadísticas existentes para la captura actual.</span><span class="sxs-lookup"><span data-stu-id="e68bf-124">When using [**Pause**](idelaydc-pause.md) and **Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="e68bf-125">Para detener la captura, llame [**a IDelaydC::Stop**](idelaydc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="e68bf-125">To stop the capture, call [**IDelaydC::Stop**](idelaydc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e68bf-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e68bf-126">Requirements</span></span>



| <span data-ttu-id="e68bf-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e68bf-127">Requirement</span></span> | <span data-ttu-id="e68bf-128">Valor</span><span class="sxs-lookup"><span data-stu-id="e68bf-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e68bf-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e68bf-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e68bf-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e68bf-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="e68bf-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e68bf-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e68bf-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e68bf-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="e68bf-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e68bf-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e68bf-134"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="e68bf-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="e68bf-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e68bf-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e68bf-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e68bf-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e68bf-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e68bf-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e68bf-138">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="e68bf-138">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="e68bf-139">**IDelaydC::Connect**</span><span class="sxs-lookup"><span data-stu-id="e68bf-139">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="e68bf-140">**IDelaydC::P ause**</span><span class="sxs-lookup"><span data-stu-id="e68bf-140">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="e68bf-141">**IDelaydC::Stop**</span><span class="sxs-lookup"><span data-stu-id="e68bf-141">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




