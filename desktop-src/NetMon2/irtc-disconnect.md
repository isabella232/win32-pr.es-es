---
description: El método Disconnect desconecta el NPP de la red.
ms.assetid: 47a0cce0-a50d-4bad-9787-672cc3d13d07
title: IRTC::D método Ulta (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: df58d6ac0e61ecc370510474c3bc067726d9824b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276278"
---
# <a name="irtcdisconnect-method"></a><span data-ttu-id="b4120-103">IRTC::D método Ulta</span><span class="sxs-lookup"><span data-stu-id="b4120-103">IRTC::Disconnect method</span></span>

<span data-ttu-id="b4120-104">El método **Disconnect** desconecta el NPP de la red.</span><span class="sxs-lookup"><span data-stu-id="b4120-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4120-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4120-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="b4120-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4120-106">Parameters</span></span>

<span data-ttu-id="b4120-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b4120-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b4120-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4120-108">Return value</span></span>

<span data-ttu-id="b4120-109">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b4120-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b4120-110">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="b4120-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="b4120-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b4120-111">Return code</span></span>                                                                                          | <span data-ttu-id="b4120-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4120-112">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b4120-113"><dt>**captura de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b4120-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="b4120-114">NPP está capturando datos.</span><span class="sxs-lookup"><span data-stu-id="b4120-114">The NPP is capturing data.</span></span> <span data-ttu-id="b4120-115">No se puede desconectar de la red mientras la captura de datos está en curso.</span><span class="sxs-lookup"><span data-stu-id="b4120-115">You cannot disconnect from the network while the data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="b4120-116"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="b4120-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="b4120-117">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="b4120-117">The NPP is not connected to the network.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="b4120-118"><dt>**NMERR \_ no es en \_ tiempo real**</dt></span><span class="sxs-lookup"><span data-stu-id="b4120-118"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="b4120-119">NPP está conectado a la red, pero no con el método [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="b4120-119">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="b4120-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4120-120">Remarks</span></span>

<span data-ttu-id="b4120-121">No se puede llamar a este método cuando NPP está capturando datos.</span><span class="sxs-lookup"><span data-stu-id="b4120-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="b4120-122">Debe llamar al método [IRTC:: Stop](irtc-stop.md) antes de llamar a IRTC::D Ulta.</span><span class="sxs-lookup"><span data-stu-id="b4120-122">You must call the [IRTC::Stop](irtc-stop.md) method before calling IRTC::Disconnect.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4120-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4120-123">Requirements</span></span>



| <span data-ttu-id="b4120-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4120-124">Requirement</span></span> | <span data-ttu-id="b4120-125">Value</span><span class="sxs-lookup"><span data-stu-id="b4120-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4120-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4120-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b4120-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b4120-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="b4120-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4120-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b4120-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b4120-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="b4120-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4120-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4120-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4120-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="b4120-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b4120-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4120-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4120-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4120-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4120-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4120-135">IRTC</span><span class="sxs-lookup"><span data-stu-id="b4120-135">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="b4120-136">IRTC:: Connect</span><span class="sxs-lookup"><span data-stu-id="b4120-136">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="b4120-137">IRTC:: Stop</span><span class="sxs-lookup"><span data-stu-id="b4120-137">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




