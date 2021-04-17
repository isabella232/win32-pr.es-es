---
description: El método GetMediaLength recupera la longitud del medio de este objeto de origen.
ms.assetid: 70298d8f-67e7-4774-a7ae-f0b48e4afda7
title: 'IAMTimelineSrc:: GetMediaLength (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5cd896ed0890a199f85838a01c4c6ebec6d0895d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680419"
---
# <a name="iamtimelinesrcgetmedialength-method"></a><span data-ttu-id="c1ef9-103">IAMTimelineSrc:: GetMediaLength (método)</span><span class="sxs-lookup"><span data-stu-id="c1ef9-103">IAMTimelineSrc::GetMediaLength method</span></span>

> [!Note]  
> <span data-ttu-id="c1ef9-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="c1ef9-104">\[Deprecated.</span></span> <span data-ttu-id="c1ef9-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c1ef9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c1ef9-106">El `GetMediaLength` método recupera la longitud del medio de este objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="c1ef9-106">The `GetMediaLength` method retrieves the media length of this source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1ef9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1ef9-107">Syntax</span></span>


```C++
HRESULT GetMediaLength(
   REFERENCE_TIME *pLength
);
```



## <a name="parameters"></a><span data-ttu-id="c1ef9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1ef9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1ef9-109">*pLength*</span><span class="sxs-lookup"><span data-stu-id="c1ef9-109">*pLength*</span></span> 
</dt> <dd>

<span data-ttu-id="c1ef9-110">Recibe la longitud del medio en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="c1ef9-110">Receives the media length in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1ef9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1ef9-111">Return value</span></span>

<span data-ttu-id="c1ef9-112">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="c1ef9-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="c1ef9-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c1ef9-113">Return code</span></span>                                                                                     | <span data-ttu-id="c1ef9-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1ef9-114">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="c1ef9-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c1ef9-115"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="c1ef9-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="c1ef9-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="c1ef9-117"><dt>**E \_ NOTDETERMINED**</dt></span><span class="sxs-lookup"><span data-stu-id="c1ef9-117"><dt>**E\_NOTDETERMINED**</dt></span></span> </dl> | <span data-ttu-id="c1ef9-118">Los tiempos de los medios no se establecen en este objeto.</span><span class="sxs-lookup"><span data-stu-id="c1ef9-118">Media times are not set on this object.</span></span><br/> |
| <dl> <span data-ttu-id="c1ef9-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="c1ef9-119"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="c1ef9-120">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="c1ef9-120">**NULL** pointer argument.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="c1ef9-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1ef9-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c1ef9-122">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="c1ef9-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c1ef9-123">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c1ef9-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c1ef9-124">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c1ef9-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c1ef9-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1ef9-125">Requirements</span></span>



| <span data-ttu-id="c1ef9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1ef9-126">Requirement</span></span> | <span data-ttu-id="c1ef9-127">Value</span><span class="sxs-lookup"><span data-stu-id="c1ef9-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1ef9-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c1ef9-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c1ef9-129"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1ef9-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c1ef9-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c1ef9-130">Library</span></span><br/> | <dl> <span data-ttu-id="c1ef9-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1ef9-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1ef9-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1ef9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1ef9-133">**Interfaz IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="c1ef9-133">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="c1ef9-134">**IAMTimelineSrc::SetMediaLength**</span><span class="sxs-lookup"><span data-stu-id="c1ef9-134">**IAMTimelineSrc::SetMediaLength**</span></span>](iamtimelinesrc-setmedialength.md)
</dt> <dt>

[<span data-ttu-id="c1ef9-135">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="c1ef9-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




