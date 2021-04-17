---
description: El método SetMediaLength especifica la duración del archivo de código fuente.
ms.assetid: 0a68ad50-91d5-4cb3-95ef-35b9460ac3e4
title: 'IAMTimelineSrc:: SetMediaLength (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d585e9076606a77c8ecd03701ad41ab421eacd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690937"
---
# <a name="iamtimelinesrcsetmedialength-method"></a><span data-ttu-id="b78b3-103">IAMTimelineSrc:: SetMediaLength (método)</span><span class="sxs-lookup"><span data-stu-id="b78b3-103">IAMTimelineSrc::SetMediaLength method</span></span>

> [!Note]  
> <span data-ttu-id="b78b3-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="b78b3-104">\[Deprecated.</span></span> <span data-ttu-id="b78b3-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b78b3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b78b3-106">El `SetMediaLength` método especifica la duración del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="b78b3-106">The `SetMediaLength` method specifies the duration of the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b78b3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b78b3-107">Syntax</span></span>


```C++
HRESULT SetMediaLength(
   REFERENCE_TIME Length
);
```



## <a name="parameters"></a><span data-ttu-id="b78b3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b78b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b78b3-109">*Duración*</span><span class="sxs-lookup"><span data-stu-id="b78b3-109">*Length*</span></span> 
</dt> <dd>

<span data-ttu-id="b78b3-110">Longitud del medio, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="b78b3-110">Media length, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b78b3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b78b3-111">Return value</span></span>

<span data-ttu-id="b78b3-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="b78b3-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b78b3-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b78b3-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b78b3-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b78b3-114">Remarks</span></span>

<span data-ttu-id="b78b3-115">Puede evitar posibles errores de representación si establece la longitud del medio antes de establecer la hora de detención del medio.</span><span class="sxs-lookup"><span data-stu-id="b78b3-115">You can avoid potential rendering errors by setting the media length before you set the media stop time.</span></span> <span data-ttu-id="b78b3-116">Al establecer el tiempo de detención del medio, DES lo comprueba con la longitud del medio.</span><span class="sxs-lookup"><span data-stu-id="b78b3-116">When you set the media stop time, DES checks it against the media length.</span></span>

<span data-ttu-id="b78b3-117">Este método no valida el parámetro de *longitud* , pero el valor debe ser igual a la duración real del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="b78b3-117">This method does not validate the *Length* parameter, but the value must equal the actual duration of the source file.</span></span> <span data-ttu-id="b78b3-118">Obtenga la duración del archivo de origen mediante una llamada a [**IMediaDet:: get \_ StreamLength**](imediadet-get-streamlength.md).</span><span class="sxs-lookup"><span data-stu-id="b78b3-118">Obtain the source file duration by calling [**IMediaDet::get\_StreamLength**](imediadet-get-streamlength.md).</span></span>

> [!Note]  
> <span data-ttu-id="b78b3-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="b78b3-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b78b3-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b78b3-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b78b3-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b78b3-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b78b3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b78b3-122">Requirements</span></span>



| <span data-ttu-id="b78b3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b78b3-123">Requirement</span></span> | <span data-ttu-id="b78b3-124">Value</span><span class="sxs-lookup"><span data-stu-id="b78b3-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b78b3-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b78b3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b78b3-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="b78b3-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b78b3-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b78b3-127">Library</span></span><br/> | <dl> <span data-ttu-id="b78b3-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b78b3-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b78b3-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b78b3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b78b3-130">**Interfaz IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="b78b3-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="b78b3-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="b78b3-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




