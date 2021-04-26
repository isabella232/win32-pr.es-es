---
description: 'Las constantes de argumento de textura se usan como valores para los siguientes miembros del tipo enumerado D3DTEXTURESTAGESTATETYPE:'
ms.assetid: 36b2b715-5ced-4246-840e-8ea343521ef4
title: D3DTA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898e1bb66f74a1087a9da186599469bb195734ce
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995292"
---
# <a name="d3dta"></a><span data-ttu-id="43a00-103">D3DTA</span><span class="sxs-lookup"><span data-stu-id="43a00-103">D3DTA</span></span>

<span data-ttu-id="43a00-104">Las constantes de argumento de textura se usan como valores para los siguientes miembros del tipo enumerado [**D3DTEXTURESTAGESTATETYPE:**](./d3dtexturestagestatetype.md)</span><span class="sxs-lookup"><span data-stu-id="43a00-104">Texture argument constants are used as values for the following members of the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type:</span></span>

-   <span data-ttu-id="43a00-105">D3DTSS \_ ALPHAARG0</span><span class="sxs-lookup"><span data-stu-id="43a00-105">D3DTSS\_ALPHAARG0</span></span>
-   <span data-ttu-id="43a00-106">D3DTSS \_ ALPHAARG1</span><span class="sxs-lookup"><span data-stu-id="43a00-106">D3DTSS\_ALPHAARG1</span></span>
-   <span data-ttu-id="43a00-107">D3DTSS \_ ALPHAARG2</span><span class="sxs-lookup"><span data-stu-id="43a00-107">D3DTSS\_ALPHAARG2</span></span>
-   <span data-ttu-id="43a00-108">D3DTSS \_ COLORARG0</span><span class="sxs-lookup"><span data-stu-id="43a00-108">D3DTSS\_COLORARG0</span></span>
-   <span data-ttu-id="43a00-109">D3DTSS \_ COLORARG1</span><span class="sxs-lookup"><span data-stu-id="43a00-109">D3DTSS\_COLORARG1</span></span>
-   <span data-ttu-id="43a00-110">D3DTSS \_ COLORARG2</span><span class="sxs-lookup"><span data-stu-id="43a00-110">D3DTSS\_COLORARG2</span></span>
-   <span data-ttu-id="43a00-111">D3DTSS \_ RESULTARG</span><span class="sxs-lookup"><span data-stu-id="43a00-111">D3DTSS\_RESULTARG</span></span>

<span data-ttu-id="43a00-112">Establezca y recupere argumentos de textura mediante una llamada a los [**métodos SetTextureStageState**](/windows/desktop/api) [**y GetTextureStageState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate)</span><span class="sxs-lookup"><span data-stu-id="43a00-112">Set and retrieve texture arguments by calling the [**SetTextureStageState**](/windows/desktop/api) and [**GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) methods.</span></span>

<span data-ttu-id="43a00-113">Marcas de argumento</span><span class="sxs-lookup"><span data-stu-id="43a00-113">Argument flags</span></span>

<span data-ttu-id="43a00-114">Puede combinar una marca de argumento con un modificador , pero no se pueden combinar dos marcas de argumento.</span><span class="sxs-lookup"><span data-stu-id="43a00-114">You can combine an argument flag with a modifier, but two argument flags cannot be combined.</span></span>



