---
title: IMsTscAxEvents OnRemoteWindowDisplayed, método
description: Se le llama cuando se muestra una ventana de RemoteApp.
ms.assetid: B1E83486-50CB-4CA4-BD01-2C72938335AF
ms.tgt_platform: multiple
keywords:
- Método OnRemoteWindowDisplayed Servicios de Escritorio remoto
- Método OnRemoteWindowDisplayed Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnRemoteWindowDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteWindowDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f03029f31e1ce2133c74c92c0d6d57f192e4d85f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422424"
---
# <a name="imstscaxeventsonremotewindowdisplayed-method"></a><span data-ttu-id="22dde-106">IMsTscAxEvents:: OnRemoteWindowDisplayed (método)</span><span class="sxs-lookup"><span data-stu-id="22dde-106">IMsTscAxEvents::OnRemoteWindowDisplayed method</span></span>

<span data-ttu-id="22dde-107">Se le llama cuando se muestra una ventana de RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="22dde-107">Called when a RemoteApp window is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="22dde-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22dde-108">Syntax</span></span>


```C++
void OnRemoteWindowDisplayed(
  [in] VARIANT_BOOL                   vbDisplayed,
  [in] HWND                           hwnd,
  [in] RemoteWindowDisplayedAttribute windowAttribute
);
```



## <a name="parameters"></a><span data-ttu-id="22dde-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22dde-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22dde-110">*vbDisplayed* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="22dde-110">*vbDisplayed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22dde-111">Tipo: **variante \_ bool**</span><span class="sxs-lookup"><span data-stu-id="22dde-111">Type: **VARIANT\_BOOL**</span></span>

<span data-ttu-id="22dde-112">Indica si la ventana de RemoteApp se muestra u oculta.</span><span class="sxs-lookup"><span data-stu-id="22dde-112">Indicates whether the RemoteApp window is displayed or hidden.</span></span>

</dd> <dt>

<span data-ttu-id="22dde-113">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="22dde-113">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22dde-114">Tipo: **hWnd**</span><span class="sxs-lookup"><span data-stu-id="22dde-114">Type: **HWND**</span></span>

<span data-ttu-id="22dde-115">Identificador de la ventana que se muestra.</span><span class="sxs-lookup"><span data-stu-id="22dde-115">The handle of the window displayed.</span></span>

</dd> <dt>

<span data-ttu-id="22dde-116">*windowAttribute* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="22dde-116">*windowAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22dde-117">Tipo: **[ **RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)**</span><span class="sxs-lookup"><span data-stu-id="22dde-117">Type: **[**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)**</span></span>

<span data-ttu-id="22dde-118">Un valor de la enumeración [**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md) que especifica más información sobre el evento.</span><span class="sxs-lookup"><span data-stu-id="22dde-118">A value of the [**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md) enumeration that specifies more information about the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22dde-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22dde-119">Return value</span></span>

<span data-ttu-id="22dde-120">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="22dde-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="22dde-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22dde-121">Requirements</span></span>



| <span data-ttu-id="22dde-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="22dde-122">Requirement</span></span> | <span data-ttu-id="22dde-123">Value</span><span class="sxs-lookup"><span data-stu-id="22dde-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22dde-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22dde-124">Minimum supported client</span></span><br/> | <span data-ttu-id="22dde-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="22dde-125">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="22dde-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22dde-126">Minimum supported server</span></span><br/> | <span data-ttu-id="22dde-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="22dde-127">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="22dde-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="22dde-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="22dde-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22dde-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="22dde-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="22dde-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22dde-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22dde-131"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22dde-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="22dde-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22dde-133">**RemoteWindowDisplayedAttribute**</span><span class="sxs-lookup"><span data-stu-id="22dde-133">**RemoteWindowDisplayedAttribute**</span></span>](remotewindowdisplayedattribute.md)
</dt> <dt>

[<span data-ttu-id="22dde-134">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="22dde-134">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





