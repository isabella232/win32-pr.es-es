---
description: El \_ método put mediatype establece el tipo de medio de salida en el filtro de tamaño.
ms.assetid: e213179e-cc88-4365-aaa0-51d4b9c97476
title: 'IResize: método de ut_MediaType de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aedaced5033c229131f548e298217e3c77ff70c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679456"
---
# <a name="iresizeput_mediatype-method"></a><span data-ttu-id="a790a-103">IResize::p el \_ método UT mediatype</span><span class="sxs-lookup"><span data-stu-id="a790a-103">IResize::put\_MediaType method</span></span>

> [!Note]  
> <span data-ttu-id="a790a-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="a790a-104">\[Deprecated.</span></span> <span data-ttu-id="a790a-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a790a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a790a-106">El `put_MediaType` método establece el tipo de medio de salida en el filtro de tamaño.</span><span class="sxs-lookup"><span data-stu-id="a790a-106">The `put_MediaType` method sets the output media type on the resizer filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a790a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a790a-107">Syntax</span></span>


```C++
HRESULT put_MediaType(
  [in] const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="a790a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a790a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a790a-109">*pago* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a790a-109">*pmt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a790a-110">Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que contiene el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="a790a-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that contains the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a790a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a790a-111">Return value</span></span>

<span data-ttu-id="a790a-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a790a-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a790a-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a790a-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a790a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a790a-114">Remarks</span></span>

<span data-ttu-id="a790a-115">DES llama a este método antes de conectar el PIN de salida del filtro.</span><span class="sxs-lookup"><span data-stu-id="a790a-115">DES calls this method before it connects the filter's output pin.</span></span> <span data-ttu-id="a790a-116">Use el tipo de medio como el tipo de medio del terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="a790a-116">Use the media type as the output pin's media type.</span></span> <span data-ttu-id="a790a-117">Devuelva este tipo de medio en el método [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) y compruebe agsint este tipo en el método [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) .</span><span class="sxs-lookup"><span data-stu-id="a790a-117">Return this media type in the [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method, and check agsint this type in the [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method.</span></span> <span data-ttu-id="a790a-118">DES nunca llama a este método después de que el PIN de salida esté conectado.</span><span class="sxs-lookup"><span data-stu-id="a790a-118">DES never calls this method after the output pin is connected.</span></span>

<span data-ttu-id="a790a-119">Actualmente, DES siempre establece el tipo de medio de salida en un formato RGB sin comprimir con un bloque de formato **VIDEOINFOHEADER** (el tipo de formato es igual a formato de \_ videoinfo).</span><span class="sxs-lookup"><span data-stu-id="a790a-119">Currently, DES always sets the output media type to an uncompressed RGB format with a **VIDEOINFOHEADER** format block (format type equals FORMAT\_VideoInfo).</span></span> <span data-ttu-id="a790a-120">El subtipo podría ser MEDIASUBTYPE \_ ARGB32, que indica RGB de 32 bits con un canal alfa.</span><span class="sxs-lookup"><span data-stu-id="a790a-120">The subtype might be MEDIASUBTYPE\_ARGB32, which indicates 32-bit RGB with an alpha channel.</span></span>

> [!Note]  
> <span data-ttu-id="a790a-121">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="a790a-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a790a-122">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a790a-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a790a-123">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a790a-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a790a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a790a-124">Requirements</span></span>



| <span data-ttu-id="a790a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a790a-125">Requirement</span></span> | <span data-ttu-id="a790a-126">Value</span><span class="sxs-lookup"><span data-stu-id="a790a-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a790a-127">Versión</span><span class="sxs-lookup"><span data-stu-id="a790a-127">Version</span></span><br/> | <span data-ttu-id="a790a-128">DirectX 9,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="a790a-128">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="a790a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a790a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="a790a-130"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="a790a-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a790a-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a790a-131">Library</span></span><br/> | <dl> <span data-ttu-id="a790a-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a790a-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a790a-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="a790a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a790a-134">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="a790a-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="a790a-135">**Interfaz IResize**</span><span class="sxs-lookup"><span data-stu-id="a790a-135">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




