---
description: El método QueryStatus recupera el estado de NPP.
ms.assetid: 86b1c1ee-3a35-4603-9e93-fe09f886c32f
title: 'IStas:: QueryStatus (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 02e013d87734b61ad26b6563c402db1b8d4cb4f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819475"
---
# <a name="istatsquerystatus-method"></a><span data-ttu-id="36c0e-103">IStas:: QueryStatus (método)</span><span class="sxs-lookup"><span data-stu-id="36c0e-103">IStats::QueryStatus method</span></span>

<span data-ttu-id="36c0e-104">El método **QueryStatus** recupera el estado de NPP.</span><span class="sxs-lookup"><span data-stu-id="36c0e-104">The **QueryStatus** method retrieves the status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="36c0e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36c0e-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="36c0e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36c0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36c0e-107">*pNetworkStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="36c0e-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36c0e-108">Puntero a una estructura [NETWORKSTATUS](networkstatus.md) devuelta que indica el estado actual (captura, en pausa, detenido, etc.) del NPP.</span><span class="sxs-lookup"><span data-stu-id="36c0e-108">Pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="36c0e-109">Es responsabilidad de la aplicación asignar y liberar la memoria de la estructura **NETWORKSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="36c0e-109">It is the application's responsibility to allocate and free the memory for the **NETWORKSTATUS** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36c0e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36c0e-110">Return value</span></span>

<span data-ttu-id="36c0e-111">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="36c0e-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="36c0e-112">Si el método no se realiza correctamente, el valor devuelto es el siguiente código de error:</span><span class="sxs-lookup"><span data-stu-id="36c0e-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="36c0e-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="36c0e-113">Return code</span></span>                                                                                              | <span data-ttu-id="36c0e-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="36c0e-114">Description</span></span>                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="36c0e-115"><dt>**NMERR \_ parámetro no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="36c0e-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="36c0e-116">El parámetro *pNetworkStatus* no está señalando a una estructura [NETWORKSTATUS](networkstatus.md) válida.</span><span class="sxs-lookup"><span data-stu-id="36c0e-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="36c0e-117">Asigne memoria para esta estructura y llame de nuevo al método **istas:: QueryStatus** .</span><span class="sxs-lookup"><span data-stu-id="36c0e-117">Allocate memory for this structure and call the **IStats::QueryStatus** method again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="36c0e-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36c0e-118">Remarks</span></span>

<span data-ttu-id="36c0e-119">Se puede llamar a este método en cualquier momento después de llamar al método [CreateNPPInterface](createnppinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="36c0e-119">This method can be called at any time after the [CreateNPPInterface](createnppinterface.md) method is called.</span></span> <span data-ttu-id="36c0e-120">Se puede llamar a para ver si el NPP está conectado a la red, para averiguar el estado de la captura actual y para ver si hay algún desencadenador pendiente.</span><span class="sxs-lookup"><span data-stu-id="36c0e-120">It can be called to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span> <span data-ttu-id="36c0e-121">Sin embargo, antes de llamar a este método, debe asignar la memoria necesaria para la estructura [NETWORKSTATUS](networkstatus.md) y liberar esa memoria cuando la estructura ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="36c0e-121">Before calling this method, however, you must allocate the memory needed for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="36c0e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36c0e-122">Requirements</span></span>



| <span data-ttu-id="36c0e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="36c0e-123">Requirement</span></span> | <span data-ttu-id="36c0e-124">Value</span><span class="sxs-lookup"><span data-stu-id="36c0e-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36c0e-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36c0e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="36c0e-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="36c0e-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="36c0e-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36c0e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="36c0e-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="36c0e-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="36c0e-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36c0e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="36c0e-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="36c0e-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="36c0e-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="36c0e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36c0e-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36c0e-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36c0e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="36c0e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36c0e-134">IStas</span><span class="sxs-lookup"><span data-stu-id="36c0e-134">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="36c0e-135">CreateNPPInterface</span><span class="sxs-lookup"><span data-stu-id="36c0e-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="36c0e-136">NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="36c0e-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




