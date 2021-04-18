---
description: El \_ método put CurrentStream especifica el número de secuencia que va a usar el detector de medios.
ms.assetid: 01fb7ccf-9b45-434c-b574-f3027d85ea8a
title: 'IMediaDet: método de ut_CurrentStream de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_CurrentStream
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 864848f646e4a9e06ca12e2bfec742c1741d77e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679534"
---
# <a name="imediadetput_currentstream-method"></a><span data-ttu-id="08293-103">IMediaDet::p \_ método CurrentStream UT</span><span class="sxs-lookup"><span data-stu-id="08293-103">IMediaDet::put\_CurrentStream method</span></span>

> [!Note]  
> <span data-ttu-id="08293-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="08293-104">\[Deprecated.</span></span> <span data-ttu-id="08293-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="08293-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="08293-106">El `put_CurrentStream` método especifica el número de secuencia que va a usar el detector de medios.</span><span class="sxs-lookup"><span data-stu-id="08293-106">The `put_CurrentStream` method specifies the stream number for the media detector to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="08293-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08293-107">Syntax</span></span>


```C++
HRESULT put_CurrentStream(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="08293-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08293-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08293-109">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="08293-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08293-110">Número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="08293-110">Stream number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08293-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08293-111">Return value</span></span>

<span data-ttu-id="08293-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="08293-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="08293-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="08293-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="08293-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08293-114">Remarks</span></span>

<span data-ttu-id="08293-115">Antes de llamar a este método, llame a [**IMediaDet::p \_ nombre**](imediadet-put-filename.md) de archivo UT para establecer el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="08293-115">Before calling this method, call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) to set the file name.</span></span> <span data-ttu-id="08293-116">Llame a [**IMediaDet:: get \_ OutputStreams**](imediadet-get-outputstreams.md) para determinar el número de flujos contenidos en el archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="08293-116">Call [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) to determine the number of streams contained in the source file.</span></span>

<span data-ttu-id="08293-117">Si el detector de medios está en modo de archivo de mapa de bits, este método devuelve E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="08293-117">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="08293-118">Para obtener más información, vea [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="08293-118">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="08293-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="08293-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="08293-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="08293-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="08293-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="08293-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="08293-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08293-122">Requirements</span></span>



| <span data-ttu-id="08293-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="08293-123">Requirement</span></span> | <span data-ttu-id="08293-124">Value</span><span class="sxs-lookup"><span data-stu-id="08293-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08293-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08293-125">Header</span></span><br/>  | <dl> <span data-ttu-id="08293-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="08293-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="08293-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="08293-127">Library</span></span><br/> | <dl> <span data-ttu-id="08293-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08293-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08293-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="08293-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08293-130">**Interfaz IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="08293-130">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="08293-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="08293-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




