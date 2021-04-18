---
description: Los Estados de representación definen los Estados de configuración para todos los tipos de procesamiento de vértices y píxeles.
ms.assetid: 2fd56388-f3bd-409f-876c-ae893840b623
title: Enumeración D3DRENDERSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRENDERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2386762eaa45f1eefbccac97723c3ad71c3a76fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707779"
---
# <a name="d3drenderstatetype-enumeration"></a><span data-ttu-id="eb6f4-103">Enumeración D3DRENDERSTATETYPE</span><span class="sxs-lookup"><span data-stu-id="eb6f4-103">D3DRENDERSTATETYPE enumeration</span></span>

<span data-ttu-id="eb6f4-104">Los Estados de representación definen los Estados de configuración para todos los tipos de procesamiento de vértices y píxeles.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-104">Render states define set-up states for all kinds of vertex and pixel processing.</span></span> <span data-ttu-id="eb6f4-105">Algunos Estados de representación establecen el procesamiento de vértices y algunos conjuntos de procesamiento de píxeles (consulte [Estados de representación (Direct3D 9)](render-states.md)).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-105">Some render states set up vertex processing, and some set up pixel processing (see [Render States (Direct3D 9)](render-states.md)).</span></span> <span data-ttu-id="eb6f4-106">Los Estados de representación se pueden guardar y restaurar mediante stateblocks (vea el [Estado de guardado y restauración de los bloques de estado (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-106">Render states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb6f4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb6f4-107">Syntax</span></span>


```C++
typedef enum D3DRENDERSTATETYPE { 
  D3DRS_ZENABLE                     = 7,
  D3DRS_FILLMODE                    = 8,
  D3DRS_SHADEMODE                   = 9,
  D3DRS_ZWRITEENABLE                = 14,
  D3DRS_ALPHATESTENABLE             = 15,
  D3DRS_LASTPIXEL                   = 16,
  D3DRS_SRCBLEND                    = 19,
  D3DRS_DESTBLEND                   = 20,
  D3DRS_CULLMODE                    = 22,
  D3DRS_ZFUNC                       = 23,
  D3DRS_ALPHAREF                    = 24,
  D3DRS_ALPHAFUNC                   = 25,
  D3DRS_DITHERENABLE                = 26,
  D3DRS_ALPHABLENDENABLE            = 27,
  D3DRS_FOGENABLE                   = 28,
  D3DRS_SPECULARENABLE              = 29,
  D3DRS_FOGCOLOR                    = 34,
  D3DRS_FOGTABLEMODE                = 35,
  D3DRS_FOGSTART                    = 36,
  D3DRS_FOGEND                      = 37,
  D3DRS_FOGDENSITY                  = 38,
  D3DRS_RANGEFOGENABLE              = 48,
  D3DRS_STENCILENABLE               = 52,
  D3DRS_STENCILFAIL                 = 53,
  D3DRS_STENCILZFAIL                = 54,
  D3DRS_STENCILPASS                 = 55,
  D3DRS_STENCILFUNC                 = 56,
  D3DRS_STENCILREF                  = 57,
  D3DRS_STENCILMASK                 = 58,
  D3DRS_STENCILWRITEMASK            = 59,
  D3DRS_TEXTUREFACTOR               = 60,
  D3DRS_WRAP0                       = 128,
  D3DRS_WRAP1                       = 129,
  D3DRS_WRAP2                       = 130,
  D3DRS_WRAP3                       = 131,
  D3DRS_WRAP4                       = 132,
  D3DRS_WRAP5                       = 133,
  D3DRS_WRAP6                       = 134,
  D3DRS_WRAP7                       = 135,
  D3DRS_CLIPPING                    = 136,
  D3DRS_LIGHTING                    = 137,
  D3DRS_AMBIENT                     = 139,
  D3DRS_FOGVERTEXMODE               = 140,
  D3DRS_COLORVERTEX                 = 141,
  D3DRS_LOCALVIEWER                 = 142,
  D3DRS_NORMALIZENORMALS            = 143,
  D3DRS_DIFFUSEMATERIALSOURCE       = 145,
  D3DRS_SPECULARMATERIALSOURCE      = 146,
  D3DRS_AMBIENTMATERIALSOURCE       = 147,
  D3DRS_EMISSIVEMATERIALSOURCE      = 148,
  D3DRS_VERTEXBLEND                 = 151,
  D3DRS_CLIPPLANEENABLE             = 152,
  D3DRS_POINTSIZE                   = 154,
  D3DRS_POINTSIZE_MIN               = 155,
  D3DRS_POINTSPRITEENABLE           = 156,
  D3DRS_POINTSCALEENABLE            = 157,
  D3DRS_POINTSCALE_A                = 158,
  D3DRS_POINTSCALE_B                = 159,
  D3DRS_POINTSCALE_C                = 160,
  D3DRS_MULTISAMPLEANTIALIAS        = 161,
  D3DRS_MULTISAMPLEMASK             = 162,
  D3DRS_PATCHEDGESTYLE              = 163,
  D3DRS_DEBUGMONITORTOKEN           = 165,
  D3DRS_POINTSIZE_MAX               = 166,
  D3DRS_INDEXEDVERTEXBLENDENABLE    = 167,
  D3DRS_COLORWRITEENABLE            = 168,
  D3DRS_TWEENFACTOR                 = 170,
  D3DRS_BLENDOP                     = 171,
  D3DRS_POSITIONDEGREE              = 172,
  D3DRS_NORMALDEGREE                = 173,
  D3DRS_SCISSORTESTENABLE           = 174,
  D3DRS_SLOPESCALEDEPTHBIAS         = 175,
  D3DRS_ANTIALIASEDLINEENABLE       = 176,
  D3DRS_MINTESSELLATIONLEVEL        = 178,
  D3DRS_MAXTESSELLATIONLEVEL        = 179,
  D3DRS_ADAPTIVETESS_X              = 180,
  D3DRS_ADAPTIVETESS_Y              = 181,
  D3DRS_ADAPTIVETESS_Z              = 182,
  D3DRS_ADAPTIVETESS_W              = 183,
  D3DRS_ENABLEADAPTIVETESSELLATION  = 184,
  D3DRS_TWOSIDEDSTENCILMODE         = 185,
  D3DRS_CCW_STENCILFAIL             = 186,
  D3DRS_CCW_STENCILZFAIL            = 187,
  D3DRS_CCW_STENCILPASS             = 188,
  D3DRS_CCW_STENCILFUNC             = 189,
  D3DRS_COLORWRITEENABLE1           = 190,
  D3DRS_COLORWRITEENABLE2           = 191,
  D3DRS_COLORWRITEENABLE3           = 192,
  D3DRS_BLENDFACTOR                 = 193,
  D3DRS_SRGBWRITEENABLE             = 194,
  D3DRS_DEPTHBIAS                   = 195,
  D3DRS_WRAP8                       = 198,
  D3DRS_WRAP9                       = 199,
  D3DRS_WRAP10                      = 200,
  D3DRS_WRAP11                      = 201,
  D3DRS_WRAP12                      = 202,
  D3DRS_WRAP13                      = 203,
  D3DRS_WRAP14                      = 204,
  D3DRS_WRAP15                      = 205,
  D3DRS_SEPARATEALPHABLENDENABLE    = 206,
  D3DRS_SRCBLENDALPHA               = 207,
  D3DRS_DESTBLENDALPHA              = 208,
  D3DRS_BLENDOPALPHA                = 209,
  D3DRS_FORCE_DWORD                 = 0x7fffffff
} D3DRENDERSTATETYPE, *LPD3DRENDERSTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="eb6f4-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="eb6f4-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="eb6f4-109"><span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS \_ ZENABLE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-109"><span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS\_ZENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-110">Estado de almacenamiento en búfer de profundidad como un miembro del tipo enumerado [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-110">Depth-buffering state as one member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-111">Establezca este estado en D3DZB \_ true para habilitar el almacenamiento en búfer z, D3DZB \_ USEW para habilitar el almacenamiento en búfer de w o D3DZB \_ false para deshabilitar el almacenamiento en búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-111">Set this state to D3DZB\_TRUE to enable z-buffering, D3DZB\_USEW to enable w-buffering, or D3DZB\_FALSE to disable depth buffering.</span></span>

<span data-ttu-id="eb6f4-112">El valor predeterminado para este estado de representación es D3DZB \_ true si se ha creado una galería de símbolos de profundidad junto con la cadena de intercambio estableciendo el miembro EnableAutoDepthStencil de la estructura de [**\_ parámetros D3DPRESENT**](d3dpresent-parameters.md) en **true** y D3DZB \_ false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-112">The default value for this render state is D3DZB\_TRUE if a depth stencil was created along with the swap chain by setting the EnableAutoDepthStencil member of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure to **TRUE**, and D3DZB\_FALSE otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-113"><span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS \_ FILLMODE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-113"><span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS\_FILLMODE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-114">Uno o más miembros del tipo enumerado [**D3DFILLMODE**](./d3dfillmode.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-114">One or more members of the [**D3DFILLMODE**](./d3dfillmode.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-115">El valor predeterminado es D3DFILL \_ Solid.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-115">The default value is D3DFILL\_SOLID.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-116"><span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS \_ SHADEMODE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-116"><span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS\_SHADEMODE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-117">Uno o más miembros del tipo enumerado [**D3DSHADEMODE**](./d3dshademode.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-117">One or more members of the [**D3DSHADEMODE**](./d3dshademode.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-118">El valor predeterminado es D3DSHADE \_ GOURAUD.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-118">The default value is D3DSHADE\_GOURAUD.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-119"><span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS \_ ZWRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-119"><span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS\_ZWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-120">**True** para permitir que la aplicación escriba en el búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-120">**TRUE** to enable the application to write to the depth buffer.</span></span> <span data-ttu-id="eb6f4-121">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-121">The default value is **TRUE**.</span></span> <span data-ttu-id="eb6f4-122">Este miembro permite a una aplicación impedir que el sistema actualice el búfer de profundidad con nuevos valores de profundidad.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-122">This member enables an application to prevent the system from updating the depth buffer with new depth values.</span></span> <span data-ttu-id="eb6f4-123">Si es **false**, las comparaciones de profundidad se siguen realizando según el estado de representación D3DRS \_ ZFUNC, suponiendo que se está llevando a cabo el almacenamiento en búfer de profundidad, pero los valores de profundidad no se escriben en el búfer.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-123">If **FALSE**, depth comparisons are still made according to the render state D3DRS\_ZFUNC, assuming that depth buffering is taking place, but depth values are not written to the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-124"><span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS \_ ALPHATESTENABLE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-124"><span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS\_ALPHATESTENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-125">**True** para habilitar las pruebas alfa por píxel.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-125">**TRUE** to enable per pixel alpha testing.</span></span> <span data-ttu-id="eb6f4-126">Si se supera la prueba, el búfer de fotogramas procesa el píxel.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-126">If the test passes, the pixel is processed by the frame buffer.</span></span> <span data-ttu-id="eb6f4-127">De lo contrario, se omite todo el procesamiento del búfer de fotogramas para el píxel.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-127">Otherwise, all frame-buffer processing is skipped for the pixel.</span></span>

<span data-ttu-id="eb6f4-128">La prueba se realiza comparando el valor alfa entrante con el valor alfa de referencia, usando la función de comparación proporcionada por el estado de representación de D3DRS \_ ALPHAFUNC.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-128">The test is done by comparing the incoming alpha value with the reference alpha value, using the comparison function provided by the D3DRS\_ALPHAFUNC render state.</span></span> <span data-ttu-id="eb6f4-129">El valor alfa de referencia viene determinado por el valor establecido para D3DRS \_ ALPHAREF.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-129">The reference alpha value is determined by the value set for D3DRS\_ALPHAREF.</span></span> <span data-ttu-id="eb6f4-130">Para obtener más información, vea estado de la [prueba alfa (Direct3D 9)](alpha-testing-state.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-130">For more information, see [Alpha Testing State (Direct3D 9)](alpha-testing-state.md).</span></span>

<span data-ttu-id="eb6f4-131">El valor predeterminado de este parámetro es **false**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-131">The default value of this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-132"><span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS \_ LASTPIXEL**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-132"><span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS\_LASTPIXEL**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-133">El valor predeterminado es **true**, que permite dibujar el último píxel en una línea.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-133">The default value is **TRUE**, which enables drawing of the last pixel in a line.</span></span> <span data-ttu-id="eb6f4-134">Para evitar el dibujo del último píxel, establezca este valor en **false**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-134">To prevent drawing of the last pixel, set this value to **FALSE**.</span></span> <span data-ttu-id="eb6f4-135">Para obtener más información, vea [resumir y rellenar el estado (Direct3D 9)](outline-and-fill-state.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-135">For more information, see [Outline and Fill State (Direct3D 9)](outline-and-fill-state.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-136"><span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS \_ SRCBLEND**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-136"><span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS\_SRCBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-137">Un miembro del tipo enumerado [**D3DBLEND**](./d3dblend.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-137">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-138">El valor predeterminado es D3DBLEND \_ uno.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-138">The default value is D3DBLEND\_ONE.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-139"><span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS \_ DESTBLEND**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-139"><span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS\_DESTBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-140">Un miembro del tipo enumerado [**D3DBLEND**](./d3dblend.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-140">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-141">El valor predeterminado es D3DBLEND \_ cero.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-141">The default value is D3DBLEND\_ZERO.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-142"><span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS \_ CULLMODE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-142"><span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS\_CULLMODE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-143">Especifica cómo se seleccionan los triángulos de conexión hacia delante, en caso de que se produzcan.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-143">Specifies how back-facing triangles are culled, if at all.</span></span> <span data-ttu-id="eb6f4-144">Se puede establecer en un miembro del tipo enumerado [**D3DCULL**](./d3dcull.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-144">This can be set to one member of the [**D3DCULL**](./d3dcull.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-145">El valor predeterminado es D3DCULL \_ CCW.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-145">The default value is D3DCULL\_CCW.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-146"><span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS \_ ZFUNC**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-146"><span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS\_ZFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-147">Un miembro del tipo enumerado [**D3DCMPFUNC**](./d3dcmpfunc.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-147">One member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-148">El valor predeterminado es D3DCMP \_ LESSEQUAL.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-148">The default value is D3DCMP\_LESSEQUAL.</span></span> <span data-ttu-id="eb6f4-149">Este miembro permite a una aplicación aceptar o rechazar un píxel, en función de su distancia de la cámara.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-149">This member enables an application to accept or reject a pixel, based on its distance from the camera.</span></span>

<span data-ttu-id="eb6f4-150">El valor de profundidad del píxel se compara con el valor del búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-150">The depth value of the pixel is compared with the depth-buffer value.</span></span> <span data-ttu-id="eb6f4-151">Si el valor de profundidad del píxel pasa la función de comparación, se escribe el píxel.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-151">If the depth value of the pixel passes the comparison function, the pixel is written.</span></span>

<span data-ttu-id="eb6f4-152">El valor de profundidad se escribe en el búfer de profundidad solo si el estado de representación es **true**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-152">The depth value is written to the depth buffer only if the render state is **TRUE**.</span></span>

<span data-ttu-id="eb6f4-153">Los rasterizadores de software y muchos aceleradores de hardware funcionan más rápido si se produce un error en la prueba de profundidad, ya que no hay necesidad de filtrar y modular la textura si el píxel no se va a representar.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-153">Software rasterizers and many hardware accelerators work faster if the depth test fails, because there is no need to filter and modulate the texture if the pixel is not going to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-154"><span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS \_ ALPHAREF**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-154"><span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS\_ALPHAREF**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-155">Valor que especifica un valor alfa de referencia con el que se prueban los píxeles cuando está habilitada la prueba alfa.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-155">Value that specifies a reference alpha value against which pixels are tested when alpha testing is enabled.</span></span> <span data-ttu-id="eb6f4-156">Se trata de un valor de 8 bits colocado en los 8 bits inferiores del valor DWORD de representación de estado.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-156">This is an 8-bit value placed in the low 8 bits of the DWORD render-state value.</span></span> <span data-ttu-id="eb6f4-157">Los valores pueden oscilar entre 0x00000000 y 0x000000FF.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-157">Values can range from 0x00000000 through 0x000000FF.</span></span> <span data-ttu-id="eb6f4-158">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-158">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-159"><span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS \_ ALPHAFUNC**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-159"><span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS\_ALPHAFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-160">Un miembro del tipo enumerado [**D3DCMPFUNC**](./d3dcmpfunc.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-160">One member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-161">El valor predeterminado es D3DCMP \_ siempre.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-161">The default value is D3DCMP\_ALWAYS.</span></span> <span data-ttu-id="eb6f4-162">Este miembro permite a una aplicación aceptar o rechazar un píxel, en función de su valor alfa.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-162">This member enables an application to accept or reject a pixel, based on its alpha value.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-163"><span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS \_ DITHERENABLE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-163"><span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS\_DITHERENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-164">**True** para habilitar el tramado.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-164">**TRUE** to enable dithering.</span></span> <span data-ttu-id="eb6f4-165">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-165">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-166"><span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS \_ ALPHABLENDENABLE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-166"><span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS\_ALPHABLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-167">**True** para habilitar la transparencia combinada alfa.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-167">**TRUE** to enable alpha-blended transparency.</span></span> <span data-ttu-id="eb6f4-168">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-168">The default value is **FALSE**.</span></span>

<span data-ttu-id="eb6f4-169">El tipo de combinación alfa viene determinado por los Estados de \_ representación D3DRS SRCBLEND y D3DRS \_ DESTBLEND.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-169">The type of alpha blending is determined by the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-170"><span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS \_ FOGENABLE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-170"><span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS\_FOGENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-171">**True** para habilitar la combinación de niebla.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-171">**TRUE** to enable fog blending.</span></span> <span data-ttu-id="eb6f4-172">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-172">The default value is **FALSE**.</span></span> <span data-ttu-id="eb6f4-173">Para obtener más información sobre el uso de la combinación de niebla, consulte [niebla](fog.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-173">For more information about using fog blending, see [Fog](fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-174"><span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS \_ SPECULARENABLE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-174"><span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS\_SPECULARENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-175">**True** para habilitar los reflejos especulares.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-175">**TRUE** to enable specular highlights.</span></span> <span data-ttu-id="eb6f4-176">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-176">The default value is **FALSE**.</span></span>

<span data-ttu-id="eb6f4-177">Los reflejos especulares se calculan como si todos los vértices del objeto que se iluminan se encuentran en el origen del objeto.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-177">Specular highlights are calculated as though every vertex in the object being lit is at the object's origin.</span></span> <span data-ttu-id="eb6f4-178">Esto proporciona los resultados esperados siempre que el objeto se modela en torno al origen y la distancia desde la luz al objeto es relativamente grande.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-178">This gives the expected results as long as the object is modeled around the origin and the distance from the light to the object is relatively large.</span></span> <span data-ttu-id="eb6f4-179">En otros casos, los resultados son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-179">In other cases, the results as undefined.</span></span>

<span data-ttu-id="eb6f4-180">Cuando este miembro está establecido en **true**, el color especular se agrega al color base después de la textura Cascade, pero antes de la combinación alfa.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-180">When this member is set to **TRUE**, the specular color is added to the base color after the texture cascade but before alpha blending.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-181"><span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRS \_ FOGCOLOR**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-181"><span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRS\_FOGCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-182">Valor cuyo tipo es [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-182">Value whose type is [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="eb6f4-183">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-183">The default value is 0.</span></span> <span data-ttu-id="eb6f4-184">Para obtener más información sobre el color de la niebla, vea [niebla color (Direct3D 9)](fog-color.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-184">For more information about fog color, see [Fog Color (Direct3D 9)](fog-color.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-185"><span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS \_ FOGTABLEMODE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-185"><span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS\_FOGTABLEMODE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-186">La fórmula de niebla que se va a utilizar para la niebla de píxeles.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-186">The fog formula to be used for pixel fog.</span></span> <span data-ttu-id="eb6f4-187">Establezca en uno de los miembros del tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-187">Set to one of the members of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-188">El valor predeterminado es D3DFOG \_ None.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-188">The default value is D3DFOG\_NONE.</span></span> <span data-ttu-id="eb6f4-189">Para obtener más información sobre la niebla de píxeles, vea [niebla de píxeles (Direct3D 9)](pixel-fog.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-189">For more information about pixel fog, see [Pixel Fog (Direct3D 9)](pixel-fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-190"><span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS \_ FOGSTART**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-190"><span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS\_FOGSTART**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-191">Profundidad a la que se inician los efectos de niebla de píxeles o vértices para el modo de niebla lineal.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-191">Depth at which pixel or vertex fog effects begin for linear fog mode.</span></span> <span data-ttu-id="eb6f4-192">El valor predeterminado es 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-192">The default value is 0.0f.</span></span> <span data-ttu-id="eb6f4-193">La profundidad se especifica en el espacio universal para la niebla de vértices y el espacio \[ de dispositivo 0,0, 1,0 \] o el espacio universal para la niebla de píxeles.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-193">Depth is specified in world space for vertex fog and either device space \[0.0, 1.0\] or world space for pixel fog.</span></span> <span data-ttu-id="eb6f4-194">En el caso de la niebla de píxeles, estos valores se encuentran en el espacio de dispositivo cuando el sistema utiliza z para los cálculos de niebla y el espacio mundial cuando el sistema utiliza la niebla relativa a la vista (niebla).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-194">For pixel fog, these values are in device space when the system uses z for fog calculations and world-world space when the system is using eye-relative fog (w-fog).</span></span> <span data-ttu-id="eb6f4-195">Para obtener más información, vea [parámetros de niebla (Direct3D 9)](fog-parameters.md) y [profundidad en relación con la profundidad basada en Z](pixel-fog.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-195">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md) and [Eye-Relative vs. Z-based Depth](pixel-fog.md).</span></span>

<span data-ttu-id="eb6f4-196">Los valores de este estado de representación son valores de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-196">Values for this render state are floating-point values.</span></span> <span data-ttu-id="eb6f4-197">Dado que el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, tal y como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-197">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
pDevice9->SetRenderState(D3DRS_FOGSTART, 
                         *((DWORD*) (&fFogStart)));
```



</dd> <dt>

<span data-ttu-id="eb6f4-198"><span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS \_ FOGEND**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-198"><span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS\_FOGEND**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-199">Profundidad en la que los efectos de niebla de píxeles o vértices terminan en el modo de niebla lineal.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-199">Depth at which pixel or vertex fog effects end for linear fog mode.</span></span> <span data-ttu-id="eb6f4-200">El valor predeterminado es 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-200">The default value is 1.0f.</span></span> <span data-ttu-id="eb6f4-201">La profundidad se especifica en el espacio universal para la niebla de vértices y el espacio \[ de dispositivo 0,0, 1,0 \] o el espacio universal para la niebla de píxeles.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-201">Depth is specified in world space for vertex fog and either device space \[0.0, 1.0\] or world space for pixel fog.</span></span> <span data-ttu-id="eb6f4-202">En el caso de la niebla de píxeles, estos valores se encuentran en el espacio de dispositivo cuando el sistema utiliza z para los cálculos de niebla y en el espacio universal cuando el sistema utiliza niebla relativa a la vista (niebla).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-202">For pixel fog, these values are in device space when the system uses z for fog calculations and in world space when the system is using eye-relative fog (w-fog).</span></span> <span data-ttu-id="eb6f4-203">Para obtener más información, vea [parámetros de niebla (Direct3D 9)](fog-parameters.md) y [profundidad en relación con la profundidad basada en Z](pixel-fog.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-203">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md) and [Eye-Relative vs. Z-based Depth](pixel-fog.md).</span></span>

<span data-ttu-id="eb6f4-204">Los valores de este estado de representación son valores de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-204">Values for this render state are floating-point values.</span></span> <span data-ttu-id="eb6f4-205">Dado que el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, tal y como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-205">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_FOGEND, *((DWORD*) (&fFogEnd)));
```



</dd> <dt>

<span data-ttu-id="eb6f4-206"><span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**D3DRS \_ FOGDENSITY**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-206"><span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**D3DRS\_FOGDENSITY**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-207">Densidad de niebla para la niebla de píxeles o vértices usada en los modos de niebla exponencial (D3DFOG \_ EXP y D3DFOG \_ EXP2).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-207">Fog density for pixel or vertex fog used in the exponential fog modes (D3DFOG\_EXP and D3DFOG\_EXP2).</span></span> <span data-ttu-id="eb6f4-208">Los valores de densidad válidos van de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-208">Valid density values range from 0.0 through 1.0.</span></span> <span data-ttu-id="eb6f4-209">El valor predeterminado es 1,0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-209">The default value is 1.0.</span></span> <span data-ttu-id="eb6f4-210">Para obtener más información, vea [parámetros de niebla (Direct3D 9)](fog-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-210">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

<span data-ttu-id="eb6f4-211">Los valores de este estado de representación son valores de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-211">Values for this render state are floating-point values.</span></span> <span data-ttu-id="eb6f4-212">Dado que el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, tal y como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-212">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
    m_pDevice9->SetRenderState(D3DRS_FOGDENSITY, *((DWORD*) (&fFogDensity)));
```



</dd> <dt>

<span data-ttu-id="eb6f4-213"><span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS \_ RANGEFOGENABLE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-213"><span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS\_RANGEFOGENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-214">**True** para habilitar la niebla de vértices basada en intervalo.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-214">**TRUE** to enable range-based vertex fog.</span></span> <span data-ttu-id="eb6f4-215">El valor predeterminado es **false**, en cuyo caso el sistema utiliza la niebla basada en la profundidad.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-215">The default value is **FALSE**, in which case the system uses depth-based fog.</span></span> <span data-ttu-id="eb6f4-216">En la niebla basada en intervalo, la distancia de un objeto desde el visor se usa para calcular los efectos de niebla, no la profundidad del objeto (es decir, la coordenada z) de la escena.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-216">In range-based fog, the distance of an object from the viewer is used to compute fog effects, not the depth of the object (that is, the z-coordinate) in the scene.</span></span> <span data-ttu-id="eb6f4-217">En la niebla basada en intervalo, todos los métodos de niebla funcionan como de costumbre, salvo que usan el intervalo en lugar de la profundidad en los cálculos.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-217">In range-based fog, all fog methods work as usual, except that they use range instead of depth in the computations.</span></span>

<span data-ttu-id="eb6f4-218">El intervalo es el factor correcto que se debe usar para los cálculos de niebla, pero la profundidad se usa normalmente en su lugar porque el intervalo lleva mucho tiempo en proceso y la profundidad ya está disponible.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-218">Range is the correct factor to use for fog computations, but depth is commonly used instead because range is time-consuming to compute and depth is generally already available.</span></span> <span data-ttu-id="eb6f4-219">El uso de Depth para calcular la niebla tiene el efecto no deseado de que la luneta térmica de los objetos periféricos cambie a medida que se mueve el ojo del visor; en este caso, la profundidad cambia y el intervalo permanece constante.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-219">Using depth to calculate fog has the undesirable effect of having the fogginess of peripheral objects change as the viewer's eye moves - in this case, the depth changes and the range remains constant.</span></span>

<span data-ttu-id="eb6f4-220">Dado que ningún hardware admite actualmente la niebla basada en intervalos por píxel, la corrección del intervalo solo se ofrece para la niebla de vértice.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-220">Because no hardware currently supports per-pixel range-based fog, range correction is offered only for vertex fog.</span></span>

<span data-ttu-id="eb6f4-221">Para obtener más información, vea [niebla de vértices (Direct3D 9)](vertex-fog.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-221">For more information, see [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-222"><span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS \_ STENCILENABLE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-222"><span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS\_STENCILENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-223">**True** para habilitar el estarcido o **false** para deshabilitar el estarcido.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-223">**TRUE** to enable stenciling, or **FALSE** to disable stenciling.</span></span> <span data-ttu-id="eb6f4-224">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-224">The default value is **FALSE**.</span></span> <span data-ttu-id="eb6f4-225">Para obtener más información, vea [técnicas de búfer de estarcido (Direct3D 9)](stencil-buffer-techniques.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-225">For more information, see [Stencil Buffer Techniques (Direct3D 9)](stencil-buffer-techniques.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-226"><span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS \_ STENCILFAIL**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-226"><span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS\_STENCILFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-227">Operación de estarcido que se va a realizar si se produce un error en la prueba de estarcido.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-227">Stencil operation to perform if the stencil test fails.</span></span> <span data-ttu-id="eb6f4-228">Los valores son del tipo enumerado [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-228">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-229">El valor predeterminado es D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-229">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-230"><span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS \_ STENCILZFAIL**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-230"><span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS\_STENCILZFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-231">Operación de estarcido que se va a realizar si se supera la prueba de estarcido y se produce un error en la prueba de profundidad (prueba z).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-231">Stencil operation to perform if the stencil test passes and the depth test (z-test) fails.</span></span> <span data-ttu-id="eb6f4-232">Los valores son del tipo enumerado [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-232">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-233">El valor predeterminado es D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-233">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-234"><span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS \_ STENCILPASS**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-234"><span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS\_STENCILPASS**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-235">Operación de estarcido que se va a realizar si se superan las pruebas de la galería de símbolos y la profundidad (z).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-235">Stencil operation to perform if both the stencil and the depth (z) tests pass.</span></span> <span data-ttu-id="eb6f4-236">Los valores son del tipo enumerado [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-236">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-237">El valor predeterminado es D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-237">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-238"><span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS \_ STENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-238"><span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS\_STENCILFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-239">Función de comparación para la prueba de estarcido.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-239">Comparison function for the stencil test.</span></span> <span data-ttu-id="eb6f4-240">Los valores son del tipo enumerado [**D3DCMPFUNC**](./d3dcmpfunc.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-240">Values are from the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-241">El valor predeterminado es D3DCMP \_ siempre.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-241">The default value is D3DCMP\_ALWAYS.</span></span>

<span data-ttu-id="eb6f4-242">La función de comparación se usa para comparar el valor de referencia con una entrada de búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-242">The comparison function is used to compare the reference value to a stencil buffer entry.</span></span> <span data-ttu-id="eb6f4-243">Esta comparación se aplica solo a los bits del valor de referencia y la entrada del búfer de estarcido que se establecen en la máscara de la galería de símbolos (establecida por el estado de representación de D3DRS \_ STENCILMASK).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-243">This comparison applies only to the bits in the reference value and stencil buffer entry that are set in the stencil mask (set by the D3DRS\_STENCILMASK render state).</span></span> <span data-ttu-id="eb6f4-244">Si **es true**, la prueba de estarcido se supera.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-244">If **TRUE**, the stencil test passes.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-245"><span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS \_ STENCILREF**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-245"><span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS\_STENCILREF**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-246">Valor de referencia int para la prueba de estarcido.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-246">An int reference value for the stencil test.</span></span> <span data-ttu-id="eb6f4-247">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-247">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-248"><span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS \_ STENCILMASK**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-248"><span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS\_STENCILMASK**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-249">Máscara aplicada al valor de referencia y a cada entrada de búfer de estarcido para determinar los bits significativos para la prueba de estarcido.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-249">Mask applied to the reference value and each stencil buffer entry to determine the significant bits for the stencil test.</span></span> <span data-ttu-id="eb6f4-250">La máscara predeterminada es 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-250">The default mask is 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-251"><span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS \_ STENCILWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-251"><span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS\_STENCILWRITEMASK**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-252">Máscara de escritura aplicada a los valores escritos en el búfer de estarcido.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-252">Write mask applied to values written into the stencil buffer.</span></span> <span data-ttu-id="eb6f4-253">La máscara predeterminada es 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-253">The default mask is 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-254"><span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS \_ TEXTUREFACTOR**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-254"><span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS\_TEXTUREFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-255">Color que se usa para la combinación de varias texturas con el \_ argumento D3DTA TFACTOR Texture-blending o la \_ operación D3DTOP BLENDFACTORALPHA Texture-blending.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-255">Color used for multiple-texture blending with the D3DTA\_TFACTOR texture-blending argument or the D3DTOP\_BLENDFACTORALPHA texture-blending operation.</span></span> <span data-ttu-id="eb6f4-256">El valor asociado es una variable [**D3DCOLOR**](d3dcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-256">The associated value is a [**D3DCOLOR**](d3dcolor.md) variable.</span></span> <span data-ttu-id="eb6f4-257">El valor predeterminado es blanco opaco (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-257">The default value is opaque white (0xFFFFFFFF).</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-258"><span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS \_ WRAP0**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-258"><span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS\_WRAP0**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-259">Comportamiento de ajuste de textura para varios conjuntos de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-259">Texture-wrapping behavior for multiple sets of texture coordinates.</span></span> <span data-ttu-id="eb6f4-260">Los valores válidos para este estado de representación pueden ser cualquier combinación de las \_ marcas D3DWRAPCOORD 0 (o D3DWRAP \_ u), D3DWRAPCOORD \_ 1 (o D3DWRAP \_ V), D3DWRAPCOORD \_ 2 (o D3DWRAP \_ W) y D3DWRAPCOORD \_ 3.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-260">Valid values for this render state can be any combination of the D3DWRAPCOORD\_0 (or D3DWRAP\_U), D3DWRAPCOORD\_1 (or D3DWRAP\_V), D3DWRAPCOORD\_2 (or D3DWRAP\_W), and D3DWRAPCOORD\_3 flags.</span></span> <span data-ttu-id="eb6f4-261">Esto hace que el sistema se ajuste en la dirección de las dimensiones primera, segunda, tercera y cuarta, que a veces se denominan direcciones s, t, r y q, para una textura determinada.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-261">These cause the system to wrap in the direction of the first, second, third, and fourth dimensions, sometimes referred to as the s, t, r, and q directions, for a given texture.</span></span> <span data-ttu-id="eb6f4-262">El valor predeterminado para este estado de representación es 0 (ajuste deshabilitado en todas las direcciones).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-262">The default value for this render state is 0 (wrapping disabled in all directions).</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-263"><span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS \_ WRAP1**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-263"><span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS\_WRAP1**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-264">Vea D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-264">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-265"><span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS \_ WRAP2**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-265"><span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS\_WRAP2**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-266">Vea D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-266">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-267"><span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS \_ WRAP3**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-267"><span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS\_WRAP3**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-268">Vea D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-268">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-269"><span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS \_ WRAP4**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-269"><span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS\_WRAP4**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-270">Vea D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-270">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-271"><span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS \_ WRAP5**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-271"><span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS\_WRAP5**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-272">Vea D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-272">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-273"><span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS \_ WRAP6**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-273"><span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS\_WRAP6**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-274">Vea D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-274">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-275"><span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS \_ WRAP7**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-275"><span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS\_WRAP7**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-276">Vea D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-276">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-277"><span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**Recorte de D3DRS \_**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-277"><span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**D3DRS\_CLIPPING**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-278">**True** para habilitar el recorte primitivo por Direct3D o **false** para deshabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-278">**TRUE** to enable primitive clipping by Direct3D, or **FALSE** to disable it.</span></span> <span data-ttu-id="eb6f4-279">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-279">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-280"><span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**\_Iluminación D3DRS**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-280"><span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**D3DRS\_LIGHTING**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-281">**True** para habilitar la iluminación de Direct3D o **false** para deshabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-281">**TRUE** to enable Direct3D lighting, or **FALSE** to disable it.</span></span> <span data-ttu-id="eb6f4-282">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-282">The default value is **TRUE**.</span></span> <span data-ttu-id="eb6f4-283">Solo los vértices que incluyen el vértice normal están correctamente iluminados; los vértices que no contienen una normal emplean un producto de punto de 0 en todos los cálculos de iluminación.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-283">Only vertices that include a vertex normal are properly lit; vertices that do not contain a normal employ a dot product of 0 in all lighting calculations.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-284"><span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**\_Ambiente D3DRS**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-284"><span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**D3DRS\_AMBIENT**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-285">Color claro ambiente.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-285">Ambient light color.</span></span> <span data-ttu-id="eb6f4-286">Este valor es de tipo [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-286">This value is of type [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="eb6f4-287">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-287">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-288"><span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**D3DRS \_ FOGVERTEXMODE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-288"><span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**D3DRS\_FOGVERTEXMODE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-289">Fórmula de niebla que se va a usar para la niebla de vértice.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-289">Fog formula to be used for vertex fog.</span></span> <span data-ttu-id="eb6f4-290">Se establece en un miembro del tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-290">Set to one member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-291">El valor predeterminado es D3DFOG \_ None.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-291">The default value is D3DFOG\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-292"><span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS \_ COLORVERTEX**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-292"><span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS\_COLORVERTEX**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-293">**True** para habilitar el color por vértice o **false** para deshabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-293">**TRUE** to enable per-vertex color or **FALSE** to disable it.</span></span> <span data-ttu-id="eb6f4-294">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-294">The default value is **TRUE**.</span></span> <span data-ttu-id="eb6f4-295">La habilitación del color por vértice permite que el sistema incluya el color definido para los vértices individuales en los cálculos de iluminación.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-295">Enabling per-vertex color allows the system to include the color defined for individual vertices in its lighting calculations.</span></span>

<span data-ttu-id="eb6f4-296">Para obtener más información, vea los siguientes Estados de representación:</span><span class="sxs-lookup"><span data-stu-id="eb6f4-296">For more information, see the following render states:</span></span>

-   <span data-ttu-id="eb6f4-297">D3DRS \_ DIFFUSEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="eb6f4-297">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>
-   <span data-ttu-id="eb6f4-298">D3DRS \_ SPECULARMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="eb6f4-298">D3DRS\_SPECULARMATERIALSOURCE</span></span>
-   <span data-ttu-id="eb6f4-299">D3DRS \_ AMBIENTMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="eb6f4-299">D3DRS\_AMBIENTMATERIALSOURCE</span></span>
-   <span data-ttu-id="eb6f4-300">D3DRS \_ EMISSIVEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="eb6f4-300">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-301"><span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS \_ LOCALVIEWER**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-301"><span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS\_LOCALVIEWER**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-302">**True** para habilitar los reflejos especulares relativos a la cámara, o **false** para usar los reflejos especulares ortogonales.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-302">**TRUE** to enable camera-relative specular highlights, or **FALSE** to use orthogonal specular highlights.</span></span> <span data-ttu-id="eb6f4-303">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-303">The default value is **TRUE**.</span></span> <span data-ttu-id="eb6f4-304">Las aplicaciones que usan la proyección ortogonal deben especificar **false**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-304">Applications that use orthogonal projection should specify **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-305"><span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS \_ NORMALIZENORMALS**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-305"><span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS\_NORMALIZENORMALS**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-306">**True** para habilitar la normalización automática de las normales de vértice o **false** para deshabilitarla.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-306">**TRUE** to enable automatic normalization of vertex normals, or **FALSE** to disable it.</span></span> <span data-ttu-id="eb6f4-307">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-307">The default value is **FALSE**.</span></span> <span data-ttu-id="eb6f4-308">Al habilitar esta característica, el sistema normaliza las normales de vértice para los vértices después de transformarlos en el espacio de la cámara, lo que puede consumir mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-308">Enabling this feature causes the system to normalize the vertex normals for vertices after transforming them to camera space, which can be computationally time-consuming.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-309"><span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS \_ DIFFUSEMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-309"><span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS\_DIFFUSEMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-310">Origen de color difuso para los cálculos de iluminación.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-310">Diffuse color source for lighting calculations.</span></span> <span data-ttu-id="eb6f4-311">Los valores válidos son miembros del tipo enumerado [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-311">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-312">El valor predeterminado es D3DMCS \_ COLOR1.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-312">The default value is D3DMCS\_COLOR1.</span></span> <span data-ttu-id="eb6f4-313">El valor de este estado de representación se usa solo si el \_ Estado de representación de D3DRS COLORVERTEX está establecido en **true**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-313">The value for this render state is used only if the D3DRS\_COLORVERTEX render state is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-314"><span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS \_ SPECULARMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-314"><span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS\_SPECULARMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-315">Origen de color especular para los cálculos de iluminación.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-315">Specular color source for lighting calculations.</span></span> <span data-ttu-id="eb6f4-316">Los valores válidos son miembros del tipo enumerado [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-316">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-317">El valor predeterminado es D3DMCS \_ COLOR2.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-317">The default value is D3DMCS\_COLOR2.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-318"><span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS \_ AMBIENTMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-318"><span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS\_AMBIENTMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-319">Origen de color ambiente para los cálculos de iluminación.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-319">Ambient color source for lighting calculations.</span></span> <span data-ttu-id="eb6f4-320">Los valores válidos son miembros del tipo enumerado [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-320">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-321">El valor predeterminado es \_ material D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-321">The default value is D3DMCS\_MATERIAL.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-322"><span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS \_ EMISSIVEMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-322"><span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS\_EMISSIVEMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-323">Origen de color emisor para los cálculos de iluminación.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-323">Emissive color source for lighting calculations.</span></span> <span data-ttu-id="eb6f4-324">Los valores válidos son miembros del tipo enumerado [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-324">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-325">El valor predeterminado es \_ material D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-325">The default value is D3DMCS\_MATERIAL.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-326"><span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS \_ VERTEXBLEND**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-326"><span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS\_VERTEXBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-327">Número de matrices que se van a usar para realizar la combinación de geometría, si existe.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-327">Number of matrices to use to perform geometry blending, if any.</span></span> <span data-ttu-id="eb6f4-328">Los valores válidos son miembros del tipo enumerado [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-328">Valid values are members of the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-329">El valor predeterminado es D3DVBF \_ Disable.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-329">The default value is D3DVBF\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-330"><span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS \_ CLIPPLANEENABLE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-330"><span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS\_CLIPPLANEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-331">Habilita o deshabilita los planos de recorte definidos por el usuario.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-331">Enables or disables user-defined clipping planes.</span></span> <span data-ttu-id="eb6f4-332">Los valores válidos son cualquier valor DWORD en el que el estado de cada bit (establecido o no establecido) alterna el estado de activación de un plano de recorte definido por el usuario correspondiente.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-332">Valid values are any DWORD in which the status of each bit (set or not set) toggles the activation state of a corresponding user-defined clipping plane.</span></span> <span data-ttu-id="eb6f4-333">El bit menos significativo (bit 0) controla el primer plano de recorte en el índice 0 y los bits subsiguientes controlan la activación de los planos de recorte en los índices más altos.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-333">The least significant bit (bit 0) controls the first clipping plane at index 0, and subsequent bits control the activation of clipping planes at higher indexes.</span></span> <span data-ttu-id="eb6f4-334">Si se establece un bit, el sistema aplica el plano de recorte adecuado durante la representación de la escena.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-334">If a bit is set, the system applies the appropriate clipping plane during scene rendering.</span></span> <span data-ttu-id="eb6f4-335">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-335">The default value is 0.</span></span>

<span data-ttu-id="eb6f4-336">Las macros [**D3DCLIPPLANEn**](d3dclipplanen.md) se definen para proporcionar una manera cómoda de habilitar los planos de recorte.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-336">The [**D3DCLIPPLANEn**](d3dclipplanen.md) macros are defined to provide a convenient way to enable clipping planes.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-337"><span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS \_ puntuación**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-337"><span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS\_POINTSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-338">Valor flotante que especifica el tamaño que se va a usar para el cálculo del tamaño de punto en los casos en los que no se especifica el tamaño de punto para cada vértice.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-338">A float value that specifies the size to use for point size computation in cases where point size is not specified for each vertex.</span></span> <span data-ttu-id="eb6f4-339">Este valor no se usa cuando el vértice contiene un tamaño de punto.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-339">This value is not used when the vertex contains point size.</span></span> <span data-ttu-id="eb6f4-340">Este valor se encuentra en unidades de espacio de pantalla si D3DRS \_ POINTSCALEENABLE es **false**; de lo contrario, este valor está en unidades de espacio universal.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-340">This value is in screen space units if D3DRS\_POINTSCALEENABLE is **FALSE**; otherwise this value is in world space units.</span></span> <span data-ttu-id="eb6f4-341">El valor predeterminado es el valor que devuelve un controlador.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-341">The default value is the value a driver returns.</span></span> <span data-ttu-id="eb6f4-342">Si un controlador devuelve 0 o 1, el valor predeterminado es 64, que permite la emulación de tamaño de punto de software.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-342">If a driver returns 0 or 1, the default value is 64, which allows software point size emulation.</span></span> <span data-ttu-id="eb6f4-343">Dado que el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, tal y como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-343">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE, *((DWORD*)&pointSize));
```



</dd> <dt>

<span data-ttu-id="eb6f4-344"><span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS de \_ puntuación \_ mín.**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-344"><span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS\_POINTSIZE\_MIN**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-345">Valor flotante que especifica el tamaño mínimo de primitivas de punto.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-345">A float value that specifies the minimum size of point primitives.</span></span> <span data-ttu-id="eb6f4-346">Los primitivos de punto se fijan a este tamaño durante la representación.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-346">Point primitives are clamped to this size during rendering.</span></span> <span data-ttu-id="eb6f4-347">Si se establece en valores inferiores a 1,0, los puntos se descartan cuando el punto no cubre un centro de píxeles y el suavizado de contorno está deshabilitado o se representa con menor intensidad cuando se habilita el suavizado de contorno.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-347">Setting this to values smaller than 1.0 results in points dropping out when the point does not cover a pixel center and antialiasing is disabled or being rendered with reduced intensity when antialiasing is enabled.</span></span> <span data-ttu-id="eb6f4-348">El valor predeterminado es 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-348">The default value is 1.0f.</span></span> <span data-ttu-id="eb6f4-349">El intervalo para este valor es mayor o igual que 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-349">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="eb6f4-350">Dado que el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, tal y como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-350">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE_MIN, *((DWORD*)&pointSizeMin));
```



</dd> <dt>

<span data-ttu-id="eb6f4-351"><span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS \_ POINTSPRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-351"><span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS\_POINTSPRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-352">valor booleano.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-352">bool value.</span></span> <span data-ttu-id="eb6f4-353">Cuando **es true**, las coordenadas de textura de los primitivos de punto se establecen para que las texturas completas se asignen en cada punto.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-353">When **TRUE**, texture coordinates of point primitives are set so that full textures are mapped on each point.</span></span> <span data-ttu-id="eb6f4-354">Cuando **es false**, las coordenadas de textura de los vértices se utilizan para todo el punto.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-354">When **FALSE**, the vertex texture coordinates are used for the entire point.</span></span> <span data-ttu-id="eb6f4-355">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-355">The default value is **FALSE**.</span></span> <span data-ttu-id="eb6f4-356">Puede obtener los puntos de un solo píxel con estilo de DirectX 7 Si establece D3DRS \_ POINTSCALEENABLE en **false** y D3DRS \_ en 1,0, que son los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-356">You can achieve DirectX 7 style single-pixel points by setting D3DRS\_POINTSCALEENABLE to **FALSE** and D3DRS\_POINTSIZE to 1.0, which are the default values.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-357"><span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS \_ POINTSCALEENABLE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-357"><span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS\_POINTSCALEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-358">valor booleano que controla el cálculo del tamaño de los primitivos de punto.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-358">bool value that controls computation of size for point primitives.</span></span> <span data-ttu-id="eb6f4-359">Si es **true**, el tamaño del punto se interpreta como un valor de espacio de la cámara y se escala mediante la función Distance y el frustum para viewport de la escala del eje y para calcular el tamaño final del punto de espacio de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-359">When **TRUE**, the point size is interpreted as a camera space value and is scaled by the distance function and the frustum to viewport y-axis scaling to compute the final screen-space point size.</span></span> <span data-ttu-id="eb6f4-360">Cuando es **false**, el tamaño del punto se interpreta como espacio de la pantalla y se usa directamente.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-360">When **FALSE**, the point size is interpreted as screen space and used directly.</span></span> <span data-ttu-id="eb6f4-361">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-361">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-362"><span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS \_ POINTSCALE \_**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-362"><span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS\_POINTSCALE\_A**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-363">Un valor de tipo float que controla la atenuación de tamaño basado en la distancia para los primitivos de punto.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-363">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="eb6f4-364">Activo solo cuando D3DRS \_ POINTSCALEENABLE es **true**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-364">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="eb6f4-365">El valor predeterminado es 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-365">The default value is 1.0f.</span></span> <span data-ttu-id="eb6f4-366">El intervalo para este valor es mayor o igual que 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-366">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="eb6f4-367">Dado que el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, tal y como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-367">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_A, *((DWORD*)&pointScaleA));
```



</dd> <dt>

<span data-ttu-id="eb6f4-368"><span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS \_ POINTSCALE \_ B**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-368"><span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS\_POINTSCALE\_B**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-369">Un valor de tipo float que controla la atenuación de tamaño basado en la distancia para los primitivos de punto.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-369">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="eb6f4-370">Activo solo cuando D3DRS \_ POINTSCALEENABLE es **true**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-370">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="eb6f4-371">El valor predeterminado es 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-371">The default value is 0.0f.</span></span> <span data-ttu-id="eb6f4-372">El intervalo para este valor es mayor o igual que 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-372">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="eb6f4-373">Dado que el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, tal y como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-373">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_B, *((DWORD*)&pointScaleB));
```



</dd> <dt>

<span data-ttu-id="eb6f4-374"><span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS \_ POINTSCALE \_ C**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-374"><span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS\_POINTSCALE\_C**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-375">Un valor de tipo float que controla la atenuación de tamaño basado en la distancia para los primitivos de punto.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-375">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="eb6f4-376">Activo solo cuando D3DRS \_ POINTSCALEENABLE es **true**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-376">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="eb6f4-377">El valor predeterminado es 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-377">The default value is 0.0f.</span></span> <span data-ttu-id="eb6f4-378">El intervalo para este valor es mayor o igual que 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-378">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="eb6f4-379">Dado que el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, tal y como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-379">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_C, *((DWORD*)&pointScaleC));
```



</dd> <dt>

<span data-ttu-id="eb6f4-380"><span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS \_ MULTISAMPLEANTIALIAS**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-380"><span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS\_MULTISAMPLEANTIALIAS**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-381">valor booleano que determina cómo se calculan los ejemplos individuales cuando se usa un búfer de representación y destino de ejemplo múltiple.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-381">bool value that determines how individual samples are computed when using a multisample render-target buffer.</span></span> <span data-ttu-id="eb6f4-382">Cuando se establece en **true**, se calculan varios ejemplos para que el suavizado de contorno completo de la escena se realice mediante el muestreo en posiciones de ejemplo diferentes para cada ejemplo múltiple.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-382">When set to **TRUE**, the multiple samples are computed so that full-scene antialiasing is performed by sampling at different sample positions for each multiple sample.</span></span> <span data-ttu-id="eb6f4-383">Cuando se establece en **false**, todos los ejemplos se escriben con el mismo valor de ejemplo, muestreado en el centro de píxeles, lo que permite la representación sin suavizado de contorno en un búfer de muestreo múltiple.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-383">When set to **FALSE**, the multiple samples are all written with the same sample value, sampled at the pixel center, which allows non-antialiased rendering to a multisample buffer.</span></span> <span data-ttu-id="eb6f4-384">Este estado de representación no tiene ningún efecto cuando se representa en un búfer de ejemplo único.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-384">This render state has no effect when rendering to a single sample buffer.</span></span> <span data-ttu-id="eb6f4-385">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-385">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-386"><span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS \_ MULTISAMPLEMASK**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-386"><span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS\_MULTISAMPLEMASK**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-387">Cada bit de esta máscara, que comienza en el bit menos significativo (LSB), controla la modificación de uno de los ejemplos en un destino de representación Multimuestra.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-387">Each bit in this mask, starting at the least significant bit (LSB), controls modification of one of the samples in a multisample render target.</span></span> <span data-ttu-id="eb6f4-388">Por lo tanto, para un destino de representación de 8 muestras, el byte bajo contiene las ocho escrituras habilitadas para cada una de las ocho muestras.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-388">Thus, for an 8-sample render target, the low byte contains the eight write enables for each of the eight samples.</span></span> <span data-ttu-id="eb6f4-389">Este estado de representación no tiene ningún efecto cuando se representa en un búfer de ejemplo único.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-389">This render state has no effect when rendering to a single sample buffer.</span></span> <span data-ttu-id="eb6f4-390">El valor predeterminado es 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-390">The default value is 0xFFFFFFFF.</span></span>

<span data-ttu-id="eb6f4-391">Este estado de representación permite el uso de un búfer de ejemplo múltiples como búfer de acumulación, con una representación de la geometría en la que cada paso actualiza un subconjunto de muestras.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-391">This render state enables use of a multisample buffer as an accumulation buffer, doing multipass rendering of geometry where each pass updates a subset of samples.</span></span>

<span data-ttu-id="eb6f4-392">Si hay n muestras de varios ejemplos y de k habilitadas, la intensidad resultante de la imagen representada debe ser k/n.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-392">If there are n multisamples and k enabled samples, the resulting intensity of the rendered image should be k/n.</span></span> <span data-ttu-id="eb6f4-393">Cada componente RGB de cada píxel se factoriza por k/n.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-393">Each component RGB of every pixel is factored by k/n.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-394"><span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS \_ PATCHEDGESTYLE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-394"><span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS\_PATCHEDGESTYLE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-395">Establece si los bordes de la revisión utilizarán la teselación de estilo flotante.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-395">Sets whether patch edges will use float style tessellation.</span></span> <span data-ttu-id="eb6f4-396">Los valores posibles se definen mediante el tipo enumerado [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-396">Possible values are defined by the [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-397">El valor predeterminado es D3DPATCHEDGE \_ discreto.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-397">The default value is D3DPATCHEDGE\_DISCRETE.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-398"><span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS \_ DEBUGMONITORTOKEN**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-398"><span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS\_DEBUGMONITORTOKEN**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-399">Solo se establece para depurar el monitor.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-399">Set only for debugging the monitor.</span></span> <span data-ttu-id="eb6f4-400">Los valores posibles se definen mediante el tipo enumerado [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-400">Possible values are defined by the [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-401">Tenga en cuenta que si \_ se establece D3DRS DEBUGMONITORTOKEN, la llamada se trata como si pasara un token al monitor de depuración.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-401">Note that if D3DRS\_DEBUGMONITORTOKEN is set, the call is treated as passing a token to the debug monitor.</span></span> <span data-ttu-id="eb6f4-402">Por ejemplo, si-después de pasar D3DDMT \_ enable o D3DDMT \_ Disable a D3DRS \_ DEBUGMONITORTOKEN-se pasan otros valores de token, el estado (habilitado o deshabilitado) del monitor de depuración seguirá siendo persistente.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-402">For example, if - after passing D3DDMT\_ENABLE or D3DDMT\_DISABLE to D3DRS\_DEBUGMONITORTOKEN - other token values are passed in, the state (enabled or disabled) of the debug monitor will still persist.</span></span>

<span data-ttu-id="eb6f4-403">Este estado solo es útil para las compilaciones de depuración.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-403">This state is only useful for debug builds.</span></span> <span data-ttu-id="eb6f4-404">El monitor de depuración tiene como valor predeterminado D3DDMT \_ enable.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-404">The debug monitor defaults to D3DDMT\_ENABLE.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-405"><span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS \_ \_ Max**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-405"><span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS\_POINTSIZE\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-406">Valor flotante que especifica el tamaño máximo al que se van a fijar los sprites de punto.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-406">A float value that specifies the maximum size to which point sprites will be clamped.</span></span> <span data-ttu-id="eb6f4-407">El valor debe ser menor o igual que el miembro MaxPointSize de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) y mayor o igual que D3DRS separar \_ \_ min.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-407">The value must be less than or equal to the MaxPointSize member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) and greater than or equal to D3DRS\_POINTSIZE\_MIN.</span></span> <span data-ttu-id="eb6f4-408">El valor predeterminado es 64,0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-408">The default value is 64.0.</span></span> <span data-ttu-id="eb6f4-409">Dado que el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, tal y como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-409">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_PONTSIZE_MAX, *((DWORD*)&pointSizeMax));
```



</dd> <dt>

<span data-ttu-id="eb6f4-410"><span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS \_ INDEXEDVERTEXBLENDENABLE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-410"><span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS\_INDEXEDVERTEXBLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-411">valor booleano que habilita o deshabilita la combinación de vértices indizados.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-411">bool value that enables or disables indexed vertex blending.</span></span> <span data-ttu-id="eb6f4-412">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-412">The default value is **FALSE**.</span></span> <span data-ttu-id="eb6f4-413">Cuando se establece en **true**, se habilita la combinación de vértices indizada.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-413">When set to **TRUE**, indexed vertex blending is enabled.</span></span> <span data-ttu-id="eb6f4-414">Cuando se establece en **false**, se deshabilita la mezcla de vértices indizados.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-414">When set to **FALSE**, indexed vertex blending is disabled.</span></span> <span data-ttu-id="eb6f4-415">Si este estado de representación está habilitado, el usuario debe pasar los índices de matriz como un DWORDwith empaquetado cada vértice.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-415">If this render state is enabled, the user must pass matrix indices as a packed DWORDwith every vertex.</span></span> <span data-ttu-id="eb6f4-416">Cuando el estado de representación es deshabilitado y la combinación de vértices se habilita a través del \_ Estado D3DRS VERTEXBLEND, equivale a tener índices de matriz 0, 1, 2, 3 en cada vértice.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-416">When the render state is disabled and vertex blending is enabled through the D3DRS\_VERTEXBLEND state, it is equivalent to having matrix indices 0, 1, 2, 3 in every vertex.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-417"><span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS \_ COLORWRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-417"><span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS\_COLORWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-418">Valor UINT que habilita una escritura por canal para el búfer de color de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-418">UINT value that enables a per-channel write for the render-target color buffer.</span></span> <span data-ttu-id="eb6f4-419">Un bit establecido hace que el canal de color se actualice durante la representación 3D.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-419">A set bit results in the color channel being updated during 3D rendering.</span></span> <span data-ttu-id="eb6f4-420">Un bit claro da lugar a que el canal de color no se vea afectado.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-420">A clear bit results in the color channel being unaffected.</span></span> <span data-ttu-id="eb6f4-421">Esta funcionalidad está disponible si el bit de funcionalidad de D3DPMISCCAPS \_ COLORWRITEENABLE se establece en el miembro PrimitiveMiscCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-421">This functionality is available if the D3DPMISCCAPS\_COLORWRITEENABLE capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="eb6f4-422">Este estado de representación no afecta a la operación de borrado.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-422">This render state does not affect the clear operation.</span></span> <span data-ttu-id="eb6f4-423">El valor predeterminado es 0x0000000F.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-423">The default value is 0x0000000F.</span></span>

<span data-ttu-id="eb6f4-424">Los valores válidos para este estado de representación pueden ser cualquier combinación de las \_ marcas D3DCOLORWRITEENABLE alfa, D3DCOLORWRITEENABLE \_ Blue, D3DCOLORWRITEENABLE \_ Green o D3DCOLORWRITEENABLE \_ roja.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-424">Valid values for this render state can be any combination of the D3DCOLORWRITEENABLE\_ALPHA, D3DCOLORWRITEENABLE\_BLUE, D3DCOLORWRITEENABLE\_GREEN, or D3DCOLORWRITEENABLE\_RED flags.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-425"><span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS \_ TWEENFACTOR**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-425"><span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS\_TWEENFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-426">Un valor de tipo float que controla el factor de intercalación.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-426">A float value that controls the tween factor.</span></span> <span data-ttu-id="eb6f4-427">El valor predeterminado es 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-427">The default value is 0.0f.</span></span> <span data-ttu-id="eb6f4-428">Dado que el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, tal y como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-428">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_TWEENFACTOR, *((DWORD*)&TweenFactor));
```



</dd> <dt>

<span data-ttu-id="eb6f4-429"><span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS \_ BLENDOP**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-429"><span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS\_BLENDOP**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-430">Valor que se usa para seleccionar la operación aritmética aplicada cuando el estado de representación de la mezcla alfa, D3DRS \_ ALPHABLENDENABLE, se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-430">Value used to select the arithmetic operation applied when the alpha blending render state, D3DRS\_ALPHABLENDENABLE, is set to **TRUE**.</span></span> <span data-ttu-id="eb6f4-431">Los valores válidos se definen mediante el tipo enumerado [**D3DBLENDOP**](./d3dblendop.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-431">Valid values are defined by the [**D3DBLENDOP**](./d3dblendop.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-432">El valor predeterminado es D3DBLENDOP \_ Add.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-432">The default value is D3DBLENDOP\_ADD.</span></span>

<span data-ttu-id="eb6f4-433">Si \_ no se admite la funcionalidad del dispositivo D3DPMISCCAPS BLENDOP, \_ se realiza D3DBLENDOP agregar.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-433">If the D3DPMISCCAPS\_BLENDOP device capability is not supported, then D3DBLENDOP\_ADD is performed.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-434"><span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS \_ POSITIONDEGREE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-434"><span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS\_POSITIONDEGREE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-435">N: grado de interpolación de la posición de la revisión.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-435">N-patch position interpolation degree.</span></span> <span data-ttu-id="eb6f4-436">Los valores pueden ser D3DDEGREE \_ cúbicos (valor predeterminado) o D3DDEGREE \_ linear.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-436">The values can be D3DDEGREE\_CUBIC (default) or D3DDEGREE\_LINEAR.</span></span> <span data-ttu-id="eb6f4-437">Para obtener más información, vea [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-437">For more information, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-438"><span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS \_ NORMALDEGREE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-438"><span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS\_NORMALDEGREE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-439">N: revisión del grado de interpolación normal.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-439">N-patch normal interpolation degree.</span></span> <span data-ttu-id="eb6f4-440">Los valores pueden ser D3DDEGREE \_ linear (default) o D3DDEGREE \_ cuadrático.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-440">The values can be D3DDEGREE\_LINEAR (default) or D3DDEGREE\_QUADRATIC.</span></span> <span data-ttu-id="eb6f4-441">Para obtener más información, vea [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-441">For more information, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-442"><span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS \_ SCISSORTESTENABLE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-442"><span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS\_SCISSORTESTENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-443">**True** para habilitar la prueba de tijera y **false** para deshabilitarla.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-443">**TRUE** to enable scissor testing and **FALSE** to disable it.</span></span> <span data-ttu-id="eb6f4-444">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-444">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-445"><span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS \_ SLOPESCALEDEPTHBIAS**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-445"><span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS\_SLOPESCALEDEPTHBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-446">Se usa para determinar la cantidad de sesgo que se puede aplicar a las primitivas coplanas para reducir la lucha de la z.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-446">Used to determine how much bias can be applied to co-planar primitives to reduce z-fighting.</span></span> <span data-ttu-id="eb6f4-447">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-447">The default value is 0.</span></span>

<span data-ttu-id="eb6f4-448">Bias = (Max \* D3DRS \_ SLOPESCALEDEPTHBIAS) + D3DRS \_ DEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-448">bias = (max \* D3DRS\_SLOPESCALEDEPTHBIAS) + D3DRS\_DEPTHBIAS.</span></span>

<span data-ttu-id="eb6f4-449">donde Max es la pendiente de profundidad máxima del triángulo que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-449">where max is the maximum depth slope of the triangle being rendered.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-450"><span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS \_ ANTIALIASEDLINEENABLE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-450"><span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS\_ANTIALIASEDLINEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-451">**True** para habilitar el suavizado de contorno de línea, **false** para deshabilitar el suavizado de línea.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-451">**TRUE** to enable line antialiasing, **FALSE** to disable line antialiasing.</span></span> <span data-ttu-id="eb6f4-452">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-452">The default value is **FALSE**.</span></span>

<span data-ttu-id="eb6f4-453">Al representar un destino de representación Multimuestra, D3DRS \_ ANTIALIASEDLINEENABLE se omite y se representan los alias de todas las líneas.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-453">When rendering to a multisample render target, D3DRS\_ANTIALIASEDLINEENABLE is ignored and all lines are rendered aliased.</span></span> <span data-ttu-id="eb6f4-454">Use [**ID3DXLine**](id3dxline.md) para la representación de líneas alisadas en un destino de representación Multimuestra.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-454">Use [**ID3DXLine**](id3dxline.md) for antialiased line rendering in a multisample render target.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-455"><span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS \_ MINTESSELLATIONLEVEL**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-455"><span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS\_MINTESSELLATIONLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-456">Nivel de teselación mínimo.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-456">Minimum tessellation level.</span></span> <span data-ttu-id="eb6f4-457">El valor predeterminado es 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-457">The default value is 1.0f.</span></span> <span data-ttu-id="eb6f4-458">Vea [teselación (Direct3D 9)](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-458">See [Tessellation (Direct3D 9)](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-459"><span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS \_ MAXTESSELLATIONLEVEL**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-459"><span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS\_MAXTESSELLATIONLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-460">Nivel máximo de teselación.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-460">Maximum tessellation level.</span></span> <span data-ttu-id="eb6f4-461">El valor predeterminado es 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-461">The default value is 1.0f.</span></span> <span data-ttu-id="eb6f4-462">Vea [teselación (Direct3D 9)](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-462">See [Tessellation (Direct3D 9)](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-463"><span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS \_ ADAPTIVETESS \_ X**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-463"><span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS\_ADAPTIVETESS\_X**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-464">Cantidad para dividirlas adaptable, en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-464">Amount to adaptively tessellate, in the x direction.</span></span> <span data-ttu-id="eb6f4-465">El valor predeterminado es 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-465">Default value is 0.0f.</span></span> <span data-ttu-id="eb6f4-466">Vea [teselación adaptable](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-466">See [Adaptive Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-467"><span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS \_ ADAPTIVETESS \_ Y**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-467"><span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS\_ADAPTIVETESS\_Y**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-468">Importe para dividirlas de modo adaptable, en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-468">Amount to adaptively tessellate, in the y direction.</span></span> <span data-ttu-id="eb6f4-469">El valor predeterminado es 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-469">Default value is 0.0f.</span></span> <span data-ttu-id="eb6f4-470">Vea [ \_ teselación adaptable](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-470">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-471"><span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS \_ ADAPTIVETESS \_ Z**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-471"><span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS\_ADAPTIVETESS\_Z**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-472">Importe para dividirlas adaptable, en la dirección z.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-472">Amount to adaptively tessellate, in the z direction.</span></span> <span data-ttu-id="eb6f4-473">El valor predeterminado es 1.0 f.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-473">Default value is 1.0f.</span></span> <span data-ttu-id="eb6f4-474">Vea [ \_ teselación adaptable](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-474">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-475"><span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS \_ ADAPTIVETESS \_ W**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-475"><span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS\_ADAPTIVETESS\_W**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-476">Cantidad para dividirlas adaptable, en la dirección w.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-476">Amount to adaptively tessellate, in the w direction.</span></span> <span data-ttu-id="eb6f4-477">El valor predeterminado es 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-477">Default value is 0.0f.</span></span> <span data-ttu-id="eb6f4-478">Vea [ \_ teselación adaptable](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-478">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-479"><span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS \_ ENABLEADAPTIVETESSELLATION**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-479"><span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS\_ENABLEADAPTIVETESSELLATION**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-480">**True** para habilitar la teselación adaptable y **false** para deshabilitarla.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-480">**TRUE** to enable adaptive tessellation, **FALSE** to disable it.</span></span> <span data-ttu-id="eb6f4-481">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-481">The default value is **FALSE**.</span></span> <span data-ttu-id="eb6f4-482">Vea [ \_ teselación adaptable](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-482">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-483"><span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS \_ TWOSIDEDSTENCILMODE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-483"><span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS\_TWOSIDEDSTENCILMODE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-484">**True** habilita el estarcido de dos caras, **false** lo deshabilita.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-484">**TRUE** enables two-sided stenciling, **FALSE** disables it.</span></span> <span data-ttu-id="eb6f4-485">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-485">The default value is **FALSE**.</span></span> <span data-ttu-id="eb6f4-486">La aplicación debe establecer D3DRS \_ CULLMODE en D3DCULL \_ None para habilitar el modo de galería de símbolos de dos caras.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-486">The application should set D3DRS\_CULLMODE to D3DCULL\_NONE to enable two-sided stencil mode.</span></span> <span data-ttu-id="eb6f4-487">Si el orden de la espiral del triángulo es el de las agujas del reloj, se \_ usarán las operaciones de la galería de símbolos D3DRS \* .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-487">If the triangle winding order is clockwise, the D3DRS\_STENCIL\* operations will be used.</span></span> <span data-ttu-id="eb6f4-488">Si el orden de bobinado es en sentido contrario a las agujas del reloj, se \_ usarán las operaciones de estarcido de D3DRS CCW \_ \* .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-488">If the winding order is counterclockwise, the D3DRS\_CCW\_STENCIL\* operations will be used.</span></span>

<span data-ttu-id="eb6f4-489">Para ver si se admite la galería de símbolos de dos caras, compruebe el miembro StencilCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para D3DSTENCILCAPS \_ TWOSIDED.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-489">To see if two-sided stencil is supported, check the StencilCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) for D3DSTENCILCAPS\_TWOSIDED.</span></span> <span data-ttu-id="eb6f4-490">Vea también [D3DSTENCILCAPS](d3dstencilcaps.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-490">See also [D3DSTENCILCAPS](d3dstencilcaps.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-491"><span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS \_ CCW \_ STENCILFAIL**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-491"><span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS\_CCW\_STENCILFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-492">Operación de estarcido que se debe realizar si se produce un error en la prueba de estarcido CCW.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-492">Stencil operation to perform if CCW stencil test fails.</span></span> <span data-ttu-id="eb6f4-493">Los valores son del tipo enumerado [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-493">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-494">El valor predeterminado es D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-494">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-495"><span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS \_ CCW \_ STENCILZFAIL**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-495"><span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS\_CCW\_STENCILZFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-496">Operación de estarcido que se va a realizar si se supera la prueba de estarcido CCW y la prueba z.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-496">Stencil operation to perform if CCW stencil test passes and z-test fails.</span></span> <span data-ttu-id="eb6f4-497">Los valores son del tipo enumerado [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-497">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-498">El valor predeterminado es D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-498">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-499"><span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS \_ CCW \_ STENCILPASS**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-499"><span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS\_CCW\_STENCILPASS**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-500">Operación de estarcido que se realizará si se superan las pruebas de la galería de símbolos CCW y z.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-500">Stencil operation to perform if both CCW stencil and z-tests pass.</span></span> <span data-ttu-id="eb6f4-501">Los valores son del tipo enumerado [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-501">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-502">El valor predeterminado es D3DSTENCILOP \_ Keep.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-502">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-503"><span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS \_ CCW \_ STENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-503"><span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS\_CCW\_STENCILFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-504">Función de comparación.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-504">The comparison function.</span></span> <span data-ttu-id="eb6f4-505">La prueba de estarcido CCW se supera si la función de estarcido (((Ref & Mask) (Galería de símbolos & máscara)) es **true**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-505">CCW stencil test passes if ((ref & mask) stencil function (stencil & mask)) is **TRUE**.</span></span> <span data-ttu-id="eb6f4-506">Los valores son del tipo enumerado [**D3DCMPFUNC**](./d3dcmpfunc.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-506">Values are from the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-507">El valor predeterminado es D3DCMP \_ siempre.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-507">The default value is D3DCMP\_ALWAYS.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-508"><span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS \_ COLORWRITEENABLE1**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-508"><span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS\_COLORWRITEENABLE1**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-509">Valores de ColorWriteEnable adicionales para los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-509">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="eb6f4-510">Vea D3DRS \_ COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-510">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="eb6f4-511">Esta funcionalidad está disponible si el bit de funcionalidad de D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS se establece en el miembro PrimitiveMiscCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-511">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="eb6f4-512">El valor predeterminado es 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-512">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-513"><span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS \_ COLORWRITEENABLE2**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-513"><span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS\_COLORWRITEENABLE2**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-514">Valores de ColorWriteEnable adicionales para los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-514">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="eb6f4-515">Vea D3DRS \_ COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-515">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="eb6f4-516">Esta funcionalidad está disponible si el bit de funcionalidad de D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS se establece en el miembro PrimitiveMiscCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-516">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="eb6f4-517">El valor predeterminado es 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-517">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-518"><span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS \_ COLORWRITEENABLE3**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-518"><span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS\_COLORWRITEENABLE3**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-519">Valores de ColorWriteEnable adicionales para los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-519">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="eb6f4-520">Vea D3DRS \_ COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-520">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="eb6f4-521">Esta funcionalidad está disponible si el bit de funcionalidad de D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS se establece en el miembro PrimitiveMiscCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-521">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="eb6f4-522">El valor predeterminado es 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-522">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-523"><span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS \_ BLENDFACTOR**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-523"><span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS\_BLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-524">[**D3DCOLOR**](d3dcolor.md) usado para un factor de mezcla constante durante la combinación alfa.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-524">[**D3DCOLOR**](d3dcolor.md) used for a constant blend-factor during alpha blending.</span></span> <span data-ttu-id="eb6f4-525">Esta funcionalidad está disponible si el bit de funcionalidad de D3DPBLENDCAPS \_ BLENDFACTOR se establece en el miembro SrcBlendCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) o en el miembro DestBlendCaps de **D3DCAPS9**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-525">This functionality is available if the D3DPBLENDCAPS\_BLENDFACTOR capabilities bit is set in the SrcBlendCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) or the DestBlendCaps member of **D3DCAPS9**.</span></span> <span data-ttu-id="eb6f4-526">Vea [**D3DRENDERSTATETYPE**]().</span><span class="sxs-lookup"><span data-stu-id="eb6f4-526">See [**D3DRENDERSTATETYPE**]().</span></span> <span data-ttu-id="eb6f4-527">El valor predeterminado es 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-527">The default value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-528"><span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS \_ SRGBWRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-528"><span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS\_SRGBWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-529">Habilite la escritura de representación-destino para que sea gamma corregida a sRGB.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-529">Enable render-target writes to be gamma corrected to sRGB.</span></span> <span data-ttu-id="eb6f4-530">El formato debe exponer D3DUSAGE \_ SRGBWRITE.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-530">The format must expose D3DUSAGE\_SRGBWRITE.</span></span> <span data-ttu-id="eb6f4-531">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-531">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-532"><span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS \_ DEPTHBIAS**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-532"><span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS\_DEPTHBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-533">Un valor de punto flotante que se usa para la comparación de valores de profundidad.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-533">A floating-point value that is used for comparison of depth values.</span></span> <span data-ttu-id="eb6f4-534">Vea [sesgo de profundidad (Direct3D 9)](depth-bias.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-534">See [Depth Bias (Direct3D 9)](depth-bias.md).</span></span> <span data-ttu-id="eb6f4-535">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-535">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-536"><span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS \_ WRAP8**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-536"><span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS\_WRAP8**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-537">Vea D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-537">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-538"><span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS \_ WRAP9**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-538"><span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS\_WRAP9**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-539">Vea D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-539">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-540"><span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS \_ WRAP10**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-540"><span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS\_WRAP10**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-541">Vea D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-541">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-542"><span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS \_ WRAP11**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-542"><span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS\_WRAP11**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-543">Vea D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-543">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-544"><span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS \_ WRAP12**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-544"><span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS\_WRAP12**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-545">Vea D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-545">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-546"><span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS \_ WRAP13**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-546"><span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS\_WRAP13**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-547">Vea D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-547">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-548"><span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS \_ WRAP14**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-548"><span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS\_WRAP14**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-549">Vea D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-549">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-550"><span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS \_ WRAP15**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-550"><span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS\_WRAP15**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-551">Vea D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-551">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-552"><span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS \_ SEPARATEALPHABLENDENABLE**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-552"><span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS\_SEPARATEALPHABLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-553">**True** habilita el modo de mezcla independiente para el canal alfa.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-553">**TRUE** enables the separate blend mode for the alpha channel.</span></span> <span data-ttu-id="eb6f4-554">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-554">The default value is **FALSE**.</span></span>

<span data-ttu-id="eb6f4-555">Cuando se establece en **false**, los factores de mezcla y las operaciones de destino de representación que se aplican a alfa se fuerzan a ser iguales que los definidos para el color.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-555">When set to **FALSE**, the render-target blending factors and operations applied to alpha are forced to be the same as those defined for color.</span></span> <span data-ttu-id="eb6f4-556">Este modo está realmente cableado a **false** en las implementaciones que no establecen el Cap D3DPMISCCAPS \_ SEPARATEALPHABLEND.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-556">This mode is effectively hardwired to **FALSE** on implementations that don't set the cap D3DPMISCCAPS\_SEPARATEALPHABLEND.</span></span> <span data-ttu-id="eb6f4-557">Vea [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-557">See [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

<span data-ttu-id="eb6f4-558">El tipo de combinación alfa independiente viene determinado por los Estados de \_ representación D3DRS SRCBLENDALPHA y D3DRS \_ DESTBLENDALPHA.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-558">The type of separate alpha blending is determined by the D3DRS\_SRCBLENDALPHA and D3DRS\_DESTBLENDALPHA render states.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-559"><span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS \_ SRCBLENDALPHA**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-559"><span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS\_SRCBLENDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-560">Un miembro del tipo enumerado [**D3DBLEND**](./d3dblend.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-560">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-561">Este valor se omite a menos que D3DRS \_ SEPARATEALPHABLENDENABLE sea **true**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-561">This value is ignored unless D3DRS\_SEPARATEALPHABLENDENABLE is **TRUE**.</span></span> <span data-ttu-id="eb6f4-562">El valor predeterminado es D3DBLEND \_ uno.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-562">The default value is D3DBLEND\_ONE.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-563"><span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS \_ DESTBLENDALPHA**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-563"><span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS\_DESTBLENDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-564">Un miembro del tipo enumerado [**D3DBLEND**](./d3dblend.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-564">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-565">Este valor se omite a menos que D3DRS \_ SEPARATEALPHABLENDENABLE sea **true**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-565">This value is ignored unless D3DRS\_SEPARATEALPHABLENDENABLE is **TRUE**.</span></span> <span data-ttu-id="eb6f4-566">El valor predeterminado es D3DBLEND \_ cero.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-566">The default value is D3DBLEND\_ZERO.</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-567"><span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS \_ BLENDOPALPHA**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-567"><span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS\_BLENDOPALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-568">Valor que se usa para seleccionar la operación aritmética que se aplica a la combinación alfa independiente cuando el estado de representación, D3DRS \_ SEPARATEALPHABLENDENABLE, se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-568">Value used to select the arithmetic operation applied to separate alpha blending when the render state, D3DRS\_SEPARATEALPHABLENDENABLE, is set to **TRUE**.</span></span>

<span data-ttu-id="eb6f4-569">Los valores válidos se definen mediante el tipo enumerado [**D3DBLENDOP**](./d3dblendop.md) .</span><span class="sxs-lookup"><span data-stu-id="eb6f4-569">Valid values are defined by the [**D3DBLENDOP**](./d3dblendop.md) enumerated type.</span></span> <span data-ttu-id="eb6f4-570">El valor predeterminado es D3DBLENDOP \_ Add.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-570">The default value is D3DBLENDOP\_ADD.</span></span>

<span data-ttu-id="eb6f4-571">Si \_ no se admite la funcionalidad del dispositivo D3DPMISCCAPS BLENDOP, \_ se realiza D3DBLENDOP agregar.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-571">If the D3DPMISCCAPS\_BLENDOP device capability is not supported, then D3DBLENDOP\_ADD is performed.</span></span> <span data-ttu-id="eb6f4-572">Vea [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-572">See [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6f4-573"><span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-573"><span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="eb6f4-574">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-574">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="eb6f4-575">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-575">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="eb6f4-576">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-576">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb6f4-577">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb6f4-577">Remarks</span></span>



| <span data-ttu-id="eb6f4-578">Estados de representación</span><span class="sxs-lookup"><span data-stu-id="eb6f4-578">Render States</span></span>        |                    |
|----------------------|--------------------|
| <span data-ttu-id="eb6f4-579">PS \_ 1 \_ 1 a PS \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="eb6f4-579">ps\_1\_1 to ps\_1\_3</span></span> | <span data-ttu-id="eb6f4-580">4 muestras de texturas</span><span class="sxs-lookup"><span data-stu-id="eb6f4-580">4 texture samplers</span></span> |



 

<span data-ttu-id="eb6f4-581">Direct3D define la \_ constante D3DRENDERSTATE WRAPBIAS para que las aplicaciones puedan habilitar o deshabilitar el ajuste de textura, en función del entero de base cero de un conjunto de coordenadas de textura (en lugar de usar explícitamente uno de los valores de estado de ajuste de D3DRS \_ n).</span><span class="sxs-lookup"><span data-stu-id="eb6f4-581">Direct3D defines the D3DRENDERSTATE\_WRAPBIAS constant as a convenience for applications to enable or disable texture wrapping, based on the zero-based integer of a texture coordinate set (rather than explicitly using one of the D3DRS\_WRAP n state values).</span></span> <span data-ttu-id="eb6f4-582">Agregue el \_ valor de WRAPBIAS D3DRENDERSTATE al índice de base cero de un conjunto de coordenadas de textura para calcular el valor del ajuste de D3DRS \_ n que corresponde a ese índice, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="eb6f4-582">Add the D3DRENDERSTATE\_WRAPBIAS value to the zero-based index of a texture coordinate set to calculate the D3DRS\_WRAP n value that corresponds to that index, as shown in the following example.</span></span>


```
// Enable U/V wrapping for textures that use the texture 
// coordinate set at the index within the dwIndex variable
    
HRESULT hr = pd3dDevice->SetRenderState(
dwIndex + D3DRENDERSTATE_WRAPBIAS,  
D3DWRAPCOORD_0 | D3DWRAPCOORD_1);
     
// If dwIndex is 3, the value that results from 
// the addition equals D3DRS_WRAP3 (131)
```



## <a name="requirements"></a><span data-ttu-id="eb6f4-583">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb6f4-583">Requirements</span></span>



| <span data-ttu-id="eb6f4-584">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb6f4-584">Requirement</span></span> | <span data-ttu-id="eb6f4-585">Value</span><span class="sxs-lookup"><span data-stu-id="eb6f4-585">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb6f4-586">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb6f4-586">Header</span></span><br/> | <dl> <span data-ttu-id="eb6f4-587"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb6f4-587"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb6f4-588">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb6f4-588">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb6f4-589">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="eb6f4-589">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="eb6f4-590">**IDirect3DDevice9::GetRenderState**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-590">**IDirect3DDevice9::GetRenderState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrenderstate)
</dt> <dt>

[<span data-ttu-id="eb6f4-591">**IDirect3DDevice9::SetRenderState**</span><span class="sxs-lookup"><span data-stu-id="eb6f4-591">**IDirect3DDevice9::SetRenderState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)
</dt> </dl>

 

 
