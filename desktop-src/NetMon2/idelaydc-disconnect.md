---
description: 'Método IDelaydC::D isconnect: el método Disconnect desconecta el NPP de la red.'
ms.assetid: 476bbce4-2e3c-448f-b85e-6adac424fb0d
title: Método IDelaydC::D isconnect (Netmon.h)
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
ms.openlocfilehash: 967bd9674cb28363804b8c8af12c541bcb8675ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110813"
---
# <a name="idelaydcdisconnect-method"></a><span data-ttu-id="774be-103">IDelaydC::D isconnect (método)</span><span class="sxs-lookup"><span data-stu-id="774be-103">IDelaydC::Disconnect method</span></span>

<span data-ttu-id="774be-104">El **método Disconnect** desconecta el NPP de la red.</span><span class="sxs-lookup"><span data-stu-id="774be-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="774be-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="774be-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="774be-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="774be-106">Parameters</span></span>

<span data-ttu-id="774be-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="774be-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="774be-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="774be-108">Return value</span></span>

<span data-ttu-id="774be-109">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="774be-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="774be-110">Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="774be-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="774be-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="774be-111">Return code</span></span>                                                                                          | <span data-ttu-id="774be-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="774be-112">Description</span></span>                                                                                                       |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="774be-113"><dt>**CAPTURA DE \_ NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="774be-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="774be-114">El NPP captura datos.</span><span class="sxs-lookup"><span data-stu-id="774be-114">The NPP is capturing data.</span></span> <span data-ttu-id="774be-115">No se puede desconectar el NPP de la red durante una captura.</span><span class="sxs-lookup"><span data-stu-id="774be-115">You cannot disconnect the NPP from the network during a capture.</span></span><br/>            |
| <dl> <span data-ttu-id="774be-116"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="774be-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="774be-117">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="774be-117">The NPP is not connected to the network.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="774be-118"><dt>**NMERR \_ NO \_ RETRASADO**</dt></span><span class="sxs-lookup"><span data-stu-id="774be-118"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="774be-119">El NPP está conectado a la red, pero no con el [método IDelaydC::Connect.](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="774be-119">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="774be-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="774be-120">Remarks</span></span>

<span data-ttu-id="774be-121">No se puede llamar a este método cuando el NPP captura datos.</span><span class="sxs-lookup"><span data-stu-id="774be-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="774be-122">Debe llamar al método **IDelaydC::Stop** antes de llamar a **Disconnect**.</span><span class="sxs-lookup"><span data-stu-id="774be-122">You must call the **IDelaydC::Stop** method before calling **Disconnect**.</span></span>

## <a name="requirements"></a><span data-ttu-id="774be-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="774be-123">Requirements</span></span>



| <span data-ttu-id="774be-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="774be-124">Requirement</span></span> | <span data-ttu-id="774be-125">Valor</span><span class="sxs-lookup"><span data-stu-id="774be-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="774be-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="774be-126">Minimum supported client</span></span><br/> | <span data-ttu-id="774be-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="774be-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="774be-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="774be-128">Minimum supported server</span></span><br/> | <span data-ttu-id="774be-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="774be-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="774be-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="774be-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="774be-131"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="774be-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="774be-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="774be-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="774be-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="774be-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="774be-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="774be-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="774be-135">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="774be-135">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="774be-136">IDelaydC::Connect</span><span class="sxs-lookup"><span data-stu-id="774be-136">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="774be-137">IDelaydC::Stop</span><span class="sxs-lookup"><span data-stu-id="774be-137">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




