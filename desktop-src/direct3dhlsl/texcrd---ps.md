---
title: texcrd-PS
description: Copia los datos de coordenadas de textura del iterador de la coordenada de textura de origen como datos de color en el registro de destino.
ms.assetid: b3330d70-6e18-4494-a01c-51f0a282e305
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e1b7bda7ab06c4af43eaa40393d2c5d64b09d9f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997068"
---
# <a name="texcrd---ps"></a><span data-ttu-id="e3294-103">texcrd-PS</span><span class="sxs-lookup"><span data-stu-id="e3294-103">texcrd - ps</span></span>

<span data-ttu-id="e3294-104">Copia los datos de coordenadas de textura del iterador de la coordenada de textura de origen como datos de color en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="e3294-104">Copies texture coordinate data from the source texture coordinate iterator register as color data in the destination register.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3294-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3294-105">Syntax</span></span>



| <span data-ttu-id="e3294-106">texcrd DST, src</span><span class="sxs-lookup"><span data-stu-id="e3294-106">texcrd dst, src</span></span> |
|-----------------|



 

<span data-ttu-id="e3294-107">, donde</span><span class="sxs-lookup"><span data-stu-id="e3294-107">where</span></span>

-   <span data-ttu-id="e3294-108">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="e3294-108">dst is the destination register.</span></span>
-   <span data-ttu-id="e3294-109">src es un registro de origen.</span><span class="sxs-lookup"><span data-stu-id="e3294-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3294-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3294-110">Remarks</span></span>



| <span data-ttu-id="e3294-111">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="e3294-111">Pixel shader versions</span></span> | <span data-ttu-id="e3294-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="e3294-112">1\_1</span></span> | <span data-ttu-id="e3294-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="e3294-113">1\_2</span></span> | <span data-ttu-id="e3294-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e3294-114">1\_3</span></span> | <span data-ttu-id="e3294-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="e3294-115">1\_4</span></span> | <span data-ttu-id="e3294-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e3294-116">2\_0</span></span> | <span data-ttu-id="e3294-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e3294-117">2\_x</span></span> | <span data-ttu-id="e3294-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e3294-118">2\_sw</span></span> | <span data-ttu-id="e3294-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e3294-119">3\_0</span></span> | <span data-ttu-id="e3294-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e3294-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e3294-121">texcrd</span><span class="sxs-lookup"><span data-stu-id="e3294-121">texcrd</span></span>                |      |      |      | <span data-ttu-id="e3294-122">x</span><span class="sxs-lookup"><span data-stu-id="e3294-122">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="e3294-123">Esta instrucción interpreta los datos de coordenadas como datos de color (RGBA).</span><span class="sxs-lookup"><span data-stu-id="e3294-123">This instruction interprets coordinate data as color data (RGBA).</span></span>

<span data-ttu-id="e3294-124">Esta instrucción no muestrea ninguna textura.</span><span class="sxs-lookup"><span data-stu-id="e3294-124">No texture is sampled by this instruction.</span></span> <span data-ttu-id="e3294-125">Solo se aplican las coordenadas de textura establecidas en esta fase de textura.</span><span class="sxs-lookup"><span data-stu-id="e3294-125">Only texture coordinates set on this texture stage are relevant.</span></span>

