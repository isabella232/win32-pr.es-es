---
description: El método QueryStatus recupera el estado de NPP.
ms.assetid: b035d495-a078-4436-9501-0a30fbfa7268
title: 'IDelaydC:: QueryStatus (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: cff92dfec95555076f9edba5a1b591f0ef905c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687323"
---
# <a name="idelaydcquerystatus-method"></a><span data-ttu-id="eee40-103">IDelaydC:: QueryStatus (método)</span><span class="sxs-lookup"><span data-stu-id="eee40-103">IDelaydC::QueryStatus method</span></span>

<span data-ttu-id="eee40-104">El método **QueryStatus** recupera el estado de NPP.</span><span class="sxs-lookup"><span data-stu-id="eee40-104">The **QueryStatus** method retrieves the status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="eee40-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eee40-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="eee40-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eee40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eee40-107">*pNetworkStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="eee40-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eee40-108">Puntero a una estructura [NETWORKSTATUS](networkstatus.md) devuelta que indica el estado actual (captura, en pausa, detenido, etc.) del NPP.</span><span class="sxs-lookup"><span data-stu-id="eee40-108">Pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="eee40-109">Es su responsabilidad asignar y liberar la memoria asociada a la estructura **NETWORKSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="eee40-109">It is your responsibility to allocate and free the memory associated with the **NETWORKSTATUS** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eee40-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eee40-110">Return value</span></span>

<span data-ttu-id="eee40-111">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="eee40-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="eee40-112">Si el método no se realiza correctamente, el valor devuelto es el siguiente código de error:</span><span class="sxs-lookup"><span data-stu-id="eee40-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="eee40-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="eee40-113">Return code</span></span>                                                                                              | <span data-ttu-id="eee40-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="eee40-114">Description</span></span>                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eee40-115"><dt>**NMERR \_ parámetro no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eee40-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="eee40-116">El parámetro *pNetworkStatus* no está señalando a una estructura [NETWORKSTATUS](networkstatus.md) válida.</span><span class="sxs-lookup"><span data-stu-id="eee40-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="eee40-117">Asigne memoria para esta estructura y llame de nuevo al método **IDelaydC:: QueryStatus** .</span><span class="sxs-lookup"><span data-stu-id="eee40-117">Allocate memory for this structure and call the **IDelaydC::QueryStatus** method again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eee40-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eee40-118">Remarks</span></span>

<span data-ttu-id="eee40-119">Se puede llamar a este método en cualquier momento después de llamar a [CreateNPPInterface](createnppinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="eee40-119">This method can be called at any time after [CreateNPPInterface](createnppinterface.md) is called.</span></span> <span data-ttu-id="eee40-120">Se puede llamar a para ver si el NPP está conectado a la red, para averiguar el estado de la captura actual y para ver si hay algún desencadenador pendiente.</span><span class="sxs-lookup"><span data-stu-id="eee40-120">It can be called to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span>

<span data-ttu-id="eee40-121">Antes de llamar a este método, debe asignar la memoria necesaria para la estructura [NETWORKSTATUS](networkstatus.md) y liberar esa memoria cuando la estructura ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="eee40-121">Before calling this method, you must allocate the memory needed for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="eee40-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eee40-122">Requirements</span></span>



| <span data-ttu-id="eee40-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="eee40-123">Requirement</span></span> | <span data-ttu-id="eee40-124">Value</span><span class="sxs-lookup"><span data-stu-id="eee40-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eee40-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eee40-125">Minimum supported client</span></span><br/> | <span data-ttu-id="eee40-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="eee40-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="eee40-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eee40-127">Minimum supported server</span></span><br/> | <span data-ttu-id="eee40-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="eee40-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="eee40-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eee40-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="eee40-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="eee40-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="eee40-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eee40-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eee40-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eee40-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eee40-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="eee40-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eee40-134">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="eee40-134">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="eee40-135">CreateNPPInterface</span><span class="sxs-lookup"><span data-stu-id="eee40-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="eee40-136">NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="eee40-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




