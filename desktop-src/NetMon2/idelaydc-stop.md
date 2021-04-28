---
description: 'Método IDelaydC::Stop: el método Stop detiene la captura actual.'
ms.assetid: 1b627137-e72d-4425-98d9-e296fb07e509
title: Método IDelaydC::Stop (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 38be5b6ba4c3f6edcd716f4d0235150e96dd692a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110783"
---
# <a name="idelaydcstop-method"></a><span data-ttu-id="bd393-103">IDelaydC::Stop (Método)</span><span class="sxs-lookup"><span data-stu-id="bd393-103">IDelaydC::Stop method</span></span>

<span data-ttu-id="bd393-104">El **método Stop** detiene la captura actual.</span><span class="sxs-lookup"><span data-stu-id="bd393-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd393-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd393-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="bd393-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd393-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd393-107">*lpStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bd393-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd393-108">Puntero a una [estructura STATISTICS que](statistics.md) contiene estadísticas de red, como fotogramas totales y bytes totales capturados.</span><span class="sxs-lookup"><span data-stu-id="bd393-108">Pointer to a [STATISTICS](statistics.md) structure that contains network statistics such as total frames and total bytes captured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd393-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd393-109">Return value</span></span>

<span data-ttu-id="bd393-110">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="bd393-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="bd393-111">Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="bd393-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="bd393-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bd393-112">Return code</span></span>                                                                                          | <span data-ttu-id="bd393-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd393-113">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bd393-114"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="bd393-114"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="bd393-115">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="bd393-115">The NPP is not connected to the network.</span></span> <span data-ttu-id="bd393-116">Llame [a IDelaydC::Connect](idelaydc-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="bd393-116">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="bd393-117"><dt>**NMERR \_ NO \_ CAPTURA**</dt></span><span class="sxs-lookup"><span data-stu-id="bd393-117"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="bd393-118">El NPP no captura datos.</span><span class="sxs-lookup"><span data-stu-id="bd393-118">The NPP is not capturing data.</span></span> <span data-ttu-id="bd393-119">Llame [a IDelaydC::Start para](idelaydc-start.md) iniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="bd393-119">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="bd393-120"><dt>**NMERR \_ NO \_ RETRASADO**</dt></span><span class="sxs-lookup"><span data-stu-id="bd393-120"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="bd393-121">El NPP está conectado a la red, pero no con el [método IDelaydC::Connect.](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="bd393-121">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="bd393-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bd393-122">Remarks</span></span>

<span data-ttu-id="bd393-123">Cuando **se llama a IDelaydC::Stop,** Monitor de red la captura de datos y cierra el archivo de [*captura*](c.md).</span><span class="sxs-lookup"><span data-stu-id="bd393-123">When **IDelaydC::Stop** is called, Network Monitor stops capturing data and closes the [*capture file*](c.md).</span></span> <span data-ttu-id="bd393-124">(El nombre del archivo de captura se devolvió [cuando se llamó a IDelaydC::Start).](idelaydc-start.md)</span><span class="sxs-lookup"><span data-stu-id="bd393-124">(The name of the capture file was returned when [IDelaydC::Start](idelaydc-start.md) was called).</span></span> <span data-ttu-id="bd393-125">Ahora puede ver el contenido del archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="bd393-125">You can now look at the contents of the capture file.</span></span>

<span data-ttu-id="bd393-126">Cuando detenga e inicie la captura, asegúrese de llamar al método [IDelaydC::Configure](idelaydc-configure.md) cada vez que llame a [IDelaydC::Start](idelaydc-start.md) para reiniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="bd393-126">When you stop and start the capture, make sure you call the [IDelaydC::Configure](idelaydc-configure.md) method each time you call [IDelaydC::Start](idelaydc-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd393-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd393-127">Requirements</span></span>



| <span data-ttu-id="bd393-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd393-128">Requirement</span></span> | <span data-ttu-id="bd393-129">Valor</span><span class="sxs-lookup"><span data-stu-id="bd393-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd393-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd393-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bd393-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bd393-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="bd393-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd393-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bd393-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bd393-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="bd393-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd393-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd393-135"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="bd393-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="bd393-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bd393-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd393-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd393-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd393-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bd393-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd393-139">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="bd393-139">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="bd393-140">IDelaydC::Connect</span><span class="sxs-lookup"><span data-stu-id="bd393-140">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="bd393-141">IDelaydC::Configure</span><span class="sxs-lookup"><span data-stu-id="bd393-141">IDelaydC::Configure</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="bd393-142">IDelaydC::Start</span><span class="sxs-lookup"><span data-stu-id="bd393-142">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="bd393-143">Estadísticas</span><span class="sxs-lookup"><span data-stu-id="bd393-143">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




