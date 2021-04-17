---
description: El método start inicia una captura.
ms.assetid: 8bf8c0c7-20be-4404-8ea5-b28b4c658523
title: 'IESP:: Start (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 2d9fc3a75fc82964f6fc5a5660ef77414ae065d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687322"
---
# <a name="iespstart-method"></a><span data-ttu-id="08d73-103">IESP:: Start (método)</span><span class="sxs-lookup"><span data-stu-id="08d73-103">IESP::Start method</span></span>

<span data-ttu-id="08d73-104">El método **Start** inicia una captura.</span><span class="sxs-lookup"><span data-stu-id="08d73-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="08d73-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08d73-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="08d73-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08d73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08d73-107">*pFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="08d73-107">*pFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08d73-108">Puntero al nombre del archivo de [*captura*](c.md) que se usa para almacenar los datos de red.</span><span class="sxs-lookup"><span data-stu-id="08d73-108">Pointer to the name of the [*capture file*](c.md) used to store the network data.</span></span> <span data-ttu-id="08d73-109">Asegúrese de almacenar en caché este nombre de archivo si es necesario para futuras referencias.</span><span class="sxs-lookup"><span data-stu-id="08d73-109">Be sure to cache this file name if it is needed for future reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08d73-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08d73-110">Return value</span></span>

<span data-ttu-id="08d73-111">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="08d73-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="08d73-112">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="08d73-112">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="08d73-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="08d73-113">Return code</span></span>                                                                                           | <span data-ttu-id="08d73-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="08d73-114">Description</span></span>                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="08d73-115"><dt>**captura de NMERR en \_ \_ pausa**</dt></span><span class="sxs-lookup"><span data-stu-id="08d73-115"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="08d73-116">La captura se pausa y debe detenerse antes de que se pueda reiniciar.</span><span class="sxs-lookup"><span data-stu-id="08d73-116">The capture is paused and must be stopped before it can be restarted.</span></span> <span data-ttu-id="08d73-117">Llame a [iesp:: Stop](iesp-stop.md) para detener la captura.</span><span class="sxs-lookup"><span data-stu-id="08d73-117">Call [IESP::Stop](iesp-stop.md) to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="08d73-118"><dt>**captura de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="08d73-118"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="08d73-119">La captura ya se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="08d73-119">The capture is already started.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="08d73-120"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="08d73-120"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="08d73-121">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="08d73-121">The NPP is not connected to the network.</span></span> <span data-ttu-id="08d73-122">Llame a [iesp:: Connect](iesp-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="08d73-122">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/>          |
| <dl> <span data-ttu-id="08d73-123"><dt>**NMERR \_ no \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="08d73-123"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>        | <span data-ttu-id="08d73-124">NPP está conectado a la red, pero no con el método [iesp:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="08d73-124">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="08d73-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08d73-125">Remarks</span></span>

<span data-ttu-id="08d73-126">La ubicación del [*archivo de captura*](c.md) se especifica en el registro de Windows, pero puede usar Monitor de red para cambiar la ubicación del directorio.</span><span class="sxs-lookup"><span data-stu-id="08d73-126">The location of the [*capture file*](c.md) is specified in the Windows registry, but you can use Network Monitor to change the directory location.</span></span>

<span data-ttu-id="08d73-127">Cuando reinicie la captura mediante los métodos IESP:: Start y [iesp:: Stop](iesp-stop.md) , debe llamar al método [iesp:: configure](iesp-configure.md) para volver a configurar la conexión cada vez que llame a iesp:: Start para reiniciar la captura de datos.</span><span class="sxs-lookup"><span data-stu-id="08d73-127">When you restart the capture by using the IESP::Start and [IESP::Stop](iesp-stop.md) methods, you must call the [IESP::Configure](iesp-configure.md) method to reconfigure the connection each time you call IESP::Start to restart capturing data.</span></span> <span data-ttu-id="08d73-128">Al iniciar y detener la captura con estos tres métodos, se crea un nuevo archivo de captura cada vez que se inicia la captura.</span><span class="sxs-lookup"><span data-stu-id="08d73-128">When you start and stop the capture with these three methods, a new capture file is created each time the capture is started.</span></span>

> [!Note]  
> <span data-ttu-id="08d73-129">También puede iniciar y detener la captura mediante los métodos [iesp::P ause](iesp-pause.md) y [iesp:: resume](iesp-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="08d73-129">You can also start and stop the capture by using the [IESP::Pause](iesp-pause.md) and [IESP::Resume](iesp-resume.md) methods.</span></span> <span data-ttu-id="08d73-130">Cuando se usan estos dos métodos, los datos capturados se almacenan en el mismo archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="08d73-130">When these two methods are used, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="08d73-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08d73-131">Requirements</span></span>



| <span data-ttu-id="08d73-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="08d73-132">Requirement</span></span> | <span data-ttu-id="08d73-133">Value</span><span class="sxs-lookup"><span data-stu-id="08d73-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08d73-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08d73-134">Minimum supported client</span></span><br/> | <span data-ttu-id="08d73-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="08d73-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="08d73-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08d73-136">Minimum supported server</span></span><br/> | <span data-ttu-id="08d73-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="08d73-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="08d73-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08d73-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="08d73-139"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="08d73-139"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="08d73-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="08d73-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08d73-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08d73-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08d73-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="08d73-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08d73-143">IESP</span><span class="sxs-lookup"><span data-stu-id="08d73-143">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="08d73-144">IESP:: configure</span><span class="sxs-lookup"><span data-stu-id="08d73-144">IESP::Configure</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="08d73-145">IESP:: Connect</span><span class="sxs-lookup"><span data-stu-id="08d73-145">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="08d73-146">IESP::P ause</span><span class="sxs-lookup"><span data-stu-id="08d73-146">IESP::Pause</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="08d73-147">IESP:: resume</span><span class="sxs-lookup"><span data-stu-id="08d73-147">IESP::Resume</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="08d73-148">IESP:: Stop</span><span class="sxs-lookup"><span data-stu-id="08d73-148">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




