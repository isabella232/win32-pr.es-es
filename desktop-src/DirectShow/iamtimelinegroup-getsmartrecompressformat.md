---
description: El método GetSmartRecompressFormat recupera el formato de compresión actual para la recompresión inteligente.
ms.assetid: 2d420fe9-691d-4cc9-a8de-363a4be1b364
title: 'IAMTimelineGroup:: GetSmartRecompressFormat (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8560bb9d8da6904cf74b62ffd238b234e9c74ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690485"
---
# <a name="iamtimelinegroupgetsmartrecompressformat-method"></a><span data-ttu-id="e103b-103">IAMTimelineGroup:: GetSmartRecompressFormat (método)</span><span class="sxs-lookup"><span data-stu-id="e103b-103">IAMTimelineGroup::GetSmartRecompressFormat method</span></span>

> [!Note]  
> <span data-ttu-id="e103b-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="e103b-104">\[Deprecated.</span></span> <span data-ttu-id="e103b-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e103b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e103b-106">El `GetSmartRecompressFormat` método recupera el formato de compresión actual para la recompresión inteligente.</span><span class="sxs-lookup"><span data-stu-id="e103b-106">The `GetSmartRecompressFormat` method retrieves the current compression format for smart recompression.</span></span>

## <a name="syntax"></a><span data-ttu-id="e103b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e103b-107">Syntax</span></span>


```C++
HRESULT GetSmartRecompressFormat(
   long **ppFormat
);
```



## <a name="parameters"></a><span data-ttu-id="e103b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e103b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e103b-109">*ppFormat*</span><span class="sxs-lookup"><span data-stu-id="e103b-109">*ppFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="e103b-110">Recibe un puntero a una estructura [**SCompFmt0**](scompfmt0.md) , convertido en un puntero a un valor Long.</span><span class="sxs-lookup"><span data-stu-id="e103b-110">Receives a pointer to an [**SCompFmt0**](scompfmt0.md) structure, cast as a pointer to a long.</span></span> <span data-ttu-id="e103b-111">Si se produce un error en el método, el valor se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="e103b-111">If the method fails, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e103b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e103b-112">Return value</span></span>

<span data-ttu-id="e103b-113">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="e103b-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e103b-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e103b-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e103b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e103b-115">Remarks</span></span>

<span data-ttu-id="e103b-116">Si la aplicación no ha establecido un formato de compresión inteligente (llamando a [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)), el formato devuelto por este método no será válido.</span><span class="sxs-lookup"><span data-stu-id="e103b-116">If the application has not set a smart compression format (by calling [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)), the format returned by this method will be invalid.</span></span> <span data-ttu-id="e103b-117">Llame al método [**IAMTimelineGroup:: IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) para determinar si se ha establecido un formato de compresión.</span><span class="sxs-lookup"><span data-stu-id="e103b-117">Call the [**IAMTimelineGroup::IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) method to determine whether a compression format was set.</span></span>

<span data-ttu-id="e103b-118">Si el método se ejecuta correctamente, el llamador debe liberar el tipo de medio devuelto y eliminar la estructura [**SCompFmt0**](scompfmt0.md) :</span><span class="sxs-lookup"><span data-stu-id="e103b-118">If the method succeeds, the caller must free the returned media type and delete the [**SCompFmt0**](scompfmt0.md) structure:</span></span>


```C++
if (pFormat) {
    FreeMediaType(pFormat->MediaType);
    delete pFormat;
}
```



> [!Note]  
> <span data-ttu-id="e103b-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="e103b-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e103b-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e103b-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e103b-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e103b-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e103b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e103b-122">Requirements</span></span>



| <span data-ttu-id="e103b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e103b-123">Requirement</span></span> | <span data-ttu-id="e103b-124">Value</span><span class="sxs-lookup"><span data-stu-id="e103b-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e103b-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e103b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e103b-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="e103b-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e103b-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e103b-127">Library</span></span><br/> | <dl> <span data-ttu-id="e103b-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e103b-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e103b-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e103b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e103b-130">**Interfaz IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="e103b-130">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="e103b-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="e103b-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




