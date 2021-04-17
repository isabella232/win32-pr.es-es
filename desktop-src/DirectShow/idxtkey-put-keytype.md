---
description: El \_ método put KeyType especifica el tipo de clave.
ms.assetid: 4a6201e6-1939-4da6-8c9f-1c34b9713ecb
title: 'IDxtKey: método de ut_KeyType de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8e5e501c1f678adb857e39d579fbd958127652a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679412"
---
# <a name="idxtkeyput_keytype-method"></a><span data-ttu-id="fb19b-103">IDxtKey: \_ método KeyType:p UT</span><span class="sxs-lookup"><span data-stu-id="fb19b-103">IDxtKey::put\_KeyType method</span></span>

> [!Note]  
> <span data-ttu-id="fb19b-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="fb19b-104">\[Deprecated.</span></span> <span data-ttu-id="fb19b-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fb19b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fb19b-106">El `put_KeyType` método especifica el tipo de clave.</span><span class="sxs-lookup"><span data-stu-id="fb19b-106">The `put_KeyType` method specifies the type of key.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb19b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb19b-107">Syntax</span></span>


```C++
HRESULT put_KeyType(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="fb19b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb19b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb19b-109">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb19b-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb19b-110">Especifica el tipo de clave.</span><span class="sxs-lookup"><span data-stu-id="fb19b-110">Specifies the key type.</span></span> <span data-ttu-id="fb19b-111">Este parámetro debe ser uno de los siguientes valores de enumeración.</span><span class="sxs-lookup"><span data-stu-id="fb19b-111">This parameter must be one of the following enumeration values.</span></span>



| <span data-ttu-id="fb19b-112">Value</span><span class="sxs-lookup"><span data-stu-id="fb19b-112">Value</span></span>             | <span data-ttu-id="fb19b-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb19b-113">Description</span></span>                                           |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="fb19b-114">DXTKEY \_ RGB</span><span class="sxs-lookup"><span data-stu-id="fb19b-114">DXTKEY\_RGB</span></span>       | <span data-ttu-id="fb19b-115">Clave cromada.</span><span class="sxs-lookup"><span data-stu-id="fb19b-115">Chroma key.</span></span> <span data-ttu-id="fb19b-116">(Clave en valor RGB).</span><span class="sxs-lookup"><span data-stu-id="fb19b-116">(Key on RGB value.)</span></span>                       |
| <span data-ttu-id="fb19b-117">DXTKEY \_ NONRED</span><span class="sxs-lookup"><span data-stu-id="fb19b-117">DXTKEY\_NONRED</span></span>    | <span data-ttu-id="fb19b-118">Clave Nonred.</span><span class="sxs-lookup"><span data-stu-id="fb19b-118">Nonred key.</span></span> <span data-ttu-id="fb19b-119">(Hace que las áreas azules y verdes sean transparentes).</span><span class="sxs-lookup"><span data-stu-id="fb19b-119">(Makes blue and green areas transparent.)</span></span> |
| <span data-ttu-id="fb19b-120">\_luminancia DXTKEY</span><span class="sxs-lookup"><span data-stu-id="fb19b-120">DXTKEY\_LUMINANCE</span></span> | <span data-ttu-id="fb19b-121">Clave de luminancia.</span><span class="sxs-lookup"><span data-stu-id="fb19b-121">Luminance key.</span></span>                                        |
| <span data-ttu-id="fb19b-122">\_alfa DXTKEY</span><span class="sxs-lookup"><span data-stu-id="fb19b-122">DXTKEY\_ALPHA</span></span>     | <span data-ttu-id="fb19b-123">Clave por valor alfa.</span><span class="sxs-lookup"><span data-stu-id="fb19b-123">Key by alpha value.</span></span>                                   |
| <span data-ttu-id="fb19b-124">\_matiz DXTKEY</span><span class="sxs-lookup"><span data-stu-id="fb19b-124">DXTKEY\_HUE</span></span>       | <span data-ttu-id="fb19b-125">Clave por matiz.</span><span class="sxs-lookup"><span data-stu-id="fb19b-125">Key by hue.</span></span>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb19b-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb19b-126">Return value</span></span>

<span data-ttu-id="fb19b-127">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="fb19b-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fb19b-128">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fb19b-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb19b-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb19b-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fb19b-130">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="fb19b-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fb19b-131">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fb19b-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fb19b-132">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="fb19b-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fb19b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb19b-133">Requirements</span></span>



| <span data-ttu-id="fb19b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb19b-134">Requirement</span></span> | <span data-ttu-id="fb19b-135">Value</span><span class="sxs-lookup"><span data-stu-id="fb19b-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb19b-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb19b-136">Header</span></span><br/>  | <dl> <span data-ttu-id="fb19b-137"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb19b-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fb19b-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb19b-138">Library</span></span><br/> | <dl> <span data-ttu-id="fb19b-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb19b-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb19b-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb19b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb19b-141">**Interfaz IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="fb19b-141">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> </dl>

 

 




