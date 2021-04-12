---
description: Función de proxy para el método CopyPixels.
ms.assetid: 020c11e9-0847-468e-b240-20529f6460cd
title: IWICBitmapSource_CopyPixels_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPixels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5c759bd1731e2f3cbc4da9c40cb590e0f39686de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278473"
---
# <a name="iwicbitmapsource_copypixels_proxy-function"></a><span data-ttu-id="728d8-103">Función de proxy de IWICBitmapSource \_ copyPixels \_</span><span class="sxs-lookup"><span data-stu-id="728d8-103">IWICBitmapSource\_CopyPixels\_Proxy function</span></span>

<span data-ttu-id="728d8-104">Función de proxy para el método [**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) .</span><span class="sxs-lookup"><span data-stu-id="728d8-104">Proxy function for the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="728d8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="728d8-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_CopyPixels_Proxy(
  _In_        IWICBitmapSource *THIS_PTR,
  _In_  const WICRect          *prc,
  _In_        UINT             cbStride,
  _In_        UINT             cbBufferSize,
  _Out_       BYTE             *pbBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="728d8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="728d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="728d8-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="728d8-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="728d8-108">Tipo: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="728d8-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="728d8-109">Puntero a este objeto [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="728d8-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="728d8-110">*PRC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="728d8-110">*prc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="728d8-111">Tipo: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="728d8-111">Type: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="728d8-112">Rectángulo que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="728d8-112">The rectangle to copy.</span></span> <span data-ttu-id="728d8-113">Un valor NULL especifica el mapa de bits completo.</span><span class="sxs-lookup"><span data-stu-id="728d8-113">A NULL value specifies the entire bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="728d8-114">_cbStride \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="728d8-114">_cbStride\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="728d8-115">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="728d8-115">Type: **UINT**</span></span>

<span data-ttu-id="728d8-116">El intervalo del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="728d8-116">The stride of the bitmap</span></span>

</dd> <dt>

<span data-ttu-id="728d8-117">*cbBufferSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="728d8-117">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="728d8-118">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="728d8-118">Type: **UINT**</span></span>

<span data-ttu-id="728d8-119">Tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="728d8-119">The size of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="728d8-120">*pbBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="728d8-120">*pbBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="728d8-121">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="728d8-121">Type: \**BYTE\** _</span></span>

<span data-ttu-id="728d8-122">Puntero al búfer.</span><span class="sxs-lookup"><span data-stu-id="728d8-122">A pointer to the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="728d8-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="728d8-123">Return value</span></span>

<span data-ttu-id="728d8-124">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="728d8-124">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="728d8-125">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="728d8-125">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="728d8-126">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="728d8-126">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="728d8-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="728d8-127">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="728d8-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="728d8-128">Requirements</span></span>



| <span data-ttu-id="728d8-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="728d8-129">Requirement</span></span> | <span data-ttu-id="728d8-130">Value</span><span class="sxs-lookup"><span data-stu-id="728d8-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="728d8-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="728d8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="728d8-132">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="728d8-132">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="728d8-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="728d8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="728d8-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="728d8-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="728d8-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="728d8-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="728d8-136"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="728d8-136"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




