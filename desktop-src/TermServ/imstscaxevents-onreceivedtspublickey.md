---
title: IMsTscAxEvents OnReceivedTSPublicKey, método
description: Se llama durante la secuencia de conexión cuando el cliente recupera la clave pública del servidor. Solo se llama a este evento si la propiedad NotifyTSPublicKey es VARIANT \_ true.
ms.assetid: 1db98b8b-2f08-4252-ad8b-6764fa25b300
ms.tgt_platform: multiple
keywords:
- Método OnReceivedTSPublicKey Servicios de Escritorio remoto
- Método OnReceivedTSPublicKey Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnReceivedTSPublicKey
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnReceivedTSPublicKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 337a9efabe48dee7a5a4194c3b796b95f35a0592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491326"
---
# <a name="imstscaxeventsonreceivedtspublickey-method"></a><span data-ttu-id="5d806-107">IMsTscAxEvents:: OnReceivedTSPublicKey (método)</span><span class="sxs-lookup"><span data-stu-id="5d806-107">IMsTscAxEvents::OnReceivedTSPublicKey method</span></span>

<span data-ttu-id="5d806-108">Se llama durante la secuencia de conexión cuando el cliente recupera la clave pública del servidor.</span><span class="sxs-lookup"><span data-stu-id="5d806-108">Called during the connection sequence when the client retrieves the public key from the server.</span></span> <span data-ttu-id="5d806-109">Solo se llama a este evento si la propiedad **NotifyTSPublicKey** es **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="5d806-109">This event is only called if the **NotifyTSPublicKey** property is **VARIANT\_TRUE**.</span></span> <span data-ttu-id="5d806-110">Esto es después de la [**conexión**](imstscaxevents-onconnecting.md), pero antes de [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) y de la [**conexión**](imstscaxevents-onconnected.md).</span><span class="sxs-lookup"><span data-stu-id="5d806-110">This is after [**OnConnecting**](imstscaxevents-onconnecting.md), but before [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) and [**OnConnected**](imstscaxevents-onconnected.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5d806-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d806-111">Syntax</span></span>


```C++
void OnReceivedTSPublicKey(
  [in]  BSTR         publicKey,
  [out] VARIANT_BOOL *pfContinueLogon
);
```



## <a name="parameters"></a><span data-ttu-id="5d806-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d806-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d806-113">*publicKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5d806-113">*publicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d806-114">Contiene la clave pública del equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="5d806-114">Contains the public key of the remote machine.</span></span>

</dd> <dt>

<span data-ttu-id="5d806-115">*pfContinueLogon* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5d806-115">*pfContinueLogon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d806-116">Un puntero a una variable de **tipo \_ bool** que recibe si el proceso de inicio de sesión debe continuar.</span><span class="sxs-lookup"><span data-stu-id="5d806-116">A pointer to a **VARIANT\_BOOL** variable that receives whether the logon process should continue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d806-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d806-117">Return value</span></span>

<span data-ttu-id="5d806-118">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5d806-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d806-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d806-119">Remarks</span></span>

<span data-ttu-id="5d806-120">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="5d806-120">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d806-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d806-121">Requirements</span></span>



| <span data-ttu-id="5d806-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d806-122">Requirement</span></span> | <span data-ttu-id="5d806-123">Value</span><span class="sxs-lookup"><span data-stu-id="5d806-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d806-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d806-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5d806-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d806-125">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5d806-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d806-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5d806-127">Windows Server 2008, Windows Server 2008 con SP1</span><span class="sxs-lookup"><span data-stu-id="5d806-127">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="5d806-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5d806-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="5d806-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d806-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5d806-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5d806-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d806-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d806-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5d806-132">IID</span><span class="sxs-lookup"><span data-stu-id="5d806-132">IID</span></span><br/>                      | <span data-ttu-id="5d806-133">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="5d806-133">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="5d806-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d806-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d806-135">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="5d806-135">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





