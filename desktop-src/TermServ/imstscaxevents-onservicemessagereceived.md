---
title: IMsTscAxEvents OnServiceMessageReceived, método
description: Se llama cuando el cliente recibe un mensaje del sistema.
ms.assetid: 9D230AA3-30F8-4BDF-89D6-D33AF42D0E85
ms.tgt_platform: multiple
keywords:
- Método OnServiceMessageReceived Servicios de Escritorio remoto
- Método OnServiceMessageReceived Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnServiceMessageReceived
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnServiceMessageReceived
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a26b78fa31667fb550848d4edd7918aa2bde3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802719"
---
# <a name="imstscaxeventsonservicemessagereceived-method"></a><span data-ttu-id="45102-106">IMsTscAxEvents:: OnServiceMessageReceived (método)</span><span class="sxs-lookup"><span data-stu-id="45102-106">IMsTscAxEvents::OnServiceMessageReceived method</span></span>

<span data-ttu-id="45102-107">Se llama cuando el cliente recibe un mensaje del sistema.</span><span class="sxs-lookup"><span data-stu-id="45102-107">Called when the client receives a system message.</span></span>

## <a name="syntax"></a><span data-ttu-id="45102-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45102-108">Syntax</span></span>


```C++
void OnServiceMessageReceived(
  [in] BSTR serviceMessage
);
```



## <a name="parameters"></a><span data-ttu-id="45102-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45102-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45102-110">*serviceMessage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45102-110">*serviceMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45102-111">Especifica el mensaje del sistema.</span><span class="sxs-lookup"><span data-stu-id="45102-111">Specifies the system message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45102-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45102-112">Return value</span></span>

<span data-ttu-id="45102-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="45102-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="45102-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45102-114">Remarks</span></span>

<span data-ttu-id="45102-115">Para obtener más información sobre los mensajes del sistema, consulte [configuración de la mensajería para un servidor de puerta de enlace de escritorio remoto](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd834700(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="45102-115">For more information about system messages, see [Configure Messaging for a Remote Desktop Gateway Server](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd834700(v=ws.11)).</span></span>

## <a name="requirements"></a><span data-ttu-id="45102-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45102-116">Requirements</span></span>



| <span data-ttu-id="45102-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="45102-117">Requirement</span></span> | <span data-ttu-id="45102-118">Value</span><span class="sxs-lookup"><span data-stu-id="45102-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45102-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45102-119">Minimum supported client</span></span><br/> | <span data-ttu-id="45102-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="45102-120">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="45102-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45102-121">Minimum supported server</span></span><br/> | <span data-ttu-id="45102-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="45102-122">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="45102-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="45102-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="45102-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45102-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="45102-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="45102-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45102-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45102-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="45102-127">IID</span><span class="sxs-lookup"><span data-stu-id="45102-127">IID</span></span><br/>                      | <span data-ttu-id="45102-128">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="45102-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="45102-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="45102-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45102-130">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="45102-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

