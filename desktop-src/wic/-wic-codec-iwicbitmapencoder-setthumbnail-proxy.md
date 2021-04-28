---
description: 'IWICBitmapEncoder_SetThumbnail_Proxy función: función de proxy para el método SetThumbnail.'
ms.assetid: 6c062eaf-27a4-4d48-8315-be9bf168f999
title: IWICBitmapEncoder_SetThumbnail_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_SetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a7666fffbac7813db8021daf38ebae9c4e68c57a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100603"
---
# <a name="iwicbitmapencoder_setthumbnail_proxy-function"></a><span data-ttu-id="0e305-103">Función \_ SetThumbnail Proxy de IWICBitmapEncoder \_</span><span class="sxs-lookup"><span data-stu-id="0e305-103">IWICBitmapEncoder\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="0e305-104">Función de proxy para [**el método SetThumbnail.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)</span><span class="sxs-lookup"><span data-stu-id="0e305-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e305-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e305-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetThumbnail_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICBitmapSource  *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="0e305-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0e305-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e305-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="0e305-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e305-108">Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="0e305-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="0e305-109">Puntero a este [**objeto IWICBitmapEncoder.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)</span><span class="sxs-lookup"><span data-stu-id="0e305-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="0e305-110">*pIThumbnail* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="0e305-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e305-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="0e305-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="0e305-112">[**IWICBitmapSource que se**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) establecerá como la miniatura global.</span><span class="sxs-lookup"><span data-stu-id="0e305-112">The [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to set as the global thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e305-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0e305-113">Return value</span></span>

<span data-ttu-id="0e305-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0e305-114">Type: **HRESULT**</span></span>

<span data-ttu-id="0e305-115">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0e305-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0e305-116">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="0e305-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e305-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e305-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0e305-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e305-118">Requirements</span></span>



| <span data-ttu-id="0e305-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e305-119">Requirement</span></span> | <span data-ttu-id="0e305-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0e305-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e305-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e305-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0e305-122">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0e305-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0e305-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e305-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0e305-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0e305-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0e305-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0e305-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e305-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e305-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




