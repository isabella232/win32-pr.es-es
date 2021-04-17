---
description: El \_ método get StreamLength recupera la duración de la secuencia actual.
ms.assetid: b3c13abe-cd56-4960-9862-bda47a0e87ed
title: 'Método IMediaDet:: get_StreamLength (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 61fe92fcb845a626fafc8ebb49126a35cf633aea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680893"
---
# <a name="imediadetget_streamlength-method"></a><span data-ttu-id="52a76-103">IMediaDet:: get \_ StreamLength (método)</span><span class="sxs-lookup"><span data-stu-id="52a76-103">IMediaDet::get\_StreamLength method</span></span>

> [!Note]  
> <span data-ttu-id="52a76-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="52a76-104">\[Deprecated.</span></span> <span data-ttu-id="52a76-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="52a76-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="52a76-106">El `get_StreamLength` método recupera la duración de la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="52a76-106">The `get_StreamLength` method retrieves the duration of the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="52a76-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52a76-107">Syntax</span></span>


```C++
HRESULT get_StreamLength(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="52a76-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52a76-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52a76-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="52a76-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="52a76-110">Recibe la duración de la secuencia, en segundos.</span><span class="sxs-lookup"><span data-stu-id="52a76-110">Receives the duration of the stream, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52a76-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52a76-111">Return value</span></span>

<span data-ttu-id="52a76-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="52a76-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="52a76-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="52a76-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="52a76-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52a76-114">Remarks</span></span>

<span data-ttu-id="52a76-115">Antes de llamar a este método, establezca el nombre de archivo y el flujo mediante una llamada a [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) y [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="52a76-115">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="52a76-116">Si el detector de medios está en modo de archivo de mapa de bits, este método devuelve E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="52a76-116">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="52a76-117">Para obtener más información, vea [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="52a76-117">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="52a76-118">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="52a76-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="52a76-119">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="52a76-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="52a76-120">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="52a76-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="52a76-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52a76-121">Requirements</span></span>



| <span data-ttu-id="52a76-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="52a76-122">Requirement</span></span> | <span data-ttu-id="52a76-123">Value</span><span class="sxs-lookup"><span data-stu-id="52a76-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52a76-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52a76-124">Header</span></span><br/>  | <dl> <span data-ttu-id="52a76-125"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="52a76-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="52a76-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52a76-126">Library</span></span><br/> | <dl> <span data-ttu-id="52a76-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52a76-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52a76-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="52a76-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52a76-129">**Interfaz IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="52a76-129">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="52a76-130">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="52a76-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




