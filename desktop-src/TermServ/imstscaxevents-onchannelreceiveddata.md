---
title: IMsTscAxEvents OnChannelReceivedData, método
description: Se llama cuando el cliente recibe datos en un canal virtual que admite scripts.
ms.assetid: 38e6c33c-6a79-4760-818e-445e33d8e0ec
ms.tgt_platform: multiple
keywords:
- Método OnChannelReceivedData Servicios de Escritorio remoto
- Método OnChannelReceivedData Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnChannelReceivedData
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnChannelReceivedData
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1cae4f35435138e219c628dd504c595939adfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150215"
---
# <a name="imstscaxeventsonchannelreceiveddata-method"></a><span data-ttu-id="0f741-106">IMsTscAxEvents:: OnChannelReceivedData (método)</span><span class="sxs-lookup"><span data-stu-id="0f741-106">IMsTscAxEvents::OnChannelReceivedData method</span></span>

<span data-ttu-id="0f741-107">Se llama cuando el cliente recibe datos en un canal virtual que admite scripts.</span><span class="sxs-lookup"><span data-stu-id="0f741-107">Called when the client receives data on a scriptable virtual channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f741-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f741-108">Syntax</span></span>


```C++
void OnChannelReceivedData(
  [in] BSTR chanName,
  [in] BSTR data
);
```



## <a name="parameters"></a><span data-ttu-id="0f741-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f741-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f741-110">*chanName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0f741-110">*chanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f741-111">Nombre del canal virtual en el que se recibieron los datos.</span><span class="sxs-lookup"><span data-stu-id="0f741-111">The name of the virtual channel on which data was received.</span></span> <span data-ttu-id="0f741-112">Este nombre coincide con uno de los canales creados por la llamada a [**IMsTscAx:: CreateVirtualChannels**](imstscax-createvirtualchannels.md).</span><span class="sxs-lookup"><span data-stu-id="0f741-112">This name matches one of the channels created by the call to [**IMsTscAx::CreateVirtualChannels**](imstscax-createvirtualchannels.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f741-113">*datos* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0f741-113">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f741-114">Los datos recibidos en el canal virtual con scripts.</span><span class="sxs-lookup"><span data-stu-id="0f741-114">The data received on the scriptable virtual channel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f741-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f741-115">Return value</span></span>

<span data-ttu-id="0f741-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0f741-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f741-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f741-117">Remarks</span></span>

<span data-ttu-id="0f741-118">Consulte [implementación de canales virtuales con scripts mediante conexión web a escritorio remoto](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) para obtener más información sobre este evento.</span><span class="sxs-lookup"><span data-stu-id="0f741-118">Refer to [Implementing Scriptable Virtual Channels using Remote Desktop Web Connection](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) for more information about this event.</span></span>

<span data-ttu-id="0f741-119">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0f741-119">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f741-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f741-120">Requirements</span></span>



| <span data-ttu-id="0f741-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f741-121">Requirement</span></span> | <span data-ttu-id="0f741-122">Value</span><span class="sxs-lookup"><span data-stu-id="0f741-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f741-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f741-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0f741-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f741-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0f741-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f741-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0f741-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f741-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0f741-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0f741-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="0f741-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f741-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0f741-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0f741-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f741-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f741-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0f741-131">IID</span><span class="sxs-lookup"><span data-stu-id="0f741-131">IID</span></span><br/>                      | <span data-ttu-id="0f741-132">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="0f741-132">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="0f741-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f741-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f741-134">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="0f741-134">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





