---
title: Método ActiveBasicDevice SetCachedSinkProtocolInfo (PlayToDevice. h)
description: Obtiene la información del protocolo del receptor almacenado en caché para el dispositivo. | Método ActiveBasicDevice SetCachedSinkProtocolInfo (PlayToDevice. h)
ms.assetid: C4856B97-89F9-43EC-B778-9E0CDAAF2C47
keywords:
- Método SetCachedSinkProtocolInfo API de streaming de multimedia
- Método SetCachedSinkProtocolInfo API de streaming de multimedia, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice API de streaming de multimedia, método SetCachedSinkProtocolInfo
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9100cb8faeb685a0cc7a8b7b73deb11afca29a3e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105707707"
---
# <a name="activebasicdevicesetcachedsinkprotocolinfo-method"></a><span data-ttu-id="7770a-107">ActiveBasicDevice:: SetCachedSinkProtocolInfo (método)</span><span class="sxs-lookup"><span data-stu-id="7770a-107">ActiveBasicDevice::SetCachedSinkProtocolInfo method</span></span>

<span data-ttu-id="7770a-108">Obtiene la información del protocolo del receptor almacenado en caché para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7770a-108">Gets the cached sink protocol info for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="7770a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7770a-109">Syntax</span></span>


```C++
HRESULT SetCachedSinkProtocolInfo(
  [in] GUID   physicalNetworkInterface,
  [in] UINT64 bitrate
);
```



## <a name="parameters"></a><span data-ttu-id="7770a-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7770a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7770a-111">*physicalNetworkInterface* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7770a-111">*physicalNetworkInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7770a-112">Especifica la interfaz de red física.</span><span class="sxs-lookup"><span data-stu-id="7770a-112">Specifies the physical network interface.</span></span>

</dd> <dt>

<span data-ttu-id="7770a-113">*velocidad de bits* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7770a-113">*bitrate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7770a-114">Valor de velocidad de bits.</span><span class="sxs-lookup"><span data-stu-id="7770a-114">The bitrate value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7770a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7770a-115">Return value</span></span>

<span data-ttu-id="7770a-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="7770a-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7770a-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7770a-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7770a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7770a-118">Requirements</span></span>



| <span data-ttu-id="7770a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7770a-119">Requirement</span></span> | <span data-ttu-id="7770a-120">Value</span><span class="sxs-lookup"><span data-stu-id="7770a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7770a-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7770a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7770a-122">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="7770a-122">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7770a-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7770a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7770a-124">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7770a-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7770a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7770a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7770a-126"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="7770a-126"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="7770a-127">IDL</span><span class="sxs-lookup"><span data-stu-id="7770a-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7770a-128"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7770a-128"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="7770a-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7770a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7770a-130"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7770a-130"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7770a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="7770a-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="7770a-132">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7770a-132">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

