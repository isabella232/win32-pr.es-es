---
description: 'IWICBitmapClipper_Initialize_Proxy función: función proxy para el método Initialize.'
ms.assetid: 60925f5c-aca4-4f49-96d2-9b58d8310e3c
title: IWICBitmapClipper_Initialize_Proxy función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapClipper_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ce3c745d27928765fdfdf664c423f7e2146cbd5f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086393"
---
# <a name="iwicbitmapclipper_initialize_proxy-function"></a><span data-ttu-id="45deb-103">IWICBitmapClipper \_ Initialize \_ Proxy function</span><span class="sxs-lookup"><span data-stu-id="45deb-103">IWICBitmapClipper\_Initialize\_Proxy function</span></span>

<span data-ttu-id="45deb-104">Función de proxy para el [**método Initialize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize)</span><span class="sxs-lookup"><span data-stu-id="45deb-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="45deb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45deb-105">Syntax</span></span>


```C++
HRESULT IWICBitmapClipper_Initialize_Proxy(
  _In_       IWICBitmapClipper *THIS_PTR,
  _In_       IWICBitmapSource  *pISource,
  _In_ const WICRect           *prc
);
```



## <a name="parameters"></a><span data-ttu-id="45deb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45deb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45deb-107">*THIS \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="45deb-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45deb-108">Tipo: **[ **IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\***</span><span class="sxs-lookup"><span data-stu-id="45deb-108">Type: **[**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\***</span></span>

<span data-ttu-id="45deb-109">Puntero a este [**objeto IWICBitmapClipper.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)</span><span class="sxs-lookup"><span data-stu-id="45deb-109">Pointer to this [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) object.</span></span>

</dd> <dt>

<span data-ttu-id="45deb-110">*pISource* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="45deb-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45deb-111">Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="45deb-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="45deb-112">Origen del mapa de bits de entrada.</span><span class="sxs-lookup"><span data-stu-id="45deb-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="45deb-113">*prc* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="45deb-113">*prc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45deb-114">Tipo: **const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \***</span><span class="sxs-lookup"><span data-stu-id="45deb-114">Type: **const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\***</span></span>

<span data-ttu-id="45deb-115">Rectángulo del origen de mapa de bits que se recortará.</span><span class="sxs-lookup"><span data-stu-id="45deb-115">The rectangle of the bitmap source to clip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45deb-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45deb-116">Return value</span></span>

<span data-ttu-id="45deb-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="45deb-117">Type: **HRESULT**</span></span>

<span data-ttu-id="45deb-118">Si esta función se realiza correctamente, devuelve **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="45deb-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="45deb-119">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="45deb-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="45deb-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45deb-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="45deb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45deb-121">Requirements</span></span>



| <span data-ttu-id="45deb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="45deb-122">Requirement</span></span> | <span data-ttu-id="45deb-123">Valor</span><span class="sxs-lookup"><span data-stu-id="45deb-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45deb-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45deb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="45deb-125">Windows XP con SP2, solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="45deb-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="45deb-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45deb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="45deb-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="45deb-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="45deb-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="45deb-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45deb-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span><span class="sxs-lookup"><span data-stu-id="45deb-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




