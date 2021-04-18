---
title: IRemoteDesktopClientEvents OnAdminMessageReceived, método
description: Se llama cuando el control de cliente recibe un mensaje administrativo.
ms.assetid: CD580207-CEC1-493B-989E-7C1D4FA71228
ms.tgt_platform: multiple
keywords:
- Método OnAdminMessageReceived Servicios de Escritorio remoto
- Método OnAdminMessageReceived Servicios de Escritorio remoto, interfaz IRemoteDesktopClientEvents
- Interfaz IRemoteDesktopClientEvents Servicios de Escritorio remoto, método OnAdminMessageReceived
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAdminMessageReceived
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 201dd3111dbac0b6395654ef8dfad21318419de3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422472"
---
# <a name="iremotedesktopclienteventsonadminmessagereceived-method"></a><span data-ttu-id="24fae-106">IRemoteDesktopClientEvents:: OnAdminMessageReceived (método)</span><span class="sxs-lookup"><span data-stu-id="24fae-106">IRemoteDesktopClientEvents::OnAdminMessageReceived method</span></span>

<span data-ttu-id="24fae-107">Se llama cuando el control de cliente recibe un mensaje administrativo.</span><span class="sxs-lookup"><span data-stu-id="24fae-107">Called when the client control receives an administrative message.</span></span>

## <a name="syntax"></a><span data-ttu-id="24fae-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24fae-108">Syntax</span></span>


```C++
void OnAdminMessageReceived(
  [in] BSTR adminMessage
);
```



## <a name="parameters"></a><span data-ttu-id="24fae-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24fae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24fae-110">*adminMessage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="24fae-110">*adminMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24fae-111">Mensaje.</span><span class="sxs-lookup"><span data-stu-id="24fae-111">The message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24fae-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24fae-112">Return value</span></span>

<span data-ttu-id="24fae-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="24fae-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="24fae-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24fae-114">Requirements</span></span>



| <span data-ttu-id="24fae-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="24fae-115">Requirement</span></span> | <span data-ttu-id="24fae-116">Value</span><span class="sxs-lookup"><span data-stu-id="24fae-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24fae-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24fae-117">Minimum supported client</span></span><br/> | <span data-ttu-id="24fae-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="24fae-118">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="24fae-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24fae-119">Minimum supported server</span></span><br/> | <span data-ttu-id="24fae-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="24fae-120">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="24fae-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="24fae-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="24fae-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24fae-122"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="24fae-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="24fae-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24fae-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24fae-124"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="24fae-125">IID</span><span class="sxs-lookup"><span data-stu-id="24fae-125">IID</span></span><br/>                      | <span data-ttu-id="24fae-126">DIID \_ IRemoteDesktopClientEvents se define como 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="24fae-126">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="24fae-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="24fae-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24fae-128">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="24fae-128">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





