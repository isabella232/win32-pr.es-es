---
title: IMsTscAxEvents OnAuthenticationWarningDisplayed, método
description: Se llama antes de que un control ActiveX muestre un cuadro de diálogo de autenticación (por ejemplo, el cuadro de diálogo error de certificado).
ms.assetid: ce307e5f-5e26-4041-bbd5-6871c0678da4
ms.tgt_platform: multiple
keywords:
- Método OnAuthenticationWarningDisplayed Servicios de Escritorio remoto
- Método OnAuthenticationWarningDisplayed Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnAuthenticationWarningDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33307adf103536cce5841effe2843a7c48fda357
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150217"
---
# <a name="imstscaxeventsonauthenticationwarningdisplayed-method"></a><span data-ttu-id="b49a1-106">IMsTscAxEvents:: OnAuthenticationWarningDisplayed (método)</span><span class="sxs-lookup"><span data-stu-id="b49a1-106">IMsTscAxEvents::OnAuthenticationWarningDisplayed method</span></span>

<span data-ttu-id="b49a1-107">Se llama antes de que un control ActiveX muestre un cuadro de diálogo de autenticación (por ejemplo, el cuadro de diálogo error de certificado).</span><span class="sxs-lookup"><span data-stu-id="b49a1-107">Called before an ActiveX control displays an authentication dialog box (for example, the certificate error dialog box).</span></span>

## <a name="syntax"></a><span data-ttu-id="b49a1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b49a1-108">Syntax</span></span>


```C++
void OnAuthenticationWarningDisplayed();
```



## <a name="parameters"></a><span data-ttu-id="b49a1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b49a1-109">Parameters</span></span>

<span data-ttu-id="b49a1-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b49a1-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b49a1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b49a1-111">Return value</span></span>

<span data-ttu-id="b49a1-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b49a1-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b49a1-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b49a1-113">Remarks</span></span>

<span data-ttu-id="b49a1-114">Si es necesario, se puede usar la propiedad [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) de la interfaz [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) para asegurarse de que el cuadro de diálogo de autenticación modal se muestre en una ventana determinada (esto puede ser necesario para evitar que los usuarios usen otros cuadros de diálogo mientras se muestra el cuadro de diálogo de autenticación).</span><span class="sxs-lookup"><span data-stu-id="b49a1-114">If needed, the [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) property of the [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) interface can be used to ensure that the modal authentication dialog to be displayed will be parented by a specified window (this may be necessary to prevent users from using other dialog boxes while the authentication dialog box is displayed).</span></span> <span data-ttu-id="b49a1-115">De forma predeterminada, el elemento primario es la ventana de control ActiveX.</span><span class="sxs-lookup"><span data-stu-id="b49a1-115">By default, the parent is the ActiveX control window.</span></span>

<span data-ttu-id="b49a1-116">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b49a1-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b49a1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b49a1-117">Requirements</span></span>



| <span data-ttu-id="b49a1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b49a1-118">Requirement</span></span> | <span data-ttu-id="b49a1-119">Value</span><span class="sxs-lookup"><span data-stu-id="b49a1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b49a1-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b49a1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b49a1-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b49a1-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b49a1-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b49a1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b49a1-123">Windows Server 2008, Windows Server 2008 con SP1</span><span class="sxs-lookup"><span data-stu-id="b49a1-123">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="b49a1-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b49a1-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="b49a1-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b49a1-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b49a1-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b49a1-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b49a1-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b49a1-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b49a1-128">IID</span><span class="sxs-lookup"><span data-stu-id="b49a1-128">IID</span></span><br/>                      | <span data-ttu-id="b49a1-129">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="b49a1-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="b49a1-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="b49a1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b49a1-131">**OnAuthenticationWarningDismissed**</span><span class="sxs-lookup"><span data-stu-id="b49a1-131">**OnAuthenticationWarningDismissed**</span></span>](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[<span data-ttu-id="b49a1-132">**UIParentWindowHandle**</span><span class="sxs-lookup"><span data-stu-id="b49a1-132">**UIParentWindowHandle**</span></span>](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[<span data-ttu-id="b49a1-133">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="b49a1-133">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





