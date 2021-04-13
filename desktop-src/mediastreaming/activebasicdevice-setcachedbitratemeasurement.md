---
title: Método ActiveBasicDevice SetCachedBitrateMeasurement (PlayToDevice. h)
description: Establece la velocidad de bits almacenada en caché.
ms.assetid: 53530217-CFF7-4376-B155-E11044621E2D
keywords:
- Método SetCachedBitrateMeasurement API de streaming de multimedia
- Método SetCachedBitrateMeasurement API de streaming de multimedia, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice API de streaming de multimedia, método SetCachedBitrateMeasurement
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c681776b00eb9d911a4fa75a9d360b39a3d2b8c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492868"
---
# <a name="activebasicdevicesetcachedbitratemeasurement-method"></a><span data-ttu-id="03c43-106">ActiveBasicDevice:: SetCachedBitrateMeasurement (método)</span><span class="sxs-lookup"><span data-stu-id="03c43-106">ActiveBasicDevice::SetCachedBitrateMeasurement method</span></span>

<span data-ttu-id="03c43-107">Establece la velocidad de bits almacenada en caché.</span><span class="sxs-lookup"><span data-stu-id="03c43-107">Sets the cached bitrate.</span></span>

## <a name="syntax"></a><span data-ttu-id="03c43-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03c43-108">Syntax</span></span>


```C++
HRESULT SetCachedBitrateMeasurement(
  [in] GUID   physicalNetworkInterface,
  [in] UINT64 bitrate
);
```



## <a name="parameters"></a><span data-ttu-id="03c43-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03c43-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03c43-110">*physicalNetworkInterface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="03c43-110">*physicalNetworkInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03c43-111">Especifica la interfaz de red física.</span><span class="sxs-lookup"><span data-stu-id="03c43-111">Specifies the physical network interface.</span></span>

</dd> <dt>

<span data-ttu-id="03c43-112">*velocidad de bits* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="03c43-112">*bitrate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03c43-113">Valor en el que se va a establecer la velocidad de bits.</span><span class="sxs-lookup"><span data-stu-id="03c43-113">The value to set the bitrate to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03c43-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03c43-114">Return value</span></span>

<span data-ttu-id="03c43-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="03c43-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="03c43-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="03c43-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="03c43-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03c43-117">Requirements</span></span>



| <span data-ttu-id="03c43-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="03c43-118">Requirement</span></span> | <span data-ttu-id="03c43-119">Value</span><span class="sxs-lookup"><span data-stu-id="03c43-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="03c43-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03c43-120">Minimum supported client</span></span><br/> | <span data-ttu-id="03c43-121">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="03c43-121">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="03c43-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03c43-122">Minimum supported server</span></span><br/> | <span data-ttu-id="03c43-123">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="03c43-123">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="03c43-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03c43-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="03c43-125"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="03c43-125"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="03c43-126">IDL</span><span class="sxs-lookup"><span data-stu-id="03c43-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="03c43-127"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="03c43-127"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="03c43-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="03c43-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03c43-129"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03c43-129"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03c43-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="03c43-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="03c43-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="03c43-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

