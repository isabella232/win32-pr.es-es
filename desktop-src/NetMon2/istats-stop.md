---
description: El método Stop detiene la captura actual.
ms.assetid: 3aeeb29e-e174-46a2-82bb-44c466b8db98
title: 'IStas:: STOP (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 7b7b58527e7bde0c3bbdec4fc162b705dd178c10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652458"
---
# <a name="istatsstop-method"></a><span data-ttu-id="5315b-103">IStas:: STOP (método)</span><span class="sxs-lookup"><span data-stu-id="5315b-103">IStats::Stop method</span></span>

<span data-ttu-id="5315b-104">El método **Stop** detiene la captura actual.</span><span class="sxs-lookup"><span data-stu-id="5315b-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="5315b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5315b-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a><span data-ttu-id="5315b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5315b-106">Parameters</span></span>

<span data-ttu-id="5315b-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5315b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5315b-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5315b-108">Return value</span></span>

<span data-ttu-id="5315b-109">Si el método se ejecuta correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="5315b-109">If the method is successful the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="5315b-110">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="5315b-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="5315b-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5315b-111">Return code</span></span>                                                                                            | <span data-ttu-id="5315b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5315b-112">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5315b-113"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="5315b-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="5315b-114">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="5315b-114">The NPP is not connected to the network.</span></span> <span data-ttu-id="5315b-115">Llame al método [istas:: Connect](istats-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="5315b-115">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="5315b-116"><dt>**NMERR \_ no se \_ captura**</dt></span><span class="sxs-lookup"><span data-stu-id="5315b-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="5315b-117">NPP no está capturando datos.</span><span class="sxs-lookup"><span data-stu-id="5315b-117">The NPP is not capturing data.</span></span> <span data-ttu-id="5315b-118">Llame al método [istas:: Start](istats-start.md) para iniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="5315b-118">Call the [IStats::Start](istats-start.md) method to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="5315b-119"><dt>**NMERR \_ no \_ solo estadísticas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5315b-119"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="5315b-120">NPP está conectado a la red, pero no con el método [istas:: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="5315b-120">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="5315b-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5315b-121">Remarks</span></span>

<span data-ttu-id="5315b-122">Al reiniciar la captura después de llamar a los autores de la llamada **:: Stop** , asegúrese de llamar al método [istas:: configure](istats-configure.md) cada vez que llame a los [ISTA:: Start](istats-start.md) para reiniciar la captura.</span><span class="sxs-lookup"><span data-stu-id="5315b-122">When restarting the capture after **IStats::Stop** has been called, make sure you call the [IStats::Configure](istats-configure.md) method each time you call [IStats::Start](istats-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="5315b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5315b-123">Requirements</span></span>



| <span data-ttu-id="5315b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5315b-124">Requirement</span></span> | <span data-ttu-id="5315b-125">Value</span><span class="sxs-lookup"><span data-stu-id="5315b-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5315b-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5315b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5315b-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5315b-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="5315b-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5315b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5315b-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5315b-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="5315b-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5315b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5315b-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5315b-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="5315b-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5315b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5315b-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5315b-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5315b-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="5315b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5315b-135">IStas</span><span class="sxs-lookup"><span data-stu-id="5315b-135">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="5315b-136">ISta:: Connect</span><span class="sxs-lookup"><span data-stu-id="5315b-136">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="5315b-137">ISta:: configurar</span><span class="sxs-lookup"><span data-stu-id="5315b-137">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="5315b-138">ISta:: Start</span><span class="sxs-lookup"><span data-stu-id="5315b-138">IStats::Start</span></span>](istats-start.md)
</dt> </dl>

 

 




