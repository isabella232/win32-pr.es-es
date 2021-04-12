---
description: Recupera el estado NPP.
ms.assetid: 48682997-f641-4ae5-b5ad-64fd84f07ae3
title: 'IESP:: QueryStatus (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 3435ed832484042bfeb9229e4b46fa34441cb395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276279"
---
# <a name="iespquerystatus-method"></a><span data-ttu-id="68748-103">IESP:: QueryStatus (método)</span><span class="sxs-lookup"><span data-stu-id="68748-103">IESP::QueryStatus method</span></span>

<span data-ttu-id="68748-104">El método **QueryStatus** recupera el estado NPP.</span><span class="sxs-lookup"><span data-stu-id="68748-104">The **QueryStatus** method retrieves the NPP status.</span></span>

## <a name="syntax"></a><span data-ttu-id="68748-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68748-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="68748-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68748-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68748-107">*pNetworkStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="68748-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68748-108">Puntero a una estructura [NETWORKSTATUS](networkstatus.md) devuelta que indica el estado actual (captura, en pausa, detenido, etc.) del NPP.</span><span class="sxs-lookup"><span data-stu-id="68748-108">A pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="68748-109">El usuario debe asignar y liberar la memoria de la estructura NETWORKSTATUS.</span><span class="sxs-lookup"><span data-stu-id="68748-109">The user must allocate and free the memory for the NETWORKSTATUS structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68748-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68748-110">Return value</span></span>

<span data-ttu-id="68748-111">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="68748-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="68748-112">Si el método no se realiza correctamente, el valor devuelto es el siguiente código de error:</span><span class="sxs-lookup"><span data-stu-id="68748-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="68748-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="68748-113">Return code</span></span>                                                                                              | <span data-ttu-id="68748-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="68748-114">Description</span></span>                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="68748-115"><dt>**NMERR \_ parámetro no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="68748-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="68748-116">El parámetro *pNetworkStatus* no está señalando a una estructura [NETWORKSTATUS](networkstatus.md) válida.</span><span class="sxs-lookup"><span data-stu-id="68748-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="68748-117">Asigne memoria para esta estructura y llame de nuevo a **iesp:: QueryStatus** .</span><span class="sxs-lookup"><span data-stu-id="68748-117">Allocate memory for this structure and call **IESP::QueryStatus** again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="68748-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68748-118">Remarks</span></span>

<span data-ttu-id="68748-119">Se puede llamar a este método en cualquier momento después de llamar a [CreateNPPInterface](createnppinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="68748-119">This method can be called at any time after the [CreateNPPInterface](createnppinterface.md) is called.</span></span> <span data-ttu-id="68748-120">Puede llamar a este método para ver si el NPP está conectado a la red, para averiguar el estado de la captura actual y para ver si hay algún desencadenador pendiente.</span><span class="sxs-lookup"><span data-stu-id="68748-120">You can call this method to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span>

<span data-ttu-id="68748-121">Antes de llamar a este método, asigne la memoria necesaria para la estructura [NETWORKSTATUS](networkstatus.md) y libere esa memoria cuando la estructura ya no sea necesaria.</span><span class="sxs-lookup"><span data-stu-id="68748-121">Before calling this method, allocate the memory required for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer required.</span></span>

## <a name="requirements"></a><span data-ttu-id="68748-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68748-122">Requirements</span></span>



| <span data-ttu-id="68748-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="68748-123">Requirement</span></span> | <span data-ttu-id="68748-124">Value</span><span class="sxs-lookup"><span data-stu-id="68748-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68748-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68748-125">Minimum supported client</span></span><br/> | <span data-ttu-id="68748-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="68748-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="68748-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68748-127">Minimum supported server</span></span><br/> | <span data-ttu-id="68748-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="68748-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="68748-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68748-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="68748-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="68748-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="68748-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68748-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68748-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68748-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68748-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="68748-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68748-134">IESP</span><span class="sxs-lookup"><span data-stu-id="68748-134">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="68748-135">CreateNPPInterface</span><span class="sxs-lookup"><span data-stu-id="68748-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="68748-136">NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="68748-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




