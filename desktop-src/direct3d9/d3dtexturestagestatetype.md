---
description: Los Estados de la fase de textura definen las operaciones de textura de varios mezcladores.
ms.assetid: 87a5a1bb-e748-4c72-8320-ea82250dcc0e
title: Enumeración D3DTEXTURESTAGESTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURESTAGESTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0530f428c9ebf89607fa89509c65ddd336fee293
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280285"
---
# <a name="d3dtexturestagestatetype-enumeration"></a><span data-ttu-id="868ad-103">Enumeración D3DTEXTURESTAGESTATETYPE</span><span class="sxs-lookup"><span data-stu-id="868ad-103">D3DTEXTURESTAGESTATETYPE enumeration</span></span>

<span data-ttu-id="868ad-104">Los Estados de la fase de textura definen las operaciones de textura de varios mezcladores.</span><span class="sxs-lookup"><span data-stu-id="868ad-104">Texture stage states define multi-blender texture operations.</span></span> <span data-ttu-id="868ad-105">Algunos Estados muestreador configuran el procesamiento de vértices y algunos establecen el procesamiento de píxeles.</span><span class="sxs-lookup"><span data-stu-id="868ad-105">Some sampler states set up vertex processing, and some set up pixel processing.</span></span> <span data-ttu-id="868ad-106">Los Estados de las fases de textura se pueden guardar y restaurar mediante stateblocks (vea el [Estado de guardado y restauración de los bloques de estado (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="868ad-106">Texture stage states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="868ad-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="868ad-107">Syntax</span></span>


```C++
typedef enum D3DTEXTURESTAGESTATETYPE { 
  D3DTSS_COLOROP                = 1,
  D3DTSS_COLORARG1              = 2,
  D3DTSS_COLORARG2              = 3,
  D3DTSS_ALPHAOP                = 4,
  D3DTSS_ALPHAARG1              = 5,
  D3DTSS_ALPHAARG2              = 6,
  D3DTSS_BUMPENVMAT00           = 7,
  D3DTSS_BUMPENVMAT01           = 8,
  D3DTSS_BUMPENVMAT10           = 9,
  D3DTSS_BUMPENVMAT11           = 10,
  D3DTSS_TEXCOORDINDEX          = 11,
  D3DTSS_BUMPENVLSCALE          = 22,
  D3DTSS_BUMPENVLOFFSET         = 23,
  D3DTSS_TEXTURETRANSFORMFLAGS  = 24,
  D3DTSS_COLORARG0              = 26,
  D3DTSS_ALPHAARG0              = 27,
  D3DTSS_RESULTARG              = 28,
  D3DTSS_CONSTANT               = 32,
  D3DTSS_FORCE_DWORD            = 0x7fffffff
} D3DTEXTURESTAGESTATETYPE, *LPD3DTEXTURESTAGESTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="868ad-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="868ad-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="868ad-109"><span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**D3DTSS \_ COLOROP**</span><span class="sxs-lookup"><span data-stu-id="868ad-109"><span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**D3DTSS\_COLOROP**</span></span>
</dt> <dd>

<span data-ttu-id="868ad-110">El estado de la fase de textura es una operación de combinación de colores de textura identificada por un miembro del tipo enumerado [**D3DTEXTUREOP**](./d3dtextureop.md) .</span><span class="sxs-lookup"><span data-stu-id="868ad-110">Texture-stage state is a texture color blending operation identified by one member of the [**D3DTEXTUREOP**](./d3dtextureop.md) enumerated type.</span></span> <span data-ttu-id="868ad-111">El valor predeterminado de la primera fase de textura (Stage 0) es D3DTOP \_ modular; para todas las demás fases, el valor predeterminado es D3DTOP \_ Disable.</span><span class="sxs-lookup"><span data-stu-id="868ad-111">The default value for the first texture stage (stage 0) is D3DTOP\_MODULATE; for all other stages the default is D3DTOP\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="868ad-112"><span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**D3DTSS \_ COLORARG1**</span><span class="sxs-lookup"><span data-stu-id="868ad-112"><span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**D3DTSS\_COLORARG1**</span></span>
</dt> <dd>

<span data-ttu-id="868ad-113">Texture: el estado de la fase es el primer argumento de color de la fase, identificado por uno de los [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="868ad-113">Texture-stage state is the first color argument for the stage, identified by one of the [D3DTA](d3dta.md).</span></span> <span data-ttu-id="868ad-114">El argumento predeterminado es D3DTA \_ Texture.</span><span class="sxs-lookup"><span data-stu-id="868ad-114">The default argument is D3DTA\_TEXTURE.</span></span>

<span data-ttu-id="868ad-115">Especifique D3DTA \_ temp para seleccionar un color de registro temporal para lectura o escritura.</span><span class="sxs-lookup"><span data-stu-id="868ad-115">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="868ad-116">D3DTA \_ Temp se admite si la \_ funcionalidad del dispositivo D3DPMISCCAPS TSSARGTEMP está presente.</span><span class="sxs-lookup"><span data-stu-id="868ad-116">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="868ad-117">El valor predeterminado del registro es (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="868ad-117">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="868ad-118"><span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**D3DTSS \_ COLORARG2**</span><span class="sxs-lookup"><span data-stu-id="868ad-118"><span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**D3DTSS\_COLORARG2**</span></span>
</dt> <dd>

<span data-ttu-id="868ad-119">Texture: el estado de la fase es el segundo argumento de color para la fase, identificado por [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="868ad-119">Texture-stage state is the second color argument for the stage, identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="868ad-120">El argumento predeterminado es D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="868ad-120">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="868ad-121">Especifique D3DTA \_ temp para seleccionar un color de registro temporal para lectura o escritura.</span><span class="sxs-lookup"><span data-stu-id="868ad-121">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="868ad-122">D3DTA \_ Temp se admite si la \_ funcionalidad del dispositivo D3DPMISCCAPS TSSARGTEMP está presente.</span><span class="sxs-lookup"><span data-stu-id="868ad-122">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="868ad-123">El valor predeterminado del registro es (0,0, 0,0, 0,0, 0,0)</span><span class="sxs-lookup"><span data-stu-id="868ad-123">The default value for the register is (0.0, 0.0, 0.0, 0.0)</span></span>

</dd> <dt>

<span data-ttu-id="868ad-124"><span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**D3DTSS \_ ALPHAOP**</span><span class="sxs-lookup"><span data-stu-id="868ad-124"><span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**D3DTSS\_ALPHAOP**</span></span>
</dt> <dd>

<span data-ttu-id="868ad-125">El estado de la fase de textura es una operación de combinación alfa de textura identificada por un miembro del tipo enumerado [**D3DTEXTUREOP**](./d3dtextureop.md) .</span><span class="sxs-lookup"><span data-stu-id="868ad-125">Texture-stage state is a texture alpha blending operation identified by one member of the [**D3DTEXTUREOP**](./d3dtextureop.md) enumerated type.</span></span> <span data-ttu-id="868ad-126">El valor predeterminado de la primera fase de textura (Stage 0) es D3DTOP \_ SELECTARG1 y, para todas las demás fases, el valor predeterminado es D3DTOP \_ Disable.</span><span class="sxs-lookup"><span data-stu-id="868ad-126">The default value for the first texture stage (stage 0) is D3DTOP\_SELECTARG1, and for all other stages the default is D3DTOP\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="868ad-127"><span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**D3DTSS \_ ALPHAARG1**</span><span class="sxs-lookup"><span data-stu-id="868ad-127"><span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**D3DTSS\_ALPHAARG1**</span></span>
</dt> <dd>

<span data-ttu-id="868ad-128">Texture: el estado de la fase es el primer argumento alfa de la fase, identificado por [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="868ad-128">Texture-stage state is the first alpha argument for the stage, identified by by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="868ad-129">El argumento predeterminado es D3DTA \_ Texture.</span><span class="sxs-lookup"><span data-stu-id="868ad-129">The default argument is D3DTA\_TEXTURE.</span></span> <span data-ttu-id="868ad-130">Si no se establece ninguna textura para esta fase, el argumento predeterminado es D3DTA \_ difuso.</span><span class="sxs-lookup"><span data-stu-id="868ad-130">If no texture is set for this stage, the default argument is D3DTA\_DIFFUSE.</span></span> <span data-ttu-id="868ad-131">Especifique D3DTA \_ temp para seleccionar un color de registro temporal para lectura o escritura.</span><span class="sxs-lookup"><span data-stu-id="868ad-131">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="868ad-132">D3DTA \_ Temp se admite si la \_ funcionalidad del dispositivo D3DPMISCCAPS TSSARGTEMP está presente.</span><span class="sxs-lookup"><span data-stu-id="868ad-132">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="868ad-133">El valor predeterminado del registro es (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="868ad-133">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="868ad-134"><span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**D3DTSS \_ ALPHAARG2**</span><span class="sxs-lookup"><span data-stu-id="868ad-134"><span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**D3DTSS\_ALPHAARG2**</span></span>
</dt> <dd>

<span data-ttu-id="868ad-135">Texture: el estado de la fase es el segundo argumento alfa de la fase, identificado por [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="868ad-135">Texture-stage state is the second alpha argument for the stage, identified by by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="868ad-136">El argumento predeterminado es D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="868ad-136">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="868ad-137">Especifique D3DTA \_ temp para seleccionar un color de registro temporal para lectura o escritura.</span><span class="sxs-lookup"><span data-stu-id="868ad-137">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="868ad-138">D3DTA \_ Temp se admite si la \_ funcionalidad del dispositivo D3DPMISCCAPS TSSARGTEMP está presente.</span><span class="sxs-lookup"><span data-stu-id="868ad-138">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="868ad-139">El valor predeterminado del registro es (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="868ad-139">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="868ad-140"><span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**D3DTSS \_ BUMPENVMAT00**</span><span class="sxs-lookup"><span data-stu-id="868ad-140"><span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**D3DTSS\_BUMPENVMAT00**</span></span>
</dt> <dd>

<span data-ttu-id="868ad-141">Texture: el estado de la fase es un valor de punto flotante para el \[ \] \[ \] coeficiente 0 0 en una matriz de asignación de rugosidad.</span><span class="sxs-lookup"><span data-stu-id="868ad-141">Texture-stage state is a floating-point value for the \[0\]\[0\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="868ad-142">El valor predeterminado es 0.0.</span><span class="sxs-lookup"><span data-stu-id="868ad-142">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="868ad-143"><span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**D3DTSS \_ BUMPENVMAT01**</span><span class="sxs-lookup"><span data-stu-id="868ad-143"><span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**D3DTSS\_BUMPENVMAT01**</span></span>
</dt> <dd>

<span data-ttu-id="868ad-144">Texture: el estado de la fase es un valor de punto flotante para el \[ \] \[ \] coeficiente 0 1 en una matriz de asignación de rugosidad.</span><span class="sxs-lookup"><span data-stu-id="868ad-144">Texture-stage state is a floating-point value for the \[0\]\[1\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="868ad-145">El valor predeterminado es 0.0.</span><span class="sxs-lookup"><span data-stu-id="868ad-145">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="868ad-146"><span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**D3DTSS \_ BUMPENVMAT10**</span><span class="sxs-lookup"><span data-stu-id="868ad-146"><span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**D3DTSS\_BUMPENVMAT10**</span></span>
</dt> <dd>

<span data-ttu-id="868ad-147">Texture: el estado de la fase es un valor de punto flotante para el \[ \] \[ \] coeficiente 1 0 en una matriz de asignación de rugosidad.</span><span class="sxs-lookup"><span data-stu-id="868ad-147">Texture-stage state is a floating-point value for the \[1\]\[0\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="868ad-148">El valor predeterminado es 0.0.</span><span class="sxs-lookup"><span data-stu-id="868ad-148">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="868ad-149"><span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**D3DTSS \_ BUMPENVMAT11**</span><span class="sxs-lookup"><span data-stu-id="868ad-149"><span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**D3DTSS\_BUMPENVMAT11**</span></span>
</dt> <dd>

<span data-ttu-id="868ad-150">Texture: el estado de la fase es un valor de punto flotante para el \[ \] \[ \] coeficiente 1 1 en una matriz de asignación de rugosidad.</span><span class="sxs-lookup"><span data-stu-id="868ad-150">Texture-stage state is a floating-point value for the \[1\]\[1\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="868ad-151">El valor predeterminado es 0.0.</span><span class="sxs-lookup"><span data-stu-id="868ad-151">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="868ad-152"><span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**D3DTSS \_ TEXCOORDINDEX**</span><span class="sxs-lookup"><span data-stu-id="868ad-152"><span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**D3DTSS\_TEXCOORDINDEX**</span></span>
</dt> <dd>

<span data-ttu-id="868ad-153">Índice del conjunto de coordenadas de textura que se va a usar con esta fase de textura.</span><span class="sxs-lookup"><span data-stu-id="868ad-153">Index of the texture coordinate set to use with this texture stage.</span></span> <span data-ttu-id="868ad-154">Puede especificar hasta ocho conjuntos de coordenadas de textura por vértice.</span><span class="sxs-lookup"><span data-stu-id="868ad-154">You can specify up to eight sets of texture coordinates per vertex.</span></span> <span data-ttu-id="868ad-155">Si un vértice no incluye un conjunto de coordenadas de textura en el índice especificado, el sistema toma como valor predeterminado las coordenadas de la TI y la v (0,0).</span><span class="sxs-lookup"><span data-stu-id="868ad-155">If a vertex does not include a set of texture coordinates at the specified index, the system defaults to the u and v coordinates (0,0).</span></span>

<span data-ttu-id="868ad-156">Al representar mediante sombreadores de vértices, el índice de coordenadas de textura de cada fase debe establecerse en su valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="868ad-156">When rendering using vertex shaders, each stage's texture coordinate index must be set to its default value.</span></span> <span data-ttu-id="868ad-157">El índice predeterminado de cada fase es igual al índice de fase.</span><span class="sxs-lookup"><span data-stu-id="868ad-157">The default index for each stage is equal to the stage index.</span></span> <span data-ttu-id="868ad-158">Establezca este estado en el índice de base cero del conjunto de coordenadas para cada vértice que use esta fase de textura.</span><span class="sxs-lookup"><span data-stu-id="868ad-158">Set this state to the zero-based index of the coordinate set for each vertex that this texture stage uses.</span></span>

<span data-ttu-id="868ad-159">Además, las aplicaciones pueden incluir, como Logical o con el índice que se está configurando, una de las constantes para solicitar que Direct3D genere automáticamente las coordenadas de textura de entrada para una transformación de textura.</span><span class="sxs-lookup"><span data-stu-id="868ad-159">Additionally, applications can include, as logical OR with the index being set, one of the constants to request that Direct3D automatically generate the input texture coordinates for a texture transformation.</span></span> <span data-ttu-id="868ad-160">Para obtener una lista de todas las constantes, vea [D3DTSS \_ TCI](d3dtss-tci.md).</span><span class="sxs-lookup"><span data-stu-id="868ad-160">For a list of all the constants, see [D3DTSS\_TCI](d3dtss-tci.md).</span></span>

<span data-ttu-id="868ad-161">Con la excepción de D3DTSS \_ TCI \_ PASSTHRU, que se resuelve como cero, si alguno de los valores siguientes se incluye con el índice que se está configurando, el sistema usa el índice estrictamente para determinar el modo de ajuste de textura.</span><span class="sxs-lookup"><span data-stu-id="868ad-161">With the exception of D3DTSS\_TCI\_PASSTHRU, which resolves to zero, if any of the following values is included with the index being set, the system uses the index strictly to determine texture wrapping mode.</span></span> <span data-ttu-id="868ad-162">Estas marcas son más útiles cuando se realiza la asignación de entorno.</span><span class="sxs-lookup"><span data-stu-id="868ad-162">These flags are most useful when performing environment mapping.</span></span>

</dd> <dt>

<span data-ttu-id="868ad-163"><span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**D3DTSS \_ BUMPENVLSCALE**</span><span class="sxs-lookup"><span data-stu-id="868ad-163"><span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**D3DTSS\_BUMPENVLSCALE**</span></span>
</dt> <dd>

<span data-ttu-id="868ad-164">Valor de escala de punto flotante para la luminancia del mapa de rugosidad.</span><span class="sxs-lookup"><span data-stu-id="868ad-164">Floating-point scale value for bump-map luminance.</span></span> <span data-ttu-id="868ad-165">El valor predeterminado es 0.0.</span><span class="sxs-lookup"><span data-stu-id="868ad-165">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="868ad-166"><span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**D3DTSS \_ BUMPENVLOFFSET**</span><span class="sxs-lookup"><span data-stu-id="868ad-166"><span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**D3DTSS\_BUMPENVLOFFSET**</span></span>
</dt> <dd>

<span data-ttu-id="868ad-167">Valor de desplazamiento de punto flotante para la luminancia del mapa de rugosidad.</span><span class="sxs-lookup"><span data-stu-id="868ad-167">Floating-point offset value for bump-map luminance.</span></span> <span data-ttu-id="868ad-168">El valor predeterminado es 0.0.</span><span class="sxs-lookup"><span data-stu-id="868ad-168">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="868ad-169"><span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**D3DTSS \_ TEXTURETRANSFORMFLAGS**</span><span class="sxs-lookup"><span data-stu-id="868ad-169"><span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**D3DTSS\_TEXTURETRANSFORMFLAGS**</span></span>
</dt> <dd>

<span data-ttu-id="868ad-170">Miembro del tipo enumerado [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) que controla la transformación de coordenadas de textura para esta fase de textura.</span><span class="sxs-lookup"><span data-stu-id="868ad-170">Member of the [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) enumerated type that controls the transformation of texture coordinates for this texture stage.</span></span> <span data-ttu-id="868ad-171">El valor predeterminado es D3DTTFF \_ Disable.</span><span class="sxs-lookup"><span data-stu-id="868ad-171">The default value is D3DTTFF\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="868ad-172"><span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**D3DTSS \_ COLORARG0**</span><span class="sxs-lookup"><span data-stu-id="868ad-172"><span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**D3DTSS\_COLORARG0**</span></span>
</dt> <dd>

<span data-ttu-id="868ad-173">Configuración del operando de tercer color para las operaciones triadic (multiplicar, agregar y interpolar linealmente), identificada por [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="868ad-173">Settings for the third color operand for triadic operations (multiply, add, and linearly interpolate), identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="868ad-174">Esta configuración es compatible Si \_ están presentes las capacidades del dispositivo D3DTEXOPCAPS MULTIPLYADD o D3DTEXOPCAPS \_ lerp.</span><span class="sxs-lookup"><span data-stu-id="868ad-174">This setting is supported if the D3DTEXOPCAPS\_MULTIPLYADD or D3DTEXOPCAPS\_LERP device capabilities are present.</span></span> <span data-ttu-id="868ad-175">El argumento predeterminado es D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="868ad-175">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="868ad-176">Especifique D3DTA \_ temp para seleccionar un color de registro temporal para lectura o escritura.</span><span class="sxs-lookup"><span data-stu-id="868ad-176">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="868ad-177">D3DTA \_ Temp se admite si la \_ funcionalidad del dispositivo D3DPMISCCAPS TSSARGTEMP está presente.</span><span class="sxs-lookup"><span data-stu-id="868ad-177">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="868ad-178">El valor predeterminado del registro es (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="868ad-178">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="868ad-179"><span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**D3DTSS \_ ALPHAARG0**</span><span class="sxs-lookup"><span data-stu-id="868ad-179"><span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**D3DTSS\_ALPHAARG0**</span></span>
</dt> <dd>

<span data-ttu-id="868ad-180">Configuración del operando selector de canal alfa para las operaciones triadic (multiplicar, agregar y interpolar linealmente), identificada por [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="868ad-180">Settings for the alpha channel selector operand for triadic operations (multiply, add, and linearly interpolate), identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="868ad-181">Esta configuración es compatible Si \_ están presentes las capacidades del dispositivo D3DTEXOPCAPS MULTIPLYADD o D3DTEXOPCAPS \_ lerp.</span><span class="sxs-lookup"><span data-stu-id="868ad-181">This setting is supported if the D3DTEXOPCAPS\_MULTIPLYADD or D3DTEXOPCAPS\_LERP device capabilities are present.</span></span> <span data-ttu-id="868ad-182">El argumento predeterminado es D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="868ad-182">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="868ad-183">Especifique D3DTA \_ temp para seleccionar un color de registro temporal para lectura o escritura.</span><span class="sxs-lookup"><span data-stu-id="868ad-183">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="868ad-184">D3DTA \_ Temp se admite si la \_ funcionalidad del dispositivo D3DPMISCCAPS TSSARGTEMP está presente.</span><span class="sxs-lookup"><span data-stu-id="868ad-184">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="868ad-185">El argumento predeterminado es (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="868ad-185">The default argument is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="868ad-186"><span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**D3DTSS \_ RESULTARG**</span><span class="sxs-lookup"><span data-stu-id="868ad-186"><span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**D3DTSS\_RESULTARG**</span></span>
</dt> <dd>

<span data-ttu-id="868ad-187">Configuración para seleccionar el registro de destino para el resultado de esta fase, identificado por [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="868ad-187">Setting to select destination register for the result of this stage, identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="868ad-188">Este valor se puede establecer en D3DTA \_ Current (el valor predeterminado) o en D3DTA \_ temp, que es un registro temporal único que se puede leer en fases posteriores como argumento de entrada.</span><span class="sxs-lookup"><span data-stu-id="868ad-188">This value can be set to D3DTA\_CURRENT (the default value) or to D3DTA\_TEMP, which is a single temporary register that can be read into subsequent stages as an input argument.</span></span> <span data-ttu-id="868ad-189">El color final que se pasa al mezclador de niebla y al búfer de fotogramas se toma del D3DTA \_ actual, por lo que el último estado activo de la fase de textura debe establecerse para escribir en el actual.</span><span class="sxs-lookup"><span data-stu-id="868ad-189">The final color passed to the fog blender and frame buffer is taken from D3DTA\_CURRENT, so the last active texture stage state must be set to write to current.</span></span> <span data-ttu-id="868ad-190">Esta configuración es compatible Si la \_ funcionalidad del dispositivo D3DPMISCCAPS TSSARGTEMP está presente.</span><span class="sxs-lookup"><span data-stu-id="868ad-190">This setting is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span>

</dd> <dt>

<span data-ttu-id="868ad-191"><span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**D3DTSS \_ constante)**</span><span class="sxs-lookup"><span data-stu-id="868ad-191"><span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**D3DTSS\_CONSTANT**</span></span>
</dt> <dd>

<span data-ttu-id="868ad-192">Color constante por fase.</span><span class="sxs-lookup"><span data-stu-id="868ad-192">Per-stage constant color.</span></span> <span data-ttu-id="868ad-193">Para ver si un dispositivo admite un color constante por fase, consulte la constante D3DPMISCCAPS \_ PERSTAGECONSTANT en [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="868ad-193">To see if a device supports a per-stage constant color, see the D3DPMISCCAPS\_PERSTAGECONSTANT constant in [D3DPMISCCAPS](d3dpmisccaps.md).</span></span> <span data-ttu-id="868ad-194">La constante \_ D3DTA usa la constante D3DTSS \_ .</span><span class="sxs-lookup"><span data-stu-id="868ad-194">D3DTSS\_CONSTANT is used by D3DTA\_CONSTANT.</span></span> <span data-ttu-id="868ad-195">Vea [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="868ad-195">See [D3DTA](d3dta.md).</span></span>

</dd> <dt>

<span data-ttu-id="868ad-196"><span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="868ad-196"><span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="868ad-197">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="868ad-197">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="868ad-198">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="868ad-198">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="868ad-199">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="868ad-199">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="868ad-200">Observaciones</span><span class="sxs-lookup"><span data-stu-id="868ad-200">Remarks</span></span>

<span data-ttu-id="868ad-201">Los miembros de este tipo enumerado se usan con los métodos [**IDirect3DDevice9:: GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) y [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) para recuperar y establecer los valores de estado de textura.</span><span class="sxs-lookup"><span data-stu-id="868ad-201">Members of this enumerated type are used with the [**IDirect3DDevice9::GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) and [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) methods to retrieve and set texture state values.</span></span>

<span data-ttu-id="868ad-202">El intervalo válido de valores para los \_ coeficientes de la matriz de D3DTSS BUMPENVMAT00, D3DTSS \_ BUMPENVMAT01, D3DTSS \_ BUMPENVMAT10 y D3DTSS \_ BUMPENVMAT11 es mayor o igual que-8,0 y menor que 8,0.</span><span class="sxs-lookup"><span data-stu-id="868ad-202">The valid range of values for the D3DTSS\_BUMPENVMAT00, D3DTSS\_BUMPENVMAT01, D3DTSS\_BUMPENVMAT10, and D3DTSS\_BUMPENVMAT11 bump-mapping matrix coefficients is greater than or equal to -8.0 and less than 8.0.</span></span> <span data-ttu-id="868ad-203">Este intervalo, expresado en notación matemática, es (-8.0, 8.0).</span><span class="sxs-lookup"><span data-stu-id="868ad-203">This range, expressed in mathematical notation is (-8.0,8.0).</span></span>

## <a name="requirements"></a><span data-ttu-id="868ad-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="868ad-204">Requirements</span></span>



| <span data-ttu-id="868ad-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="868ad-205">Requirement</span></span> | <span data-ttu-id="868ad-206">Value</span><span class="sxs-lookup"><span data-stu-id="868ad-206">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="868ad-207">Encabezado</span><span class="sxs-lookup"><span data-stu-id="868ad-207">Header</span></span><br/> | <dl> <span data-ttu-id="868ad-208"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="868ad-208"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="868ad-209">Vea también</span><span class="sxs-lookup"><span data-stu-id="868ad-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="868ad-210">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="868ad-210">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="868ad-211">**IDirect3DDevice9::GetTextureStageState**</span><span class="sxs-lookup"><span data-stu-id="868ad-211">**IDirect3DDevice9::GetTextureStageState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate)
</dt> <dt>

[<span data-ttu-id="868ad-212">**IDirect3DDevice9::SetTextureStageState**</span><span class="sxs-lookup"><span data-stu-id="868ad-212">**IDirect3DDevice9::SetTextureStageState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
</dt> </dl>

 

 
