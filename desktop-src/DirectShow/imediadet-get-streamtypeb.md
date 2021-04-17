---
description: El \_ método get StreamTypeB recupera una cadena que representa el GUID del tipo de medio para la secuencia actual.
ms.assetid: 99ae4b52-4449-4b7c-babf-1a6cba479499
title: 'Método IMediaDet:: get_StreamTypeB (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamTypeB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd1cdf4bbadfa769654f20792cf2fda17dbe2806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680965"
---
# <a name="imediadetget_streamtypeb-method"></a><span data-ttu-id="d7ec1-103">IMediaDet:: get \_ StreamTypeB (método)</span><span class="sxs-lookup"><span data-stu-id="d7ec1-103">IMediaDet::get\_StreamTypeB method</span></span>

> [!Note]  
> <span data-ttu-id="d7ec1-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="d7ec1-104">\[Deprecated.</span></span> <span data-ttu-id="d7ec1-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d7ec1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d7ec1-106">El `get_StreamTypeB` método recupera una cadena que representa el GUID del tipo de medio para la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="d7ec1-106">The `get_StreamTypeB` method retrieves a string representing the GUID of the media type for the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7ec1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7ec1-107">Syntax</span></span>


```C++
HRESULT get_StreamTypeB(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="d7ec1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7ec1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7ec1-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d7ec1-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d7ec1-110">Recibe una representación de cadena del GUID de tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="d7ec1-110">Receives a string representation of the media type GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7ec1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7ec1-111">Return value</span></span>

<span data-ttu-id="d7ec1-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d7ec1-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d7ec1-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d7ec1-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7ec1-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7ec1-114">Remarks</span></span>

<span data-ttu-id="d7ec1-115">El **BSTR** devuelto tiene un formato similar al siguiente: `{73647561-0000-0010-8000-00AA00389B71}`</span><span class="sxs-lookup"><span data-stu-id="d7ec1-115">The returned **BSTR** is formatted like the following: `{73647561-0000-0010-8000-00AA00389B71}`</span></span>

<span data-ttu-id="d7ec1-116">El método asigna memoria para la cadena.</span><span class="sxs-lookup"><span data-stu-id="d7ec1-116">The method allocates memory for the string.</span></span> <span data-ttu-id="d7ec1-117">La aplicación debe llamar a **SysFreeString** para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="d7ec1-117">The application must call **SysFreeString** to free the memory.</span></span>

<span data-ttu-id="d7ec1-118">Antes de llamar a este método, establezca el nombre de archivo y el flujo mediante una llamada a [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) y [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="d7ec1-118">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="d7ec1-119">Si el detector de medios está en modo de archivo de mapa de bits, este método devuelve E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="d7ec1-119">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="d7ec1-120">Para obtener más información, vea [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="d7ec1-120">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="d7ec1-121">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="d7ec1-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d7ec1-122">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d7ec1-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d7ec1-123">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d7ec1-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d7ec1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7ec1-124">Requirements</span></span>



| <span data-ttu-id="d7ec1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7ec1-125">Requirement</span></span> | <span data-ttu-id="d7ec1-126">Value</span><span class="sxs-lookup"><span data-stu-id="d7ec1-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ec1-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7ec1-127">Header</span></span><br/>  | <dl> <span data-ttu-id="d7ec1-128"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7ec1-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d7ec1-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d7ec1-129">Library</span></span><br/> | <dl> <span data-ttu-id="d7ec1-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7ec1-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7ec1-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7ec1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7ec1-132">**Interfaz IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="d7ec1-132">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="d7ec1-133">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="d7ec1-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




