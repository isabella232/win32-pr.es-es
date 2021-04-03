---
description: La interfaz ID3DXLine implementa el dibujo de línea mediante triángulos con textura.
ms.assetid: 87472618-d3e4-4008-9009-ae17fc7b696d
title: Interfaz ID3DXLine (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1c535ff736e9a26e8316e4715f4be4022a6417df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083816"
---
# <a name="id3dxline-interface"></a><span data-ttu-id="76d4a-103">Interfaz ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="76d4a-103">ID3DXLine interface</span></span>

<span data-ttu-id="76d4a-104">La interfaz ID3DXLine implementa el dibujo de línea mediante triángulos con textura.</span><span class="sxs-lookup"><span data-stu-id="76d4a-104">The ID3DXLine interface implements line drawing using textured triangles.</span></span>

## <a name="members"></a><span data-ttu-id="76d4a-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="76d4a-105">Members</span></span>

<span data-ttu-id="76d4a-106">La interfaz **ID3DXLine** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="76d4a-106">The **ID3DXLine** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="76d4a-107">**ID3DXLine** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="76d4a-107">**ID3DXLine** also has these types of members:</span></span>

-   [<span data-ttu-id="76d4a-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="76d4a-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="76d4a-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="76d4a-109">Methods</span></span>

<span data-ttu-id="76d4a-110">La interfaz **ID3DXLine** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="76d4a-110">The **ID3DXLine** interface has these methods.</span></span>



| <span data-ttu-id="76d4a-111">Método</span><span class="sxs-lookup"><span data-stu-id="76d4a-111">Method</span></span>                                                | <span data-ttu-id="76d4a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="76d4a-112">Description</span></span>                                                                                                                                                                                      |
|:------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76d4a-113">**Comenzar**</span><span class="sxs-lookup"><span data-stu-id="76d4a-113">**Begin**</span></span>](id3dxline--begin.md)                     | <span data-ttu-id="76d4a-114">Prepara un dispositivo para dibujar líneas.</span><span class="sxs-lookup"><span data-stu-id="76d4a-114">Prepares a device for drawing lines.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="76d4a-115">**Dibujar**</span><span class="sxs-lookup"><span data-stu-id="76d4a-115">**Draw**</span></span>](id3dxline--draw.md)                       | <span data-ttu-id="76d4a-116">Dibuja una franja de líneas en el espacio de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="76d4a-116">Draws a line strip in screen space.</span></span> <span data-ttu-id="76d4a-117">La entrada está en forma de una matriz que define los puntos (de [**D3DXVECTOR2**](d3dxvector2.md)) en la franja de línea.</span><span class="sxs-lookup"><span data-stu-id="76d4a-117">Input is in the form of an array that defines points (of [**D3DXVECTOR2**](d3dxvector2.md)) on the line strip.</span></span><br/>                                   |
| [<span data-ttu-id="76d4a-118">**DrawTransform**</span><span class="sxs-lookup"><span data-stu-id="76d4a-118">**DrawTransform**</span></span>](id3dxline--drawtransform.md)     | <span data-ttu-id="76d4a-119">Dibuja una franja de líneas en el espacio de la pantalla con una matriz de transformación de entrada especificada.</span><span class="sxs-lookup"><span data-stu-id="76d4a-119">Draws a line strip in screen space with a specified input transformation matrix.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="76d4a-120">**Fin**</span><span class="sxs-lookup"><span data-stu-id="76d4a-120">**End**</span></span>](id3dxline--end.md)                         | <span data-ttu-id="76d4a-121">Restaura el estado del dispositivo al modo en que se encontraba cuando se llamó a [**ID3DXLine:: Begin**](id3dxline--begin.md) .</span><span class="sxs-lookup"><span data-stu-id="76d4a-121">Restores the device state to how it was when [**ID3DXLine::Begin**](id3dxline--begin.md) was called.</span></span><br/>                                                                                 |
| [<span data-ttu-id="76d4a-122">**GetAntialias**</span><span class="sxs-lookup"><span data-stu-id="76d4a-122">**GetAntialias**</span></span>](id3dxline--getantialias.md)       | <span data-ttu-id="76d4a-123">Obtiene el estado de suavizado de línea.</span><span class="sxs-lookup"><span data-stu-id="76d4a-123">Gets the line antialiasing state.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="76d4a-124">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="76d4a-124">**GetDevice**</span></span>](id3dxline--getdevice.md)             | <span data-ttu-id="76d4a-125">Recupera el dispositivo Direct3D asociado al objeto de línea.</span><span class="sxs-lookup"><span data-stu-id="76d4a-125">Retrieves the Direct3D device associated with the line object.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="76d4a-126">**GetGLLines**</span><span class="sxs-lookup"><span data-stu-id="76d4a-126">**GetGLLines**</span></span>](id3dxline--getgllines.md)           | <span data-ttu-id="76d4a-127">Obtiene el modo de dibujo de líneas de estilo OpenGL.</span><span class="sxs-lookup"><span data-stu-id="76d4a-127">Gets the OpenGL-style line-drawing mode.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="76d4a-128">**GetPattern**</span><span class="sxs-lookup"><span data-stu-id="76d4a-128">**GetPattern**</span></span>](id3dxline--getpattern.md)           | <span data-ttu-id="76d4a-129">Obtiene el patrón punteado de línea.</span><span class="sxs-lookup"><span data-stu-id="76d4a-129">Gets the line stipple pattern.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="76d4a-130">**GetPatternScale**</span><span class="sxs-lookup"><span data-stu-id="76d4a-130">**GetPatternScale**</span></span>](id3dxline--getpatternscale.md) | <span data-ttu-id="76d4a-131">Obtiene el valor de escala del patrón punteado.</span><span class="sxs-lookup"><span data-stu-id="76d4a-131">Gets the stipple-pattern scale value.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="76d4a-132">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="76d4a-132">**GetWidth**</span></span>](id3dxline--getwidth.md)               | <span data-ttu-id="76d4a-133">Obtiene el grosor de la línea.</span><span class="sxs-lookup"><span data-stu-id="76d4a-133">Gets the thickness of the line.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="76d4a-134">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="76d4a-134">**OnLostDevice**</span></span>](id3dxline--onlostdevice.md)       | <span data-ttu-id="76d4a-135">Utilice este método para liberar todas las referencias a los recursos de memoria de vídeo y eliminar todos los stateblocks.</span><span class="sxs-lookup"><span data-stu-id="76d4a-135">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="76d4a-136">Se debe llamar a este método cada vez que se pierde un dispositivo o antes de restablecer un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="76d4a-136">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="76d4a-137">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="76d4a-137">**OnResetDevice**</span></span>](id3dxline--onresetdevice.md)     | <span data-ttu-id="76d4a-138">Use este método para volver a adquirir recursos y guardar el estado inicial.</span><span class="sxs-lookup"><span data-stu-id="76d4a-138">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="76d4a-139">**SetAntialias**</span><span class="sxs-lookup"><span data-stu-id="76d4a-139">**SetAntialias**</span></span>](id3dxline--setantialias.md)       | <span data-ttu-id="76d4a-140">Alterna el suavizado de contorno de línea.</span><span class="sxs-lookup"><span data-stu-id="76d4a-140">Toggles line antialiasing.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="76d4a-141">**SetGLLines**</span><span class="sxs-lookup"><span data-stu-id="76d4a-141">**SetGLLines**</span></span>](id3dxline--setgllines.md)           | <span data-ttu-id="76d4a-142">Alterna el modo para dibujar líneas de estilo OpenGL.</span><span class="sxs-lookup"><span data-stu-id="76d4a-142">Toggles the mode to draw OpenGL-style lines.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="76d4a-143">**SetPattern**</span><span class="sxs-lookup"><span data-stu-id="76d4a-143">**SetPattern**</span></span>](id3dxline--setpattern.md)           | <span data-ttu-id="76d4a-144">Aplica un patrón punteado a la línea.</span><span class="sxs-lookup"><span data-stu-id="76d4a-144">Applies a stipple pattern to the line.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="76d4a-145">**SetPatternScale**</span><span class="sxs-lookup"><span data-stu-id="76d4a-145">**SetPatternScale**</span></span>](id3dxline--setpatternscale.md) | <span data-ttu-id="76d4a-146">Estira el patrón punteado a lo largo de la dirección de la línea.</span><span class="sxs-lookup"><span data-stu-id="76d4a-146">Stretches the stipple pattern along the line direction.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="76d4a-147">**SetWidth**</span><span class="sxs-lookup"><span data-stu-id="76d4a-147">**SetWidth**</span></span>](id3dxline--setwidth.md)               | <span data-ttu-id="76d4a-148">Especifica el grosor de la línea.</span><span class="sxs-lookup"><span data-stu-id="76d4a-148">Specifies the thickness of the line.</span></span><br/>                                                                                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="76d4a-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76d4a-149">Remarks</span></span>

