---
description: 'El método GetMediaLength2 recupera la longitud del medio de este objeto de origen. Este método es equivalente a IAMTimelineSrc:: GetMediaLength, pero toma valores REFTIME.'
ms.assetid: 96685e00-4e16-4205-a6ad-8b83cf2f8c29
title: 'IAMTimelineSrc:: GetMediaLength2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: caee510db9ddeda1923327176a634a9011601e4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689964"
---
# <a name="iamtimelinesrcgetmedialength2-method"></a><span data-ttu-id="b2eba-104">IAMTimelineSrc:: GetMediaLength2 (método)</span><span class="sxs-lookup"><span data-stu-id="b2eba-104">IAMTimelineSrc::GetMediaLength2 method</span></span>

> [!Note]  
> <span data-ttu-id="b2eba-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="b2eba-105">\[Deprecated.</span></span> <span data-ttu-id="b2eba-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b2eba-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b2eba-107">El `GetMediaLength2` método recupera la longitud del medio de este objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="b2eba-107">The `GetMediaLength2` method retrieves the media length of this source object.</span></span> <span data-ttu-id="b2eba-108">Este método es equivalente a [**IAMTimelineSrc:: GetMediaLength**](iamtimelinesrc-getmedialength.md), pero toma valores [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="b2eba-108">This method is equivalent to [**IAMTimelineSrc::GetMediaLength**](iamtimelinesrc-getmedialength.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2eba-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2eba-109">Syntax</span></span>


```C++
HRESULT GetMediaLength2(
   REFTIME *pLength
);
```



## <a name="parameters"></a><span data-ttu-id="b2eba-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2eba-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2eba-111">*pLength*</span><span class="sxs-lookup"><span data-stu-id="b2eba-111">*pLength*</span></span> 
</dt> <dd>

<span data-ttu-id="b2eba-112">Recibe la longitud del medio en segundos.</span><span class="sxs-lookup"><span data-stu-id="b2eba-112">Receives the media length in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2eba-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2eba-113">Return value</span></span>

<span data-ttu-id="b2eba-114">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="b2eba-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="b2eba-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b2eba-115">Return code</span></span>                                                                                     | <span data-ttu-id="b2eba-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2eba-116">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="b2eba-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b2eba-117"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="b2eba-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="b2eba-118">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="b2eba-119"><dt>**E \_ NOTDETERMINED**</dt></span><span class="sxs-lookup"><span data-stu-id="b2eba-119"><dt>**E\_NOTDETERMINED**</dt></span></span> </dl> | <span data-ttu-id="b2eba-120">Los tiempos de los medios no se establecen en este objeto.</span><span class="sxs-lookup"><span data-stu-id="b2eba-120">Media times are not set on this object.</span></span><br/> |
| <dl> <span data-ttu-id="b2eba-121"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="b2eba-121"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="b2eba-122">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="b2eba-122">**NULL** pointer argument.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="b2eba-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b2eba-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b2eba-124">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="b2eba-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b2eba-125">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b2eba-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b2eba-126">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b2eba-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b2eba-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2eba-127">Requirements</span></span>



| <span data-ttu-id="b2eba-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2eba-128">Requirement</span></span> | <span data-ttu-id="b2eba-129">Value</span><span class="sxs-lookup"><span data-stu-id="b2eba-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2eba-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2eba-130">Header</span></span><br/>  | <dl> <span data-ttu-id="b2eba-131"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2eba-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b2eba-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b2eba-132">Library</span></span><br/> | <dl> <span data-ttu-id="b2eba-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2eba-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2eba-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2eba-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2eba-135">**Interfaz IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="b2eba-135">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="b2eba-136">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="b2eba-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




