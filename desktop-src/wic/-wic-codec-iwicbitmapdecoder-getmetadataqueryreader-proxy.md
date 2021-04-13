---
description: Función de proxy para el método GetMetadataQueryReader.
ms.assetid: cc32bdf1-d807-46ac-87b7-77bf2d498e72
title: IWICBitmapDecoder_GetMetadataQueryReader_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetMetadataQueryReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 72b47652c76934fdf3ea518925990d6d4d1d3eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360243"
---
# <a name="iwicbitmapdecoder_getmetadataqueryreader_proxy-function"></a><span data-ttu-id="4825f-103">IWICBitmapDecoder \_ GetMetadataQueryReader, \_ función de proxy</span><span class="sxs-lookup"><span data-stu-id="4825f-103">IWICBitmapDecoder\_GetMetadataQueryReader\_Proxy function</span></span>

<span data-ttu-id="4825f-104">Función de proxy para el método [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader) .</span><span class="sxs-lookup"><span data-stu-id="4825f-104">Proxy function for the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4825f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4825f-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapDecoder       *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a><span data-ttu-id="4825f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4825f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4825f-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="4825f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4825f-108">Tipo: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="4825f-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="4825f-109">Puntero a este objeto [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) .</span><span class="sxs-lookup"><span data-stu-id="4825f-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="4825f-110">*ppIMetadataQueryReader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4825f-110">*ppIMetadataQueryReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4825f-111">Tipo: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span><span class="sxs-lookup"><span data-stu-id="4825f-111">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span></span>

<span data-ttu-id="4825f-112">Puntero que recibe un puntero a los metadatos.</span><span class="sxs-lookup"><span data-stu-id="4825f-112">A pointer that receives a pointer to the metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4825f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4825f-113">Return value</span></span>

<span data-ttu-id="4825f-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4825f-114">Type: **HRESULT**</span></span>

<span data-ttu-id="4825f-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="4825f-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4825f-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4825f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4825f-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4825f-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4825f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4825f-118">Requirements</span></span>



| <span data-ttu-id="4825f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4825f-119">Requirement</span></span> | <span data-ttu-id="4825f-120">Value</span><span class="sxs-lookup"><span data-stu-id="4825f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4825f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4825f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4825f-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4825f-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="4825f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4825f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4825f-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4825f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="4825f-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4825f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4825f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4825f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




