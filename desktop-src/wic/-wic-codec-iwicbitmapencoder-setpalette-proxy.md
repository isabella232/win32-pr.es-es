---
description: 'IWICBitmapEncoder_SetPalette_Proxy función: función proxy para el método SetPalette.'
ms.assetid: d8e2c36e-6886-4959-b2a2-469bebfe1cdc
title: IWICBitmapEncoder_SetPalette_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8503698a1e91b86698ba288e56cc65e4447c906e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091183"
---
# <a name="iwicbitmapencoder_setpalette_proxy-function"></a><span data-ttu-id="d9459-103">Función \_ SetPalette Proxy de IWICBitmapEncoder \_</span><span class="sxs-lookup"><span data-stu-id="d9459-103">IWICBitmapEncoder\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="d9459-104">Función de proxy para el [**método SetPalette.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette)</span><span class="sxs-lookup"><span data-stu-id="d9459-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9459-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9459-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetPalette_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="d9459-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9459-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9459-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="d9459-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9459-108">Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="d9459-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="d9459-109">Puntero a este [**objeto IWICBitmapEncoder.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)</span><span class="sxs-lookup"><span data-stu-id="d9459-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="d9459-110">*pIPalette* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="d9459-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9459-111">Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="d9459-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="d9459-112">[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) que se usará como paleta global.</span><span class="sxs-lookup"><span data-stu-id="d9459-112">The [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) to use as the global palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9459-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9459-113">Return value</span></span>

<span data-ttu-id="d9459-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d9459-114">Type: **HRESULT**</span></span>

<span data-ttu-id="d9459-115">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d9459-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d9459-116">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="d9459-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9459-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9459-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d9459-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9459-118">Requirements</span></span>



| <span data-ttu-id="d9459-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9459-119">Requirement</span></span> | <span data-ttu-id="d9459-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d9459-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9459-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9459-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d9459-122">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d9459-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d9459-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9459-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d9459-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9459-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d9459-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d9459-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9459-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9459-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




