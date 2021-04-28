---
description: 'IWICBitmap_SetResolution_Proxy función: función proxy para el método SetResolution.'
ms.assetid: c4e3927c-6f9d-401d-acd7-711674cdbb53
title: IWICBitmap_SetResolution_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f11189307ad14dde6ea1e1373583a8ab4b08b9be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086383"
---
# <a name="iwicbitmap_setresolution_proxy-function"></a><span data-ttu-id="71201-103">Función IWICBitmap \_ SetResolution \_ Proxy</span><span class="sxs-lookup"><span data-stu-id="71201-103">IWICBitmap\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="71201-104">Función de proxy para el [**método SetResolution.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution)</span><span class="sxs-lookup"><span data-stu-id="71201-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="71201-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71201-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetResolution_Proxy(
  _In_ IWICBitmap *THIS_PTR,
  _In_ double     dpiX,
  _In_ double     dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="71201-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71201-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71201-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="71201-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71201-108">Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span><span class="sxs-lookup"><span data-stu-id="71201-108">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span></span>

<span data-ttu-id="71201-109">Puntero a este [**objeto IWICBitmap.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)</span><span class="sxs-lookup"><span data-stu-id="71201-109">Pointer to this [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="71201-110">*pppX* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="71201-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71201-111">Tipo: **double**</span><span class="sxs-lookup"><span data-stu-id="71201-111">Type: **double**</span></span>

<span data-ttu-id="71201-112">Resolución horizontal.</span><span class="sxs-lookup"><span data-stu-id="71201-112">The horizontal resolution.</span></span>

</dd> <dt>

<span data-ttu-id="71201-113">*pppY* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="71201-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71201-114">Tipo: **double**</span><span class="sxs-lookup"><span data-stu-id="71201-114">Type: **double**</span></span>

<span data-ttu-id="71201-115">Resolución vertical.</span><span class="sxs-lookup"><span data-stu-id="71201-115">The vertical resolution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71201-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71201-116">Return value</span></span>

<span data-ttu-id="71201-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="71201-117">Type: **HRESULT**</span></span>

<span data-ttu-id="71201-118">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="71201-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="71201-119">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="71201-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="71201-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71201-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="71201-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71201-121">Requirements</span></span>



| <span data-ttu-id="71201-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="71201-122">Requirement</span></span> | <span data-ttu-id="71201-123">Valor</span><span class="sxs-lookup"><span data-stu-id="71201-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71201-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71201-124">Minimum supported client</span></span><br/> | <span data-ttu-id="71201-125">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="71201-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="71201-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71201-126">Minimum supported server</span></span><br/> | <span data-ttu-id="71201-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="71201-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="71201-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="71201-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71201-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="71201-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




