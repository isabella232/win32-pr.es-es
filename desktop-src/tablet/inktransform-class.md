---
description: Representa una matriz de 3x3 que, a su vez, representa una transformación afín.
ms.assetid: 79abff2e-d1d3-4a32-9ac2-f46c1b21f742
title: Clase InkTransform (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkTransform
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 61641f0fed8ec98321e155f82ff9a35150e7fdcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717159"
---
# <a name="inktransform-class"></a><span data-ttu-id="e8d54-103">Clase InkTransform</span><span class="sxs-lookup"><span data-stu-id="e8d54-103">InkTransform class</span></span>

<span data-ttu-id="e8d54-104">Representa una matriz de 3x3 que, a su vez, representa una transformación afín.</span><span class="sxs-lookup"><span data-stu-id="e8d54-104">Represents a 3x3 matrix that, in turn, represents an affine transformation.</span></span>

<span data-ttu-id="e8d54-105">**InkTransform** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e8d54-105">**InkTransform** has these types of members:</span></span>

-   [<span data-ttu-id="e8d54-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="e8d54-106">Methods</span></span>](#methods)
-   [<span data-ttu-id="e8d54-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e8d54-107">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e8d54-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="e8d54-108">Methods</span></span>

<span data-ttu-id="e8d54-109">La clase **InkTransform** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e8d54-109">The **InkTransform** class has these methods.</span></span>



| <span data-ttu-id="e8d54-110">Método</span><span class="sxs-lookup"><span data-stu-id="e8d54-110">Method</span></span>                                                  | <span data-ttu-id="e8d54-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8d54-111">Description</span></span>                                                                                                                 |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e8d54-112">**GetTransform**</span><span class="sxs-lookup"><span data-stu-id="e8d54-112">**GetTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-gettransform)       | <span data-ttu-id="e8d54-113">Recupera el **InkTransform** como 6 flotantes.</span><span class="sxs-lookup"><span data-stu-id="e8d54-113">Retrieves the **InkTransform** as 6 floats.</span></span><br/>                                                                      |
| [<span data-ttu-id="e8d54-114">**Mostrar**</span><span class="sxs-lookup"><span data-stu-id="e8d54-114">**Reflect**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reflect)                 | <span data-ttu-id="e8d54-115">Refleja la transformación en las direcciones horizontal o vertical.</span><span class="sxs-lookup"><span data-stu-id="e8d54-115">Reflects the transform in either the horizontal or vertical directions.</span></span><br/>                                          |
| [<span data-ttu-id="e8d54-116">**Reset**</span><span class="sxs-lookup"><span data-stu-id="e8d54-116">**Reset**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reset)                     | <span data-ttu-id="e8d54-117">Restablece el estado original de la transformación.</span><span class="sxs-lookup"><span data-stu-id="e8d54-117">Resets the transform to its original state.</span></span><br/>                                                                      |
| [<span data-ttu-id="e8d54-118">**Girar**</span><span class="sxs-lookup"><span data-stu-id="e8d54-118">**Rotate**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-rotate)                   | <span data-ttu-id="e8d54-119">Gira la transformación por un ángulo medido en grados y, opcionalmente, especifica un punto central para la rotación.</span><span class="sxs-lookup"><span data-stu-id="e8d54-119">Rotates the transform by an angle measured in degrees, and optionally specifies a center point for the rotation.</span></span><br/> |
| [<span data-ttu-id="e8d54-120">**ScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="e8d54-120">**ScaleTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-scaletransform) | <span data-ttu-id="e8d54-121">Escala la transformación por factores X e y.</span><span class="sxs-lookup"><span data-stu-id="e8d54-121">Scales the transform by X and Y factors.</span></span><br/>                                                                         |
| [<span data-ttu-id="e8d54-122">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="e8d54-122">**SetTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-settransform)       | <span data-ttu-id="e8d54-123">Modifica **InkTransform** con 6 flotantes.</span><span class="sxs-lookup"><span data-stu-id="e8d54-123">Modifies the **InkTransform** using 6 floats.</span></span><br/>                                                                    |
| [<span data-ttu-id="e8d54-124">**Sesgo**</span><span class="sxs-lookup"><span data-stu-id="e8d54-124">**Shear**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-shear)                     | <span data-ttu-id="e8d54-125">Aplica un recorte con los factores horizontales y verticales especificados.</span><span class="sxs-lookup"><span data-stu-id="e8d54-125">Applies a shear with the specified horizontal and vertical factors.</span></span><br/>                                              |
| [<span data-ttu-id="e8d54-126">**Traducir**</span><span class="sxs-lookup"><span data-stu-id="e8d54-126">**Translate**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-translate)             | <span data-ttu-id="e8d54-127">Mueve la transformación por los componentes horizontal y vertical especificados.</span><span class="sxs-lookup"><span data-stu-id="e8d54-127">Moves the transform by the specified horizontal and vertical components.</span></span><br/>                                         |



 

### <a name="properties"></a><span data-ttu-id="e8d54-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e8d54-128">Properties</span></span>

<span data-ttu-id="e8d54-129">La clase **InkTransform** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e8d54-129">The **InkTransform** class has these properties.</span></span>



| <span data-ttu-id="e8d54-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e8d54-130">Property</span></span>                                     | <span data-ttu-id="e8d54-131">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="e8d54-131">Access type</span></span>           | <span data-ttu-id="e8d54-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8d54-132">Description</span></span>                                                                                          |
|:---------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e8d54-133">**Data**</span><span class="sxs-lookup"><span data-stu-id="e8d54-133">**Data**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_data)<br/> | <span data-ttu-id="e8d54-134">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e8d54-134">Read/write</span></span><br/> | <span data-ttu-id="e8d54-135">Obtiene o establece la versión de automatización del struct XFORM de WIN32.</span><span class="sxs-lookup"><span data-stu-id="e8d54-135">Gets or sets the Automation version of the WIN32 XFORM struct.</span></span><br/>                            |
| [<span data-ttu-id="e8d54-136">**eDx**</span><span class="sxs-lookup"><span data-stu-id="e8d54-136">**eDx**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edx)<br/>   | <span data-ttu-id="e8d54-137">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e8d54-137">Read/write</span></span><br/> | <span data-ttu-id="e8d54-138">Obtiene o establece el número real que especifica el elemento de la tercera fila, primera columna.</span><span class="sxs-lookup"><span data-stu-id="e8d54-138">Gets or sets the real number that specifies the element in the third row, first column.</span></span><br/>   |
| [<span data-ttu-id="e8d54-139">**eDy**</span><span class="sxs-lookup"><span data-stu-id="e8d54-139">**eDy**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edy)<br/>   | <span data-ttu-id="e8d54-140">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e8d54-140">Read/write</span></span><br/> | <span data-ttu-id="e8d54-141">Obtiene o establece el número real que especifica el elemento de la tercera fila, segunda columna.</span><span class="sxs-lookup"><span data-stu-id="e8d54-141">Gets or sets the real number that specifies the element in the third row, second column.</span></span><br/>  |
| [<span data-ttu-id="e8d54-142">**eM11**</span><span class="sxs-lookup"><span data-stu-id="e8d54-142">**eM11**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em11)<br/> | <span data-ttu-id="e8d54-143">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e8d54-143">Read/write</span></span><br/> | <span data-ttu-id="e8d54-144">Obtiene o establece el número real que especifica el elemento de la primera fila, la primera columna.</span><span class="sxs-lookup"><span data-stu-id="e8d54-144">Gets or sets the real number that specifies the element in the first row, first column.</span></span><br/>   |
| [<span data-ttu-id="e8d54-145">**eM12**</span><span class="sxs-lookup"><span data-stu-id="e8d54-145">**eM12**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em12)<br/> | <span data-ttu-id="e8d54-146">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e8d54-146">Read/write</span></span><br/> | <span data-ttu-id="e8d54-147">Obtiene o establece el número real que especifica el elemento de la primera fila, segunda columna.</span><span class="sxs-lookup"><span data-stu-id="e8d54-147">Gets or sets the real number that specifies the element in the first row, second column.</span></span><br/>  |
| [<span data-ttu-id="e8d54-148">**eM21**</span><span class="sxs-lookup"><span data-stu-id="e8d54-148">**eM21**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em21)<br/> | <span data-ttu-id="e8d54-149">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e8d54-149">Read/write</span></span><br/> | <span data-ttu-id="e8d54-150">Obtiene o establece el número real que especifica el elemento de la segunda fila, la primera columna.</span><span class="sxs-lookup"><span data-stu-id="e8d54-150">Gets or sets the real number that specifies the element in the second row, first column.</span></span><br/>  |
| [<span data-ttu-id="e8d54-151">**eM22**</span><span class="sxs-lookup"><span data-stu-id="e8d54-151">**eM22**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em22)<br/> | <span data-ttu-id="e8d54-152">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e8d54-152">Read/write</span></span><br/> | <span data-ttu-id="e8d54-153">Obtiene o establece el número real que especifica el elemento de la segunda fila, segunda columna.</span><span class="sxs-lookup"><span data-stu-id="e8d54-153">Gets or sets the real number that specifies the element in the second row, second column.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e8d54-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8d54-154">Remarks</span></span>

<span data-ttu-id="e8d54-155">Se puede crear una instancia de este objeto llamando al método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.</span><span class="sxs-lookup"><span data-stu-id="e8d54-155">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="e8d54-156">El objeto solo almacena seis de los nueve números en una matriz de 3x3 porque todas las matrices de 3x3 que representan transformaciones afines tienen la misma tercera columna (0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="e8d54-156">The object stores only six of the nine numbers in a 3x3 matrix because all 3x3 matrices that represent affine transformations have the same third column (0, 0, 1).</span></span> <span data-ttu-id="e8d54-157">A su vez, este objeto se usa para describir operaciones de transformación, como mover, distorsionar, escalar o rotar en un objeto [**InkRenderer**](inkrenderer-class.md) , un objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) o una colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e8d54-157">This object in turn is used to describe transformation operations such as moving, shearing, scaling, or rotating in an [**InkRenderer**](inkrenderer-class.md) object, [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object, or [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

> [!Note]  
> <span data-ttu-id="e8d54-158">El objeto **InkTransform** se correlaciona con la estructura [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) .</span><span class="sxs-lookup"><span data-stu-id="e8d54-158">The **InkTransform** object correlates to the [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8d54-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8d54-159">Requirements</span></span>



| <span data-ttu-id="e8d54-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8d54-160">Requirement</span></span> | <span data-ttu-id="e8d54-161">Value</span><span class="sxs-lookup"><span data-stu-id="e8d54-161">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8d54-162">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8d54-162">Minimum supported client</span></span><br/> | <span data-ttu-id="e8d54-163">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e8d54-163">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e8d54-164">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8d54-164">Minimum supported server</span></span><br/> | <span data-ttu-id="e8d54-165">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e8d54-165">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e8d54-166">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8d54-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8d54-167"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e8d54-167"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e8d54-168">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e8d54-168">Library</span></span><br/>                  | <dl> <span data-ttu-id="e8d54-169"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8d54-169"><dt>InkObj.dll</dt></span></span> </dl>                               |



 

