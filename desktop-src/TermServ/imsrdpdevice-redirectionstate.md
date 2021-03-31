---
title: Propiedad RedirectionState de IMsRdpDevice
description: Indica el estado de la redirección del dispositivo.
ms.assetid: 967734c9-64d8-4604-a133-4649279f4475
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RedirectionState
- Propiedad RedirectionState Servicios de Escritorio remoto, interfaz IMsRdpDevice
- Servicios de Escritorio remoto de la interfaz IMsRdpDevice, propiedad RedirectionState
topic_type:
- apiref
api_name:
- IMsRdpDevice.RedirectionState
- IMsRdpDevice.get_RedirectionState
- IMsRdpDevice.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0f6fb5781700daa8a65443d2713253e97f73bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490343"
---
# <a name="imsrdpdeviceredirectionstate-property"></a><span data-ttu-id="e2f51-106">IMsRdpDevice:: RedirectionState (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e2f51-106">IMsRdpDevice::RedirectionState property</span></span>

<span data-ttu-id="e2f51-107">Indica el estado de la redirección del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e2f51-107">Indicates the redirection state of the device.</span></span>

<span data-ttu-id="e2f51-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e2f51-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2f51-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2f51-109">Syntax</span></span>


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a><span data-ttu-id="e2f51-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e2f51-110">Property value</span></span>

<span data-ttu-id="e2f51-111">Establezca este parámetro en **Variant \_ false** para deshabilitar la redirección o **Variant \_ true** para habilitar la redirección.</span><span class="sxs-lookup"><span data-stu-id="e2f51-111">Set this parameter to **VARIANT\_FALSE** to disable redirection or **VARIANT\_TRUE** to enable redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e2f51-112">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="e2f51-112">Error codes</span></span>

<span data-ttu-id="e2f51-113">Si el método se ejecuta correctamente, se devuelve **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="e2f51-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="e2f51-114">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="e2f51-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2f51-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2f51-115">Requirements</span></span>



| <span data-ttu-id="e2f51-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2f51-116">Requirement</span></span> | <span data-ttu-id="e2f51-117">Value</span><span class="sxs-lookup"><span data-stu-id="e2f51-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f51-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2f51-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e2f51-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2f51-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e2f51-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2f51-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e2f51-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2f51-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e2f51-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e2f51-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="e2f51-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2f51-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e2f51-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e2f51-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2f51-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2f51-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e2f51-126">IID</span><span class="sxs-lookup"><span data-stu-id="e2f51-126">IID</span></span><br/>                      | <span data-ttu-id="e2f51-127">IID \_ IMsRdpDevice se define como 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="e2f51-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="e2f51-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2f51-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2f51-129">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="e2f51-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





