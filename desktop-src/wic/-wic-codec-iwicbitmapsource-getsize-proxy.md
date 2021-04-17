---
description: Función de proxy para el método que se obtiene.
ms.assetid: a9b7d01c-78d9-47b8-a373-a7c49f7bccfd
title: IWICBitmapSource_GetSize_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetSize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 978748125b7c7f643027077182b9136b577cb00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706495"
---
# <a name="iwicbitmapsource_getsize_proxy-function"></a><span data-ttu-id="1f10a-103">\_ \_ Función de proxy de IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="1f10a-103">IWICBitmapSource\_GetSize\_Proxy function</span></span>

<span data-ttu-id="1f10a-104">Función de proxy para el método que se [**obtiene**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize) .</span><span class="sxs-lookup"><span data-stu-id="1f10a-104">Proxy function for the [**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f10a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f10a-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_GetSize_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ UINT             *puiWidth,
  _Out_ UINT             *puiHeight
);
```



## <a name="parameters"></a><span data-ttu-id="1f10a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f10a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f10a-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="1f10a-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f10a-108">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="1f10a-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="1f10a-109">Puntero a este objeto [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="1f10a-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="1f10a-110">*puiWidth* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1f10a-110">*puiWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f10a-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="1f10a-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="1f10a-112">Puntero que recibe el ancho en píxeles del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="1f10a-112">A pointer that receives the pixel width of the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="1f10a-113">_puiHeight \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1f10a-113">_puiHeight\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f10a-114">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="1f10a-114">Type: \**UINT\** _</span></span>

<span data-ttu-id="1f10a-115">Puntero que recibe el alto en píxeles del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="1f10a-115">A pointer that receives the pixel height of the bitmap</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f10a-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f10a-116">Return value</span></span>

<span data-ttu-id="1f10a-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="1f10a-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="1f10a-118">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="1f10a-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1f10a-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1f10a-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f10a-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1f10a-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="1f10a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f10a-121">Requirements</span></span>



| <span data-ttu-id="1f10a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f10a-122">Requirement</span></span> | <span data-ttu-id="1f10a-123">Value</span><span class="sxs-lookup"><span data-stu-id="1f10a-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f10a-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f10a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1f10a-125">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1f10a-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="1f10a-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f10a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1f10a-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1f10a-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="1f10a-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1f10a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f10a-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f10a-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




