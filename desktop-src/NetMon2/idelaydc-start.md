---
description: 'Método IDelaydC::Start: el método Start inicia una captura.'
ms.assetid: 92b25afc-d5d8-47e4-a155-4ed2a3571038
title: Método IDelaydC::Start (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 25bf778d9cccce20c736c5f8b83e6af9754ac933
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118443"
---
# <a name="idelaydcstart-method"></a><span data-ttu-id="cf83b-103">IDelaydC::Start (método)</span><span class="sxs-lookup"><span data-stu-id="cf83b-103">IDelaydC::Start method</span></span>

<span data-ttu-id="cf83b-104">El **método Start** inicia una captura.</span><span class="sxs-lookup"><span data-stu-id="cf83b-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf83b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf83b-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="cf83b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cf83b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf83b-107">*pFileName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cf83b-107">*pFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf83b-108">Puntero al nombre del archivo [*de captura utilizado*](c.md) para almacenar los datos de red.</span><span class="sxs-lookup"><span data-stu-id="cf83b-108">Pointer to the name of the [*capture file*](c.md) used to store the network data.</span></span> <span data-ttu-id="cf83b-109">Asegúrese de almacenar en caché este nombre de archivo si es necesario para futuras referencias.</span><span class="sxs-lookup"><span data-stu-id="cf83b-109">Be sure to cache this file name if it is needed for future reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf83b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf83b-110">Return value</span></span>

<span data-ttu-id="cf83b-111">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="cf83b-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="cf83b-112">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="cf83b-112">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="cf83b-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="cf83b-113">Return code</span></span>                                                                                           | <span data-ttu-id="cf83b-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf83b-114">Description</span></span>                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cf83b-115"><dt>**CAPTURA DE NMERR \_ \_ EN PAUSA**</dt></span><span class="sxs-lookup"><span data-stu-id="cf83b-115"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="cf83b-116">La captura está en estado en pausa y debe detenerse antes de poder reiniciarse.</span><span class="sxs-lookup"><span data-stu-id="cf83b-116">The capture is in a paused state and must be stopped before it can be restarted.</span></span> <span data-ttu-id="cf83b-117">Llame [**a IDelaydC::Stop**](idelaydc-stop.md) para detener la captura.</span><span class="sxs-lookup"><span data-stu-id="cf83b-117">Call [**IDelaydC::Stop**](idelaydc-stop.md) to stop the capture.</span></span> <span data-ttu-id="cf83b-118">Para obtener más información, vea la sección Comentarios de este tema.</span><span class="sxs-lookup"><span data-stu-id="cf83b-118">For more information, see the Remarks section in this topic.</span></span><br/> |
| <dl> <span data-ttu-id="cf83b-119"><dt>**CAPTURA DE \_ NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="cf83b-119"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="cf83b-120">La captura ya se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="cf83b-120">The capture is already started.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="cf83b-121"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="cf83b-121"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="cf83b-122">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="cf83b-122">The NPP is not connected to the network.</span></span> <span data-ttu-id="cf83b-123">Llame [**a IDelaydC::Connect**](idelaydc-connect.md) para conectarse a la red.</span><span class="sxs-lookup"><span data-stu-id="cf83b-123">Call [**IDelaydC::Connect**](idelaydc-connect.md) to connect to the network.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="cf83b-124"><dt>**NMERR \_ NO \_ RETRASADA**</dt></span><span class="sxs-lookup"><span data-stu-id="cf83b-124"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>    | <span data-ttu-id="cf83b-125">El NPP está conectado a la red, pero no con [**el método IDelaydC::Connect.**](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="cf83b-125">The NPP is connected to the network but not with the [**IDelaydC::Connect**](idelaydc-connect.md) method.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="cf83b-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cf83b-126">Remarks</span></span>

<span data-ttu-id="cf83b-127">La ubicación del [*archivo de captura*](c.md) se especifica en el registro de Windows, pero puede usar Monitor de red para cambiar la ubicación del archivo.</span><span class="sxs-lookup"><span data-stu-id="cf83b-127">The location of the [*capture file*](c.md) is specified in your Windows registry, but you can use Network Monitor to change the file's location.</span></span>

<span data-ttu-id="cf83b-128">Para reiniciar la captura mediante **IDelaydC::Start** e [**IDelaydC::Stop**](idelaydc-stop.md), debe llamar al método [**IDelaydC::Configure**](idelaydc-configure.md) para volver a configurar la conexión cada vez que llame al método **IDelaydC::Start** para reiniciar la captura de datos.</span><span class="sxs-lookup"><span data-stu-id="cf83b-128">To restart the capture by using **IDelaydC::Start** and [**IDelaydC::Stop**](idelaydc-stop.md), you must call the [**IDelaydC::Configure**](idelaydc-configure.md) method to reconfigure the connection each time you call the **IDelaydC::Start** method to restart capturing data.</span></span> <span data-ttu-id="cf83b-129">Al iniciar y detener la captura con estos tres métodos, se crea un nuevo archivo de captura cada vez que se inicia la captura.</span><span class="sxs-lookup"><span data-stu-id="cf83b-129">When you start and stop the capture with these three methods, a new capture file is created each time the capture is started.</span></span>

> [!Note]  
> <span data-ttu-id="cf83b-130">También puede iniciar y detener la captura mediante los métodos [**IDelaydC::P ause**](idelaydc-pause.md) e [**IDelaydC::Resume.**](idelaydc-resume.md)</span><span class="sxs-lookup"><span data-stu-id="cf83b-130">You can also start and stop the capture by using the [**IDelaydC::Pause**](idelaydc-pause.md) and [**IDelaydC::Resume**](idelaydc-resume.md) methods.</span></span> <span data-ttu-id="cf83b-131">Cuando se usan estos dos métodos, los datos capturados se almacenan en el mismo archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="cf83b-131">When you use these two methods, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cf83b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf83b-132">Requirements</span></span>



| <span data-ttu-id="cf83b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf83b-133">Requirement</span></span> | <span data-ttu-id="cf83b-134">Valor</span><span class="sxs-lookup"><span data-stu-id="cf83b-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf83b-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf83b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cf83b-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cf83b-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="cf83b-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf83b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cf83b-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cf83b-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="cf83b-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf83b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf83b-140"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="cf83b-140"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="cf83b-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cf83b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf83b-142"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf83b-142"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf83b-143">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cf83b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf83b-144">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="cf83b-144">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="cf83b-145">**IDelaydC::Configure**</span><span class="sxs-lookup"><span data-stu-id="cf83b-145">**IDelaydC::Configure**</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="cf83b-146">**IDelaydC::Connect**</span><span class="sxs-lookup"><span data-stu-id="cf83b-146">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="cf83b-147">**IDelaydC::P ause**</span><span class="sxs-lookup"><span data-stu-id="cf83b-147">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="cf83b-148">**IDelaydC::Resume**</span><span class="sxs-lookup"><span data-stu-id="cf83b-148">**IDelaydC::Resume**</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="cf83b-149">**IDelaydC::Stop**</span><span class="sxs-lookup"><span data-stu-id="cf83b-149">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




