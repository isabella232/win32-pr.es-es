---
description: 'Método IESP::Start: el método Start inicia una captura.'
ms.assetid: 8bf8c0c7-20be-4404-8ea5-b28b4c658523
title: Método IESP::Start (Netmon.h)
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
ms.openlocfilehash: 6dd0d1159132e594b6d48ea6799da5846eeb626e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103803"
---
# <a name="iespstart-method"></a><span data-ttu-id="79f05-103">IESP::Start (método)</span><span class="sxs-lookup"><span data-stu-id="79f05-103">IESP::Start method</span></span>

<span data-ttu-id="79f05-104">El **método Start** inicia una captura.</span><span class="sxs-lookup"><span data-stu-id="79f05-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="79f05-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79f05-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="79f05-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79f05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79f05-107">*pFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="79f05-107">*pFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79f05-108">Puntero al nombre del archivo [*de captura utilizado*](c.md) para almacenar los datos de red.</span><span class="sxs-lookup"><span data-stu-id="79f05-108">Pointer to the name of the [*capture file*](c.md) used to store the network data.</span></span> <span data-ttu-id="79f05-109">Asegúrese de almacenar en caché este nombre de archivo si es necesario para futuras referencias.</span><span class="sxs-lookup"><span data-stu-id="79f05-109">Be sure to cache this file name if it is needed for future reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79f05-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79f05-110">Return value</span></span>

<span data-ttu-id="79f05-111">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="79f05-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="79f05-112">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="79f05-112">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="79f05-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="79f05-113">Return code</span></span>                                                                                           | <span data-ttu-id="79f05-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="79f05-114">Description</span></span>                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="79f05-115"><dt>**CAPTURA DE NMERR \_ \_ EN PAUSA**</dt></span><span class="sxs-lookup"><span data-stu-id="79f05-115"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="79f05-116">La captura está en pausa y debe detenerse antes de poder reiniciarse.</span><span class="sxs-lookup"><span data-stu-id="79f05-116">The capture is paused and must be stopped before it can be restarted.</span></span> <span data-ttu-id="79f05-117">Llame [a IESP::Stop](iesp-stop.md) para detener la captura.</span><span class="sxs-lookup"><span data-stu-id="79f05-117">Call [IESP::Stop](iesp-stop.md) to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="79f05-118"><dt>**CAPTURA DE \_ NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="79f05-118"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="79f05-119">La captura ya se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="79f05-119">The capture is already started.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="79f05-120"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="79f05-120"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="79f05-121">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="79f05-121">The NPP is not connected to the network.</span></span> <span data-ttu-id="79f05-122">Llame [a IESP::Connect](iesp-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="79f05-122">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/>          |
| <dl> <span data-ttu-id="79f05-123"><dt>**NMERR \_ NOT \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="79f05-123"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>        | <span data-ttu-id="79f05-124">El NPP está conectado a la red, pero no con el [método IESP::Connect.](iesp-connect.md)</span><span class="sxs-lookup"><span data-stu-id="79f05-124">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="79f05-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="79f05-125">Remarks</span></span>

<span data-ttu-id="79f05-126">La ubicación del [*archivo de captura*](c.md) se especifica en el Registro de Windows, pero puede usar Monitor de red para cambiar la ubicación del directorio.</span><span class="sxs-lookup"><span data-stu-id="79f05-126">The location of the [*capture file*](c.md) is specified in the Windows registry, but you can use Network Monitor to change the directory location.</span></span>

<span data-ttu-id="79f05-127">Al reiniciar la captura mediante los métodos IESP::Start e [IESP::Stop,](iesp-stop.md) debe llamar al método [IESP::Configure](iesp-configure.md) para volver a configurar la conexión cada vez que llame a IESP::Start para reiniciar la captura de datos.</span><span class="sxs-lookup"><span data-stu-id="79f05-127">When you restart the capture by using the IESP::Start and [IESP::Stop](iesp-stop.md) methods, you must call the [IESP::Configure](iesp-configure.md) method to reconfigure the connection each time you call IESP::Start to restart capturing data.</span></span> <span data-ttu-id="79f05-128">Al iniciar y detener la captura con estos tres métodos, se crea un nuevo archivo de captura cada vez que se inicia la captura.</span><span class="sxs-lookup"><span data-stu-id="79f05-128">When you start and stop the capture with these three methods, a new capture file is created each time the capture is started.</span></span>

> [!Note]  
> <span data-ttu-id="79f05-129">También puede iniciar y detener la captura mediante los métodos [IESP::P ause](iesp-pause.md) e [IESP::Resume.](iesp-resume.md)</span><span class="sxs-lookup"><span data-stu-id="79f05-129">You can also start and stop the capture by using the [IESP::Pause](iesp-pause.md) and [IESP::Resume](iesp-resume.md) methods.</span></span> <span data-ttu-id="79f05-130">Cuando se usan estos dos métodos, los datos capturados se almacenan en el mismo archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="79f05-130">When these two methods are used, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="79f05-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79f05-131">Requirements</span></span>



| <span data-ttu-id="79f05-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="79f05-132">Requirement</span></span> | <span data-ttu-id="79f05-133">Valor</span><span class="sxs-lookup"><span data-stu-id="79f05-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79f05-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79f05-134">Minimum supported client</span></span><br/> | <span data-ttu-id="79f05-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="79f05-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="79f05-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79f05-136">Minimum supported server</span></span><br/> | <span data-ttu-id="79f05-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="79f05-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="79f05-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79f05-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="79f05-139"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="79f05-139"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="79f05-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79f05-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79f05-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79f05-141"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79f05-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="79f05-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79f05-143">IESP</span><span class="sxs-lookup"><span data-stu-id="79f05-143">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="79f05-144">IESP::Configure</span><span class="sxs-lookup"><span data-stu-id="79f05-144">IESP::Configure</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="79f05-145">IESP::Connect</span><span class="sxs-lookup"><span data-stu-id="79f05-145">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="79f05-146">IESP::P ause</span><span class="sxs-lookup"><span data-stu-id="79f05-146">IESP::Pause</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="79f05-147">IESP::Resume</span><span class="sxs-lookup"><span data-stu-id="79f05-147">IESP::Resume</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="79f05-148">IESP::Stop</span><span class="sxs-lookup"><span data-stu-id="79f05-148">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




