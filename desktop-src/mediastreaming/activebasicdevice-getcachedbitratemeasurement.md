---
title: Método ActiveBasicDevice GetCachedBitrateMeasurement (PlayToDevice. h)
description: Obtiene la velocidad de bits almacenada en caché.
ms.assetid: 78C3C5D7-C46B-413D-BC18-C3861E5FDAA5
keywords:
- Método GetCachedBitrateMeasurement API de streaming de multimedia
- Método GetCachedBitrateMeasurement API de streaming de multimedia, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice API de streaming de multimedia, método GetCachedBitrateMeasurement
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d15b38ba2730d2023b09c2fa0352ade1f1532724
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535086"
---
# <a name="activebasicdevicegetcachedbitratemeasurement-method"></a><span data-ttu-id="1a284-106">ActiveBasicDevice:: GetCachedBitrateMeasurement (método)</span><span class="sxs-lookup"><span data-stu-id="1a284-106">ActiveBasicDevice::GetCachedBitrateMeasurement method</span></span>

<span data-ttu-id="1a284-107">Obtiene la velocidad de bits almacenada en caché.</span><span class="sxs-lookup"><span data-stu-id="1a284-107">Gets the cached bitrate.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a284-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a284-108">Syntax</span></span>


```C++
HRESULT GetCachedBitrateMeasurement(
  [in]          GUID   physicalNetworkInterface,
  [out, retval] UINT64 *bitrate
);
```



## <a name="parameters"></a><span data-ttu-id="1a284-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a284-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a284-110">*physicalNetworkInterface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1a284-110">*physicalNetworkInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a284-111">Especifica la interfaz de red física.</span><span class="sxs-lookup"><span data-stu-id="1a284-111">Specifies the physical network interface.</span></span>

</dd> <dt>

<span data-ttu-id="1a284-112">*velocidad de bits* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1a284-112">*bitrate* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1a284-113">Recibe el valor de velocidad de bits.</span><span class="sxs-lookup"><span data-stu-id="1a284-113">Receives the bitrate value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a284-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a284-114">Return value</span></span>

<span data-ttu-id="1a284-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="1a284-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1a284-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1a284-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a284-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a284-117">Requirements</span></span>



| <span data-ttu-id="1a284-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a284-118">Requirement</span></span> | <span data-ttu-id="1a284-119">Value</span><span class="sxs-lookup"><span data-stu-id="1a284-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a284-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a284-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1a284-121">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="1a284-121">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1a284-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a284-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1a284-123">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1a284-123">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1a284-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1a284-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a284-125"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a284-125"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="1a284-126">IDL</span><span class="sxs-lookup"><span data-stu-id="1a284-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1a284-127"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1a284-127"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="1a284-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1a284-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a284-129"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a284-129"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a284-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a284-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="1a284-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1a284-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

