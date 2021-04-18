---
description: El método GetMediaType recupera el tipo de medio sin comprimir para el grupo.
ms.assetid: 129ed688-0f03-4ccb-b65f-d61f02cb94b2
title: 'IAMTimelineGroup:: GetMediaType (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2122b5429ffa66d278ccfe59553ac85fb0dee562
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681249"
---
# <a name="iamtimelinegroupgetmediatype-method"></a><span data-ttu-id="b55b5-103">IAMTimelineGroup:: GetMediaType (método)</span><span class="sxs-lookup"><span data-stu-id="b55b5-103">IAMTimelineGroup::GetMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="b55b5-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="b55b5-104">\[Deprecated.</span></span> <span data-ttu-id="b55b5-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b55b5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b55b5-106">El `GetMediaType` método recupera el tipo de medio sin comprimir para el grupo.</span><span class="sxs-lookup"><span data-stu-id="b55b5-106">The `GetMediaType` method retrieves the uncompressed media type for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="b55b5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b55b5-107">Syntax</span></span>


```C++
HRESULT GetMediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="b55b5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b55b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b55b5-109">*pago* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b55b5-109">*pmt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b55b5-110">Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) rellenada con el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="b55b5-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that is filled with the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b55b5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b55b5-111">Return value</span></span>

<span data-ttu-id="b55b5-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="b55b5-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b55b5-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b55b5-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b55b5-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b55b5-114">Remarks</span></span>

<span data-ttu-id="b55b5-115">El llamador debe liberar el bloque de formato del tipo de medio devuelto, dado en el miembro **pbFormat** de la estructura de tipo de medio am devuelta \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b55b5-115">The caller must free the returned media type's format block, given in the **pbFormat** member of the returned AM\_MEDIA\_TYPE structure.</span></span> <span data-ttu-id="b55b5-116">Puede usar la función auxiliar [**FreeMediaType**](freemediatype.md) de la biblioteca de clases base.</span><span class="sxs-lookup"><span data-stu-id="b55b5-116">You can use the helper function [**FreeMediaType**](freemediatype.md) from the base class library.</span></span>

> [!Note]  
> <span data-ttu-id="b55b5-117">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="b55b5-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b55b5-118">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b55b5-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b55b5-119">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b55b5-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b55b5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b55b5-120">Requirements</span></span>



| <span data-ttu-id="b55b5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b55b5-121">Requirement</span></span> | <span data-ttu-id="b55b5-122">Value</span><span class="sxs-lookup"><span data-stu-id="b55b5-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b55b5-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b55b5-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b55b5-124"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="b55b5-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b55b5-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b55b5-125">Library</span></span><br/> | <dl> <span data-ttu-id="b55b5-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b55b5-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b55b5-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b55b5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b55b5-128">**Interfaz IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="b55b5-128">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="b55b5-129">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="b55b5-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




