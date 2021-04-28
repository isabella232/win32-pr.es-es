---
description: 'Método IWiaUIExtension2::GetDeviceIcon: obtiene un icono de dispositivo personalizado.'
ms.assetid: ea768dd1-22fe-4a0f-8851-b152e28d65fb
title: Método IWiaUIExtension2::GetDeviceIcon (Wiadevd.h)
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
ms.openlocfilehash: fe1498a804de5adeeea459464e95640b3b81ef06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116623"
---
# <a name="iwiauiextension2getdeviceicon-method"></a><span data-ttu-id="79c43-103">IWiaUIExtension2::GetDeviceIcon (método)</span><span class="sxs-lookup"><span data-stu-id="79c43-103">IWiaUIExtension2::GetDeviceIcon method</span></span>

<span data-ttu-id="79c43-104">Obtiene un icono de dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="79c43-104">Gets a custom device icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="79c43-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79c43-105">Syntax</span></span>


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a><span data-ttu-id="79c43-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79c43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79c43-107">*bstrDeviceId* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="79c43-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79c43-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="79c43-108">Type: **BSTR**</span></span>

<span data-ttu-id="79c43-109">Especifica el identificador de dispositivo del dispositivo WIA para el que se va a obtener el icono.</span><span class="sxs-lookup"><span data-stu-id="79c43-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="79c43-110">*phIcon* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="79c43-110">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79c43-111">Tipo: **HICON \***</span><span class="sxs-lookup"><span data-stu-id="79c43-111">Type: **HICON\***</span></span>

<span data-ttu-id="79c43-112">Apunta a una ubicación de memoria que recibirá un identificador para el icono del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="79c43-112">Points to a memory location that will receive a handle for the icon for the device.</span></span>

</dd> <dt>

<span data-ttu-id="79c43-113">*nSize* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="79c43-113">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79c43-114">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="79c43-114">Type: **ULONG**</span></span>

<span data-ttu-id="79c43-115">Especifica el tamaño de icono deseado, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="79c43-115">Specifies the desired icon size, in pixels.</span></span> <span data-ttu-id="79c43-116">Se supone que el icono es cuadrado y nSize especifica el ancho y el alto del icono solicitado.</span><span class="sxs-lookup"><span data-stu-id="79c43-116">The icon is assumed to be square, and nSize specifies both the width and height of the requested icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79c43-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79c43-117">Return value</span></span>

<span data-ttu-id="79c43-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="79c43-118">Type: **HRESULT**</span></span>

<span data-ttu-id="79c43-119">Si el método se realiza correctamente, devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="79c43-119">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="79c43-120">Si se produce un error en el método, devuelve un código de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="79c43-120">If the method fails, it returns an appropriate error code.</span></span> <span data-ttu-id="79c43-121">En la tabla siguiente se muestran algunos de los códigos de estado de devolución posibles.</span><span class="sxs-lookup"><span data-stu-id="79c43-121">The following table shows some of the possible return status codes.</span></span>



| <span data-ttu-id="79c43-122">Código de error</span><span class="sxs-lookup"><span data-stu-id="79c43-122">Error code</span></span>    | <span data-ttu-id="79c43-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="79c43-123">Description</span></span>                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79c43-124">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="79c43-124">E\_INVALIDARG</span></span> | <span data-ttu-id="79c43-125">El parámetro bstrDeviceId o phIcon **es NULL** o bstrDeviceId no apunta a una cadena de identificador de dispositivo WIA válida</span><span class="sxs-lookup"><span data-stu-id="79c43-125">Parameter bstrDeviceId or phIcon is **NULL**, or bstrDeviceId does not point to a valid WIA device ID string</span></span> |
| <span data-ttu-id="79c43-126">E \_ FAIL</span><span class="sxs-lookup"><span data-stu-id="79c43-126">E\_FAIL</span></span>       | <span data-ttu-id="79c43-127">No hay ningún recurso de icono disponible.</span><span class="sxs-lookup"><span data-stu-id="79c43-127">No icon resource is available.</span></span>                                                                               |
| <span data-ttu-id="79c43-128">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="79c43-128">E\_NOTIMPL</span></span>    | <span data-ttu-id="79c43-129">No hay ningún icono del tamaño solicitado disponible.</span><span class="sxs-lookup"><span data-stu-id="79c43-129">No icon of the size requested is available.</span></span>                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="79c43-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79c43-130">Requirements</span></span>



| <span data-ttu-id="79c43-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="79c43-131">Requirement</span></span> | <span data-ttu-id="79c43-132">Valor</span><span class="sxs-lookup"><span data-stu-id="79c43-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="79c43-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79c43-133">Minimum supported client</span></span><br/> | <span data-ttu-id="79c43-134">Solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="79c43-134">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="79c43-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79c43-135">Minimum supported server</span></span><br/> | <span data-ttu-id="79c43-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="79c43-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="79c43-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79c43-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="79c43-138"><dt>Wiadevd.h</dt></span><span class="sxs-lookup"><span data-stu-id="79c43-138"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




