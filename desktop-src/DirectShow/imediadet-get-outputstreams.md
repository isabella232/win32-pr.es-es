---
description: El \_ método get OutputStreams recupera el número de secuencias de audio y vídeo contenidas en el origen de medios. Cualquier otro tipo de flujo, como flujos de datos, se omite.
ms.assetid: 9acd0a1e-c968-4c3b-a71a-b6aa2219a8cd
title: 'Método IMediaDet:: get_OutputStreams (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_OutputStreams
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0fa53a5ab5c315c4bedb3804ae7cefa618399590
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680894"
---
# <a name="imediadetget_outputstreams-method"></a><span data-ttu-id="27190-104">IMediaDet:: get \_ OutputStreams (método)</span><span class="sxs-lookup"><span data-stu-id="27190-104">IMediaDet::get\_OutputStreams method</span></span>

> [!Note]  
> <span data-ttu-id="27190-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="27190-105">\[Deprecated.</span></span> <span data-ttu-id="27190-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="27190-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="27190-107">El `get_OutputStreams` método recupera el número de secuencias de audio y vídeo contenidas en el origen de los medios.</span><span class="sxs-lookup"><span data-stu-id="27190-107">The `get_OutputStreams` method retrieves the number of audio and video streams contained in the media source.</span></span> <span data-ttu-id="27190-108">Cualquier otro tipo de flujo, como flujos de datos, se omite.</span><span class="sxs-lookup"><span data-stu-id="27190-108">Any other stream types, such as data streams, are ignored.</span></span>

## <a name="syntax"></a><span data-ttu-id="27190-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27190-109">Syntax</span></span>


```C++
HRESULT get_OutputStreams(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="27190-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27190-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27190-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="27190-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="27190-112">Recibe el número de flujos de salida.</span><span class="sxs-lookup"><span data-stu-id="27190-112">Receives the number of output streams.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27190-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27190-113">Return value</span></span>

<span data-ttu-id="27190-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="27190-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="27190-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="27190-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="27190-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27190-116">Remarks</span></span>

<span data-ttu-id="27190-117">Antes de llamar a este método, llame a [**IMediaDet::p \_ nombre**](imediadet-put-filename.md) de archivo UT para establecer el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="27190-117">Before calling this method, call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) to set the file name.</span></span> <span data-ttu-id="27190-118">Si el detector de medios está en modo de archivo de mapa de bits, este método devuelve E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="27190-118">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="27190-119">Para obtener más información, vea [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="27190-119">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="27190-120">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="27190-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="27190-121">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="27190-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="27190-122">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="27190-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="27190-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27190-123">Requirements</span></span>



| <span data-ttu-id="27190-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="27190-124">Requirement</span></span> | <span data-ttu-id="27190-125">Value</span><span class="sxs-lookup"><span data-stu-id="27190-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27190-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27190-126">Header</span></span><br/>  | <dl> <span data-ttu-id="27190-127"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="27190-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="27190-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="27190-128">Library</span></span><br/> | <dl> <span data-ttu-id="27190-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27190-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27190-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="27190-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27190-131">**Interfaz IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="27190-131">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="27190-132">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="27190-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




