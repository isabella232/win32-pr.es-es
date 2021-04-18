---
description: El método QueryStatus recupera el estado de NPP.
ms.assetid: 4517eb34-087a-491c-97b5-cbe9190fa7a2
title: 'IRTC:: QueryStatus (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: e05120353cd39db661cf1b4309353034c184cd66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652559"
---
# <a name="irtcquerystatus-method"></a><span data-ttu-id="fdcf3-103">IRTC:: QueryStatus (método)</span><span class="sxs-lookup"><span data-stu-id="fdcf3-103">IRTC::QueryStatus method</span></span>

<span data-ttu-id="fdcf3-104">El método **QueryStatus** recupera el estado de NPP.</span><span class="sxs-lookup"><span data-stu-id="fdcf3-104">The **QueryStatus** method retrieves the status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdcf3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fdcf3-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="fdcf3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fdcf3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdcf3-107">*pNetworkStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fdcf3-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdcf3-108">Puntero a una estructura [NETWORKSTATUS](networkstatus.md) devuelta que indica el estado actual (captura, en pausa, detenido, etc.) del NPP.</span><span class="sxs-lookup"><span data-stu-id="fdcf3-108">Pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="fdcf3-109">Es responsabilidad de la aplicación asignar y liberar la memoria de la estructura **NETWORKSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="fdcf3-109">It is the application's responsibility to allocate and free the memory for the **NETWORKSTATUS** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdcf3-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fdcf3-110">Return value</span></span>

<span data-ttu-id="fdcf3-111">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="fdcf3-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="fdcf3-112">Si el método no se realiza correctamente, el valor devuelto es el siguiente código de error:</span><span class="sxs-lookup"><span data-stu-id="fdcf3-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="fdcf3-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fdcf3-113">Return code</span></span>                                                                                              | <span data-ttu-id="fdcf3-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="fdcf3-114">Description</span></span>                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fdcf3-115"><dt>**NMERR \_ parámetro no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fdcf3-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="fdcf3-116">El parámetro *pNetworkStatus* no está señalando a una estructura [NETWORKSTATUS](networkstatus.md) válida.</span><span class="sxs-lookup"><span data-stu-id="fdcf3-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="fdcf3-117">Asigne memoria para esta estructura y llame de nuevo a **IRTC:: QueryStatus** .</span><span class="sxs-lookup"><span data-stu-id="fdcf3-117">Allocate memory for this structure and call **IRTC::QueryStatus** again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fdcf3-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fdcf3-118">Remarks</span></span>

<span data-ttu-id="fdcf3-119">Se puede llamar a este método en cualquier momento después de llamar al método [CreateNPPInterface](createnppinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="fdcf3-119">This method can be called at any time after the [CreateNPPInterface](createnppinterface.md) method is called.</span></span> <span data-ttu-id="fdcf3-120">Puede llamar a este método para ver si el NPP está conectado a la red, para averiguar el estado de la captura actual y para ver si hay algún desencadenador pendiente.</span><span class="sxs-lookup"><span data-stu-id="fdcf3-120">You can call this method to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span> <span data-ttu-id="fdcf3-121">Sin embargo, antes de llamar a este método, debe asignar la memoria necesaria para la estructura [NETWORKSTATUS](networkstatus.md) y liberar esa memoria cuando la estructura ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="fdcf3-121">Before calling this method, however, you must allocate the memory needed for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdcf3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdcf3-122">Requirements</span></span>



| <span data-ttu-id="fdcf3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdcf3-123">Requirement</span></span> | <span data-ttu-id="fdcf3-124">Value</span><span class="sxs-lookup"><span data-stu-id="fdcf3-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdcf3-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fdcf3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fdcf3-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fdcf3-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="fdcf3-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fdcf3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fdcf3-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fdcf3-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="fdcf3-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fdcf3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdcf3-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdcf3-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="fdcf3-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fdcf3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdcf3-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdcf3-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdcf3-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="fdcf3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdcf3-134">IRTC</span><span class="sxs-lookup"><span data-stu-id="fdcf3-134">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="fdcf3-135">CreateNPPInterface</span><span class="sxs-lookup"><span data-stu-id="fdcf3-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="fdcf3-136">NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="fdcf3-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




