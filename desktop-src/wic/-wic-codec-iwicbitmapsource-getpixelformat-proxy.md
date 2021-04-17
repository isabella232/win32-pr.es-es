---
description: Función de proxy para el método GetPixelFormat.
ms.assetid: 0879bfb7-0175-4275-a093-a69b39c66a41
title: IWICBitmapSource_GetPixelFormat_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetPixelFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ff795dd028c8d8f1e18a944df60a87f1e7cee670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706494"
---
# <a name="iwicbitmapsource_getpixelformat_proxy-function"></a><span data-ttu-id="a5b60-103">Función de proxy de \_ GetPixelFormat de IWICBitmapSource \_</span><span class="sxs-lookup"><span data-stu-id="a5b60-103">IWICBitmapSource\_GetPixelFormat\_Proxy function</span></span>

<span data-ttu-id="a5b60-104">Función de proxy para el método [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat) .</span><span class="sxs-lookup"><span data-stu-id="a5b60-104">Proxy function for the [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5b60-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5b60-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_GetPixelFormat_Proxy(
  _In_  IWICBitmapSource   *THIS_PTR,
  _Out_ WICPixelFormatGUID *pPixelFormat
);
```



## <a name="parameters"></a><span data-ttu-id="a5b60-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5b60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5b60-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="a5b60-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5b60-108">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="a5b60-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="a5b60-109">Puntero a este objeto [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="a5b60-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="a5b60-110">*pPixelFormat* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a5b60-110">*pPixelFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5b60-111">Tipo: \**WICPixelFormatGUID \** _</span><span class="sxs-lookup"><span data-stu-id="a5b60-111">Type: \**WICPixelFormatGUID\** _</span></span>

<span data-ttu-id="a5b60-112">Puntero que recibe el GUID de formato de píxel en el que se almacena el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="a5b60-112">A pointer that receives the pixel format GUID the bitmap is stored in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5b60-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5b60-113">Return value</span></span>

<span data-ttu-id="a5b60-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="a5b60-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="a5b60-115">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a5b60-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a5b60-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a5b60-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5b60-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5b60-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a5b60-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5b60-118">Requirements</span></span>



| <span data-ttu-id="a5b60-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5b60-119">Requirement</span></span> | <span data-ttu-id="a5b60-120">Value</span><span class="sxs-lookup"><span data-stu-id="a5b60-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b60-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5b60-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a5b60-122">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a5b60-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a5b60-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5b60-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a5b60-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a5b60-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a5b60-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a5b60-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5b60-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5b60-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




