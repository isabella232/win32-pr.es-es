---
description: Función de proxy para el método Initialize.
ms.assetid: 60925f5c-aca4-4f49-96d2-9b58d8310e3c
title: IWICBitmapClipper_Initialize_Proxy función)
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
ms.openlocfilehash: 83c41b8802546b36ad309306ecc83a34c5d3a0c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154171"
---
# <a name="iwicbitmapclipper_initialize_proxy-function"></a><span data-ttu-id="5d41e-103">IWICBitmapClipper \_ inicializar \_ función de proxy</span><span class="sxs-lookup"><span data-stu-id="5d41e-103">IWICBitmapClipper\_Initialize\_Proxy function</span></span>

<span data-ttu-id="5d41e-104">Función de proxy para el método [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) .</span><span class="sxs-lookup"><span data-stu-id="5d41e-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d41e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d41e-105">Syntax</span></span>


```C++
HRESULT IWICBitmapClipper_Initialize_Proxy(
  _In_       IWICBitmapClipper *THIS_PTR,
  _In_       IWICBitmapSource  *pISource,
  _In_ const WICRect           *prc
);
```



## <a name="parameters"></a><span data-ttu-id="5d41e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d41e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d41e-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="5d41e-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d41e-108">Tipo: \**[**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) \** _</span><span class="sxs-lookup"><span data-stu-id="5d41e-108">Type: \**[**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\** _</span></span>

<span data-ttu-id="5d41e-109">Puntero a este objeto [_ *IWICBitmapClipper* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) .</span><span class="sxs-lookup"><span data-stu-id="5d41e-109">Pointer to this [_ *IWICBitmapClipper*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper) object.</span></span>

</dd> <dt>

<span data-ttu-id="5d41e-110">*pISource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5d41e-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d41e-111">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="5d41e-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="5d41e-112">Origen del mapa de bits de entrada.</span><span class="sxs-lookup"><span data-stu-id="5d41e-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="5d41e-113">_prc \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="5d41e-113">_prc\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d41e-114">Tipo: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="5d41e-114">Type: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="5d41e-115">Rectángulo del origen del mapa de bits que se va a recortar.</span><span class="sxs-lookup"><span data-stu-id="5d41e-115">The rectangle of the bitmap source to clip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d41e-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d41e-116">Return value</span></span>

<span data-ttu-id="5d41e-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="5d41e-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="5d41e-118">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="5d41e-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5d41e-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5d41e-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d41e-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d41e-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5d41e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d41e-121">Requirements</span></span>



| <span data-ttu-id="5d41e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d41e-122">Requirement</span></span> | <span data-ttu-id="5d41e-123">Value</span><span class="sxs-lookup"><span data-stu-id="5d41e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d41e-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d41e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5d41e-125">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5d41e-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5d41e-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d41e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5d41e-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5d41e-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5d41e-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5d41e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d41e-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d41e-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




