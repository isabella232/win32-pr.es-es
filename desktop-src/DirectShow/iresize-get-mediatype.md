---
description: El \_ método get mediatype devuelve el tipo de medio de salida actual del filtro de tamaño.
ms.assetid: b9900f7c-05f6-47e4-9cb0-683df2aea404
title: 'Método IResize:: get_MediaType (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b03bad7f8686fd580f7dd5fc347c347ade1c1c97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681022"
---
# <a name="iresizeget_mediatype-method"></a><span data-ttu-id="93924-103">IResize:: get \_ mediatype (método)</span><span class="sxs-lookup"><span data-stu-id="93924-103">IResize::get\_MediaType method</span></span>

> [!Note]  
> <span data-ttu-id="93924-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="93924-104">\[Deprecated.</span></span> <span data-ttu-id="93924-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="93924-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="93924-106">El `get_MediaType` método devuelve el tipo de medio de salida actual del filtro de tamaño.</span><span class="sxs-lookup"><span data-stu-id="93924-106">The `get_MediaType` method returns the resizer filter's current output media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="93924-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93924-107">Syntax</span></span>


```C++
HRESULT get_MediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="93924-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="93924-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93924-109">*pago* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="93924-109">*pmt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93924-110">Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) asignada por el llamador.</span><span class="sxs-lookup"><span data-stu-id="93924-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure allocated by the caller.</span></span> <span data-ttu-id="93924-111">El método rellena esta estructura con el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="93924-111">The method fills this structure with the media type.</span></span> <span data-ttu-id="93924-112">El llamador debe liberar el bloque de formato, si lo hay.</span><span class="sxs-lookup"><span data-stu-id="93924-112">The caller must release the format block, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93924-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93924-113">Return value</span></span>

<span data-ttu-id="93924-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="93924-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="93924-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="93924-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="93924-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93924-116">Remarks</span></span>

<span data-ttu-id="93924-117">Si no se ha establecido el tipo de medio de salida, devuelve un tipo de medio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="93924-117">If the output media type has not been set, return a default media type.</span></span> <span data-ttu-id="93924-118">El filtro debe actualizar su tipo de medio de salida cuando se llama a los métodos **Put \_ mediatype** o **Put \_ size** ; el tipo de medio devuelto por `get_MediaType` debe reflejar estos cambios.</span><span class="sxs-lookup"><span data-stu-id="93924-118">The filter must update its output media type when the **put\_MediaType** or **put\_Size** methods are called; the media type returned by `get_MediaType` must reflect these changes.</span></span>

> [!Note]  
> <span data-ttu-id="93924-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="93924-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="93924-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="93924-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="93924-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="93924-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="93924-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93924-122">Requirements</span></span>



| <span data-ttu-id="93924-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="93924-123">Requirement</span></span> | <span data-ttu-id="93924-124">Value</span><span class="sxs-lookup"><span data-stu-id="93924-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93924-125">Versión</span><span class="sxs-lookup"><span data-stu-id="93924-125">Version</span></span><br/> | <span data-ttu-id="93924-126">DirectX 9,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="93924-126">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="93924-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="93924-127">Header</span></span><br/>  | <dl> <span data-ttu-id="93924-128"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="93924-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="93924-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93924-129">Library</span></span><br/> | <dl> <span data-ttu-id="93924-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93924-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93924-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="93924-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93924-132">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="93924-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="93924-133">**Interfaz IResize**</span><span class="sxs-lookup"><span data-stu-id="93924-133">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




