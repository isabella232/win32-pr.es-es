---
title: Función de tipo Rect (D2d1helper. h)
description: Crea una estructura de rectángulo que almacena sus coordenadas con el tipo de datos especificado.
ms.assetid: b152efaf-0779-4024-b998-82a347abba71
keywords:
- Rect (función de tipo Direct2D)
topic_type:
- apiref
api_name:
- Rect Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ed16ecd5a79c73ecb7341b9aa7f3378854dd4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658243"
---
# <a name="recttype-function"></a><span data-ttu-id="26219-104"><Type>Función Rect</span><span class="sxs-lookup"><span data-stu-id="26219-104">Rect<Type> Function</span></span>

<span data-ttu-id="26219-105">Crea una estructura de rectángulo que almacena sus coordenadas con el tipo de datos especificado.</span><span class="sxs-lookup"><span data-stu-id="26219-105">Creates a rectangle structure that stores its coordinates using the specified data type.</span></span>

``` syntax
template<typename Type>
typename TypeTraits<Type>::Rect Rect(
  Type left,
  Type top,
  Type right,
  Type bottom
);
```

## <a name="template-parameters"></a><span data-ttu-id="26219-106">Parámetros de plantilla</span><span class="sxs-lookup"><span data-stu-id="26219-106">Template Parameters</span></span>



| <span data-ttu-id="26219-107">Parámetro</span><span class="sxs-lookup"><span data-stu-id="26219-107">Parameter</span></span> | <span data-ttu-id="26219-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="26219-108">Description</span></span>                                                                                                |
|-----------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26219-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="26219-109">Type</span></span>      | <span data-ttu-id="26219-110">El tipo de datos que se usa para almacenar las dimensiones del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="26219-110">The data type used to store the dimensions of the rectangle.</span></span> <span data-ttu-id="26219-111">Los valores posibles son **float** y **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="26219-111">Possible values are **FLOAT** and **UINT32**.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="26219-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26219-112">Parameters</span></span>



| <span data-ttu-id="26219-113">Parámetro</span><span class="sxs-lookup"><span data-stu-id="26219-113">Parameter</span></span> | <span data-ttu-id="26219-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="26219-114">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="26219-115">izquierda</span><span class="sxs-lookup"><span data-stu-id="26219-115">left</span></span>      | <span data-ttu-id="26219-116">Coordenada x de la esquina superior izquierda del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="26219-116">The x-coordinate of the rectangle's upper-left corner.</span></span>  |
| <span data-ttu-id="26219-117">top</span><span class="sxs-lookup"><span data-stu-id="26219-117">top</span></span>       | <span data-ttu-id="26219-118">Coordenada y de la esquina superior izquierda del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="26219-118">The y-coordinate of the rectangle's upper-left corner.</span></span>  |
| <span data-ttu-id="26219-119">right</span><span class="sxs-lookup"><span data-stu-id="26219-119">right</span></span>     | <span data-ttu-id="26219-120">Coordenada x de la esquina inferior derecha del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="26219-120">The x-coordinate of the rectangle's lower-right corner.</span></span> |
| <span data-ttu-id="26219-121">abajo</span><span class="sxs-lookup"><span data-stu-id="26219-121">bottom</span></span>    | <span data-ttu-id="26219-122">Coordenada y de la esquina inferior derecha del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="26219-122">The y-coordinate of the rectangle's lower-right corner.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="26219-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26219-123">Return Value</span></span>

<span data-ttu-id="26219-124">Estructura de rectángulo que contiene las coordenadas especificadas.</span><span class="sxs-lookup"><span data-stu-id="26219-124">A rectangle structure that contains the specified coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="26219-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26219-125">Requirements</span></span>



| <span data-ttu-id="26219-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="26219-126">Requirement</span></span> | <span data-ttu-id="26219-127">Value</span><span class="sxs-lookup"><span data-stu-id="26219-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26219-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26219-128">Minimum supported client</span></span><br/> | <span data-ttu-id="26219-129">Windows 7, Windows Vista con SP2 y actualización de plataforma para aplicaciones de UWP de aplicaciones de escritorio de Windows Vista \[ \|\]</span><span class="sxs-lookup"><span data-stu-id="26219-129">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="26219-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26219-130">Minimum supported server</span></span><br/> | <span data-ttu-id="26219-131">Windows Server 2008 R2, Windows Server 2008 con SP2 y la actualización de la plataforma de aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="26219-131">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="26219-132">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26219-132">Minimum supported phone</span></span><br/>  | <span data-ttu-id="26219-133">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="26219-133">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="26219-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26219-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="26219-135"><dt>D2d1helper. h</dt></span><span class="sxs-lookup"><span data-stu-id="26219-135"><dt>D2d1helper.h</dt></span></span> </dl>                                                  |
| <span data-ttu-id="26219-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="26219-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="26219-137"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26219-137"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="26219-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="26219-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26219-139"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26219-139"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

 





