---
description: Función de proxy para el método Initialize.
ms.assetid: 47a717d2-9aac-4230-bdb3-093212eb5448
title: IWICBitmapScaler_Initialize_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapScaler_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cc317adc831b0cf0759580d5c6924fb3f0997524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707420"
---
# <a name="iwicbitmapscaler_initialize_proxy-function"></a><span data-ttu-id="9fef3-103">IWICBitmapScaler \_ inicializar \_ función de proxy</span><span class="sxs-lookup"><span data-stu-id="9fef3-103">IWICBitmapScaler\_Initialize\_Proxy function</span></span>

<span data-ttu-id="9fef3-104">Función de proxy para el método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) .</span><span class="sxs-lookup"><span data-stu-id="9fef3-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fef3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fef3-105">Syntax</span></span>


```C++
HRESULT IWICBitmapScaler_Initialize_Proxy(
  _In_ IWICBitmapScaler           *THIS_PTR,
  _In_ IWICBitmapSource           *pISource,
  _In_ UINT                       uiWidth,
  _In_ UINT                       uiHeight,
  _In_ WICBitmapInterpolationMode mode
);
```



## <a name="parameters"></a><span data-ttu-id="9fef3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9fef3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fef3-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="9fef3-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fef3-108">Tipo: \**[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) \** _</span><span class="sxs-lookup"><span data-stu-id="9fef3-108">Type: \**[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\** _</span></span>

<span data-ttu-id="9fef3-109">Puntero a este objeto [_ *IWICBitmapScaler* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) .</span><span class="sxs-lookup"><span data-stu-id="9fef3-109">Pointer to this [_ *IWICBitmapScaler*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) object.</span></span>

</dd> <dt>

<span data-ttu-id="9fef3-110">*pISource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9fef3-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fef3-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="9fef3-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="9fef3-112">Origen del mapa de bits de entrada.</span><span class="sxs-lookup"><span data-stu-id="9fef3-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="9fef3-113">_uiWidth \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="9fef3-113">_uiWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fef3-114">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="9fef3-114">Type: **UINT**</span></span>

<span data-ttu-id="9fef3-115">Ancho de destino.</span><span class="sxs-lookup"><span data-stu-id="9fef3-115">The destination width.</span></span>

</dd> <dt>

<span data-ttu-id="9fef3-116">*uiHeight* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9fef3-116">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fef3-117">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="9fef3-117">Type: **UINT**</span></span>

<span data-ttu-id="9fef3-118">Alto de desination.</span><span class="sxs-lookup"><span data-stu-id="9fef3-118">The desination height.</span></span>

</dd> <dt>

<span data-ttu-id="9fef3-119">*modo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="9fef3-119">*mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fef3-120">Tipo: **[ **WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span><span class="sxs-lookup"><span data-stu-id="9fef3-120">Type: **[**WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span></span>

<span data-ttu-id="9fef3-121">El modo de interpolación que se va a utilizar al ajustar el tamaño.</span><span class="sxs-lookup"><span data-stu-id="9fef3-121">The interpolation mode to use when scaling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fef3-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9fef3-122">Return value</span></span>

<span data-ttu-id="9fef3-123">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9fef3-123">Type: **HRESULT**</span></span>

<span data-ttu-id="9fef3-124">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="9fef3-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9fef3-125">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9fef3-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fef3-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9fef3-126">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9fef3-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fef3-127">Requirements</span></span>



| <span data-ttu-id="9fef3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fef3-128">Requirement</span></span> | <span data-ttu-id="9fef3-129">Value</span><span class="sxs-lookup"><span data-stu-id="9fef3-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fef3-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fef3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9fef3-131">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9fef3-131">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9fef3-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fef3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9fef3-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9fef3-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9fef3-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9fef3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fef3-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9fef3-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