| <span data-ttu-id="43a00-115">\#Definir</span><span class="sxs-lookup"><span data-stu-id="43a00-115">\#define</span></span>          | <span data-ttu-id="43a00-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="43a00-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43a00-117">D3DTA \_ (CONSTANTE)</span><span class="sxs-lookup"><span data-stu-id="43a00-117">D3DTA\_CONSTANT</span></span>   | <span data-ttu-id="43a00-118">Seleccione una constante de una fase de textura.</span><span class="sxs-lookup"><span data-stu-id="43a00-118">Select a constant from a texture stage.</span></span> <span data-ttu-id="43a00-119">El valor predeterminado es 0xffffffff.</span><span class="sxs-lookup"><span data-stu-id="43a00-119">The default value is 0xffffffff.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="43a00-120">D3DTA \_ ACTUAL</span><span class="sxs-lookup"><span data-stu-id="43a00-120">D3DTA\_CURRENT</span></span>    | <span data-ttu-id="43a00-121">El argumento de textura es el resultado de la fase de mezcla anterior.</span><span class="sxs-lookup"><span data-stu-id="43a00-121">The texture argument is the result of the previous blending stage.</span></span> <span data-ttu-id="43a00-122">En la primera fase de textura (fase 0), este argumento es equivalente a D3DTA \_ DIFFUSE.</span><span class="sxs-lookup"><span data-stu-id="43a00-122">In the first texture stage (stage 0), this argument is equivalent to D3DTA\_DIFFUSE.</span></span> <span data-ttu-id="43a00-123">Si la fase de mezcla anterior usa una textura de mapa de protuberancia (la operación D3DTOP BUMPENVMAP), el sistema elige la textura de la fase antes de la textura del mapa de \_ protuberancia.</span><span class="sxs-lookup"><span data-stu-id="43a00-123">If the previous blending stage uses a bump-map texture (the D3DTOP\_BUMPENVMAP operation), the system chooses the texture from the stage before the bump-map texture.</span></span> <span data-ttu-id="43a00-124">Si s representa la fase de textura actual y s - 1 contiene una textura de mapa de protuberancia, este argumento se convierte en la salida del resultado por fases de textura s - 2.</span><span class="sxs-lookup"><span data-stu-id="43a00-124">If s represents the current texture stage and s - 1 contains a bump-map texture, this argument becomes the result output by texture stage s - 2.</span></span> <span data-ttu-id="43a00-125">Los permisos son de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="43a00-125">Permissions are read/write.</span></span> |
| <span data-ttu-id="43a00-126">DIFUSO D3DTA \_</span><span class="sxs-lookup"><span data-stu-id="43a00-126">D3DTA\_DIFFUSE</span></span>    | <span data-ttu-id="43a00-127">El argumento de textura es el color difuso interpolado a partir de los componentes de vértice durante el sombreado de Gouraud.</span><span class="sxs-lookup"><span data-stu-id="43a00-127">The texture argument is the diffuse color interpolated from vertex components during Gouraud shading.</span></span> <span data-ttu-id="43a00-128">Si el vértice no contiene un color difuso, el color predeterminado es 0xffffffff.</span><span class="sxs-lookup"><span data-stu-id="43a00-128">If the vertex does not contain a diffuse color, the default color is 0xffffffff.</span></span> <span data-ttu-id="43a00-129">Los permisos son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="43a00-129">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="43a00-130">D3DTA \_ SELECTMASK</span><span class="sxs-lookup"><span data-stu-id="43a00-130">D3DTA\_SELECTMASK</span></span> | <span data-ttu-id="43a00-131">Valor de máscara para todos los argumentos; no se usa al establecer argumentos de textura.</span><span class="sxs-lookup"><span data-stu-id="43a00-131">Mask value for all arguments; not used when setting texture arguments.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="43a00-132">ESPECULAR D3DTA \_</span><span class="sxs-lookup"><span data-stu-id="43a00-132">D3DTA\_SPECULAR</span></span>   | <span data-ttu-id="43a00-133">El argumento de textura es el color especular interpolado a partir de los componentes de vértice durante el sombreado de Gouraud.</span><span class="sxs-lookup"><span data-stu-id="43a00-133">The texture argument is the specular color interpolated from vertex components during Gouraud shading.</span></span> <span data-ttu-id="43a00-134">Si el vértice no contiene un color especular, el color predeterminado es 0xffffffff.</span><span class="sxs-lookup"><span data-stu-id="43a00-134">If the vertex does not contain a specular color, the default color is 0xffffffff.</span></span> <span data-ttu-id="43a00-135">Los permisos son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="43a00-135">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="43a00-136">D3DTA \_ TEMP</span><span class="sxs-lookup"><span data-stu-id="43a00-136">D3DTA\_TEMP</span></span>       | <span data-ttu-id="43a00-137">El argumento de textura es un color de registro temporal para lectura o escritura.</span><span class="sxs-lookup"><span data-stu-id="43a00-137">The texture argument is a temporary register color for read or write.</span></span> <span data-ttu-id="43a00-138">D3DTA TEMP se admite si la funcionalidad del dispositivo \_ [D3DPMISCCAPS \_ TSSARGTEMP](d3dpmisccaps.md) está presente.</span><span class="sxs-lookup"><span data-stu-id="43a00-138">D3DTA\_TEMP is supported if the [D3DPMISCCAPS\_TSSARGTEMP](d3dpmisccaps.md) device capability is present.</span></span> <span data-ttu-id="43a00-139">El valor predeterminado del registro es (0.0, 0.0, 0.0, 0.0).</span><span class="sxs-lookup"><span data-stu-id="43a00-139">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span> <span data-ttu-id="43a00-140">Los permisos son de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="43a00-140">Permissions are read/write.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="43a00-141">TEXTURA \_ D3DTA</span><span class="sxs-lookup"><span data-stu-id="43a00-141">D3DTA\_TEXTURE</span></span>    | <span data-ttu-id="43a00-142">El argumento de textura es el color de textura de esta fase de textura.</span><span class="sxs-lookup"><span data-stu-id="43a00-142">The texture argument is the texture color for this texture stage.</span></span> <span data-ttu-id="43a00-143">Los permisos son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="43a00-143">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="43a00-144">D3DTA \_ TFACTOR</span><span class="sxs-lookup"><span data-stu-id="43a00-144">D3DTA\_TFACTOR</span></span>    | <span data-ttu-id="43a00-145">El argumento de textura es el factor de textura establecido en una llamada anterior a [**SetRenderState**](/windows/desktop/api) con el valor de estado de representación [**\_ TEXTUREFACTOR de D3DRS.**](./d3drenderstatetype.md)</span><span class="sxs-lookup"><span data-stu-id="43a00-145">The texture argument is the texture factor set in a previous call to the [**SetRenderState**](/windows/desktop/api) with the [**D3DRS\_TEXTUREFACTOR**](./d3drenderstatetype.md) render-state value.</span></span> <span data-ttu-id="43a00-146">Los permisos son de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="43a00-146">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="43a00-147">Marcas modificadoras</span><span class="sxs-lookup"><span data-stu-id="43a00-147">Modifier flags</span></span>

