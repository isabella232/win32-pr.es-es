---
title: IMsRdpClient8 SendRemoteAction, método
description: Hace que se realice una acción en la sesión remota.
ms.assetid: d6a43662-7e51-404a-a3f9-a8b51cbc69d1
ms.tgt_platform: multiple
keywords:
- Método SendRemoteAction Servicios de Escritorio remoto
- Método SendRemoteAction Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto, método SendRemoteAction
- Método SendRemoteAction Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, método SendRemoteAction
- Método SendRemoteAction Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto, método SendRemoteAction
topic_type:
- apiref
api_name:
- IMsRdpClient8.SendRemoteAction
- IMsRdpClient9.SendRemoteAction
- IMsRdpClient10.SendRemoteAction
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a28fc9695686402e0a8e98ed17fc1bc6a47939d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493193"
---
# <a name="imsrdpclient8sendremoteaction-method"></a><span data-ttu-id="c5088-110">IMsRdpClient8:: SendRemoteAction (método)</span><span class="sxs-lookup"><span data-stu-id="c5088-110">IMsRdpClient8::SendRemoteAction method</span></span>

<span data-ttu-id="c5088-111">Hace que se realice una acción en la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="c5088-111">Causes an action to be performed in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5088-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5088-112">Syntax</span></span>


```C++
HRESULT SendRemoteAction(
  [in] RemoteSessionActionType actionType
);
```



## <a name="parameters"></a><span data-ttu-id="c5088-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5088-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5088-114">*actionType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5088-114">*actionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5088-115">Un valor de la enumeración [**RemoteSessionActionType**](remotesessionactiontype.md) que especifica la acción que se va a enviar a la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="c5088-115">A value of the [**RemoteSessionActionType**](remotesessionactiontype.md) enumeration that specifies the action to send to the remote session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5088-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5088-116">Return value</span></span>

<span data-ttu-id="c5088-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c5088-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c5088-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c5088-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5088-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5088-119">Requirements</span></span>



| <span data-ttu-id="c5088-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5088-120">Requirement</span></span> | <span data-ttu-id="c5088-121">Value</span><span class="sxs-lookup"><span data-stu-id="c5088-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5088-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5088-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c5088-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c5088-123">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="c5088-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5088-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c5088-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c5088-125">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="c5088-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c5088-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="c5088-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5088-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c5088-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c5088-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5088-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5088-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c5088-130">IID</span><span class="sxs-lookup"><span data-stu-id="c5088-130">IID</span></span><br/>                      | <span data-ttu-id="c5088-131">IID \_ IMsRdpClient8 se define como 4247E044-9271-43A9-BC49-E2AD9E855D62</span><span class="sxs-lookup"><span data-stu-id="c5088-131">IID\_IMsRdpClient8 is defined as 4247E044-9271-43A9-BC49-E2AD9E855D62</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c5088-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5088-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5088-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="c5088-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="c5088-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="c5088-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="c5088-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="c5088-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





