---
title: Método remove_ConnectionStatusChanged IBasicDevice
description: Anula el registro de un controlador de eventos para el evento ConnectionStatusChanged. | Método remove_ConnectionStatusChanged IBasicDevice
ms.assetid: 577D9C50-486D-441A-A9FE-AF79D1FC2B52
keywords:
- método remove_ConnectionStatusChanged API de streaming multimedia
- método remove_ConnectionStatusChanged API de streaming multimedia, interfaz IBasicDevice
- IBasicDevice interface media streaming API, método remove_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- IBasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c2bfa2886774ad637e66385a057c9d4e21efe0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105707681"
---
# <a name="ibasicdeviceremove_connectionstatuschanged-method"></a><span data-ttu-id="43aa4-107">IBasicDevice:: Remove \_ ConnectionStatusChanged (método)</span><span class="sxs-lookup"><span data-stu-id="43aa4-107">IBasicDevice::remove\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="43aa4-108">Anula el registro de un controlador de eventos para el evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="43aa4-108">Unregisters an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="43aa4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43aa4-109">Syntax</span></span>


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a><span data-ttu-id="43aa4-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43aa4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43aa4-111">*token* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="43aa4-111">*token* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43aa4-112">Referencia a un token obtenido del método [**Add \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) cuando se registró el controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="43aa4-112">A reference to a token obtained from the [**add\_ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) method when the event handler was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43aa4-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43aa4-113">Return value</span></span>

<span data-ttu-id="43aa4-114">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="43aa4-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="43aa4-115">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="43aa4-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="43aa4-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="43aa4-116">Return code</span></span>                                                                          | <span data-ttu-id="43aa4-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="43aa4-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="43aa4-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="43aa4-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="43aa4-119">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="43aa4-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="43aa4-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="43aa4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43aa4-121">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="43aa4-121">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





