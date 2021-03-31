---
title: IRemoteDesktopClientEvents OnRemoteDesktopSizeChanged, método
description: Se llama cuando el tamaño del escritorio remoto ha cambiado.
ms.assetid: DA641CA7-3214-4DB6-9A7F-75903FE93DB4
ms.tgt_platform: multiple
keywords:
- Método OnRemoteDesktopSizeChanged Servicios de Escritorio remoto
- Método OnRemoteDesktopSizeChanged Servicios de Escritorio remoto, interfaz IRemoteDesktopClientEvents
- Interfaz IRemoteDesktopClientEvents Servicios de Escritorio remoto, método OnRemoteDesktopSizeChanged
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnRemoteDesktopSizeChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7431d1a6f41a6f87bb34fe1486c203168f2c3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802138"
---
# <a name="iremotedesktopclienteventsonremotedesktopsizechanged-method"></a><span data-ttu-id="ee22f-106">IRemoteDesktopClientEvents:: OnRemoteDesktopSizeChanged (método)</span><span class="sxs-lookup"><span data-stu-id="ee22f-106">IRemoteDesktopClientEvents::OnRemoteDesktopSizeChanged method</span></span>

<span data-ttu-id="ee22f-107">Se llama cuando el tamaño del escritorio remoto ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="ee22f-107">Called when the remote desktop size has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee22f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee22f-108">Syntax</span></span>


```C++
void OnRemoteDesktopSizeChanged(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a><span data-ttu-id="ee22f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee22f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee22f-110">*ancho* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ee22f-110">*width* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="ee22f-111">*alto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ee22f-111">*height* \[in\]</span></span>
<span data-ttu-id="ee22f-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ee22f-112"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="ee22f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee22f-113">Return value</span></span>

<span data-ttu-id="ee22f-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ee22f-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee22f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee22f-115">Requirements</span></span>



| <span data-ttu-id="ee22f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee22f-116">Requirement</span></span> | <span data-ttu-id="ee22f-117">Value</span><span class="sxs-lookup"><span data-stu-id="ee22f-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee22f-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee22f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ee22f-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ee22f-119">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="ee22f-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee22f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ee22f-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ee22f-121">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="ee22f-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ee22f-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="ee22f-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee22f-123"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="ee22f-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ee22f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee22f-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee22f-125"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="ee22f-126">IID</span><span class="sxs-lookup"><span data-stu-id="ee22f-126">IID</span></span><br/>                      | <span data-ttu-id="ee22f-127">DIID \_ IRemoteDesktopClientEvents se define como 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="ee22f-127">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee22f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee22f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee22f-129">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="ee22f-129">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





