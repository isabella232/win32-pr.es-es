---
title: IRemoteDesktopClientEvents OnTouchPointerCursorMoved, método
description: Se llama cuando se ha cambiado el cursor del puntero táctil y la propiedad EventsEnabled está establecida en true.
ms.assetid: 55A6AC99-0723-4215-9428-D2DAAC77A74A
ms.tgt_platform: multiple
keywords:
- Método OnTouchPointerCursorMoved Servicios de Escritorio remoto
- Método OnTouchPointerCursorMoved Servicios de Escritorio remoto, interfaz IRemoteDesktopClientEvents
- Interfaz IRemoteDesktopClientEvents Servicios de Escritorio remoto, método OnTouchPointerCursorMoved
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnTouchPointerCursorMoved
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae347e19942bf0c82112e5cec6a3fb4fe131349f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676757"
---
# <a name="iremotedesktopclienteventsontouchpointercursormoved-method"></a><span data-ttu-id="25828-106">IRemoteDesktopClientEvents:: OnTouchPointerCursorMoved (método)</span><span class="sxs-lookup"><span data-stu-id="25828-106">IRemoteDesktopClientEvents::OnTouchPointerCursorMoved method</span></span>

<span data-ttu-id="25828-107">Se llama cuando se ha cambiado el cursor del puntero táctil y la propiedad [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) está establecida en true.</span><span class="sxs-lookup"><span data-stu-id="25828-107">Called when the touch pointer cursor has moved and the [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) property is set to true.</span></span>

## <a name="syntax"></a><span data-ttu-id="25828-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25828-108">Syntax</span></span>


```C++
void OnTouchPointerCursorMoved(
  [in] long x,
  [in] long y
);
```



## <a name="parameters"></a><span data-ttu-id="25828-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25828-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25828-110">*x* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="25828-110">*x* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="25828-111">*y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="25828-111">*y* \[in\]</span></span>
<span data-ttu-id="25828-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="25828-112"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="25828-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25828-113">Return value</span></span>

<span data-ttu-id="25828-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="25828-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="25828-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25828-115">Requirements</span></span>



| <span data-ttu-id="25828-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="25828-116">Requirement</span></span> | <span data-ttu-id="25828-117">Value</span><span class="sxs-lookup"><span data-stu-id="25828-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25828-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25828-118">Minimum supported client</span></span><br/> | <span data-ttu-id="25828-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="25828-119">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="25828-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25828-120">Minimum supported server</span></span><br/> | <span data-ttu-id="25828-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="25828-121">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="25828-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="25828-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="25828-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25828-123"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="25828-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="25828-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25828-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25828-125"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="25828-126">IID</span><span class="sxs-lookup"><span data-stu-id="25828-126">IID</span></span><br/>                      | <span data-ttu-id="25828-127">DIID \_ IRemoteDesktopClientEvents se define como 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="25828-127">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="25828-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="25828-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25828-129">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="25828-129">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

