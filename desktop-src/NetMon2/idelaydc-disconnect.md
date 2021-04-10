---
description: El método Disconnect desconecta el NPP de la red.
ms.assetid: 476bbce4-2e3c-448f-b85e-6adac424fb0d
title: IDelaydC::D método Ulta (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d192aa80f543706eea4bc197bc3dc8d57dd64aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153855"
---
# <a name="idelaydcdisconnect-method"></a><span data-ttu-id="bad89-103">IDelaydC::D método Ulta</span><span class="sxs-lookup"><span data-stu-id="bad89-103">IDelaydC::Disconnect method</span></span>

<span data-ttu-id="bad89-104">El método **Disconnect** desconecta el NPP de la red.</span><span class="sxs-lookup"><span data-stu-id="bad89-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="bad89-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bad89-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="bad89-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bad89-106">Parameters</span></span>

<span data-ttu-id="bad89-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="bad89-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bad89-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bad89-108">Return value</span></span>

<span data-ttu-id="bad89-109">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="bad89-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="bad89-110">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="bad89-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="bad89-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bad89-111">Return code</span></span>                                                                                          | <span data-ttu-id="bad89-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="bad89-112">Description</span></span>                                                                                                       |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bad89-113"><dt>**captura de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bad89-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="bad89-114">NPP está capturando datos.</span><span class="sxs-lookup"><span data-stu-id="bad89-114">The NPP is capturing data.</span></span> <span data-ttu-id="bad89-115">No se puede desconectar el NPP de la red durante una captura.</span><span class="sxs-lookup"><span data-stu-id="bad89-115">You cannot disconnect the NPP from the network during a capture.</span></span><br/>            |
| <dl> <span data-ttu-id="bad89-116"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="bad89-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="bad89-117">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="bad89-117">The NPP is not connected to the network.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="bad89-118"><dt>**NMERR \_ no \_ retrasado**</dt></span><span class="sxs-lookup"><span data-stu-id="bad89-118"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="bad89-119">NPP está conectado a la red, pero no con el método [IDelaydC:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="bad89-119">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bad89-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bad89-120">Remarks</span></span>

<span data-ttu-id="bad89-121">No se puede llamar a este método cuando NPP está capturando datos.</span><span class="sxs-lookup"><span data-stu-id="bad89-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="bad89-122">Debe llamar al método **IDelaydC:: Stop** antes de llamar a **Disconnect**.</span><span class="sxs-lookup"><span data-stu-id="bad89-122">You must call the **IDelaydC::Stop** method before calling **Disconnect**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bad89-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bad89-123">Requirements</span></span>



| <span data-ttu-id="bad89-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bad89-124">Requirement</span></span> | <span data-ttu-id="bad89-125">Value</span><span class="sxs-lookup"><span data-stu-id="bad89-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bad89-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bad89-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bad89-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bad89-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="bad89-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bad89-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bad89-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bad89-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="bad89-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bad89-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="bad89-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bad89-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="bad89-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bad89-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bad89-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bad89-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bad89-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="bad89-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bad89-135">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="bad89-135">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="bad89-136">IDelaydC:: Connect</span><span class="sxs-lookup"><span data-stu-id="bad89-136">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="bad89-137">IDelaydC:: Stop</span><span class="sxs-lookup"><span data-stu-id="bad89-137">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




