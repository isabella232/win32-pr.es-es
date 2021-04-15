---
title: IMsTscAxEvents OnAuthenticationWarningDismissed, método
description: Se llama después de que un control ActiveX muestre un cuadro de diálogo de autenticación (por ejemplo, el cuadro de diálogo error de certificado).
ms.assetid: bf5dbe4a-9129-47b3-9808-ed09d9010099
ms.tgt_platform: multiple
keywords:
- Método OnAuthenticationWarningDismissed Servicios de Escritorio remoto
- Método OnAuthenticationWarningDismissed Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnAuthenticationWarningDismissed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDismissed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86bdadfdbc8e0a1387a1f3aaf712188689d0f808
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422274"
---
# <a name="imstscaxeventsonauthenticationwarningdismissed-method"></a><span data-ttu-id="f849f-106">IMsTscAxEvents:: OnAuthenticationWarningDismissed (método)</span><span class="sxs-lookup"><span data-stu-id="f849f-106">IMsTscAxEvents::OnAuthenticationWarningDismissed method</span></span>

<span data-ttu-id="f849f-107">Se llama después de que un control ActiveX muestre un cuadro de diálogo de autenticación (por ejemplo, el cuadro de diálogo error de certificado).</span><span class="sxs-lookup"><span data-stu-id="f849f-107">Called after an ActiveX control displays an authentication dialog box (for example, the certificate error dialog box).</span></span>

## <a name="syntax"></a><span data-ttu-id="f849f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f849f-108">Syntax</span></span>


```C++
void OnAuthenticationWarningDismissed();
```



## <a name="parameters"></a><span data-ttu-id="f849f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f849f-109">Parameters</span></span>

<span data-ttu-id="f849f-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f849f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f849f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f849f-111">Return value</span></span>

<span data-ttu-id="f849f-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f849f-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f849f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f849f-113">Remarks</span></span>

<span data-ttu-id="f849f-114">Si es necesario, se puede usar la propiedad [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) de la interfaz [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) para revertir cualquier elemento primario que pueda haberse realizado en el método [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) .</span><span class="sxs-lookup"><span data-stu-id="f849f-114">If needed, the [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) property of the [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) interface can be used to revert any parenting that may have been done in the [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) method.</span></span>

<span data-ttu-id="f849f-115">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f849f-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f849f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f849f-116">Requirements</span></span>



| <span data-ttu-id="f849f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f849f-117">Requirement</span></span> | <span data-ttu-id="f849f-118">Value</span><span class="sxs-lookup"><span data-stu-id="f849f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f849f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f849f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f849f-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f849f-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f849f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f849f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f849f-122">Windows Server 2008, Windows Server 2008 con SP1</span><span class="sxs-lookup"><span data-stu-id="f849f-122">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="f849f-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f849f-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="f849f-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f849f-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f849f-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f849f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f849f-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f849f-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f849f-127">IID</span><span class="sxs-lookup"><span data-stu-id="f849f-127">IID</span></span><br/>                      | <span data-ttu-id="f849f-128">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="f849f-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="f849f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f849f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f849f-130">**OnAuthenticationWarningDisplayed**</span><span class="sxs-lookup"><span data-stu-id="f849f-130">**OnAuthenticationWarningDisplayed**</span></span>](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[<span data-ttu-id="f849f-131">**UIParentWindowHandle**</span><span class="sxs-lookup"><span data-stu-id="f849f-131">**UIParentWindowHandle**</span></span>](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[<span data-ttu-id="f849f-132">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="f849f-132">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





