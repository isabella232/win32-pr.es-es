---
title: Método ActiveBasicDevice GetCachedSinkProtocolInfo (PlayToDevice. h)
description: Obtiene la información del protocolo del receptor almacenado en caché para el dispositivo. | Método ActiveBasicDevice GetCachedSinkProtocolInfo (PlayToDevice. h)
ms.assetid: C6A3C4B5-1883-4E71-83D2-11E378A4FBCA
keywords:
- Método GetCachedSinkProtocolInfo API de streaming de multimedia
- Método GetCachedSinkProtocolInfo API de streaming de multimedia, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice API de streaming de multimedia, método GetCachedSinkProtocolInfo
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056cc351a1ecd1c8eef07d4e994da8e895aa85f8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698134"
---
# <a name="activebasicdevicegetcachedsinkprotocolinfo-method"></a><span data-ttu-id="9ff86-107">ActiveBasicDevice:: GetCachedSinkProtocolInfo (método)</span><span class="sxs-lookup"><span data-stu-id="9ff86-107">ActiveBasicDevice::GetCachedSinkProtocolInfo method</span></span>

<span data-ttu-id="9ff86-108">Obtiene la información del protocolo del receptor almacenado en caché para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ff86-108">Gets the cached sink protocol info for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ff86-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ff86-109">Syntax</span></span>


```C++
HRESULT GetCachedSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="9ff86-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ff86-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ff86-111">*valor* \[ de out, retval\]</span><span class="sxs-lookup"><span data-stu-id="9ff86-111">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9ff86-112">Información del protocolo receptor en caché para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ff86-112">The cached sink protocol info for the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ff86-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ff86-113">Return value</span></span>

<span data-ttu-id="9ff86-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9ff86-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9ff86-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9ff86-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ff86-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ff86-116">Requirements</span></span>



| <span data-ttu-id="9ff86-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ff86-117">Requirement</span></span> | <span data-ttu-id="9ff86-118">Value</span><span class="sxs-lookup"><span data-stu-id="9ff86-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff86-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ff86-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9ff86-120">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="9ff86-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9ff86-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ff86-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9ff86-122">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9ff86-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9ff86-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ff86-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ff86-124"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ff86-124"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ff86-125">IDL</span><span class="sxs-lookup"><span data-stu-id="9ff86-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9ff86-126"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9ff86-126"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="9ff86-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9ff86-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ff86-128"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ff86-128"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ff86-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ff86-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="9ff86-130">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9ff86-130">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

