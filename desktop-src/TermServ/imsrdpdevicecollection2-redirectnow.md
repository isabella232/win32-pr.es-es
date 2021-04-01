---
title: IMsRdpDeviceCollection2 RedirectNow, método
description: Fuerza la redirección o eliminación de los dispositivos que se seleccionaron o anularon de la colección.
ms.assetid: 9cd5849d-a589-43f3-b904-6b2e15ca033d
ms.tgt_platform: multiple
keywords:
- Método RedirectNow Servicios de Escritorio remoto
- Método RedirectNow Servicios de Escritorio remoto, interfaz IMsRdpDeviceCollection2
- Interfaz IMsRdpDeviceCollection2 Servicios de Escritorio remoto, método RedirectNow
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.RedirectNow
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893d1e26f504d5aeb45f795ea7425eeefc3a6232
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995945"
---
# <a name="imsrdpdevicecollection2redirectnow-method"></a><span data-ttu-id="f4013-106">IMsRdpDeviceCollection2:: RedirectNow (método)</span><span class="sxs-lookup"><span data-stu-id="f4013-106">IMsRdpDeviceCollection2::RedirectNow method</span></span>

<span data-ttu-id="f4013-107">Fuerza la redirección o eliminación de los dispositivos que se seleccionaron o anularon de la colección.</span><span class="sxs-lookup"><span data-stu-id="f4013-107">Forces devices that were selected or unselected from the collection to be redirected or removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4013-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4013-108">Syntax</span></span>


```C++
HRESULT RedirectNow(
  [in] RedirectDeviceType Type
);
```



## <a name="parameters"></a><span data-ttu-id="f4013-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4013-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4013-110">*Tipo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f4013-110">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4013-111">Tipo: **[ **RedirectDeviceType**](redirectdevicetype.md)**</span><span class="sxs-lookup"><span data-stu-id="f4013-111">Type: **[**RedirectDeviceType**](redirectdevicetype.md)**</span></span>

<span data-ttu-id="f4013-112">Un valor de la enumeración [**RedirectDeviceType**](redirectdevicetype.md) que especifica el tipo de dispositivo que se va a redirigir.</span><span class="sxs-lookup"><span data-stu-id="f4013-112">A value of the [**RedirectDeviceType**](redirectdevicetype.md) enumeration that specifies the type of device to be redirected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4013-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4013-113">Return value</span></span>

<span data-ttu-id="f4013-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f4013-114">Type: **HRESULT**</span></span>

<span data-ttu-id="f4013-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f4013-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f4013-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f4013-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4013-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4013-117">Requirements</span></span>



| <span data-ttu-id="f4013-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4013-118">Requirement</span></span> | <span data-ttu-id="f4013-119">Value</span><span class="sxs-lookup"><span data-stu-id="f4013-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4013-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4013-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f4013-121">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f4013-121">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="f4013-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4013-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f4013-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f4013-123">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="f4013-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f4013-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="f4013-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4013-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f4013-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f4013-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4013-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4013-127"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4013-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4013-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4013-129">**RedirectDeviceType**</span><span class="sxs-lookup"><span data-stu-id="f4013-129">**RedirectDeviceType**</span></span>](redirectdevicetype.md)
</dt> <dt>

[<span data-ttu-id="f4013-130">**IMsRdpDeviceCollection2**</span><span class="sxs-lookup"><span data-stu-id="f4013-130">**IMsRdpDeviceCollection2**</span></span>](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





