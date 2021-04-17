---
description: El \_ método get StreamType recupera el identificador único global (GUID) para el tipo de medio de la secuencia actual.
ms.assetid: 2f61b3fe-c041-4031-9211-2f5fc189542b
title: 'Método IMediaDet:: get_StreamType (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5834183229580c1aadbcbe80e54a30e9b9b60c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690837"
---
# <a name="imediadetget_streamtype-method"></a><span data-ttu-id="3c6f7-103">IMediaDet:: get \_ StreamType (método)</span><span class="sxs-lookup"><span data-stu-id="3c6f7-103">IMediaDet::get\_StreamType method</span></span>

> [!Note]  
> <span data-ttu-id="3c6f7-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="3c6f7-104">\[Deprecated.</span></span> <span data-ttu-id="3c6f7-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3c6f7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3c6f7-106">El `get_StreamType` método recupera el identificador único global (GUID) para el tipo de medio de la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="3c6f7-106">The `get_StreamType` method retrieves the globally unique identifier (GUID) for the media type of the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c6f7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c6f7-107">Syntax</span></span>


```C++
HRESULT get_StreamType(
  [out, retval] GUID *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="3c6f7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c6f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c6f7-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3c6f7-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3c6f7-110">Recibe el GUID de tipo principal para el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="3c6f7-110">Receives the major type GUID for the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c6f7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c6f7-111">Return value</span></span>

<span data-ttu-id="3c6f7-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="3c6f7-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3c6f7-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3c6f7-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c6f7-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c6f7-114">Remarks</span></span>

<span data-ttu-id="3c6f7-115">Este método recupera el miembro **majortype** de la estructura [**de \_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="3c6f7-115">This method retrieves the **majortype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="3c6f7-116">La estructura de **\_ \_ tipo de medio am** describe el formato de la secuencia y el miembro **majortype** es un GUID que indica la categoría general, como audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="3c6f7-116">The **AM\_MEDIA\_TYPE** structure describes the format of the stream, and the **majortype** member is a GUID that indicates the general category, such as audio or video.</span></span> <span data-ttu-id="3c6f7-117">En el caso de una secuencia de vídeo, el GUID es el vídeo de MEDIATYPE \_ .</span><span class="sxs-lookup"><span data-stu-id="3c6f7-117">For a video stream, the GUID is MEDIATYPE\_Video.</span></span> <span data-ttu-id="3c6f7-118">En el caso de audio, es de \_ audio MEDIATYPE.</span><span class="sxs-lookup"><span data-stu-id="3c6f7-118">For audio, it is MEDIATYPE\_Audio.</span></span> <span data-ttu-id="3c6f7-119">Para recuperar toda la estructura de **\_ \_ tipo de medio am** , llame al método [**IMediaDet:: get \_ StreamMediaType**](imediadet-get-streammediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="3c6f7-119">To retrieve the entire **AM\_MEDIA\_TYPE** structure, call the [**IMediaDet::get\_StreamMediaType**](imediadet-get-streammediatype.md) method.</span></span>

<span data-ttu-id="3c6f7-120">Antes de llamar a este método, establezca el nombre de archivo y el flujo mediante una llamada a [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) y [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="3c6f7-120">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="3c6f7-121">Si el detector de medios está en modo de archivo de mapa de bits, este método devuelve E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="3c6f7-121">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="3c6f7-122">Para obtener más información, vea [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="3c6f7-122">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="3c6f7-123">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="3c6f7-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3c6f7-124">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3c6f7-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3c6f7-125">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3c6f7-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3c6f7-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c6f7-126">Requirements</span></span>



| <span data-ttu-id="3c6f7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c6f7-127">Requirement</span></span> | <span data-ttu-id="3c6f7-128">Value</span><span class="sxs-lookup"><span data-stu-id="3c6f7-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c6f7-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c6f7-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3c6f7-130"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c6f7-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3c6f7-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c6f7-131">Library</span></span><br/> | <dl> <span data-ttu-id="3c6f7-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c6f7-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c6f7-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c6f7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c6f7-134">**Interfaz IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="3c6f7-134">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="3c6f7-135">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="3c6f7-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




