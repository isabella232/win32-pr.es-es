---
description: Función de proxy para el método GetMetadataQueryWriter.
ms.assetid: 3186d473-f8a7-405a-8429-3f50104bee4a
title: IWICBitmapEncoder_GetMetadataQueryWriter_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b536e7c4c0553df5dae0f8e11db33c6d709e8c00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696320"
---
# <a name="iwicbitmapencoder_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="88d30-103">IWICBitmapEncoder \_ GetMetadataQueryWriter \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="88d30-103">IWICBitmapEncoder\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="88d30-104">Función de proxy para el método [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="88d30-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="88d30-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88d30-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapEncoder       *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="88d30-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88d30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88d30-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="88d30-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88d30-108">Tipo: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="88d30-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="88d30-109">Puntero a este objeto [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="88d30-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="88d30-110">*ppIMetadataQueryWriter* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="88d30-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88d30-111">Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="88d30-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="88d30-112">Puntero que recibe un puntero a un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span><span class="sxs-lookup"><span data-stu-id="88d30-112">A pointer that receives a pointer to an [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88d30-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88d30-113">Return value</span></span>

<span data-ttu-id="88d30-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="88d30-114">Type: **HRESULT**</span></span>

<span data-ttu-id="88d30-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="88d30-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="88d30-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="88d30-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="88d30-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88d30-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="88d30-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88d30-118">Requirements</span></span>



| <span data-ttu-id="88d30-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="88d30-119">Requirement</span></span> | <span data-ttu-id="88d30-120">Value</span><span class="sxs-lookup"><span data-stu-id="88d30-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88d30-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88d30-121">Minimum supported client</span></span><br/> | <span data-ttu-id="88d30-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="88d30-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="88d30-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88d30-123">Minimum supported server</span></span><br/> | <span data-ttu-id="88d30-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="88d30-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="88d30-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="88d30-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88d30-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88d30-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




