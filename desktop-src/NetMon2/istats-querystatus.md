---
description: 'Método IStats::QueryStatus: el método QueryStatus recupera el estado del NPP.'
ms.assetid: 86b1c1ee-3a35-4603-9e93-fe09f886c32f
title: Método IStats::QueryStatus (Netmon.h)
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
ms.openlocfilehash: 7587c2fff56d305c0298948bdf8690fd801f3f3b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113483"
---
# <a name="istatsquerystatus-method"></a><span data-ttu-id="2678f-103">IStats::QueryStatus (método)</span><span class="sxs-lookup"><span data-stu-id="2678f-103">IStats::QueryStatus method</span></span>

<span data-ttu-id="2678f-104">El **método QueryStatus** recupera el estado del NPP.</span><span class="sxs-lookup"><span data-stu-id="2678f-104">The **QueryStatus** method retrieves the status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="2678f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2678f-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a><span data-ttu-id="2678f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2678f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2678f-107">*pNetworkStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2678f-107">*pNetworkStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2678f-108">Puntero a una estructura [NETWORKSTATUS devuelta](networkstatus.md) que indica el estado actual (captura, pausada, detenida, y así sucesivamente) del NPP.</span><span class="sxs-lookup"><span data-stu-id="2678f-108">Pointer to a returned [NETWORKSTATUS](networkstatus.md) structure that indicates the current state (capturing, paused, stopped, and so on) of the NPP.</span></span> <span data-ttu-id="2678f-109">Es responsabilidad de la aplicación asignar y liberar la memoria para la **estructura NETWORKSTATUS.**</span><span class="sxs-lookup"><span data-stu-id="2678f-109">It is the application's responsibility to allocate and free the memory for the **NETWORKSTATUS** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2678f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2678f-110">Return value</span></span>

<span data-ttu-id="2678f-111">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="2678f-111">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="2678f-112">Si el método no se realiza correctamente, el valor devuelto es el código de error siguiente:</span><span class="sxs-lookup"><span data-stu-id="2678f-112">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="2678f-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2678f-113">Return code</span></span>                                                                                              | <span data-ttu-id="2678f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2678f-114">Description</span></span>                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2678f-115"><dt>**NMERR \_ INVALID \_ PARAMETER**</dt></span><span class="sxs-lookup"><span data-stu-id="2678f-115"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="2678f-116">El *parámetro pNetworkStatus* no apunta a una estructura [NETWORKSTATUS](networkstatus.md) válida.</span><span class="sxs-lookup"><span data-stu-id="2678f-116">The *pNetworkStatus* parameter is not pointing to a valid [NETWORKSTATUS](networkstatus.md) structure.</span></span> <span data-ttu-id="2678f-117">Asigne memoria para esta estructura y llame de nuevo **al método IStats::QueryStatus.**</span><span class="sxs-lookup"><span data-stu-id="2678f-117">Allocate memory for this structure and call the **IStats::QueryStatus** method again.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2678f-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2678f-118">Remarks</span></span>

<span data-ttu-id="2678f-119">Se puede llamar a este método en cualquier momento después de llamar al método [CreateNPPInterface.](createnppinterface.md)</span><span class="sxs-lookup"><span data-stu-id="2678f-119">This method can be called at any time after the [CreateNPPInterface](createnppinterface.md) method is called.</span></span> <span data-ttu-id="2678f-120">Se puede llamar para ver si el NPP está conectado a la red, para averiguar el estado de la captura actual y para ver si hay algún desencadenador pendiente.</span><span class="sxs-lookup"><span data-stu-id="2678f-120">It can be called to see if the NPP is connected to the network, to find out the status of the current capture, and to see if any triggers are pending.</span></span> <span data-ttu-id="2678f-121">Sin embargo, antes de llamar a este método, debe asignar la memoria necesaria para la estructura [NETWORKSTATUS](networkstatus.md) y liberar esa memoria cuando la estructura ya no sea necesaria.</span><span class="sxs-lookup"><span data-stu-id="2678f-121">Before calling this method, however, you must allocate the memory needed for the [NETWORKSTATUS](networkstatus.md) structure and free that memory when the structure is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2678f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2678f-122">Requirements</span></span>



| <span data-ttu-id="2678f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2678f-123">Requirement</span></span> | <span data-ttu-id="2678f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="2678f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2678f-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2678f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2678f-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2678f-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="2678f-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2678f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2678f-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2678f-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="2678f-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2678f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2678f-130"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="2678f-130"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="2678f-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2678f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2678f-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2678f-132"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2678f-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2678f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2678f-134">IStats</span><span class="sxs-lookup"><span data-stu-id="2678f-134">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="2678f-135">CreateNPPInterface</span><span class="sxs-lookup"><span data-stu-id="2678f-135">CreateNPPInterface</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="2678f-136">NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="2678f-136">NETWORKSTATUS</span></span>](networkstatus.md)
</dt> </dl>

 

 




