---
description: 'Método IESP::Stop: el método Stop detiene la captura actual.'
ms.assetid: d2d4e51a-c6a4-4aec-a805-929af621ffb3
title: Método IESP::Stop (Netmon.h)
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
ms.openlocfilehash: ac262d8da5ab218db7300ea38da59d5c738421c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103773"
---
# <a name="iespstop-method"></a><span data-ttu-id="3d045-103">IESP::Stop (método)</span><span class="sxs-lookup"><span data-stu-id="3d045-103">IESP::Stop method</span></span>

<span data-ttu-id="3d045-104">El **método Stop** detiene la captura actual.</span><span class="sxs-lookup"><span data-stu-id="3d045-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d045-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d045-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="3d045-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d045-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d045-107">*lpStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3d045-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d045-108">Puntero a una [estructura STATISTICS que](statistics.md) contiene estadísticas de red, como el total de fotogramas y el total de bytes capturados.</span><span class="sxs-lookup"><span data-stu-id="3d045-108">Pointer to a [STATISTICS](statistics.md) structure that contains network statistics such as total frames and total bytes captured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d045-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d045-109">Return value</span></span>

<span data-ttu-id="3d045-110">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="3d045-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3d045-111">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="3d045-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="3d045-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3d045-112">Return code</span></span>                                                                                          | <span data-ttu-id="3d045-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d045-113">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3d045-114"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="3d045-114"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="3d045-115">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="3d045-115">The NPP is not connected to the network.</span></span> <span data-ttu-id="3d045-116">Llame [a IESP::Connect](iesp-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="3d045-116">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="3d045-117"><dt>**NMERR \_ NO \_ CAPTURA**</dt></span><span class="sxs-lookup"><span data-stu-id="3d045-117"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="3d045-118">El NPP no captura datos.</span><span class="sxs-lookup"><span data-stu-id="3d045-118">The NPP is not capturing data.</span></span> <span data-ttu-id="3d045-119">Llame [a IESP::Start](iesp-start.md) para iniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="3d045-119">Call [IESP::Start](iesp-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="3d045-120"><dt>**NMERR \_ NOT \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="3d045-120"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="3d045-121">El NPP está conectado a la red, pero no con el [método IESP::Connect.](iesp-connect.md)</span><span class="sxs-lookup"><span data-stu-id="3d045-121">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="3d045-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3d045-122">Remarks</span></span>

<span data-ttu-id="3d045-123">Cuando se **llama al método IESP::Stop,** Monitor de red detiene la captura de datos y cierra el [*archivo de captura.*](c.md)</span><span class="sxs-lookup"><span data-stu-id="3d045-123">When the **IESP::Stop** method is called, Network Monitor stops capturing data and closes the [*capture file.*](c.md)</span></span> <span data-ttu-id="3d045-124">(El nombre del archivo de captura se devolvió cuando se llamó a [IESP::Start).](iesp-start.md) Ahora puede ver el contenido del archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="3d045-124">(The name of the capture file was returned when [IESP::Start](iesp-start.md) was called.) You can now look at the contents of the capture file.</span></span>

<span data-ttu-id="3d045-125">Cuando detenga y reinicie la captura, asegúrese de llamar al método [IESP::Configure](iesp-configure.md) cada vez que llame a [IESP::Start](iesp-start.md) para reiniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="3d045-125">When you stop and restart the capture, make sure to call the [IESP::Configure](iesp-configure.md) method each time you call [IESP::Start](iesp-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d045-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d045-126">Requirements</span></span>



| <span data-ttu-id="3d045-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d045-127">Requirement</span></span> | <span data-ttu-id="3d045-128">Valor</span><span class="sxs-lookup"><span data-stu-id="3d045-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d045-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d045-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3d045-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3d045-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="3d045-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d045-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3d045-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3d045-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="3d045-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d045-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d045-134"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="3d045-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="3d045-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3d045-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d045-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d045-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d045-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3d045-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d045-138">IESP</span><span class="sxs-lookup"><span data-stu-id="3d045-138">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="3d045-139">IESP::Connect</span><span class="sxs-lookup"><span data-stu-id="3d045-139">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="3d045-140">IESP::Start</span><span class="sxs-lookup"><span data-stu-id="3d045-140">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="3d045-141">Estadísticas</span><span class="sxs-lookup"><span data-stu-id="3d045-141">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




