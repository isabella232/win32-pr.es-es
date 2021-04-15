---
description: El método Stop detiene la captura actual.
ms.assetid: 1b627137-e72d-4425-98d9-e296fb07e509
title: 'IDelaydC:: STOP (método) (Netmon. h)'
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
ms.openlocfilehash: 42c9cc1c4b6da7b5f934dd96f26aa9348c43ac0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496984"
---
# <a name="idelaydcstop-method"></a><span data-ttu-id="aa9c8-103">IDelaydC:: STOP (método)</span><span class="sxs-lookup"><span data-stu-id="aa9c8-103">IDelaydC::Stop method</span></span>

<span data-ttu-id="aa9c8-104">El método **Stop** detiene la captura actual.</span><span class="sxs-lookup"><span data-stu-id="aa9c8-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa9c8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa9c8-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="aa9c8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa9c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa9c8-107">*lpStats* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="aa9c8-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa9c8-108">Puntero a una estructura de [estadísticas](statistics.md) que contiene estadísticas de red como el total de tramas y el total de bytes capturados.</span><span class="sxs-lookup"><span data-stu-id="aa9c8-108">Pointer to a [STATISTICS](statistics.md) structure that contains network statistics such as total frames and total bytes captured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa9c8-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa9c8-109">Return value</span></span>

<span data-ttu-id="aa9c8-110">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="aa9c8-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="aa9c8-111">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="aa9c8-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="aa9c8-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="aa9c8-112">Return code</span></span>                                                                                          | <span data-ttu-id="aa9c8-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa9c8-113">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aa9c8-114"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="aa9c8-114"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="aa9c8-115">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="aa9c8-115">The NPP is not connected to the network.</span></span> <span data-ttu-id="aa9c8-116">Llame a [IDelaydC:: Connect](idelaydc-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="aa9c8-116">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="aa9c8-117"><dt>**NMERR \_ no se \_ captura**</dt></span><span class="sxs-lookup"><span data-stu-id="aa9c8-117"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="aa9c8-118">NPP no está capturando datos.</span><span class="sxs-lookup"><span data-stu-id="aa9c8-118">The NPP is not capturing data.</span></span> <span data-ttu-id="aa9c8-119">Llame a [IDelaydC:: Start](idelaydc-start.md) para iniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="aa9c8-119">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="aa9c8-120"><dt>**NMERR \_ no \_ retrasado**</dt></span><span class="sxs-lookup"><span data-stu-id="aa9c8-120"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="aa9c8-121">NPP está conectado a la red, pero no con el método [IDelaydC:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="aa9c8-121">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="aa9c8-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa9c8-122">Remarks</span></span>

<span data-ttu-id="aa9c8-123">Cuando se llama a **IDelaydC:: Stop** , monitor de red detiene la captura de datos y cierra el [*archivo de captura*](c.md).</span><span class="sxs-lookup"><span data-stu-id="aa9c8-123">When **IDelaydC::Stop** is called, Network Monitor stops capturing data and closes the [*capture file*](c.md).</span></span> <span data-ttu-id="aa9c8-124">(El nombre del archivo de captura se devolvió cuando se llamó a [IDelaydC:: Start](idelaydc-start.md) ).</span><span class="sxs-lookup"><span data-stu-id="aa9c8-124">(The name of the capture file was returned when [IDelaydC::Start](idelaydc-start.md) was called).</span></span> <span data-ttu-id="aa9c8-125">Ahora puede examinar el contenido del archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="aa9c8-125">You can now look at the contents of the capture file.</span></span>

<span data-ttu-id="aa9c8-126">Al detener e iniciar la captura, asegúrese de llamar al método [IDelaydC:: configure](idelaydc-configure.md) cada vez que llame a [IDelaydC:: Start](idelaydc-start.md) para reiniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="aa9c8-126">When you stop and start the capture, make sure you call the [IDelaydC::Configure](idelaydc-configure.md) method each time you call [IDelaydC::Start](idelaydc-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa9c8-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa9c8-127">Requirements</span></span>



| <span data-ttu-id="aa9c8-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa9c8-128">Requirement</span></span> | <span data-ttu-id="aa9c8-129">Value</span><span class="sxs-lookup"><span data-stu-id="aa9c8-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa9c8-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa9c8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="aa9c8-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="aa9c8-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="aa9c8-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa9c8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="aa9c8-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aa9c8-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="aa9c8-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa9c8-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa9c8-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa9c8-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="aa9c8-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aa9c8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa9c8-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa9c8-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa9c8-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa9c8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa9c8-139">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="aa9c8-139">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="aa9c8-140">IDelaydC:: Connect</span><span class="sxs-lookup"><span data-stu-id="aa9c8-140">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="aa9c8-141">IDelaydC:: configure</span><span class="sxs-lookup"><span data-stu-id="aa9c8-141">IDelaydC::Configure</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="aa9c8-142">IDelaydC:: Start</span><span class="sxs-lookup"><span data-stu-id="aa9c8-142">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="aa9c8-143">¡</span><span class="sxs-lookup"><span data-stu-id="aa9c8-143">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




