---
description: El método start inicia una captura.
ms.assetid: 92b25afc-d5d8-47e4-a155-4ed2a3571038
title: 'IDelaydC:: Start (método) (Netmon. h)'
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
ms.openlocfilehash: a912af44dddb8a25d3279a5cdd7f021646c26e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686563"
---
# <a name="idelaydcstart-method"></a><span data-ttu-id="2cb10-103">IDelaydC:: Start (método)</span><span class="sxs-lookup"><span data-stu-id="2cb10-103">IDelaydC::Start method</span></span>

<span data-ttu-id="2cb10-104">El método **Start** inicia una captura.</span><span class="sxs-lookup"><span data-stu-id="2cb10-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cb10-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2cb10-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="2cb10-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2cb10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cb10-107">*pFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2cb10-107">*pFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cb10-108">Puntero al nombre del archivo de [*captura*](c.md) que se usa para almacenar los datos de red.</span><span class="sxs-lookup"><span data-stu-id="2cb10-108">Pointer to the name of the [*capture file*](c.md) used to store the network data.</span></span> <span data-ttu-id="2cb10-109">Asegúrese de almacenar en caché este nombre de archivo si es necesario para futuras referencias.</span><span class="sxs-lookup"><span data-stu-id="2cb10-109">Be sure to cache this file name if it is needed for future reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cb10-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2cb10-110">Return value</span></span>

<span data-ttu-id="2cb10-111">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="2cb10-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="2cb10-112">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="2cb10-112">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="2cb10-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2cb10-113">Return code</span></span>                                                                                           | <span data-ttu-id="2cb10-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cb10-114">Description</span></span>                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2cb10-115"><dt>**captura de NMERR en \_ \_ pausa**</dt></span><span class="sxs-lookup"><span data-stu-id="2cb10-115"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="2cb10-116">La captura está en un estado de pausa y debe detenerse antes de que se pueda reiniciar.</span><span class="sxs-lookup"><span data-stu-id="2cb10-116">The capture is in a paused state and must be stopped before it can be restarted.</span></span> <span data-ttu-id="2cb10-117">Llame a [**IDelaydC:: Stop**](idelaydc-stop.md) para detener la captura.</span><span class="sxs-lookup"><span data-stu-id="2cb10-117">Call [**IDelaydC::Stop**](idelaydc-stop.md) to stop the capture.</span></span> <span data-ttu-id="2cb10-118">Para obtener más información, consulte la sección Comentarios de este tema.</span><span class="sxs-lookup"><span data-stu-id="2cb10-118">For more information, see the Remarks section in this topic.</span></span><br/> |
| <dl> <span data-ttu-id="2cb10-119"><dt>**captura de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2cb10-119"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="2cb10-120">La captura ya se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="2cb10-120">The capture is already started.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="2cb10-121"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="2cb10-121"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="2cb10-122">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="2cb10-122">The NPP is not connected to the network.</span></span> <span data-ttu-id="2cb10-123">Llame a [**IDelaydC:: Connect**](idelaydc-connect.md) para conectarse a la red.</span><span class="sxs-lookup"><span data-stu-id="2cb10-123">Call [**IDelaydC::Connect**](idelaydc-connect.md) to connect to the network.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="2cb10-124"><dt>**NMERR \_ no \_ retrasado**</dt></span><span class="sxs-lookup"><span data-stu-id="2cb10-124"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>    | <span data-ttu-id="2cb10-125">NPP está conectado a la red, pero no con el método [**IDelaydC:: Connect**](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="2cb10-125">The NPP is connected to the network but not with the [**IDelaydC::Connect**](idelaydc-connect.md) method.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="2cb10-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2cb10-126">Remarks</span></span>

<span data-ttu-id="2cb10-127">La ubicación del [*archivo de captura*](c.md) se especifica en el registro de Windows, pero puede usar Monitor de red para cambiar la ubicación del archivo.</span><span class="sxs-lookup"><span data-stu-id="2cb10-127">The location of the [*capture file*](c.md) is specified in your Windows registry, but you can use Network Monitor to change the file's location.</span></span>

<span data-ttu-id="2cb10-128">Para reiniciar la captura mediante **IDelaydC:: Start** y [**IDelaydC:: Stop**](idelaydc-stop.md), debe llamar al método [**IDelaydC:: configure**](idelaydc-configure.md) para volver a configurar la conexión cada vez que llame al método **IDelaydC:: Start** para reiniciar la captura de datos.</span><span class="sxs-lookup"><span data-stu-id="2cb10-128">To restart the capture by using **IDelaydC::Start** and [**IDelaydC::Stop**](idelaydc-stop.md), you must call the [**IDelaydC::Configure**](idelaydc-configure.md) method to reconfigure the connection each time you call the **IDelaydC::Start** method to restart capturing data.</span></span> <span data-ttu-id="2cb10-129">Al iniciar y detener la captura con estos tres métodos, se crea un nuevo archivo de captura cada vez que se inicia la captura.</span><span class="sxs-lookup"><span data-stu-id="2cb10-129">When you start and stop the capture with these three methods, a new capture file is created each time the capture is started.</span></span>

> [!Note]  
> <span data-ttu-id="2cb10-130">También puede iniciar y detener la captura mediante los métodos [**IDelaydC::P ause**](idelaydc-pause.md) y [**IDelaydC:: resume**](idelaydc-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="2cb10-130">You can also start and stop the capture by using the [**IDelaydC::Pause**](idelaydc-pause.md) and [**IDelaydC::Resume**](idelaydc-resume.md) methods.</span></span> <span data-ttu-id="2cb10-131">Cuando se usan estos dos métodos, los datos capturados se almacenan en el mismo archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="2cb10-131">When you use these two methods, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2cb10-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cb10-132">Requirements</span></span>



| <span data-ttu-id="2cb10-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cb10-133">Requirement</span></span> | <span data-ttu-id="2cb10-134">Value</span><span class="sxs-lookup"><span data-stu-id="2cb10-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cb10-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cb10-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2cb10-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2cb10-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="2cb10-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cb10-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2cb10-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2cb10-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="2cb10-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2cb10-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cb10-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cb10-140"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="2cb10-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2cb10-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cb10-142"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cb10-142"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cb10-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="2cb10-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cb10-144">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="2cb10-144">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="2cb10-145">**IDelaydC:: configure**</span><span class="sxs-lookup"><span data-stu-id="2cb10-145">**IDelaydC::Configure**</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="2cb10-146">**IDelaydC:: Connect**</span><span class="sxs-lookup"><span data-stu-id="2cb10-146">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="2cb10-147">**IDelaydC::P ause**</span><span class="sxs-lookup"><span data-stu-id="2cb10-147">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="2cb10-148">**IDelaydC:: resume**</span><span class="sxs-lookup"><span data-stu-id="2cb10-148">**IDelaydC::Resume**</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="2cb10-149">**IDelaydC:: Stop**</span><span class="sxs-lookup"><span data-stu-id="2cb10-149">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




