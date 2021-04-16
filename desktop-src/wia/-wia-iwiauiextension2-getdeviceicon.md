---
description: Obtiene un icono de dispositivo personalizado.
ms.assetid: ea768dd1-22fe-4a0f-8851-b152e28d65fb
title: 'IWiaUIExtension2:: GetDeviceIcon (método) (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: d071332a1947c4eb6398235d6941a6843a4fa54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541950"
---
# <a name="iwiauiextension2getdeviceicon-method"></a><span data-ttu-id="9922b-103">IWiaUIExtension2:: GetDeviceIcon (método)</span><span class="sxs-lookup"><span data-stu-id="9922b-103">IWiaUIExtension2::GetDeviceIcon method</span></span>

<span data-ttu-id="9922b-104">Obtiene un icono de dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="9922b-104">Gets a custom device icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="9922b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9922b-105">Syntax</span></span>


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a><span data-ttu-id="9922b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9922b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9922b-107">*bstrDeviceId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9922b-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9922b-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="9922b-108">Type: **BSTR**</span></span>

<span data-ttu-id="9922b-109">Especifica el identificador del dispositivo WIA para el que se va a obtener el icono.</span><span class="sxs-lookup"><span data-stu-id="9922b-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="9922b-110">*phIcon* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9922b-110">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9922b-111">Tipo: \**HICON \** _</span><span class="sxs-lookup"><span data-stu-id="9922b-111">Type: \**HICON\** _</span></span>

<span data-ttu-id="9922b-112">Apunta a una ubicación de memoria que recibirá un identificador para el icono del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9922b-112">Points to a memory location that will receive a handle for the icon for the device.</span></span>

</dd> <dt>

<span data-ttu-id="9922b-113">_nSize \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="9922b-113">_nSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9922b-114">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="9922b-114">Type: **ULONG**</span></span>

<span data-ttu-id="9922b-115">Especifica el tamaño de icono deseado, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="9922b-115">Specifies the desired icon size, in pixels.</span></span> <span data-ttu-id="9922b-116">Se supone que el icono es cuadrado y nSize especifica el ancho y el alto del icono solicitado.</span><span class="sxs-lookup"><span data-stu-id="9922b-116">The icon is assumed to be square, and nSize specifies both the width and height of the requested icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9922b-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9922b-117">Return value</span></span>

<span data-ttu-id="9922b-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9922b-118">Type: **HRESULT**</span></span>

<span data-ttu-id="9922b-119">Si el método se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="9922b-119">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="9922b-120">Si se produce un error en el método, devuelve un código de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="9922b-120">If the method fails, it returns an appropriate error code.</span></span> <span data-ttu-id="9922b-121">En la tabla siguiente se muestran algunos de los códigos de estado devueltos posibles.</span><span class="sxs-lookup"><span data-stu-id="9922b-121">The following table shows some of the possible return status codes.</span></span>



| <span data-ttu-id="9922b-122">Código de error</span><span class="sxs-lookup"><span data-stu-id="9922b-122">Error code</span></span>    | <span data-ttu-id="9922b-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="9922b-123">Description</span></span>                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9922b-124">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="9922b-124">E\_INVALIDARG</span></span> | <span data-ttu-id="9922b-125">El parámetro bstrDeviceId o phIcon es **null**, o bstrDeviceId no apunta a una cadena de identificador de dispositivo WIA válida</span><span class="sxs-lookup"><span data-stu-id="9922b-125">Parameter bstrDeviceId or phIcon is **NULL**, or bstrDeviceId does not point to a valid WIA device ID string</span></span> |
| <span data-ttu-id="9922b-126">E \_ FAIL</span><span class="sxs-lookup"><span data-stu-id="9922b-126">E\_FAIL</span></span>       | <span data-ttu-id="9922b-127">No hay ningún recurso de icono disponible.</span><span class="sxs-lookup"><span data-stu-id="9922b-127">No icon resource is available.</span></span>                                                                               |
| <span data-ttu-id="9922b-128">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="9922b-128">E\_NOTIMPL</span></span>    | <span data-ttu-id="9922b-129">No hay disponible ningún icono del tamaño solicitado.</span><span class="sxs-lookup"><span data-stu-id="9922b-129">No icon of the size requested is available.</span></span>                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="9922b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9922b-130">Requirements</span></span>



| <span data-ttu-id="9922b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9922b-131">Requirement</span></span> | <span data-ttu-id="9922b-132">Value</span><span class="sxs-lookup"><span data-stu-id="9922b-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9922b-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9922b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9922b-134">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="9922b-134">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9922b-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9922b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9922b-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9922b-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9922b-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9922b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="9922b-138"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="9922b-138"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