<span data-ttu-id="76d4a-150">Cree un objeto de dibujo de línea con [**D3DXCreateLine**](d3dxcreateline.md).</span><span class="sxs-lookup"><span data-stu-id="76d4a-150">Create a line drawing object with [**D3DXCreateLine**](d3dxcreateline.md).</span></span>

<span data-ttu-id="76d4a-151">El tipo LPD3DXLINE se define como un puntero a la interfaz **ID3DXLine** .</span><span class="sxs-lookup"><span data-stu-id="76d4a-151">The LPD3DXLINE type is defined as a pointer to the **ID3DXLine** interface.</span></span>


```
typedef interface ID3DXLine ID3DXLine;
typedef interface ID3DXLine *LPD3DXLINE;
```



## <a name="requirements"></a><span data-ttu-id="76d4a-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76d4a-152">Requirements</span></span>



| <span data-ttu-id="76d4a-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="76d4a-153">Requirement</span></span> | <span data-ttu-id="76d4a-154">Value</span><span class="sxs-lookup"><span data-stu-id="76d4a-154">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76d4a-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="76d4a-155">Header</span></span><br/>  | <dl> <span data-ttu-id="76d4a-156"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="76d4a-156"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="76d4a-157">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="76d4a-157">Library</span></span><br/> | <dl> <span data-ttu-id="76d4a-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76d4a-158"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="76d4a-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="76d4a-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76d4a-160">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="76d4a-160">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
