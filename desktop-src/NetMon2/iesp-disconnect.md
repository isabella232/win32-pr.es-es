---
description: El método Disconnect desconecta el NPP de la red.
ms.assetid: 962e033d-a51c-47a2-83dc-cee1e7150ab8
title: IESP::D método Ulta (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b0dac1843083d77121883b2609c32addffbae290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153851"
---
# <a name="iespdisconnect-method"></a><span data-ttu-id="68244-103">IESP::D método Ulta</span><span class="sxs-lookup"><span data-stu-id="68244-103">IESP::Disconnect method</span></span>

<span data-ttu-id="68244-104">El método **Disconnect** desconecta el NPP de la red.</span><span class="sxs-lookup"><span data-stu-id="68244-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="68244-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68244-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="68244-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68244-106">Parameters</span></span>

<span data-ttu-id="68244-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="68244-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="68244-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68244-108">Return value</span></span>

<span data-ttu-id="68244-109">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="68244-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="68244-110">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="68244-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="68244-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="68244-111">Return code</span></span>                                                                                          | <span data-ttu-id="68244-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="68244-112">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="68244-113"><dt>**captura de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="68244-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="68244-114">NPP está capturando datos.</span><span class="sxs-lookup"><span data-stu-id="68244-114">The NPP is capturing data.</span></span> <span data-ttu-id="68244-115">No se puede desconectar de la red mientras la captura de datos está en curso.</span><span class="sxs-lookup"><span data-stu-id="68244-115">You cannot disconnect from the network while data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="68244-116"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="68244-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="68244-117">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="68244-117">The NPP is not connected to the network.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="68244-118"><dt>**NMERR \_ no \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="68244-118"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="68244-119">NPP está conectado a la red, pero no con el método [iesp:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="68244-119">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="68244-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68244-120">Remarks</span></span>

<span data-ttu-id="68244-121">No se puede llamar a este método cuando NPP está capturando datos.</span><span class="sxs-lookup"><span data-stu-id="68244-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="68244-122">Debe llamar al método **iesp:: Stop** antes de llamar a **iesp::D Ulta**.</span><span class="sxs-lookup"><span data-stu-id="68244-122">You must call the **IESP::Stop** method before calling **IESP::Disconnect**.</span></span>

## <a name="requirements"></a><span data-ttu-id="68244-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68244-123">Requirements</span></span>



| <span data-ttu-id="68244-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="68244-124">Requirement</span></span> | <span data-ttu-id="68244-125">Value</span><span class="sxs-lookup"><span data-stu-id="68244-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68244-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68244-126">Minimum supported client</span></span><br/> | <span data-ttu-id="68244-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="68244-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="68244-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68244-128">Minimum supported server</span></span><br/> | <span data-ttu-id="68244-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="68244-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="68244-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68244-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="68244-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="68244-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="68244-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68244-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68244-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68244-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68244-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="68244-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68244-135">IESP</span><span class="sxs-lookup"><span data-stu-id="68244-135">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="68244-136">IESP:: Connect</span><span class="sxs-lookup"><span data-stu-id="68244-136">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="68244-137">IESP:: Stop</span><span class="sxs-lookup"><span data-stu-id="68244-137">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




