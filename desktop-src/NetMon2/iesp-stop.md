---
description: El método Stop detiene la captura actual.
ms.assetid: d2d4e51a-c6a4-4aec-a805-929af621ffb3
title: 'IESP:: STOP (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 50dfb274e1355af93c473609f95607e6b3faf1fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686556"
---
# <a name="iespstop-method"></a><span data-ttu-id="11373-103">IESP:: STOP (método)</span><span class="sxs-lookup"><span data-stu-id="11373-103">IESP::Stop method</span></span>

<span data-ttu-id="11373-104">El método **Stop** detiene la captura actual.</span><span class="sxs-lookup"><span data-stu-id="11373-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="11373-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11373-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="11373-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11373-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11373-107">*lpStats* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="11373-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11373-108">Puntero a una estructura de [estadísticas](statistics.md) que contiene estadísticas de red como el total de tramas y el total de bytes capturados.</span><span class="sxs-lookup"><span data-stu-id="11373-108">Pointer to a [STATISTICS](statistics.md) structure that contains network statistics such as total frames and total bytes captured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11373-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11373-109">Return value</span></span>

<span data-ttu-id="11373-110">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="11373-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="11373-111">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="11373-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="11373-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="11373-112">Return code</span></span>                                                                                          | <span data-ttu-id="11373-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="11373-113">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11373-114"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="11373-114"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="11373-115">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="11373-115">The NPP is not connected to the network.</span></span> <span data-ttu-id="11373-116">Llame a [iesp:: Connect](iesp-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="11373-116">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="11373-117"><dt>**NMERR \_ no se \_ captura**</dt></span><span class="sxs-lookup"><span data-stu-id="11373-117"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="11373-118">NPP no está capturando datos.</span><span class="sxs-lookup"><span data-stu-id="11373-118">The NPP is not capturing data.</span></span> <span data-ttu-id="11373-119">Llame a [iesp:: Start](iesp-start.md) para iniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="11373-119">Call [IESP::Start](iesp-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="11373-120"><dt>**NMERR \_ no \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="11373-120"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="11373-121">NPP está conectado a la red, pero no con el método [iesp:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="11373-121">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="11373-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11373-122">Remarks</span></span>

<span data-ttu-id="11373-123">Cuando se llama al método **iesp:: Stop** , monitor de red detiene la captura de datos y cierra el [*archivo de captura.*](c.md)</span><span class="sxs-lookup"><span data-stu-id="11373-123">When the **IESP::Stop** method is called, Network Monitor stops capturing data and closes the [*capture file.*](c.md)</span></span> <span data-ttu-id="11373-124">(El nombre del archivo de captura se devolvió cuando se llamó a [iesp:: Start](iesp-start.md) ). Ahora puede examinar el contenido del archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="11373-124">(The name of the capture file was returned when [IESP::Start](iesp-start.md) was called.) You can now look at the contents of the capture file.</span></span>

<span data-ttu-id="11373-125">Cuando detenga y reinicie la captura, asegúrese de llamar al método [iesp:: configure](iesp-configure.md) cada vez que llame a [iesp:: Start](iesp-start.md) para reiniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="11373-125">When you stop and restart the capture, make sure to call the [IESP::Configure](iesp-configure.md) method each time you call [IESP::Start](iesp-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="11373-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11373-126">Requirements</span></span>



| <span data-ttu-id="11373-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="11373-127">Requirement</span></span> | <span data-ttu-id="11373-128">Value</span><span class="sxs-lookup"><span data-stu-id="11373-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11373-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11373-129">Minimum supported client</span></span><br/> | <span data-ttu-id="11373-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="11373-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="11373-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11373-131">Minimum supported server</span></span><br/> | <span data-ttu-id="11373-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="11373-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="11373-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11373-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="11373-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="11373-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="11373-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="11373-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11373-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11373-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11373-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="11373-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11373-138">IESP</span><span class="sxs-lookup"><span data-stu-id="11373-138">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="11373-139">IESP:: Connect</span><span class="sxs-lookup"><span data-stu-id="11373-139">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="11373-140">IESP:: Start</span><span class="sxs-lookup"><span data-stu-id="11373-140">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="11373-141">¡</span><span class="sxs-lookup"><span data-stu-id="11373-141">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




