---
title: IMsTscAxEvents OnFocusReleased, método
description: Se le llama cuando se presiona la combinación de teclas de foco de versión. Por ejemplo, se llama a este evento cuando el usuario presiona las teclas CTRL + ALT + Flecha izquierda o CTRL + ALT + Flecha derecha.
ms.assetid: f5d755b0-4b8f-4d62-8dc4-f6b63e3819e5
ms.tgt_platform: multiple
keywords:
- Método OnFocusReleased Servicios de Escritorio remoto
- Método OnFocusReleased Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnFocusReleased
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFocusReleased
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eff03f95d4ebbb068bccbfd9f68a930c00f0b00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686022"
---
# <a name="imstscaxeventsonfocusreleased-method"></a><span data-ttu-id="68dc2-107">IMsTscAxEvents:: OnFocusReleased (método)</span><span class="sxs-lookup"><span data-stu-id="68dc2-107">IMsTscAxEvents::OnFocusReleased method</span></span>

<span data-ttu-id="68dc2-108">Se le llama cuando se presiona la combinación de teclas de foco de versión.</span><span class="sxs-lookup"><span data-stu-id="68dc2-108">Called when the release focus key combination is pressed.</span></span> <span data-ttu-id="68dc2-109">Por ejemplo, se llama a este evento cuando el usuario presiona las teclas CTRL + ALT + Flecha izquierda o CTRL + ALT + Flecha derecha.</span><span class="sxs-lookup"><span data-stu-id="68dc2-109">For example, this event is called when the user presses the CTRL+ALT+LEFT ARROW or the CTRL+ALT+RIGHT ARROW key combination.</span></span>

<span data-ttu-id="68dc2-110">Este evento permite al contenedor de controles ActiveX quitar el control del control ActiveX.</span><span class="sxs-lookup"><span data-stu-id="68dc2-110">This event enables the ActiveX control container to take away control from the ActiveX control.</span></span> <span data-ttu-id="68dc2-111">Por ejemplo, esto es útil en un escenario en el que no hay un mouse, y las combinaciones de teclas especiales, como ALT + TAB, se redirigen al servidor.</span><span class="sxs-lookup"><span data-stu-id="68dc2-111">For example, this is useful in a scenario where you do not have a mouse, and special key combinations such as ALT+TAB are being redirected to the server.</span></span> <span data-ttu-id="68dc2-112">En este caso, no tiene una manera de devolver el foco de teclado al escritorio local.</span><span class="sxs-lookup"><span data-stu-id="68dc2-112">In this case, you do not have a way to return the keyboard focus back to the local desktop.</span></span> <span data-ttu-id="68dc2-113">Sin embargo, con la combinación de teclas CTRL + ALT + Flecha izquierda o CTRL + ALT + Flecha derecha, el contenedor ActiveX puede realizar escuchas para este evento y responder tomando el foco fuera del control ActiveX.</span><span class="sxs-lookup"><span data-stu-id="68dc2-113">However, with the CTRL+ALT+LEFT ARROW or the CTRL+ALT+RIGHT ARROW key combination, the ActiveX container can listen for this event and respond by taking focus away from the ActiveX control.</span></span>

## <a name="syntax"></a><span data-ttu-id="68dc2-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68dc2-114">Syntax</span></span>


```C++
void OnFocusReleased(
  [in] INT iDirection
);
```



## <a name="parameters"></a><span data-ttu-id="68dc2-115">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68dc2-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68dc2-116">*iDirection* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="68dc2-116">*iDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68dc2-117">El parámetro Direction de 1 (CTRL + ALT + Flecha derecha) o 1 (CTRL + ALT + Flecha izquierda).</span><span class="sxs-lookup"><span data-stu-id="68dc2-117">The direction parameter of 1 (CTRL+ALT+RIGHT ARROW) or  1 (CTRL+ALT+LEFT ARROW).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68dc2-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68dc2-118">Return value</span></span>

<span data-ttu-id="68dc2-119">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="68dc2-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68dc2-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68dc2-120">Remarks</span></span>

<span data-ttu-id="68dc2-121">Este evento está disponible cuando se utiliza Conexión a Escritorio remoto 6,0 en el cliente.</span><span class="sxs-lookup"><span data-stu-id="68dc2-121">This event is available when Remote Desktop Connection 6.0 is used on the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="68dc2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68dc2-122">Requirements</span></span>



| <span data-ttu-id="68dc2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="68dc2-123">Requirement</span></span> | <span data-ttu-id="68dc2-124">Value</span><span class="sxs-lookup"><span data-stu-id="68dc2-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68dc2-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68dc2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="68dc2-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68dc2-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="68dc2-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68dc2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="68dc2-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68dc2-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="68dc2-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="68dc2-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="68dc2-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68dc2-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="68dc2-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68dc2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68dc2-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68dc2-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="68dc2-133">IID</span><span class="sxs-lookup"><span data-stu-id="68dc2-133">IID</span></span><br/>                      | <span data-ttu-id="68dc2-134">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="68dc2-134">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="68dc2-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="68dc2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68dc2-136">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="68dc2-136">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





