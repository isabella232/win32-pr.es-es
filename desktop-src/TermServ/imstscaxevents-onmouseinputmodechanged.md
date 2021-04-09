---
title: IMsTscAxEvents OnMouseInputModeChanged, método
description: Se le llama cuando cambia el modo de entrada del mouse.
ms.assetid: d0554c59-967d-4181-98cd-9e88dde32752
ms.tgt_platform: multiple
keywords:
- Método OnMouseInputModeChanged Servicios de Escritorio remoto
- Método OnMouseInputModeChanged Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnMouseInputModeChanged
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnMouseInputModeChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dbfef19aa79ba634a13d92b8d11866b8016e893
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150499"
---
# <a name="imstscaxeventsonmouseinputmodechanged-method"></a><span data-ttu-id="b6741-106">IMsTscAxEvents:: OnMouseInputModeChanged (método)</span><span class="sxs-lookup"><span data-stu-id="b6741-106">IMsTscAxEvents::OnMouseInputModeChanged method</span></span>

<span data-ttu-id="b6741-107">Se le llama cuando cambia el modo de entrada del mouse.</span><span class="sxs-lookup"><span data-stu-id="b6741-107">Called when the mouse input mode has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6741-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6741-108">Syntax</span></span>


```C++
void OnMouseInputModeChanged(
  [in] VARIANT_BOOL fMouseModeRelative
);
```



## <a name="parameters"></a><span data-ttu-id="b6741-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6741-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6741-110">*fMouseModeRelative* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b6741-110">*fMouseModeRelative* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6741-111">Indica si el mouse está en modo relativo.</span><span class="sxs-lookup"><span data-stu-id="b6741-111">Indicates whether the mouse is in relative mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6741-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6741-112">Return value</span></span>

<span data-ttu-id="b6741-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b6741-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6741-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6741-114">Remarks</span></span>

<span data-ttu-id="b6741-115">Implemente este método en el receptor de eventos para recibir la notificación de que el modo de entrada del mouse ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="b6741-115">Implement this method in your event sink to receive notification that the mouse input mode has changed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6741-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6741-116">Requirements</span></span>



| <span data-ttu-id="b6741-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6741-117">Requirement</span></span> | <span data-ttu-id="b6741-118">Value</span><span class="sxs-lookup"><span data-stu-id="b6741-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6741-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6741-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b6741-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6741-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b6741-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6741-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b6741-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6741-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b6741-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b6741-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="b6741-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6741-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b6741-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b6741-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6741-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6741-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b6741-127">IID</span><span class="sxs-lookup"><span data-stu-id="b6741-127">IID</span></span><br/>                      | <span data-ttu-id="b6741-128">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="b6741-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="b6741-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6741-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6741-130">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="b6741-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





