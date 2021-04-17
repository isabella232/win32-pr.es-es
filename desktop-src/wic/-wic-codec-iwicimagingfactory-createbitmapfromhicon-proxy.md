---
description: Función de proxy para el método CreateBitmapFromHICON.
ms.assetid: 5df3d9d9-1b23-4f38-b97e-0b77d6db99d8
title: IWICImagingFactory_CreateBitmapFromHICON_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromHICON_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 58f9f37dc27c76a9eaa55d6baec52efbb773343e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706951"
---
# <a name="iwicimagingfactory_createbitmapfromhicon_proxy-function"></a><span data-ttu-id="8b88a-103">IWICImagingFactory \_ CreateBitmapFromHICON \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="8b88a-103">IWICImagingFactory\_CreateBitmapFromHICON\_Proxy function</span></span>

<span data-ttu-id="8b88a-104">Función de proxy para el método [**CreateBitmapFromHICON**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhicon) .</span><span class="sxs-lookup"><span data-stu-id="8b88a-104">Proxy function for the [**CreateBitmapFromHICON**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhicon) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b88a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b88a-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromHICON_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _In_  HICON              hIcon,
  _Out_ IWICBitmap         **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="8b88a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b88a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b88a-107">*pFactory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8b88a-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b88a-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="8b88a-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="8b88a-109">_hIcon \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="8b88a-109">_hIcon\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b88a-110">Tipo: **HICON**</span><span class="sxs-lookup"><span data-stu-id="8b88a-110">Type: **HICON**</span></span>

<span data-ttu-id="8b88a-111">Identificador de icono del que se va a crear el nuevo mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="8b88a-111">The icon handle to create the new bitmap from.</span></span>

</dd> <dt>

<span data-ttu-id="8b88a-112">*ppIBitmap* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8b88a-112">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b88a-113">Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="8b88a-113">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="8b88a-114">Puntero que recibe un puntero al nuevo mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="8b88a-114">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b88a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b88a-115">Return value</span></span>

<span data-ttu-id="8b88a-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8b88a-116">Type: **HRESULT**</span></span>

<span data-ttu-id="8b88a-117">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8b88a-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8b88a-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8b88a-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b88a-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8b88a-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8b88a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b88a-120">Requirements</span></span>



| <span data-ttu-id="8b88a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b88a-121">Requirement</span></span> | <span data-ttu-id="8b88a-122">Value</span><span class="sxs-lookup"><span data-stu-id="8b88a-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b88a-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b88a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8b88a-124">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8b88a-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8b88a-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b88a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8b88a-126">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8b88a-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8b88a-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8b88a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b88a-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b88a-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




