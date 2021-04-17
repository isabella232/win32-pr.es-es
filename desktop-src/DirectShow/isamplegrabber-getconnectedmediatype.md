---
description: El método GetConnectedMediaType recupera el tipo de medio para la conexión en el PIN de entrada del enganche de ejemplo.
ms.assetid: 65f5603a-1151-4ffd-a662-84e265663b04
title: 'ISampleGrabber:: GetConnectedMediaType (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetConnectedMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 85e30820afdca865f438ac40521a9be540fd4a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679066"
---
# <a name="isamplegrabbergetconnectedmediatype-method"></a><span data-ttu-id="c86ef-103">ISampleGrabber:: GetConnectedMediaType (método)</span><span class="sxs-lookup"><span data-stu-id="c86ef-103">ISampleGrabber::GetConnectedMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="c86ef-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="c86ef-104">\[Deprecated.</span></span> <span data-ttu-id="c86ef-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c86ef-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c86ef-106">El `GetConnectedMediaType` método recupera el tipo de medio para la conexión en el PIN de entrada del enganche de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c86ef-106">The `GetConnectedMediaType` method retrieves the media type for the connection on the input pin of the Sample Grabber.</span></span>

## <a name="syntax"></a><span data-ttu-id="c86ef-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c86ef-107">Syntax</span></span>


```C++
HRESULT GetConnectedMediaType(
   AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a><span data-ttu-id="c86ef-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c86ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c86ef-109">*pType*</span><span class="sxs-lookup"><span data-stu-id="c86ef-109">*pType*</span></span> 
</dt> <dd>

<span data-ttu-id="c86ef-110">Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) asignada por el llamador.</span><span class="sxs-lookup"><span data-stu-id="c86ef-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure allocated by the caller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c86ef-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c86ef-111">Return value</span></span>

<span data-ttu-id="c86ef-112">Devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c86ef-112">Returns one of the following values.</span></span>



| <span data-ttu-id="c86ef-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c86ef-113">Return code</span></span>                                                                                           | <span data-ttu-id="c86ef-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="c86ef-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="c86ef-115"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="c86ef-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="c86ef-116">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="c86ef-116">**NULL** pointer argument.</span></span><br/>   |
| <dl> <span data-ttu-id="c86ef-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c86ef-117"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="c86ef-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="c86ef-118">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="c86ef-119"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="c86ef-119"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="c86ef-120">El filtro no está conectado.</span><span class="sxs-lookup"><span data-stu-id="c86ef-120">The filter is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c86ef-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c86ef-121">Remarks</span></span>

<span data-ttu-id="c86ef-122">Este método copia el tipo de medio en la estructura de **\_ \_ tipo de medio am** especificada por *pType*.</span><span class="sxs-lookup"><span data-stu-id="c86ef-122">This method copies the media type into the **AM\_MEDIA\_TYPE** structure specified by *pType*.</span></span> <span data-ttu-id="c86ef-123">El autor de la llamada debe liberar el bloque de formato del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="c86ef-123">The caller must free the format block of the media type.</span></span> <span data-ttu-id="c86ef-124">Puede usar la función **CoTaskMemFree** o la función [**FreeMediaType**](freemediatype.md) en la biblioteca de clase base.</span><span class="sxs-lookup"><span data-stu-id="c86ef-124">You can use the **CoTaskMemFree** function, or the [**FreeMediaType**](freemediatype.md) function in the base-class library.</span></span>

> [!Note]  
> <span data-ttu-id="c86ef-125">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="c86ef-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c86ef-126">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c86ef-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c86ef-127">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c86ef-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c86ef-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c86ef-128">Requirements</span></span>



| <span data-ttu-id="c86ef-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c86ef-129">Requirement</span></span> | <span data-ttu-id="c86ef-130">Value</span><span class="sxs-lookup"><span data-stu-id="c86ef-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c86ef-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c86ef-131">Header</span></span><br/>  | <dl> <span data-ttu-id="c86ef-132"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="c86ef-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c86ef-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c86ef-133">Library</span></span><br/> | <dl> <span data-ttu-id="c86ef-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c86ef-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c86ef-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c86ef-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c86ef-136">Usar el enganche de ejemplo</span><span class="sxs-lookup"><span data-stu-id="c86ef-136">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="c86ef-137">**Interfaz ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="c86ef-137">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




