---
title: Método ActiveBasicDevice GetCachedExtraSinkProtocolInfo (PlayToDevice. h)
description: Obtiene información adicional del protocolo receptor en caché para el dispositivo.
ms.assetid: 97112921-1C1D-4FC9-8FE6-1381F3773351
keywords:
- Método GetCachedExtraSinkProtocolInfo API de streaming de multimedia
- Método GetCachedExtraSinkProtocolInfo API de streaming de multimedia, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice API de streaming de multimedia, método GetCachedExtraSinkProtocolInfo
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedExtraSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be5bb013d1356d5ff02e709a92f01eceff6c2e0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422409"
---
# <a name="activebasicdevicegetcachedextrasinkprotocolinfo-method"></a><span data-ttu-id="3bedc-106">ActiveBasicDevice:: GetCachedExtraSinkProtocolInfo (método)</span><span class="sxs-lookup"><span data-stu-id="3bedc-106">ActiveBasicDevice::GetCachedExtraSinkProtocolInfo method</span></span>

<span data-ttu-id="3bedc-107">Obtiene información adicional del protocolo receptor en caché para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3bedc-107">Gets additional cached sink protocol info for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bedc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3bedc-108">Syntax</span></span>


```C++
HRESULT GetCachedExtraSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="3bedc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3bedc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bedc-110">*valor* \[ de out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3bedc-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3bedc-111">Información adicional del protocolo receptor en caché para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3bedc-111">The extra cached sink protocol info for the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bedc-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3bedc-112">Return value</span></span>

<span data-ttu-id="3bedc-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="3bedc-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3bedc-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3bedc-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bedc-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bedc-115">Requirements</span></span>



| <span data-ttu-id="3bedc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bedc-116">Requirement</span></span> | <span data-ttu-id="3bedc-117">Value</span><span class="sxs-lookup"><span data-stu-id="3bedc-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bedc-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3bedc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3bedc-119">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="3bedc-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3bedc-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3bedc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3bedc-121">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3bedc-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3bedc-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3bedc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bedc-123"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bedc-123"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="3bedc-124">IDL</span><span class="sxs-lookup"><span data-stu-id="3bedc-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3bedc-125"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3bedc-125"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="3bedc-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3bedc-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bedc-127"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bedc-127"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bedc-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="3bedc-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="3bedc-129">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3bedc-129">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