<span data-ttu-id="e3294-126">Al utilizar texcrd, tenga en cuenta los siguientes detalles sobre cómo se copian los datos del registro de origen en el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="e3294-126">When using texcrd, keep in mind the following detail about how data is copied from the source register to the destination register.</span></span> <span data-ttu-id="e3294-127">El registro de coordenadas de textura de origen (t \# ) contiene datos en el intervalo \[ -D3DCAPS9. MaxTextureRepeat, D3DCAPS9. MaxTextureRepeat \] , mientras que el registro de destino (r \# ) solo puede contener datos en el intervalo de D3DCAPS9 (probablemente más pequeño) \[ . PixelShader1xMaxValue, D3DCAPS9. PixelShader1xMaxValue \] .</span><span class="sxs-lookup"><span data-stu-id="e3294-127">The source texture coordinate register (t\#) holds data in the range \[-D3DCAPS9.MaxTextureRepeat, D3DCAPS9.MaxTextureRepeat\], while the destination register (r\#) can hold data only in the (likely smaller) range \[-D3DCAPS9.PixelShader1xMaxValue, D3DCAPS9.PixelShader1xMaxValue\].</span></span> <span data-ttu-id="e3294-128">Tenga en cuenta que para el sombreador de píxeles versión 1 \_ 4, D3DCAPS9. PixelShader1xMaxValue debe tener un mínimo de ocho.</span><span class="sxs-lookup"><span data-stu-id="e3294-128">Note that for pixel shader version 1\_4, D3DCAPS9.PixelShader1xMaxValue must be a minimum of eight.</span></span> <span data-ttu-id="e3294-129">La instrucción texcrd, en el proceso de compresión de datos de origen que está fuera del intervalo del registro de destino, es probable que se comporte de forma diferente en hardware diferente.</span><span class="sxs-lookup"><span data-stu-id="e3294-129">The texcrd instruction, in the process of clamping source data that is out of range of the destination register, is likely to behave differently on different hardware.</span></span> <span data-ttu-id="e3294-130">El primer hardware del sombreador de píxeles versión 1 \_ 4 en el mercado llevará a cabo una abrazadera especial para los valores fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="e3294-130">The first pixel shader version 1\_4 hardware on the market will perform a special clamp for values outside of range.</span></span> <span data-ttu-id="e3294-131">Esta abrazadera está diseñada para generar un número que puede caber en el registro de destino, pero también para conservar el comportamiento del direccionamiento de texturas para los datos fuera del intervalo (vea [**D3DTEXTUREADDRESS**](/windows/desktop/direct3d9/d3dtextureaddress)) si los datos se van a usar posteriormente para el muestreo de textura.</span><span class="sxs-lookup"><span data-stu-id="e3294-131">This clamp is designed to produce a number that can fit into the destination register, but also to preserve texture addressing behavior for out-of-range data (see [**D3DTEXTUREADDRESS**](/windows/desktop/direct3d9/d3dtextureaddress)) if the data were to be subsequently used for texture sampling.</span></span> <span data-ttu-id="e3294-132">Sin embargo, es posible que el nuevo hardware de distintos fabricantes no muestre este comportamiento y que simplemente Chop los datos para que se ajusten al intervalo de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="e3294-132">However, new hardware from different manufacturers might not exhibit this behavior and might just chop data to fit the destination register range.</span></span> <span data-ttu-id="e3294-133">Por lo tanto, el curso de acción más seguro al usar el sombreador de píxeles versión 1 \_ 4 texcrd es proporcionar datos de coordenadas de textura solo en el sombreador de píxeles que ya está dentro del intervalo \[ -8, 8 \] para que no se base en la forma en que se fija el hardware.</span><span class="sxs-lookup"><span data-stu-id="e3294-133">Therefore, the safest course of action when using pixel shader version 1\_4 texcrd is to supply texture coordinate data only into the pixel shader that is already within the range \[-8,8\] so that you do not rely on the way hardware clamps.</span></span>

<span data-ttu-id="e3294-134">A diferencia \_ de texcoord, texcrd no fija valores entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="e3294-134">Unlike texcoord\_, texcrd does not clamp values between 0 and 1.</span></span>

<span data-ttu-id="e3294-135">Reglas para usar texcrd:</span><span class="sxs-lookup"><span data-stu-id="e3294-135">Rules for using texcrd :</span></span>

1.  <span data-ttu-id="e3294-136">Se debe aplicar el mismo modificador. XYZ o. xyw a cada lectura de un registro t (n) individual dentro de una instrucción texcrd o texld.</span><span class="sxs-lookup"><span data-stu-id="e3294-136">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within a texcrd or texld instruction.</span></span>
2.  <span data-ttu-id="e3294-137">El resultado del cuarto canal de texcrd es unset/undefined en todos los casos.</span><span class="sxs-lookup"><span data-stu-id="e3294-137">The fourth channel result of texcrd is unset/undefined in all cases.</span></span>
3.  <span data-ttu-id="e3294-138">El tercer canal no está establecido o no está definido para el caso de almacenamiento de xyw \_ .</span><span class="sxs-lookup"><span data-stu-id="e3294-138">The third channel is unset/undefined for the xyw\_dw case.</span></span>

## <a name="examples"></a><span data-ttu-id="e3294-139">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e3294-139">Examples</span></span>

<span data-ttu-id="e3294-140">A continuación se muestra el conjunto completo de sintaxis permitida para texcrd, teniendo en cuenta todas las combinaciones válidas de modificador/selector de origen y máscara de escritura de destino.</span><span class="sxs-lookup"><span data-stu-id="e3294-140">The complete set of allowed syntax for texcrd, taking into account all valid source modifier/selector and destination write mask combinations, is shown below.</span></span> <span data-ttu-id="e3294-141">Tenga en cuenta que la notación. RGBA y. xyzw se puede usar indistintamente.</span><span class="sxs-lookup"><span data-stu-id="e3294-141">Note that the .rgba and .xyzw notation can be used interchangeably.</span></span>

<span data-ttu-id="e3294-142">Copia los tres primeros canales de un iterador de la coordenada de textura Register, t (n), en r (m).</span><span class="sxs-lookup"><span data-stu-id="e3294-142">Copies first three channels of texture coordinate iterator register, t(n), into r(m).</span></span> <span data-ttu-id="e3294-143">El cuarto canal de r (m) no está inicializado.</span><span class="sxs-lookup"><span data-stu-id="e3294-143">The fourth channel of r(m) is uninitialized.</span></span>


```
texcrd  r(m).rgb, t(n).xyz  

// Produces the same result as the previous instruction
texcrd  r(m).rgb, t(n)
```



<span data-ttu-id="e3294-144">Coloca los componentes primero, segundo y cuarto de t (n) en los primeros tres canales de r (m).</span><span class="sxs-lookup"><span data-stu-id="e3294-144">Puts first, second, and fourth components of t(n) into first three channels of r(m).</span></span> <span data-ttu-id="e3294-145">El cuarto canal de r (m) no está inicializado.</span><span class="sxs-lookup"><span data-stu-id="e3294-145">The fourth channel of r(m) is uninitialized.</span></span>


```
texcrd  r(m).rgb, t(n).xyw
```



<span data-ttu-id="e3294-146">Este es un ejemplo de división proyectada mediante el \_ modificador DW.</span><span class="sxs-lookup"><span data-stu-id="e3294-146">Here is a projective divide example using the \_dw modifier.</span></span>

<span data-ttu-id="e3294-147">Este ejemplo copia x/w e y/w de t (n) en los dos primeros canales de r (m).</span><span class="sxs-lookup"><span data-stu-id="e3294-147">This example copies x/w and y/w from t(n) into the first two channels of r(m).</span></span> <span data-ttu-id="e3294-148">Los canales tercero y cuarto de r (m) no están inicializados.</span><span class="sxs-lookup"><span data-stu-id="e3294-148">The third and fourth channels of r(m) are uninitialized.</span></span> <span data-ttu-id="e3294-149">Se perderán los datos escritos previamente en el tercer canal de r (m).</span><span class="sxs-lookup"><span data-stu-id="e3294-149">Any data previously written to the third channel of r(m) will be lost.</span></span> <span data-ttu-id="e3294-150">Los datos del cuarto canal de r (m) se pierden debido al marcador de fase.</span><span class="sxs-lookup"><span data-stu-id="e3294-150">Data in the fourth channel of r(m) is lost due to the phase marker.</span></span> <span data-ttu-id="e3294-151">En el caso de \_ la versión 4, \_ se omite la marca proyectada D3DTTFF.</span><span class="sxs-lookup"><span data-stu-id="e3294-151">For version 1\_4, the D3DTTFF\_PROJECTED flag is ignored.</span></span>


```
texcrd  r(m).rg,  t(n)_dw.xyw
```



## <a name="related-topics"></a><span data-ttu-id="e3294-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e3294-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3294-153">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="e3294-153">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 