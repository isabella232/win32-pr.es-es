---
title: Función de tipo de tamaño (D2d1helper. h)
description: Crea una estructura de tamaño que almacena su ancho y alto mediante el tipo de datos especificado.
ms.assetid: 9f7e37a3-440e-40c0-a527-9fcbd207dce8
keywords:
- Size Type (función) Direct2D
topic_type:
- apiref
api_name:
- Size Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a300ab0ce7da57440516733459f703379cf5a943
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490150"
---
# <a name="sizetype-function"></a><span data-ttu-id="80878-104"><Type>Función size</span><span class="sxs-lookup"><span data-stu-id="80878-104">Size<Type> Function</span></span>

<span data-ttu-id="80878-105">Crea una estructura de tamaño que almacena su ancho y alto mediante el tipo de datos especificado.</span><span class="sxs-lookup"><span data-stu-id="80878-105">Creates a size structure that stores its width and height using the specified data type.</span></span>

``` syntax
template<typename Type>
typename TypeTraits<Type>::Size Size(
  Type width,
  Type height
);
```

## <a name="template-parameters"></a><span data-ttu-id="80878-106">Parámetros de plantilla</span><span class="sxs-lookup"><span data-stu-id="80878-106">Template Parameters</span></span>



| <span data-ttu-id="80878-107">Parámetro</span><span class="sxs-lookup"><span data-stu-id="80878-107">Parameter</span></span> | <span data-ttu-id="80878-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="80878-108">Description</span></span>                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80878-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="80878-109">Type</span></span>      | <span data-ttu-id="80878-110">El tipo de datos utilizado para almacenar el ancho y el alto del tamaño.</span><span class="sxs-lookup"><span data-stu-id="80878-110">The data type used to store the width and height of the size.</span></span> <span data-ttu-id="80878-111">Los valores posibles son FLOAT y UINT32.</span><span class="sxs-lookup"><span data-stu-id="80878-111">Possible values are FLOAT and UINT32.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="80878-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80878-112">Parameters</span></span>



| <span data-ttu-id="80878-113">Parámetro</span><span class="sxs-lookup"><span data-stu-id="80878-113">Parameter</span></span> | <span data-ttu-id="80878-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="80878-114">Description</span></span>        |
|-----------|--------------------|
| <span data-ttu-id="80878-115">width</span><span class="sxs-lookup"><span data-stu-id="80878-115">width</span></span>     | <span data-ttu-id="80878-116">Ancho del tamaño.</span><span class="sxs-lookup"><span data-stu-id="80878-116">The size's width.</span></span>  |
| <span data-ttu-id="80878-117">height</span><span class="sxs-lookup"><span data-stu-id="80878-117">height</span></span>    | <span data-ttu-id="80878-118">Alto del tamaño.</span><span class="sxs-lookup"><span data-stu-id="80878-118">The size's height.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="80878-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80878-119">Return Value</span></span>

<span data-ttu-id="80878-120">Tamaño que contiene el ancho y el alto especificados.</span><span class="sxs-lookup"><span data-stu-id="80878-120">A size that contains the specified width and height.</span></span>

## <a name="requirements"></a><span data-ttu-id="80878-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80878-121">Requirements</span></span>



| <span data-ttu-id="80878-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="80878-122">Requirement</span></span> | <span data-ttu-id="80878-123">Value</span><span class="sxs-lookup"><span data-stu-id="80878-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80878-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80878-124">Minimum supported client</span></span><br/> | <span data-ttu-id="80878-125">Windows 7, Windows Vista con SP2 y actualización de plataforma para aplicaciones de UWP de aplicaciones de escritorio de Windows Vista \[ \|\]</span><span class="sxs-lookup"><span data-stu-id="80878-125">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="80878-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80878-126">Minimum supported server</span></span><br/> | <span data-ttu-id="80878-127">Windows Server 2008 R2, Windows Server 2008 con SP2 y la actualización de la plataforma de aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="80878-127">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="80878-128">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80878-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="80878-129">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="80878-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="80878-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80878-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="80878-131"><dt>D2d1helper. h</dt></span><span class="sxs-lookup"><span data-stu-id="80878-131"><dt>D2d1helper.h</dt></span></span> </dl>                                                  |
| <span data-ttu-id="80878-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80878-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="80878-133"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80878-133"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="80878-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="80878-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80878-135"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80878-135"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

 





