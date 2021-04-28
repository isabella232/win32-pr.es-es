---
description: 'IWICBitmapCodecInfo_GetContainerFormat_Proxy función: función proxy para el método GetContainerFormat.'
ms.assetid: d8a2387a-fb75-4812-b046-51359071281d
title: IWICBitmapCodecInfo_GetContainerFormat_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 729b4e2fe0f21fd1e96082e53194fd49bbc39ae1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086373"
---
# <a name="iwicbitmapcodecinfo_getcontainerformat_proxy-function"></a><span data-ttu-id="4df96-103">Función IWICBitmapCodecInfo \_ GetContainerFormat \_ Proxy</span><span class="sxs-lookup"><span data-stu-id="4df96-103">IWICBitmapCodecInfo\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="4df96-104">Función de proxy para [**el método GetContainerFormat.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat)</span><span class="sxs-lookup"><span data-stu-id="4df96-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4df96-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4df96-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetContainerFormat_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ GUID                *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="4df96-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4df96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4df96-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="4df96-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4df96-108">Tipo: **[ **IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***</span><span class="sxs-lookup"><span data-stu-id="4df96-108">Type: **[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***</span></span>

<span data-ttu-id="4df96-109">Puntero a este [**objeto IWICBitmapCodecInfo.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)</span><span class="sxs-lookup"><span data-stu-id="4df96-109">Pointer to this [**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="4df96-110">*pguidContainerFormat* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4df96-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4df96-111">Tipo: **\* GUID**</span><span class="sxs-lookup"><span data-stu-id="4df96-111">Type: **GUID\***</span></span>

<span data-ttu-id="4df96-112">Puntero que recibe el GUID del contenedor.</span><span class="sxs-lookup"><span data-stu-id="4df96-112">A pointer that receives the container GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4df96-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4df96-113">Return value</span></span>

<span data-ttu-id="4df96-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4df96-114">Type: **HRESULT**</span></span>

<span data-ttu-id="4df96-115">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4df96-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4df96-116">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="4df96-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4df96-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4df96-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4df96-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4df96-118">Requirements</span></span>



| <span data-ttu-id="4df96-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4df96-119">Requirement</span></span> | <span data-ttu-id="4df96-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4df96-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4df96-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4df96-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4df96-122">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4df96-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="4df96-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4df96-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4df96-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4df96-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="4df96-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4df96-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4df96-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4df96-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