<span data-ttu-id="43a00-148">Una marca de argumento se puede combinar con una de las siguientes marcas modificadoras.</span><span class="sxs-lookup"><span data-stu-id="43a00-148">An argument flag may be combined with one of the following modifier flags.</span></span>



| <span data-ttu-id="43a00-149">\#Definir</span><span class="sxs-lookup"><span data-stu-id="43a00-149">\#define</span></span>              | <span data-ttu-id="43a00-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="43a00-150">Description</span></span>                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43a00-151">D3DTA \_ ALPHAREPLICATE</span><span class="sxs-lookup"><span data-stu-id="43a00-151">D3DTA\_ALPHAREPLICATE</span></span> | <span data-ttu-id="43a00-152">Replique la información alfa en todos los canales de color antes de que finalice la operación.</span><span class="sxs-lookup"><span data-stu-id="43a00-152">Replicate the alpha information to all color channels before the operation completes.</span></span> <span data-ttu-id="43a00-153">Se trata de un modificador de lectura.</span><span class="sxs-lookup"><span data-stu-id="43a00-153">This is a read modifier.</span></span> |
| <span data-ttu-id="43a00-154">COMPLEMENTO D3DTA \_</span><span class="sxs-lookup"><span data-stu-id="43a00-154">D3DTA\_COMPLEMENT</span></span>     | <span data-ttu-id="43a00-155">Tome el complemento del argumento x, (1.0 - x).</span><span class="sxs-lookup"><span data-stu-id="43a00-155">Take the complement of the argument x, (1.0 - x).</span></span> <span data-ttu-id="43a00-156">Se trata de un modificador de lectura.</span><span class="sxs-lookup"><span data-stu-id="43a00-156">This is a read modifier.</span></span>                                     |



 

## <a name="constant-information"></a><span data-ttu-id="43a00-157">Información constante</span><span class="sxs-lookup"><span data-stu-id="43a00-157">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="43a00-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43a00-158">Header</span></span>                   | <span data-ttu-id="43a00-159">d3d9types.h</span><span class="sxs-lookup"><span data-stu-id="43a00-159">d3d9types.h</span></span> |
| <span data-ttu-id="43a00-160">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="43a00-160">Minimum operating system</span></span> | <span data-ttu-id="43a00-161">Windows 98</span><span class="sxs-lookup"><span data-stu-id="43a00-161">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="43a00-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="43a00-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43a00-163">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="43a00-163">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
