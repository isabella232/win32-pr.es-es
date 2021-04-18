---
description: Función de proxy para el método SetResolution.
ms.assetid: c4e3927c-6f9d-401d-acd7-711674cdbb53
title: IWICBitmap_SetResolution_Proxy función)
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
ms.openlocfilehash: eef599147a67986c6b9853f7a67e53a15be68e00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715070"
---
# <a name="iwicbitmap_setresolution_proxy-function"></a><span data-ttu-id="7113e-103">IWICBitmap \_ SetResolution \_ función proxy</span><span class="sxs-lookup"><span data-stu-id="7113e-103">IWICBitmap\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="7113e-104">Función de proxy para el método [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) .</span><span class="sxs-lookup"><span data-stu-id="7113e-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7113e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7113e-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetResolution_Proxy(
  _In_ IWICBitmap *THIS_PTR,
  _In_ double     dpiX,
  _In_ double     dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="7113e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7113e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7113e-107">*Este \_ PTR* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="7113e-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7113e-108">Tipo: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _</span><span class="sxs-lookup"><span data-stu-id="7113e-108">Type: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\** _</span></span>

<span data-ttu-id="7113e-109">Puntero a este objeto [_ *IWICBitmap* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="7113e-109">Pointer to this [_ *IWICBitmap*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="7113e-110">*dpiX* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7113e-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7113e-111">Tipo: **Double**</span><span class="sxs-lookup"><span data-stu-id="7113e-111">Type: **double**</span></span>

<span data-ttu-id="7113e-112">Resolución horizontal.</span><span class="sxs-lookup"><span data-stu-id="7113e-112">The horizontal resolution.</span></span>

</dd> <dt>

<span data-ttu-id="7113e-113">*dpiY* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7113e-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7113e-114">Tipo: **Double**</span><span class="sxs-lookup"><span data-stu-id="7113e-114">Type: **double**</span></span>

<span data-ttu-id="7113e-115">Resolución vertical.</span><span class="sxs-lookup"><span data-stu-id="7113e-115">The vertical resolution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7113e-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7113e-116">Return value</span></span>

<span data-ttu-id="7113e-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7113e-117">Type: **HRESULT**</span></span>

<span data-ttu-id="7113e-118">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="7113e-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7113e-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7113e-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7113e-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7113e-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="7113e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7113e-121">Requirements</span></span>



| <span data-ttu-id="7113e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7113e-122">Requirement</span></span> | <span data-ttu-id="7113e-123">Value</span><span class="sxs-lookup"><span data-stu-id="7113e-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7113e-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7113e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7113e-125">Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7113e-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="7113e-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7113e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7113e-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7113e-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="7113e-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7113e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7113e-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7113e-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




