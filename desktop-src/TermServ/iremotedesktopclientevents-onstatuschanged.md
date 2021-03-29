---
title: Método IRemoteDesktopClientEvents OnStatusChanged (Locationapi. h)
description: Se llama cuando el control de cliente ha actualizado su estado.
ms.assetid: AAFBDC9E-C8B5-4924-AA69-82EF09996AF7
ms.tgt_platform: multiple
keywords:
- Método OnStatusChanged Servicios de Escritorio remoto
- Método OnStatusChanged Servicios de Escritorio remoto, interfaz IRemoteDesktopClientEvents
- Interfaz IRemoteDesktopClientEvents Servicios de Escritorio remoto, método OnStatusChanged
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b17e42e75072033f952c7ef790365d6a363a5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492772"
---
# <a name="iremotedesktopclienteventsonstatuschanged-method"></a><span data-ttu-id="5b137-106">IRemoteDesktopClientEvents:: OnStatusChanged (método)</span><span class="sxs-lookup"><span data-stu-id="5b137-106">IRemoteDesktopClientEvents::OnStatusChanged method</span></span>

<span data-ttu-id="5b137-107">Se llama cuando el control de cliente ha actualizado su estado.</span><span class="sxs-lookup"><span data-stu-id="5b137-107">Called when the client control has updated its status.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b137-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b137-108">Syntax</span></span>


```C++
void OnStatusChanged(
   long statusCode,
   BSTR statusMessage
);
```



## <a name="parameters"></a><span data-ttu-id="5b137-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b137-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b137-110">*statusCode*</span><span class="sxs-lookup"><span data-stu-id="5b137-110">*statusCode*</span></span> 
</dt> <dd>

<span data-ttu-id="5b137-111">El nuevo código de estado.</span><span class="sxs-lookup"><span data-stu-id="5b137-111">The new status code.</span></span>

</dd> <dt>

<span data-ttu-id="5b137-112">*statusMessage*</span><span class="sxs-lookup"><span data-stu-id="5b137-112">*statusMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="5b137-113">El texto del mensaje de estado.</span><span class="sxs-lookup"><span data-stu-id="5b137-113">The status message text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b137-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b137-114">Return value</span></span>

<span data-ttu-id="5b137-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5b137-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b137-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b137-116">Requirements</span></span>



| <span data-ttu-id="5b137-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b137-117">Requirement</span></span> | <span data-ttu-id="5b137-118">Value</span><span class="sxs-lookup"><span data-stu-id="5b137-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b137-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b137-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5b137-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5b137-120">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="5b137-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b137-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5b137-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5b137-122">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="5b137-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b137-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b137-124"><dt>Locationapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b137-124"><dt>Locationapi.h</dt></span></span> </dl>       |
| <span data-ttu-id="5b137-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5b137-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="5b137-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b137-126"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="5b137-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5b137-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b137-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b137-128"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="5b137-129">IID</span><span class="sxs-lookup"><span data-stu-id="5b137-129">IID</span></span><br/>                      | <span data-ttu-id="5b137-130">DIID \_ IRemoteDesktopClientEvents se define como 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="5b137-130">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5b137-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b137-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b137-132">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="5b137-132">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





