---
title: IMsTscAxEvents OnRemoteProgramDisplayed, método
description: Se le llama cuando se muestra un programa RemoteApp.
ms.assetid: 24f5ea52-0c13-4024-9448-5c2c1896ca8b
ms.tgt_platform: multiple
keywords:
- Método OnRemoteProgramDisplayed Servicios de Escritorio remoto
- Método OnRemoteProgramDisplayed Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnRemoteProgramDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 584e54c487ec24a3c165fdd5eb8e22f243e07f23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802732"
---
# <a name="imstscaxeventsonremoteprogramdisplayed-method"></a><span data-ttu-id="e17bf-106">IMsTscAxEvents:: OnRemoteProgramDisplayed (método)</span><span class="sxs-lookup"><span data-stu-id="e17bf-106">IMsTscAxEvents::OnRemoteProgramDisplayed method</span></span>

<span data-ttu-id="e17bf-107">Se le llama cuando se muestra un programa RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e17bf-107">Called when a RemoteApp program is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e17bf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e17bf-108">Syntax</span></span>


```C++
VOID OnRemoteProgramDisplayed(
  [in] VARIANT_BOOL vbDisplayed,
  [in] ULONG        uDisplayInformation
);
```



## <a name="parameters"></a><span data-ttu-id="e17bf-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e17bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e17bf-110">*vbDisplayed* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e17bf-110">*vbDisplayed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e17bf-111">Indica si se muestra u oculta el programa RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e17bf-111">Indicates whether the RemoteApp program is displayed or hidden.</span></span>

</dd> <dt>

<span data-ttu-id="e17bf-112">*uDisplayInformation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e17bf-112">*uDisplayInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e17bf-113">Información de presentación.</span><span class="sxs-lookup"><span data-stu-id="e17bf-113">The display information.</span></span>

<dt>

<span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>

<span data-ttu-id="e17bf-114"><span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>**RAÍL \_ APPDISPLAY \_ reconexión automática**</span><span class="sxs-lookup"><span data-stu-id="e17bf-114"><span id="RAIL_APPDISPLAY_AUTORECONNECT"></span><span id="rail_appdisplay_autoreconnect"></span>**RAIL\_APPDISPLAY\_AUTORECONNECT**</span></span>


</dt> <dd>

<span data-ttu-id="e17bf-115">La reconexión automática está en curso.</span><span class="sxs-lookup"><span data-stu-id="e17bf-115">Automatic reconnect is in progress.</span></span>

</dd> <dt>

<span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>

<span data-ttu-id="e17bf-116"><span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>**RAÍL \_ APPDISPLAY \_ DESKTOPHOOKED**</span><span class="sxs-lookup"><span data-stu-id="e17bf-116"><span id="RAIL_APPDISPLAY_DESKTOPHOOKED"></span><span id="rail_appdisplay_desktophooked"></span>**RAIL\_APPDISPLAY\_DESKTOPHOOKED**</span></span>


</dt> <dd>

<span data-ttu-id="e17bf-117">El número de RemoteApp llegó a cero.</span><span class="sxs-lookup"><span data-stu-id="e17bf-117">The RemoteApp count just went to zero.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e17bf-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e17bf-118">Return value</span></span>

<span data-ttu-id="e17bf-119">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e17bf-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e17bf-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e17bf-120">Remarks</span></span>

<span data-ttu-id="e17bf-121">Implemente este método en el receptor de eventos para recibir la notificación de que se ha mostrado una RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e17bf-121">Implement this method in your event sink to receive notification that a RemoteApp has been displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e17bf-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e17bf-122">Requirements</span></span>



| <span data-ttu-id="e17bf-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e17bf-123">Requirement</span></span> | <span data-ttu-id="e17bf-124">Value</span><span class="sxs-lookup"><span data-stu-id="e17bf-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e17bf-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e17bf-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e17bf-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e17bf-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e17bf-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e17bf-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e17bf-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e17bf-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e17bf-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e17bf-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="e17bf-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e17bf-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e17bf-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e17bf-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e17bf-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e17bf-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e17bf-133">IID</span><span class="sxs-lookup"><span data-stu-id="e17bf-133">IID</span></span><br/>                      | <span data-ttu-id="e17bf-134">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="e17bf-134">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



 

 





