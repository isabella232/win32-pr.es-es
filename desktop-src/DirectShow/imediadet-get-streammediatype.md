---
description: El \_ método get StreamMediaType recupera el tipo de medio de la secuencia actual. Todas las secuencias de vídeo se convierten en tipos VIDEOINFOHEADER y todas las secuencias de audio se convierten en tipos WAVEFORMATEX.
ms.assetid: 7fc15cb3-af77-42c1-b5eb-d1d88bf9cd1d
title: 'Método IMediaDet:: get_StreamMediaType (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0c2bea0c9cad7e1a25666cc38735107e14a884ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680892"
---
# <a name="imediadetget_streammediatype-method"></a><span data-ttu-id="f1619-104">IMediaDet:: get \_ StreamMediaType (método)</span><span class="sxs-lookup"><span data-stu-id="f1619-104">IMediaDet::get\_StreamMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="f1619-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="f1619-105">\[Deprecated.</span></span> <span data-ttu-id="f1619-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f1619-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f1619-107">El `get_StreamMediaType` método recupera el tipo de medio de la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="f1619-107">The `get_StreamMediaType` method retrieves the media type of the current stream.</span></span> <span data-ttu-id="f1619-108">Todas las secuencias de vídeo se convierten en tipos [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) y todas las secuencias de audio se convierten en tipos [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f1619-108">All video streams are converted to [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) types, and all audio streams are converted to [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) types.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1619-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1619-109">Syntax</span></span>


```C++
HRESULT get_StreamMediaType(
  [out, retval] AM_MEDIA_TYPE *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="f1619-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1619-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1619-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f1619-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f1619-112">Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) rellenada con el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="f1619-112">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that is filled with the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1619-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1619-113">Return value</span></span>

<span data-ttu-id="f1619-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f1619-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f1619-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f1619-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1619-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1619-116">Remarks</span></span>

<span data-ttu-id="f1619-117">Antes de llamar a este método, establezca el nombre de archivo y el flujo mediante una llamada a [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) y [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="f1619-117">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="f1619-118">Si el detector de medios está en modo de archivo de mapa de bits, este método devuelve E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="f1619-118">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="f1619-119">Para obtener más información, vea [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="f1619-119">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="f1619-120">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="f1619-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f1619-121">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f1619-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f1619-122">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f1619-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f1619-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1619-123">Requirements</span></span>



| <span data-ttu-id="f1619-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1619-124">Requirement</span></span> | <span data-ttu-id="f1619-125">Value</span><span class="sxs-lookup"><span data-stu-id="f1619-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1619-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1619-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f1619-127"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1619-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f1619-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f1619-128">Library</span></span><br/> | <dl> <span data-ttu-id="f1619-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1619-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1619-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1619-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1619-131">**Interfaz IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="f1619-131">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="f1619-132">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="f1619-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 
