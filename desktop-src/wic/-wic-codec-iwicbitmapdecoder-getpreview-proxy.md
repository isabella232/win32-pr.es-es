---
description: Función de proxy para el método GetPreview.
ms.assetid: 8251af14-68db-4e4a-a501-115e7bbd53cd
title: IWICBitmapDecoder_GetPreview_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetPreview_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0fc6808d94cdc1cdcdaf65e252107b939e12eeaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696321"
---
# <a name="iwicbitmapdecoder_getpreview_proxy-function"></a><span data-ttu-id="4b42b-103">IWICBitmapDecoder \_ GetPreview, \_ función de proxy</span><span class="sxs-lookup"><span data-stu-id="4b42b-103">IWICBitmapDecoder\_GetPreview\_Proxy function</span></span>

<span data-ttu-id="4b42b-104">Función de proxy para el método [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) .</span><span class="sxs-lookup"><span data-stu-id="4b42b-104">Proxy function for the [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b42b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b42b-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetPreview_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ IWICBitmapSource  **ppIBitmapSource
);
```



## <a name="parameters"></a><span data-ttu-id="4b42b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b42b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b42b-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="4b42b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b42b-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="4b42b-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="4b42b-109">Puntero a este objeto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="4b42b-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="4b42b-110">*ppIBitmapSource* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4b42b-110">*ppIBitmapSource* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b42b-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="4b42b-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="4b42b-112">Un puntero que recibe un puntero al mapa de bits de vista previa si es compatible.</span><span class="sxs-lookup"><span data-stu-id="4b42b-112">A pointer that receives a pointer to the preview bitmap if supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b42b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b42b-113">Return value</span></span>

<span data-ttu-id="4b42b-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4b42b-114">Type: **HRESULT**</span></span>

<span data-ttu-id="4b42b-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4b42b-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4b42b-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4b42b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b42b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b42b-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4b42b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b42b-118">Requirements</span></span>



| <span data-ttu-id="4b42b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b42b-119">Requirement</span></span> | <span data-ttu-id="4b42b-120">Value</span><span class="sxs-lookup"><span data-stu-id="4b42b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b42b-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b42b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4b42b-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4b42b-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="4b42b-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b42b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4b42b-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4b42b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="4b42b-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4b42b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b42b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b42b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




