---
description: 'IWICBitmap_SetPalette_Proxy función: función proxy para el método SetPalette.'
ms.assetid: 3fd60833-7f21-4654-883a-2dd88c403bc8
title: IWICBitmap_SetPalette_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fc8d6181cf9fe9313755fd52d54319f266f4cae6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086413"
---
# <a name="iwicbitmap_setpalette_proxy-function"></a><span data-ttu-id="db1c2-103">Función \_ SetPalette Proxy de IWICBitmap \_</span><span class="sxs-lookup"><span data-stu-id="db1c2-103">IWICBitmap\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="db1c2-104">Función de proxy para el [**método SetPalette.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette)</span><span class="sxs-lookup"><span data-stu-id="db1c2-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="db1c2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db1c2-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetPalette_Proxy(
  _In_ IWICBitmap  *THIS_PTR,
  _In_ IWICPalette *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="db1c2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db1c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db1c2-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="db1c2-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db1c2-108">Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span><span class="sxs-lookup"><span data-stu-id="db1c2-108">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span></span>

<span data-ttu-id="db1c2-109">Puntero a este [**objeto IWICBitmap.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)</span><span class="sxs-lookup"><span data-stu-id="db1c2-109">Pointer to this [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="db1c2-110">*pIPalette* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="db1c2-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db1c2-111">Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="db1c2-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="db1c2-112">Paleta que se usará para la conversión.</span><span class="sxs-lookup"><span data-stu-id="db1c2-112">The palette to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db1c2-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db1c2-113">Return value</span></span>

<span data-ttu-id="db1c2-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="db1c2-114">Type: **HRESULT**</span></span>

<span data-ttu-id="db1c2-115">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="db1c2-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="db1c2-116">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="db1c2-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="db1c2-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db1c2-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="db1c2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db1c2-118">Requirements</span></span>



| <span data-ttu-id="db1c2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="db1c2-119">Requirement</span></span> | <span data-ttu-id="db1c2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="db1c2-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db1c2-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db1c2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="db1c2-122">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="db1c2-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="db1c2-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db1c2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="db1c2-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="db1c2-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="db1c2-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="db1c2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db1c2-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="db1c2-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




