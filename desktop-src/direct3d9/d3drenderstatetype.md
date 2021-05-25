---
description: Los estados de representación definen los estados de configuración para todos los tipos de procesamiento de vértices y píxeles.
ms.assetid: 2fd56388-f3bd-409f-876c-ae893840b623
title: Enumeración D3DRENDERSTATETYPE (D3D9Types.h)
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
ms.openlocfilehash: 0a7ad803535032705e6e1bb5456109486c59d190
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343070"
---
# <a name="d3drenderstatetype-enumeration"></a><span data-ttu-id="445e8-103">D3DRENDERSTATETYPE (enumeración)</span><span class="sxs-lookup"><span data-stu-id="445e8-103">D3DRENDERSTATETYPE enumeration</span></span>

<span data-ttu-id="445e8-104">Los estados de representación definen los estados de configuración para todos los tipos de procesamiento de vértices y píxeles.</span><span class="sxs-lookup"><span data-stu-id="445e8-104">Render states define set-up states for all kinds of vertex and pixel processing.</span></span> <span data-ttu-id="445e8-105">Algunos estados de representación configurarán el procesamiento de vértices y otros configurarán el procesamiento de píxeles (vea Estados de representación [(Direct3D 9).](render-states.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-105">Some render states set up vertex processing, and some set up pixel processing (see [Render States (Direct3D 9)](render-states.md)).</span></span> <span data-ttu-id="445e8-106">Los estados de representación se pueden guardar y restaurar mediante bloques de estado (vea State Blocks Save and Restore State (Direct3D 9) [Estado de guardado y restauración de bloques de estado [(Direct3D 9)]).](state-blocks-save-and-restore-state.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-106">Render states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="445e8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="445e8-107">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="445e8-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="445e8-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="445e8-109"><span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS \_ ZENABLE**</span><span class="sxs-lookup"><span data-stu-id="445e8-109"><span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS\_ZENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-110">Estado de almacenamiento en búfer de profundidad como un miembro del tipo enumerado [**D3BUFFERBUFFERTYPE.**](./d3dzbuffertype.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-110">Depth-buffering state as one member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumerated type.</span></span> <span data-ttu-id="445e8-111">Establezca este estado en D3D WLAN TRUE para habilitar el almacenamiento en búfer \_ z, D3D BUFFERING USEW para habilitar \_ w-buffering o D3D WLAN FALSE para deshabilitar el almacenamiento en búfer de \_ profundidad.</span><span class="sxs-lookup"><span data-stu-id="445e8-111">Set this state to D3DZB\_TRUE to enable z-buffering, D3DZB\_USEW to enable w-buffering, or D3DZB\_FALSE to disable depth buffering.</span></span>

<span data-ttu-id="445e8-112">El valor predeterminado de este estado de representación es D3DMUT TRUE si se creó una galería de símbolos de profundidad junto con la cadena de intercambio estableciendo el miembro \_ EnableAutoDepthStencil de la estructura [**PARAMETERS \_ D3DPRESENT**](d3dpresent-parameters.md) en **TRUE** y D3DOXI FALSE en caso \_ contrario.</span><span class="sxs-lookup"><span data-stu-id="445e8-112">The default value for this render state is D3DZB\_TRUE if a depth stencil was created along with the swap chain by setting the EnableAutoDepthStencil member of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure to **TRUE**, and D3DZB\_FALSE otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-113"><span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS \_ FILLMODE**</span><span class="sxs-lookup"><span data-stu-id="445e8-113"><span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS\_FILLMODE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-114">Uno o varios miembros del [**tipo enumerado D3DFILLMODE.**](./d3dfillmode.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-114">One or more members of the [**D3DFILLMODE**](./d3dfillmode.md) enumerated type.</span></span> <span data-ttu-id="445e8-115">El valor predeterminado es D3DFILL \_ SOLID.</span><span class="sxs-lookup"><span data-stu-id="445e8-115">The default value is D3DFILL\_SOLID.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-116"><span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS \_ SHADEMODE**</span><span class="sxs-lookup"><span data-stu-id="445e8-116"><span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS\_SHADEMODE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-117">Uno o varios miembros del [**tipo enumerado D3DSHADEMODE.**](./d3dshademode.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-117">One or more members of the [**D3DSHADEMODE**](./d3dshademode.md) enumerated type.</span></span> <span data-ttu-id="445e8-118">El valor predeterminado es D3DSHADE \_ GOURAUD.</span><span class="sxs-lookup"><span data-stu-id="445e8-118">The default value is D3DSHADE\_GOURAUD.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-119"><span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS \_ ZWRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="445e8-119"><span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS\_ZWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-120">**TRUE** para permitir que la aplicación escriba en el búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="445e8-120">**TRUE** to enable the application to write to the depth buffer.</span></span> <span data-ttu-id="445e8-121">El valor predeterminado es **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="445e8-121">The default value is **TRUE**.</span></span> <span data-ttu-id="445e8-122">Este miembro permite que una aplicación impida que el sistema actualice el búfer de profundidad con nuevos valores de profundidad.</span><span class="sxs-lookup"><span data-stu-id="445e8-122">This member enables an application to prevent the system from updating the depth buffer with new depth values.</span></span> <span data-ttu-id="445e8-123">Si **es FALSE,** las comparaciones de profundidad se siguen haciendo según el estado de representación D3DRS RAGUNC, suponiendo que se está llevando a cabo el almacenamiento en búfer de profundidad, pero los valores de profundidad no se escriben en el \_ búfer.</span><span class="sxs-lookup"><span data-stu-id="445e8-123">If **FALSE**, depth comparisons are still made according to the render state D3DRS\_ZFUNC, assuming that depth buffering is taking place, but depth values are not written to the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-124"><span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS \_ ALPHATESTENABLE**</span><span class="sxs-lookup"><span data-stu-id="445e8-124"><span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS\_ALPHATESTENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-125">**TRUE** para habilitar las pruebas alfa por píxel.</span><span class="sxs-lookup"><span data-stu-id="445e8-125">**TRUE** to enable per pixel alpha testing.</span></span> <span data-ttu-id="445e8-126">Si la prueba se supera, el búfer de fotogramas procesa el píxel.</span><span class="sxs-lookup"><span data-stu-id="445e8-126">If the test passes, the pixel is processed by the frame buffer.</span></span> <span data-ttu-id="445e8-127">De lo contrario, se omite todo el procesamiento del búfer de fotogramas para el píxel.</span><span class="sxs-lookup"><span data-stu-id="445e8-127">Otherwise, all frame-buffer processing is skipped for the pixel.</span></span>

<span data-ttu-id="445e8-128">La prueba se realiza comparando el valor alfa entrante con el valor alfa de referencia, mediante la función de comparación proporcionada por el estado de representación de D3DRS \_ ALPHAFUNC.</span><span class="sxs-lookup"><span data-stu-id="445e8-128">The test is done by comparing the incoming alpha value with the reference alpha value, using the comparison function provided by the D3DRS\_ALPHAFUNC render state.</span></span> <span data-ttu-id="445e8-129">El valor alfa de referencia viene determinado por el valor establecido para D3DRS \_ ALPHAREF.</span><span class="sxs-lookup"><span data-stu-id="445e8-129">The reference alpha value is determined by the value set for D3DRS\_ALPHAREF.</span></span> <span data-ttu-id="445e8-130">Para obtener más información, vea [Alpha Testing State (Direct3D 9).](alpha-testing-state.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-130">For more information, see [Alpha Testing State (Direct3D 9)](alpha-testing-state.md).</span></span>

<span data-ttu-id="445e8-131">El valor predeterminado de este parámetro es **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="445e8-131">The default value of this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-132"><span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS \_ LASTPIXEL**</span><span class="sxs-lookup"><span data-stu-id="445e8-132"><span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS\_LASTPIXEL**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-133">El valor predeterminado es **TRUE,** que permite dibujar el último píxel de una línea.</span><span class="sxs-lookup"><span data-stu-id="445e8-133">The default value is **TRUE**, which enables drawing of the last pixel in a line.</span></span> <span data-ttu-id="445e8-134">Para evitar el dibujo del último píxel, establezca este valor en **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="445e8-134">To prevent drawing of the last pixel, set this value to **FALSE**.</span></span> <span data-ttu-id="445e8-135">Para obtener más información, vea [Esquema y estado de relleno (Direct3D 9).](outline-and-fill-state.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-135">For more information, see [Outline and Fill State (Direct3D 9)](outline-and-fill-state.md).</span></span>

</dd> <dt>

<span data-ttu-id="445e8-136"><span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS \_ SRCBLEND**</span><span class="sxs-lookup"><span data-stu-id="445e8-136"><span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS\_SRCBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-137">Un miembro del [**tipo enumerado D3DBLEND.**](./d3dblend.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-137">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="445e8-138">El valor predeterminado es D3DBLEND \_ ONE.</span><span class="sxs-lookup"><span data-stu-id="445e8-138">The default value is D3DBLEND\_ONE.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-139"><span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS \_ DESTBLEND**</span><span class="sxs-lookup"><span data-stu-id="445e8-139"><span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS\_DESTBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-140">Un miembro del [**tipo enumerado D3DBLEND.**](./d3dblend.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-140">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="445e8-141">El valor predeterminado es D3DBLEND \_ ZERO.</span><span class="sxs-lookup"><span data-stu-id="445e8-141">The default value is D3DBLEND\_ZERO.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-142"><span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS \_ CULLMODE**</span><span class="sxs-lookup"><span data-stu-id="445e8-142"><span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS\_CULLMODE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-143">Especifica cómo se encuentran los triángulos orientados hacia atrás, en caso de que sea así.</span><span class="sxs-lookup"><span data-stu-id="445e8-143">Specifies how back-facing triangles are culled, if at all.</span></span> <span data-ttu-id="445e8-144">Se puede establecer en un miembro del [**tipo enumerado D3DCULL.**](./d3dcull.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-144">This can be set to one member of the [**D3DCULL**](./d3dcull.md) enumerated type.</span></span> <span data-ttu-id="445e8-145">El valor predeterminado es D3DCULL \_ CCW.</span><span class="sxs-lookup"><span data-stu-id="445e8-145">The default value is D3DCULL\_CCW.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-146"><span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRSUNC \_**</span><span class="sxs-lookup"><span data-stu-id="445e8-146"><span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS\_ZFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-147">Un miembro del [**tipo enumerado D3DCMPFUNC.**](./d3dcmpfunc.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-147">One member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="445e8-148">El valor predeterminado es D3DCMP \_ LESSEQUAL.</span><span class="sxs-lookup"><span data-stu-id="445e8-148">The default value is D3DCMP\_LESSEQUAL.</span></span> <span data-ttu-id="445e8-149">Este miembro permite que una aplicación acepte o rechace un píxel, en función de su distancia desde la cámara.</span><span class="sxs-lookup"><span data-stu-id="445e8-149">This member enables an application to accept or reject a pixel, based on its distance from the camera.</span></span>

<span data-ttu-id="445e8-150">El valor de profundidad del píxel se compara con el valor de búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="445e8-150">The depth value of the pixel is compared with the depth-buffer value.</span></span> <span data-ttu-id="445e8-151">Si el valor de profundidad del píxel pasa la función de comparación, se escribe el píxel.</span><span class="sxs-lookup"><span data-stu-id="445e8-151">If the depth value of the pixel passes the comparison function, the pixel is written.</span></span>

<span data-ttu-id="445e8-152">El valor de profundidad se escribe en el búfer de profundidad solo si el estado de representación es **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="445e8-152">The depth value is written to the depth buffer only if the render state is **TRUE**.</span></span>

<span data-ttu-id="445e8-153">Los rasterizadores de software y muchos aceleradores de hardware funcionan más rápido si se produce un error en la prueba de profundidad, ya que no es necesario filtrar y modular la textura si el píxel no se va a representar.</span><span class="sxs-lookup"><span data-stu-id="445e8-153">Software rasterizers and many hardware accelerators work faster if the depth test fails, because there is no need to filter and modulate the texture if the pixel is not going to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-154"><span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS \_ ALPHAREF**</span><span class="sxs-lookup"><span data-stu-id="445e8-154"><span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS\_ALPHAREF**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-155">Valor que especifica un valor alfa de referencia con el que se prueban los píxeles cuando se habilitan las pruebas alfa.</span><span class="sxs-lookup"><span data-stu-id="445e8-155">Value that specifies a reference alpha value against which pixels are tested when alpha testing is enabled.</span></span> <span data-ttu-id="445e8-156">Se trata de un valor de 8 bits colocado en los 8 bits inferiores del valor de estado de representación DWORD.</span><span class="sxs-lookup"><span data-stu-id="445e8-156">This is an 8-bit value placed in the low 8 bits of the DWORD render-state value.</span></span> <span data-ttu-id="445e8-157">Los valores pueden oscilar entre 0x00000000 a 0x000000FF.</span><span class="sxs-lookup"><span data-stu-id="445e8-157">Values can range from 0x00000000 through 0x000000FF.</span></span> <span data-ttu-id="445e8-158">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="445e8-158">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-159"><span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS \_ ALPHAFUNC**</span><span class="sxs-lookup"><span data-stu-id="445e8-159"><span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS\_ALPHAFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-160">Un miembro del [**tipo enumerado D3DCMPFUNC.**](./d3dcmpfunc.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-160">One member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="445e8-161">El valor predeterminado es D3DCMP \_ ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="445e8-161">The default value is D3DCMP\_ALWAYS.</span></span> <span data-ttu-id="445e8-162">Este miembro permite que una aplicación acepte o rechace un píxel, en función de su valor alfa.</span><span class="sxs-lookup"><span data-stu-id="445e8-162">This member enables an application to accept or reject a pixel, based on its alpha value.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-163"><span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS \_ DITHERENABLE**</span><span class="sxs-lookup"><span data-stu-id="445e8-163"><span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS\_DITHERENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-164">**TRUE** para habilitar la dithering.</span><span class="sxs-lookup"><span data-stu-id="445e8-164">**TRUE** to enable dithering.</span></span> <span data-ttu-id="445e8-165">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="445e8-165">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-166"><span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS \_ ALPHABLENDENABLE**</span><span class="sxs-lookup"><span data-stu-id="445e8-166"><span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS\_ALPHABLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-167">**TRUE** para habilitar la transparencia alfa blended.</span><span class="sxs-lookup"><span data-stu-id="445e8-167">**TRUE** to enable alpha-blended transparency.</span></span> <span data-ttu-id="445e8-168">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="445e8-168">The default value is **FALSE**.</span></span>

<span data-ttu-id="445e8-169">El tipo de combinación alfa viene determinado por los estados de representación D3DRS \_ SRCBLEND y D3DRS \_ DESTBLEND.</span><span class="sxs-lookup"><span data-stu-id="445e8-169">The type of alpha blending is determined by the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-170"><span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS \_ LEGIBLE**</span><span class="sxs-lookup"><span data-stu-id="445e8-170"><span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS\_FOGENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-171">**TRUE para** habilitar la mezcla de mezcla.</span><span class="sxs-lookup"><span data-stu-id="445e8-171">**TRUE** to enable fog blending.</span></span> <span data-ttu-id="445e8-172">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="445e8-172">The default value is **FALSE**.</span></span> <span data-ttu-id="445e8-173">Para obtener más información sobre el uso de la mezcla de mezcla, vea [Blend](fog.md).</span><span class="sxs-lookup"><span data-stu-id="445e8-173">For more information about using fog blending, see [Fog](fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="445e8-174"><span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS \_ SPECULARENABLE**</span><span class="sxs-lookup"><span data-stu-id="445e8-174"><span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS\_SPECULARENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-175">**TRUE** para habilitar los resaltados especulares.</span><span class="sxs-lookup"><span data-stu-id="445e8-175">**TRUE** to enable specular highlights.</span></span> <span data-ttu-id="445e8-176">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="445e8-176">The default value is **FALSE**.</span></span>

<span data-ttu-id="445e8-177">Los resaltados especulares se calculan como si cada vértice del objeto que se va a encender se encuentra en el origen del objeto.</span><span class="sxs-lookup"><span data-stu-id="445e8-177">Specular highlights are calculated as though every vertex in the object being lit is at the object's origin.</span></span> <span data-ttu-id="445e8-178">Esto proporciona los resultados esperados siempre que el objeto se modele en torno al origen y la distancia entre la luz y el objeto sea relativamente grande.</span><span class="sxs-lookup"><span data-stu-id="445e8-178">This gives the expected results as long as the object is modeled around the origin and the distance from the light to the object is relatively large.</span></span> <span data-ttu-id="445e8-179">En otros casos, los resultados son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="445e8-179">In other cases, the results as undefined.</span></span>

<span data-ttu-id="445e8-180">Cuando este miembro se establece en **TRUE,** el color especular se agrega al color base después de la cascada de textura, pero antes de la combinación alfa.</span><span class="sxs-lookup"><span data-stu-id="445e8-180">When this member is set to **TRUE**, the specular color is added to the base color after the texture cascade but before alpha blending.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-181"><span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRSCOLOR \_**</span><span class="sxs-lookup"><span data-stu-id="445e8-181"><span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRS\_FOGCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-182">Valor cuyo tipo es [**D3DCOLOR.**](d3dcolor.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-182">Value whose type is [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="445e8-183">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="445e8-183">The default value is 0.</span></span> <span data-ttu-id="445e8-184">Para obtener más información sobre el color de color blanco, vea [Color de color blanco (Direct3D 9).](fog-color.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-184">For more information about fog color, see [Fog Color (Direct3D 9)](fog-color.md).</span></span>

</dd> <dt>

<span data-ttu-id="445e8-185"><span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS \_ CONFIGURABLEMODE**</span><span class="sxs-lookup"><span data-stu-id="445e8-185"><span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS\_FOGTABLEMODE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-186">Fórmula de ánxeles que se va a usar para píxeles.</span><span class="sxs-lookup"><span data-stu-id="445e8-186">The fog formula to be used for pixel fog.</span></span> <span data-ttu-id="445e8-187">Establezca en uno de los miembros del tipo [**enumerado D3DFOGMODE.**](./d3dfogmode.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-187">Set to one of the members of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="445e8-188">El valor predeterminado es D3DFOG \_ NONE.</span><span class="sxs-lookup"><span data-stu-id="445e8-188">The default value is D3DFOG\_NONE.</span></span> <span data-ttu-id="445e8-189">Para obtener más información sobre píxeles de píxeles, vea [Pixel Pixel (Direct3D 9)](pixel-fog.md).</span><span class="sxs-lookup"><span data-stu-id="445e8-189">For more information about pixel fog, see [Pixel Fog (Direct3D 9)](pixel-fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="445e8-190"><span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRSSTART \_**</span><span class="sxs-lookup"><span data-stu-id="445e8-190"><span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS\_FOGSTART**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-191">Profundidad a la que comienzan los efectos de vértice o píxel para el modo de ángulo lineal.</span><span class="sxs-lookup"><span data-stu-id="445e8-191">Depth at which pixel or vertex fog effects begin for linear fog mode.</span></span> <span data-ttu-id="445e8-192">El valor predeterminado es 0,0f.</span><span class="sxs-lookup"><span data-stu-id="445e8-192">The default value is 0.0f.</span></span> <span data-ttu-id="445e8-193">La profundidad se especifica en el espacio mundial para el vértice de vértice y el espacio del dispositivo \[ 0,0, 1,0 o el espacio del mundo para el \] píxel de píxel.</span><span class="sxs-lookup"><span data-stu-id="445e8-193">Depth is specified in world space for vertex fog and either device space \[0.0, 1.0\] or world space for pixel fog.</span></span> <span data-ttu-id="445e8-194">En el caso de píxeles de píxeles, estos valores están en el espacio del dispositivo cuando el sistema usa z para los cálculos de cálculos de cálculo y el espacio del mundo mundial cuando el sistema usa la sombra relativa a los ojos (w-wu).</span><span class="sxs-lookup"><span data-stu-id="445e8-194">For pixel fog, these values are in device space when the system uses z for fog calculations and world-world space when the system is using eye-relative fog (w-fog).</span></span> <span data-ttu-id="445e8-195">Para obtener más información, vea Parámetros de parámetros de vuelo [(Direct3D 9)](fog-parameters.md) y Relación con los ojos frente a profundidad [basada en Z.](pixel-fog.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-195">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md) and [Eye-Relative vs. Z-based Depth](pixel-fog.md).</span></span>

<span data-ttu-id="445e8-196">Los valores para este estado de representación son valores de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="445e8-196">Values for this render state are floating-point values.</span></span> <span data-ttu-id="445e8-197">Dado que [**el método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="445e8-197">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
pDevice9->SetRenderState(D3DRS_FOGSTART, 
                         *((DWORD*) (&fFogStart)));
```



</dd> <dt>

<span data-ttu-id="445e8-198"><span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRSEND \_**</span><span class="sxs-lookup"><span data-stu-id="445e8-198"><span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS\_FOGEND**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-199">Profundidad a la que finalizan los efectos de vértices o píxeles para el modo de fusión lineal.</span><span class="sxs-lookup"><span data-stu-id="445e8-199">Depth at which pixel or vertex fog effects end for linear fog mode.</span></span> <span data-ttu-id="445e8-200">El valor predeterminado es 1,0f.</span><span class="sxs-lookup"><span data-stu-id="445e8-200">The default value is 1.0f.</span></span> <span data-ttu-id="445e8-201">La profundidad se especifica en el espacio mundial para el vértice de vértice y el espacio del dispositivo \[ 0,0, 1,0 o el espacio del mundo para el \] píxel de píxel.</span><span class="sxs-lookup"><span data-stu-id="445e8-201">Depth is specified in world space for vertex fog and either device space \[0.0, 1.0\] or world space for pixel fog.</span></span> <span data-ttu-id="445e8-202">En el caso de píxeles de píxeles, estos valores están en el espacio del dispositivo cuando el sistema usa z para los cálculos de cálculos de cálculo y en el espacio mundial cuando el sistema usa el ojo relativo a los ojos (w-wu).</span><span class="sxs-lookup"><span data-stu-id="445e8-202">For pixel fog, these values are in device space when the system uses z for fog calculations and in world space when the system is using eye-relative fog (w-fog).</span></span> <span data-ttu-id="445e8-203">Para obtener más información, vea Parámetros de parámetros de vuelo [(Direct3D 9)](fog-parameters.md) y Relación con los ojos frente a profundidad [basada en Z.](pixel-fog.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-203">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md) and [Eye-Relative vs. Z-based Depth](pixel-fog.md).</span></span>

<span data-ttu-id="445e8-204">Los valores para este estado de representación son valores de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="445e8-204">Values for this render state are floating-point values.</span></span> <span data-ttu-id="445e8-205">Dado que [**el método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="445e8-205">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_FOGEND, *((DWORD*) (&fFogEnd)));
```



</dd> <dt>

<span data-ttu-id="445e8-206"><span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**\_D3DRSRDDENSITY**</span><span class="sxs-lookup"><span data-stu-id="445e8-206"><span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**D3DRS\_FOGDENSITY**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-207">Densidad de densidad de densidad para píxeles o vértices usados en los modos de aceleración exponencial (D3DFOG \_ EXP y D3DFOG \_ EXP2).</span><span class="sxs-lookup"><span data-stu-id="445e8-207">Fog density for pixel or vertex fog used in the exponential fog modes (D3DFOG\_EXP and D3DFOG\_EXP2).</span></span> <span data-ttu-id="445e8-208">Los valores de densidad válidos oscilan entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="445e8-208">Valid density values range from 0.0 through 1.0.</span></span> <span data-ttu-id="445e8-209">El valor predeterminado es 1,0.</span><span class="sxs-lookup"><span data-stu-id="445e8-209">The default value is 1.0.</span></span> <span data-ttu-id="445e8-210">Para obtener más información, vea [Parámetros de parámetros de parámetros de parámetros (Direct3D 9)](fog-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="445e8-210">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

<span data-ttu-id="445e8-211">Los valores de este estado de representación son valores de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="445e8-211">Values for this render state are floating-point values.</span></span> <span data-ttu-id="445e8-212">Dado que [**el método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor , como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="445e8-212">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
    m_pDevice9->SetRenderState(D3DRS_FOGDENSITY, *((DWORD*) (&fFogDensity)));
```



</dd> <dt>

<span data-ttu-id="445e8-213"><span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS \_ RANGEFOGENABLE**</span><span class="sxs-lookup"><span data-stu-id="445e8-213"><span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS\_RANGEFOGENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-214">**TRUE** para habilitar el vértice basado en intervalos.</span><span class="sxs-lookup"><span data-stu-id="445e8-214">**TRUE** to enable range-based vertex fog.</span></span> <span data-ttu-id="445e8-215">El valor predeterminado es **FALSE,** en cuyo caso el sistema usa el sistema basado en profundidad.</span><span class="sxs-lookup"><span data-stu-id="445e8-215">The default value is **FALSE**, in which case the system uses depth-based fog.</span></span> <span data-ttu-id="445e8-216">En los intervalos basados en intervalos, la distancia de un objeto desde el visor se usa para calcular los efectos de sonido, no la profundidad del objeto (es decir, la coordenada z) de la escena.</span><span class="sxs-lookup"><span data-stu-id="445e8-216">In range-based fog, the distance of an object from the viewer is used to compute fog effects, not the depth of the object (that is, the z-coordinate) in the scene.</span></span> <span data-ttu-id="445e8-217">En los intervalos basados en intervalos, todos los métodos de métodos de distribución funcionan como de costumbre, excepto que usan el intervalo en lugar de la profundidad en los cálculos.</span><span class="sxs-lookup"><span data-stu-id="445e8-217">In range-based fog, all fog methods work as usual, except that they use range instead of depth in the computations.</span></span>

<span data-ttu-id="445e8-218">El intervalo es el factor correcto que se debe usar para los cálculos de cálculos de computación, pero la profundidad se usa normalmente en su lugar porque el intervalo tarda mucho tiempo en calcularse y la profundidad ya está disponible con carácter general.</span><span class="sxs-lookup"><span data-stu-id="445e8-218">Range is the correct factor to use for fog computations, but depth is commonly used instead because range is time-consuming to compute and depth is generally already available.</span></span> <span data-ttu-id="445e8-219">El uso de profundidad para calcular la profundidad tiene el efecto no deseado de que la disponibilidad de los objetos periféricos cambie a medida que se mueve el ojo del visor; en este caso, la profundidad cambia y el intervalo permanece constante.</span><span class="sxs-lookup"><span data-stu-id="445e8-219">Using depth to calculate fog has the undesirable effect of having the fogginess of peripheral objects change as the viewer's eye moves - in this case, the depth changes and the range remains constant.</span></span>

<span data-ttu-id="445e8-220">Dado que actualmente ningún hardware admite el rango por píxel basado en el rango, la corrección de intervalo solo se ofrece para vértices.</span><span class="sxs-lookup"><span data-stu-id="445e8-220">Because no hardware currently supports per-pixel range-based fog, range correction is offered only for vertex fog.</span></span>

<span data-ttu-id="445e8-221">Para obtener más información, vea [Vértices de vértice (Direct3D 9).](vertex-fog.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-221">For more information, see [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="445e8-222"><span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS \_ STENCILENABLE**</span><span class="sxs-lookup"><span data-stu-id="445e8-222"><span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS\_STENCILENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-223">**TRUE** para habilitar la galería de símbolos o **FALSE para** deshabilitar la galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="445e8-223">**TRUE** to enable stenciling, or **FALSE** to disable stenciling.</span></span> <span data-ttu-id="445e8-224">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="445e8-224">The default value is **FALSE**.</span></span> <span data-ttu-id="445e8-225">Para obtener más información, vea Técnicas de búfer de galería [de símbolos (Direct3D 9).](stencil-buffer-techniques.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-225">For more information, see [Stencil Buffer Techniques (Direct3D 9)](stencil-buffer-techniques.md).</span></span>

</dd> <dt>

<span data-ttu-id="445e8-226"><span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS \_ STENCINCIIL**</span><span class="sxs-lookup"><span data-stu-id="445e8-226"><span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS\_STENCILFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-227">Operación de galería de símbolos que se realizará si se produce un error en la prueba de galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="445e8-227">Stencil operation to perform if the stencil test fails.</span></span> <span data-ttu-id="445e8-228">Los valores son del [**tipo enumerado D3DSTENCISTONE.**](./d3dstencilop.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-228">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="445e8-229">El valor predeterminado es D3DSTENCI \_ KEEP.</span><span class="sxs-lookup"><span data-stu-id="445e8-229">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-230"><span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS \_ STENCILZFAIL**</span><span class="sxs-lookup"><span data-stu-id="445e8-230"><span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS\_STENCILZFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-231">Operación de galería de símbolos que se realiza si se supera la prueba de galería de símbolos y se produce un error en la prueba de profundidad (z-test).</span><span class="sxs-lookup"><span data-stu-id="445e8-231">Stencil operation to perform if the stencil test passes and the depth test (z-test) fails.</span></span> <span data-ttu-id="445e8-232">Los valores son del [**tipo enumerado D3DSTENCISTONE.**](./d3dstencilop.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-232">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="445e8-233">El valor predeterminado es D3DSTENCI \_ KEEP.</span><span class="sxs-lookup"><span data-stu-id="445e8-233">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-234"><span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS \_ STENCILPASS**</span><span class="sxs-lookup"><span data-stu-id="445e8-234"><span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS\_STENCILPASS**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-235">Operación de galería de símbolos que se va a realizar si se supera la galería de símbolos y las pruebas de profundidad (z).</span><span class="sxs-lookup"><span data-stu-id="445e8-235">Stencil operation to perform if both the stencil and the depth (z) tests pass.</span></span> <span data-ttu-id="445e8-236">Los valores son del [**tipo enumerado D3DSTENCISTONE.**](./d3dstencilop.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-236">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="445e8-237">El valor predeterminado es D3DSTENCI \_ KEEP.</span><span class="sxs-lookup"><span data-stu-id="445e8-237">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-238"><span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS \_ STENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="445e8-238"><span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS\_STENCILFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-239">Función de comparación para la prueba de galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="445e8-239">Comparison function for the stencil test.</span></span> <span data-ttu-id="445e8-240">Los valores son del [**tipo enumerado D3DCMPFUNC.**](./d3dcmpfunc.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-240">Values are from the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="445e8-241">El valor predeterminado es D3DCMP \_ ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="445e8-241">The default value is D3DCMP\_ALWAYS.</span></span>

<span data-ttu-id="445e8-242">La función de comparación se usa para comparar el valor de referencia con una entrada de búfer de galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="445e8-242">The comparison function is used to compare the reference value to a stencil buffer entry.</span></span> <span data-ttu-id="445e8-243">Esta comparación solo se aplica a los bits del valor de referencia y la entrada del búfer de galería de símbolos que se establecen en la máscara de galería de símbolos (establecida por el estado de representación \_ STENCILMASK de D3DRS).</span><span class="sxs-lookup"><span data-stu-id="445e8-243">This comparison applies only to the bits in the reference value and stencil buffer entry that are set in the stencil mask (set by the D3DRS\_STENCILMASK render state).</span></span> <span data-ttu-id="445e8-244">Si **es TRUE,** se supera la prueba de galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="445e8-244">If **TRUE**, the stencil test passes.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-245"><span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS \_ STENCILREF**</span><span class="sxs-lookup"><span data-stu-id="445e8-245"><span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS\_STENCILREF**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-246">Valor de referencia int para la prueba de galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="445e8-246">An int reference value for the stencil test.</span></span> <span data-ttu-id="445e8-247">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="445e8-247">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-248"><span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS \_ STENCILMASK**</span><span class="sxs-lookup"><span data-stu-id="445e8-248"><span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS\_STENCILMASK**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-249">Máscara aplicada al valor de referencia y a cada entrada de búfer de galería de símbolos para determinar los bits significativos de la prueba de galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="445e8-249">Mask applied to the reference value and each stencil buffer entry to determine the significant bits for the stencil test.</span></span> <span data-ttu-id="445e8-250">La máscara predeterminada es 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="445e8-250">The default mask is 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-251"><span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS \_ STENCILWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="445e8-251"><span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS\_STENCILWRITEMASK**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-252">Máscara de escritura aplicada a los valores escritos en el búfer de galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="445e8-252">Write mask applied to values written into the stencil buffer.</span></span> <span data-ttu-id="445e8-253">La máscara predeterminada es 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="445e8-253">The default mask is 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-254"><span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS \_ TEXTUREFACTOR**</span><span class="sxs-lookup"><span data-stu-id="445e8-254"><span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS\_TEXTUREFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-255">Color que se usa para la combinación de varias texturas con el argumento de mezcla de textura de TFACTOR D3DTA o la operación de mezcla de \_ texturas D3DTOP \_ BLENDFACTORALPHA.</span><span class="sxs-lookup"><span data-stu-id="445e8-255">Color used for multiple-texture blending with the D3DTA\_TFACTOR texture-blending argument or the D3DTOP\_BLENDFACTORALPHA texture-blending operation.</span></span> <span data-ttu-id="445e8-256">El valor asociado es una variable [**D3DCOLOR.**](d3dcolor.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-256">The associated value is a [**D3DCOLOR**](d3dcolor.md) variable.</span></span> <span data-ttu-id="445e8-257">El valor predeterminado es blanco opaco (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="445e8-257">The default value is opaque white (0xFFFFFFFF).</span></span>

</dd> <dt>

<span data-ttu-id="445e8-258"><span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS \_ WRAP0**</span><span class="sxs-lookup"><span data-stu-id="445e8-258"><span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS\_WRAP0**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-259">Comportamiento de ajuste de textura para varios conjuntos de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="445e8-259">Texture-wrapping behavior for multiple sets of texture coordinates.</span></span> <span data-ttu-id="445e8-260">Los valores válidos para este estado de representación pueden ser cualquier combinación de las marcas D3DWRAPCOORD \_ 0 (o D3DWRAP \_ U), D3DWRAPCOORD \_ 1 (o D3DWRAP \_ V), D3DWRAPCOORD \_ 2 (o D3DWRAP W) y \_ D3DWRAPCOORD \_ 3.</span><span class="sxs-lookup"><span data-stu-id="445e8-260">Valid values for this render state can be any combination of the D3DWRAPCOORD\_0 (or D3DWRAP\_U), D3DWRAPCOORD\_1 (or D3DWRAP\_V), D3DWRAPCOORD\_2 (or D3DWRAP\_W), and D3DWRAPCOORD\_3 flags.</span></span> <span data-ttu-id="445e8-261">Esto hace que el sistema se ajuste en la dirección de las dimensiones primera, segunda, tercera y cuarta, a veces denominadas direcciones s, t, r y q, para una textura determinada.</span><span class="sxs-lookup"><span data-stu-id="445e8-261">These cause the system to wrap in the direction of the first, second, third, and fourth dimensions, sometimes referred to as the s, t, r, and q directions, for a given texture.</span></span> <span data-ttu-id="445e8-262">El valor predeterminado para este estado de representación es 0 (encapsulado deshabilitado en todas las direcciones).</span><span class="sxs-lookup"><span data-stu-id="445e8-262">The default value for this render state is 0 (wrapping disabled in all directions).</span></span>

</dd> <dt>

<span data-ttu-id="445e8-263"><span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS \_ WRAP1**</span><span class="sxs-lookup"><span data-stu-id="445e8-263"><span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS\_WRAP1**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-264">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="445e8-264">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-265"><span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS \_ WRAP2**</span><span class="sxs-lookup"><span data-stu-id="445e8-265"><span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS\_WRAP2**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-266">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="445e8-266">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-267"><span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS \_ WRAP3**</span><span class="sxs-lookup"><span data-stu-id="445e8-267"><span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS\_WRAP3**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-268">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="445e8-268">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-269"><span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS \_ WRAP4**</span><span class="sxs-lookup"><span data-stu-id="445e8-269"><span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS\_WRAP4**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-270">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="445e8-270">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-271"><span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS \_ WRAP5**</span><span class="sxs-lookup"><span data-stu-id="445e8-271"><span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS\_WRAP5**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-272">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="445e8-272">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-273"><span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS \_ WRAP6**</span><span class="sxs-lookup"><span data-stu-id="445e8-273"><span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS\_WRAP6**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-274">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="445e8-274">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-275"><span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS \_ WRAP7**</span><span class="sxs-lookup"><span data-stu-id="445e8-275"><span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS\_WRAP7**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-276">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="445e8-276">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-277"><span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**RECORTE DE \_ D3DRS**</span><span class="sxs-lookup"><span data-stu-id="445e8-277"><span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**D3DRS\_CLIPPING**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-278">**TRUE** para habilitar el recorte primitivo de Direct3D o **FALSE** para deshabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="445e8-278">**TRUE** to enable primitive clipping by Direct3D, or **FALSE** to disable it.</span></span> <span data-ttu-id="445e8-279">El valor predeterminado es **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="445e8-279">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-280"><span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**ILUMINACIÓN D3DRS \_**</span><span class="sxs-lookup"><span data-stu-id="445e8-280"><span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**D3DRS\_LIGHTING**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-281">**TRUE** para habilitar la iluminación de Direct3D o **FALSE** para deshabilitarla.</span><span class="sxs-lookup"><span data-stu-id="445e8-281">**TRUE** to enable Direct3D lighting, or **FALSE** to disable it.</span></span> <span data-ttu-id="445e8-282">El valor predeterminado es **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="445e8-282">The default value is **TRUE**.</span></span> <span data-ttu-id="445e8-283">Solo los vértices que incluyen un vértice normal se encienden correctamente; Los vértices que no contienen un normal emplean un producto de punto de 0 en todos los cálculos de iluminación.</span><span class="sxs-lookup"><span data-stu-id="445e8-283">Only vertices that include a vertex normal are properly lit; vertices that do not contain a normal employ a dot product of 0 in all lighting calculations.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-284"><span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**D3DRS \_ AMBIENT**</span><span class="sxs-lookup"><span data-stu-id="445e8-284"><span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**D3DRS\_AMBIENT**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-285">Color claro ambiente.</span><span class="sxs-lookup"><span data-stu-id="445e8-285">Ambient light color.</span></span> <span data-ttu-id="445e8-286">Este valor es de tipo [**D3DCOLOR.**](d3dcolor.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-286">This value is of type [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="445e8-287">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="445e8-287">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-288"><span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**\_D3DRSVERTEXMODE**</span><span class="sxs-lookup"><span data-stu-id="445e8-288"><span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**D3DRS\_FOGVERTEXMODE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-289">Fórmula de vértice que se va a usar para vértices.</span><span class="sxs-lookup"><span data-stu-id="445e8-289">Fog formula to be used for vertex fog.</span></span> <span data-ttu-id="445e8-290">Se establece en un miembro del [**tipo enumerado D3DFOGMODE.**](./d3dfogmode.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-290">Set to one member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="445e8-291">El valor predeterminado es D3DFOG \_ NONE.</span><span class="sxs-lookup"><span data-stu-id="445e8-291">The default value is D3DFOG\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-292"><span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS \_ COLORVERTEX**</span><span class="sxs-lookup"><span data-stu-id="445e8-292"><span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS\_COLORVERTEX**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-293">**TRUE** para habilitar el color por vértice o **FALSE** para deshabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="445e8-293">**TRUE** to enable per-vertex color or **FALSE** to disable it.</span></span> <span data-ttu-id="445e8-294">El valor predeterminado es **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="445e8-294">The default value is **TRUE**.</span></span> <span data-ttu-id="445e8-295">Al habilitar el color por vértice, el sistema puede incluir el color definido para los vértices individuales en sus cálculos de iluminación.</span><span class="sxs-lookup"><span data-stu-id="445e8-295">Enabling per-vertex color allows the system to include the color defined for individual vertices in its lighting calculations.</span></span>

<span data-ttu-id="445e8-296">Para obtener más información, vea los siguientes estados de representación:</span><span class="sxs-lookup"><span data-stu-id="445e8-296">For more information, see the following render states:</span></span>

-   <span data-ttu-id="445e8-297">D3DRS \_ DIFFUSEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="445e8-297">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>
-   <span data-ttu-id="445e8-298">D3DRS \_ SPECULARMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="445e8-298">D3DRS\_SPECULARMATERIALSOURCE</span></span>
-   <span data-ttu-id="445e8-299">D3DRS \_ AMBIENTMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="445e8-299">D3DRS\_AMBIENTMATERIALSOURCE</span></span>
-   <span data-ttu-id="445e8-300">D3DRS \_ EMISSIVEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="445e8-300">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>

</dd> <dt>

<span data-ttu-id="445e8-301"><span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS \_ LOCALVIEWER**</span><span class="sxs-lookup"><span data-stu-id="445e8-301"><span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS\_LOCALVIEWER**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-302">**TRUE** para habilitar los resaltados especulares relativos a la cámara o **FALSE** para usar resaltados ortogonales especulares.</span><span class="sxs-lookup"><span data-stu-id="445e8-302">**TRUE** to enable camera-relative specular highlights, or **FALSE** to use orthogonal specular highlights.</span></span> <span data-ttu-id="445e8-303">El valor predeterminado es **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="445e8-303">The default value is **TRUE**.</span></span> <span data-ttu-id="445e8-304">Las aplicaciones que usan proyección ortogonal deben especificar **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="445e8-304">Applications that use orthogonal projection should specify **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-305"><span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS \_ NORMALIZENORMALS**</span><span class="sxs-lookup"><span data-stu-id="445e8-305"><span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS\_NORMALIZENORMALS**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-306">**TRUE** para habilitar la normalización automática de normales de vértices o **FALSE** para deshabilitarla.</span><span class="sxs-lookup"><span data-stu-id="445e8-306">**TRUE** to enable automatic normalization of vertex normals, or **FALSE** to disable it.</span></span> <span data-ttu-id="445e8-307">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="445e8-307">The default value is **FALSE**.</span></span> <span data-ttu-id="445e8-308">La habilitación de esta característica hace que el sistema normalice los normales de vértices para los vértices después de transformarlos en espacio de la cámara, lo que puede llevar mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="445e8-308">Enabling this feature causes the system to normalize the vertex normals for vertices after transforming them to camera space, which can be computationally time-consuming.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-309"><span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS \_ DIFFUSEMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="445e8-309"><span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS\_DIFFUSEMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-310">Origen de color difuso para cálculos de iluminación.</span><span class="sxs-lookup"><span data-stu-id="445e8-310">Diffuse color source for lighting calculations.</span></span> <span data-ttu-id="445e8-311">Los valores válidos son miembros del tipo enumerado [**D3DMATERIALCOLORSOURCE.**](./d3dmaterialcolorsource.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-311">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="445e8-312">El valor predeterminado es D3DMCS \_ COLOR1.</span><span class="sxs-lookup"><span data-stu-id="445e8-312">The default value is D3DMCS\_COLOR1.</span></span> <span data-ttu-id="445e8-313">El valor de este estado de representación solo se usa si el estado de representación COLORVERTEX de D3DRS \_ está establecido en **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="445e8-313">The value for this render state is used only if the D3DRS\_COLORVERTEX render state is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-314"><span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS \_ SPECULARMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="445e8-314"><span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS\_SPECULARMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-315">Origen de color especular para los cálculos de iluminación.</span><span class="sxs-lookup"><span data-stu-id="445e8-315">Specular color source for lighting calculations.</span></span> <span data-ttu-id="445e8-316">Los valores válidos son miembros del tipo enumerado [**D3DMATERIALCOLORSOURCE.**](./d3dmaterialcolorsource.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-316">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="445e8-317">El valor predeterminado es D3DMCS \_ COLOR2.</span><span class="sxs-lookup"><span data-stu-id="445e8-317">The default value is D3DMCS\_COLOR2.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-318"><span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS \_ AMBIENTMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="445e8-318"><span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS\_AMBIENTMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-319">Origen de color ambiente para los cálculos de iluminación.</span><span class="sxs-lookup"><span data-stu-id="445e8-319">Ambient color source for lighting calculations.</span></span> <span data-ttu-id="445e8-320">Los valores válidos son miembros del tipo enumerado [**D3DMATERIALCOLORSOURCE.**](./d3dmaterialcolorsource.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-320">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="445e8-321">El valor predeterminado es D3DMCS \_ MATERIAL.</span><span class="sxs-lookup"><span data-stu-id="445e8-321">The default value is D3DMCS\_MATERIAL.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-322"><span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS \_ EMISSIVEMATERIALSOURCE**</span><span class="sxs-lookup"><span data-stu-id="445e8-322"><span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS\_EMISSIVEMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-323">Origen de color emisivo para los cálculos de iluminación.</span><span class="sxs-lookup"><span data-stu-id="445e8-323">Emissive color source for lighting calculations.</span></span> <span data-ttu-id="445e8-324">Los valores válidos son miembros del tipo enumerado [**D3DMATERIALCOLORSOURCE.**](./d3dmaterialcolorsource.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-324">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="445e8-325">El valor predeterminado es D3DMCS \_ MATERIAL.</span><span class="sxs-lookup"><span data-stu-id="445e8-325">The default value is D3DMCS\_MATERIAL.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-326"><span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**VERTEXBLEND de D3DRS \_**</span><span class="sxs-lookup"><span data-stu-id="445e8-326"><span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS\_VERTEXBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-327">Número de matrices que se usarán para realizar la mezcla de geometría, si la hay.</span><span class="sxs-lookup"><span data-stu-id="445e8-327">Number of matrices to use to perform geometry blending, if any.</span></span> <span data-ttu-id="445e8-328">Los valores válidos son miembros del tipo enumerado [**D3DVERTEXBLENDFLAGS.**](./d3dvertexblendflags.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-328">Valid values are members of the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="445e8-329">El valor predeterminado es D3DVBF \_ DISABLE.</span><span class="sxs-lookup"><span data-stu-id="445e8-329">The default value is D3DVBF\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-330"><span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**CLIPPLANEENABLE DE D3DRS \_**</span><span class="sxs-lookup"><span data-stu-id="445e8-330"><span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS\_CLIPPLANEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-331">Habilita o deshabilita los planos de recorte definidos por el usuario.</span><span class="sxs-lookup"><span data-stu-id="445e8-331">Enables or disables user-defined clipping planes.</span></span> <span data-ttu-id="445e8-332">Los valores válidos son cualquier DWORD en el que el estado de cada bit (establecido o no establecido) alterna el estado de activación de un plano de recorte definido por el usuario correspondiente.</span><span class="sxs-lookup"><span data-stu-id="445e8-332">Valid values are any DWORD in which the status of each bit (set or not set) toggles the activation state of a corresponding user-defined clipping plane.</span></span> <span data-ttu-id="445e8-333">El bit menos significativo (bit 0) controla el primer plano de recorte en el índice 0 y los bits posteriores controlan la activación de los planos de recorte en índices más altos.</span><span class="sxs-lookup"><span data-stu-id="445e8-333">The least significant bit (bit 0) controls the first clipping plane at index 0, and subsequent bits control the activation of clipping planes at higher indexes.</span></span> <span data-ttu-id="445e8-334">Si se establece un bit, el sistema aplica el plano de recorte adecuado durante la representación de la escena.</span><span class="sxs-lookup"><span data-stu-id="445e8-334">If a bit is set, the system applies the appropriate clipping plane during scene rendering.</span></span> <span data-ttu-id="445e8-335">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="445e8-335">The default value is 0.</span></span>

<span data-ttu-id="445e8-336">Las macros [**D3DCLIPPLANEn**](d3dclipplanen.md) se definen para proporcionar una manera cómoda de habilitar los planos de recorte.</span><span class="sxs-lookup"><span data-stu-id="445e8-336">The [**D3DCLIPPLANEn**](d3dclipplanen.md) macros are defined to provide a convenient way to enable clipping planes.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-337"><span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS \_ POINTSIZE**</span><span class="sxs-lookup"><span data-stu-id="445e8-337"><span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS\_POINTSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-338">Valor float que especifica el tamaño que se va a usar para el cálculo de tamaño de punto en casos en los que no se especifica el tamaño de punto para cada vértice.</span><span class="sxs-lookup"><span data-stu-id="445e8-338">A float value that specifies the size to use for point size computation in cases where point size is not specified for each vertex.</span></span> <span data-ttu-id="445e8-339">Este valor no se usa cuando el vértice contiene el tamaño de punto.</span><span class="sxs-lookup"><span data-stu-id="445e8-339">This value is not used when the vertex contains point size.</span></span> <span data-ttu-id="445e8-340">Este valor está en unidades de espacio de pantalla si D3DRS POINTSCALEENABLE es FALSE; de lo contrario, este \_ valor está en unidades espaciales del mundo.</span><span class="sxs-lookup"><span data-stu-id="445e8-340">This value is in screen space units if D3DRS\_POINTSCALEENABLE is **FALSE**; otherwise this value is in world space units.</span></span> <span data-ttu-id="445e8-341">El valor predeterminado es el valor que devuelve un controlador.</span><span class="sxs-lookup"><span data-stu-id="445e8-341">The default value is the value a driver returns.</span></span> <span data-ttu-id="445e8-342">Si un controlador devuelve 0 o 1, el valor predeterminado es 64, lo que permite emular el tamaño del punto de software.</span><span class="sxs-lookup"><span data-stu-id="445e8-342">If a driver returns 0 or 1, the default value is 64, which allows software point size emulation.</span></span> <span data-ttu-id="445e8-343">Dado que [**el método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor , como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="445e8-343">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE, *((DWORD*)&pointSize));
```



</dd> <dt>

<span data-ttu-id="445e8-344"><span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS \_ POINTSIZE \_ MIN**</span><span class="sxs-lookup"><span data-stu-id="445e8-344"><span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS\_POINTSIZE\_MIN**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-345">Valor float que especifica el tamaño mínimo de los primitivos de punto.</span><span class="sxs-lookup"><span data-stu-id="445e8-345">A float value that specifies the minimum size of point primitives.</span></span> <span data-ttu-id="445e8-346">Las primitivas de punto se fijan a este tamaño durante la representación.</span><span class="sxs-lookup"><span data-stu-id="445e8-346">Point primitives are clamped to this size during rendering.</span></span> <span data-ttu-id="445e8-347">Si se establece en valores menores que 1,0, los puntos se descartan cuando el punto no cubre un centro de píxeles y el suavizado de contorno está deshabilitado o se representa con una intensidad reducida cuando se habilita el suavizado de contorno.</span><span class="sxs-lookup"><span data-stu-id="445e8-347">Setting this to values smaller than 1.0 results in points dropping out when the point does not cover a pixel center and antialiasing is disabled or being rendered with reduced intensity when antialiasing is enabled.</span></span> <span data-ttu-id="445e8-348">El valor predeterminado es 1,0f.</span><span class="sxs-lookup"><span data-stu-id="445e8-348">The default value is 1.0f.</span></span> <span data-ttu-id="445e8-349">El intervalo de este valor es mayor o igual que 0,0f.</span><span class="sxs-lookup"><span data-stu-id="445e8-349">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="445e8-350">Dado que [**el método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor , como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="445e8-350">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE_MIN, *((DWORD*)&pointSizeMin));
```



</dd> <dt>

<span data-ttu-id="445e8-351"><span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**PUNTOS \_ D3DRSPRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="445e8-351"><span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS\_POINTSPRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-352">valor bool.</span><span class="sxs-lookup"><span data-stu-id="445e8-352">bool value.</span></span> <span data-ttu-id="445e8-353">Cuando **es TRUE,** las coordenadas de textura de las primitivas de punto se establecen para que las texturas completa se asignen a cada punto.</span><span class="sxs-lookup"><span data-stu-id="445e8-353">When **TRUE**, texture coordinates of point primitives are set so that full textures are mapped on each point.</span></span> <span data-ttu-id="445e8-354">Cuando **es FALSE,** las coordenadas de textura de vértice se usan para todo el punto.</span><span class="sxs-lookup"><span data-stu-id="445e8-354">When **FALSE**, the vertex texture coordinates are used for the entire point.</span></span> <span data-ttu-id="445e8-355">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="445e8-355">The default value is **FALSE**.</span></span> <span data-ttu-id="445e8-356">Puede lograr puntos de un solo píxel de estilo DirectX 7 estableciendo D3DRS \_ POINTSCALEENABLE en **FALSE** y D3DRS POINTSIZE en 1.0, que son los valores \_ predeterminados.</span><span class="sxs-lookup"><span data-stu-id="445e8-356">You can achieve DirectX 7 style single-pixel points by setting D3DRS\_POINTSCALEENABLE to **FALSE** and D3DRS\_POINTSIZE to 1.0, which are the default values.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-357"><span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS \_ POINTSCALEENABLE**</span><span class="sxs-lookup"><span data-stu-id="445e8-357"><span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS\_POINTSCALEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-358">valor bool que controla el cálculo del tamaño de las primitivas de punto.</span><span class="sxs-lookup"><span data-stu-id="445e8-358">bool value that controls computation of size for point primitives.</span></span> <span data-ttu-id="445e8-359">Cuando **es TRUE,** el tamaño del punto se interpreta como un valor de espacio de la cámara y se escala mediante la función distance y el frustum para la ventanilla y el escalado del eje Y para calcular el tamaño final del punto de espacio en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="445e8-359">When **TRUE**, the point size is interpreted as a camera space value and is scaled by the distance function and the frustum to viewport y-axis scaling to compute the final screen-space point size.</span></span> <span data-ttu-id="445e8-360">Cuando **es FALSE,** el tamaño del punto se interpreta como espacio de pantalla y se usa directamente.</span><span class="sxs-lookup"><span data-stu-id="445e8-360">When **FALSE**, the point size is interpreted as screen space and used directly.</span></span> <span data-ttu-id="445e8-361">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="445e8-361">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-362"><span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS \_ POINTSCALE \_ A**</span><span class="sxs-lookup"><span data-stu-id="445e8-362"><span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS\_POINTSCALE\_A**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-363">Valor float que controla la atenuación del tamaño basado en la distancia para las primitivas de punto.</span><span class="sxs-lookup"><span data-stu-id="445e8-363">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="445e8-364">Activo solo cuando D3DRS \_ POINTSCALEENABLE es **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="445e8-364">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="445e8-365">El valor predeterminado es 1,0f.</span><span class="sxs-lookup"><span data-stu-id="445e8-365">The default value is 1.0f.</span></span> <span data-ttu-id="445e8-366">El intervalo de este valor es mayor o igual que 0,0f.</span><span class="sxs-lookup"><span data-stu-id="445e8-366">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="445e8-367">Dado que [**el método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="445e8-367">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_A, *((DWORD*)&pointScaleA));
```



</dd> <dt>

<span data-ttu-id="445e8-368"><span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS \_ POINTSCALE \_ B**</span><span class="sxs-lookup"><span data-stu-id="445e8-368"><span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS\_POINTSCALE\_B**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-369">Valor float que controla la atenuación del tamaño basado en la distancia para las primitivas de punto.</span><span class="sxs-lookup"><span data-stu-id="445e8-369">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="445e8-370">Activo solo cuando D3DRS \_ POINTSCALEENABLE es **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="445e8-370">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="445e8-371">El valor predeterminado es 0,0f.</span><span class="sxs-lookup"><span data-stu-id="445e8-371">The default value is 0.0f.</span></span> <span data-ttu-id="445e8-372">El intervalo de este valor es mayor o igual que 0,0f.</span><span class="sxs-lookup"><span data-stu-id="445e8-372">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="445e8-373">Dado que [**el método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="445e8-373">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_B, *((DWORD*)&pointScaleB));
```



</dd> <dt>

<span data-ttu-id="445e8-374"><span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS \_ POINTSCALE \_ C**</span><span class="sxs-lookup"><span data-stu-id="445e8-374"><span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS\_POINTSCALE\_C**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-375">Valor float que controla la atenuación del tamaño basado en la distancia para las primitivas de punto.</span><span class="sxs-lookup"><span data-stu-id="445e8-375">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="445e8-376">Activo solo cuando D3DRS \_ POINTSCALEENABLE es **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="445e8-376">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="445e8-377">El valor predeterminado es 0,0f.</span><span class="sxs-lookup"><span data-stu-id="445e8-377">The default value is 0.0f.</span></span> <span data-ttu-id="445e8-378">El intervalo de este valor es mayor o igual que 0,0f.</span><span class="sxs-lookup"><span data-stu-id="445e8-378">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="445e8-379">Dado que [**el método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor , como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="445e8-379">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_C, *((DWORD*)&pointScaleC));
```



</dd> <dt>

<span data-ttu-id="445e8-380"><span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS \_ MULTISAMPLEANTIALIAS**</span><span class="sxs-lookup"><span data-stu-id="445e8-380"><span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS\_MULTISAMPLEANTIALIAS**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-381">valor bool que determina cómo se calculan muestras individuales al usar un búfer de destino de representación multimuestreo.</span><span class="sxs-lookup"><span data-stu-id="445e8-381">bool value that determines how individual samples are computed when using a multisample render-target buffer.</span></span> <span data-ttu-id="445e8-382">Cuando se establece en **TRUE**, se calculan las múltiples muestras para que el suavizado de contorno de escena completa se realice mediante el muestreo en diferentes posiciones de muestra para cada muestra múltiple.</span><span class="sxs-lookup"><span data-stu-id="445e8-382">When set to **TRUE**, the multiple samples are computed so that full-scene antialiasing is performed by sampling at different sample positions for each multiple sample.</span></span> <span data-ttu-id="445e8-383">Cuando se establece en **FALSE,** todas las muestras se escriben con el mismo valor de ejemplo, muestreados en el centro de píxeles, lo que permite la representación sin suavizado de contorno en un búfer de varios ejemplos.</span><span class="sxs-lookup"><span data-stu-id="445e8-383">When set to **FALSE**, the multiple samples are all written with the same sample value, sampled at the pixel center, which allows non-antialiased rendering to a multisample buffer.</span></span> <span data-ttu-id="445e8-384">Este estado de representación no tiene ningún efecto al representar en un solo búfer de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="445e8-384">This render state has no effect when rendering to a single sample buffer.</span></span> <span data-ttu-id="445e8-385">El valor predeterminado es **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="445e8-385">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-386"><span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS \_ MULTISAMPLEMASK**</span><span class="sxs-lookup"><span data-stu-id="445e8-386"><span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS\_MULTISAMPLEMASK**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-387">Cada bit de esta máscara, empezando por el bit menos significativo (LSB), controla la modificación de uno de los ejemplos en un destino de representación multimuestreo.</span><span class="sxs-lookup"><span data-stu-id="445e8-387">Each bit in this mask, starting at the least significant bit (LSB), controls modification of one of the samples in a multisample render target.</span></span> <span data-ttu-id="445e8-388">Por lo tanto, para un destino de representación de 8 muestras, el byte bajo contiene las ocho escrituras que se habilitan para cada una de las ocho muestras.</span><span class="sxs-lookup"><span data-stu-id="445e8-388">Thus, for an 8-sample render target, the low byte contains the eight write enables for each of the eight samples.</span></span> <span data-ttu-id="445e8-389">Este estado de representación no tiene ningún efecto al representar en un único búfer de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="445e8-389">This render state has no effect when rendering to a single sample buffer.</span></span> <span data-ttu-id="445e8-390">El valor predeterminado es 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="445e8-390">The default value is 0xFFFFFFFF.</span></span>

<span data-ttu-id="445e8-391">Este estado de representación permite el uso de un búfer de varios ejemplos como búfer de acumulación, realizando la representación multipass de geometry donde cada paso actualiza un subconjunto de ejemplos.</span><span class="sxs-lookup"><span data-stu-id="445e8-391">This render state enables use of a multisample buffer as an accumulation buffer, doing multipass rendering of geometry where each pass updates a subset of samples.</span></span>

<span data-ttu-id="445e8-392">Si hay n muestras habilitadas para varios ejemplos y k, la intensidad resultante de la imagen representada debe ser k/n.</span><span class="sxs-lookup"><span data-stu-id="445e8-392">If there are n multisamples and k enabled samples, the resulting intensity of the rendered image should be k/n.</span></span> <span data-ttu-id="445e8-393">Cada componente RGB de cada píxel se factorizó por k/n.</span><span class="sxs-lookup"><span data-stu-id="445e8-393">Each component RGB of every pixel is factored by k/n.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-394"><span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS \_ PATCHEDGESTYLE**</span><span class="sxs-lookup"><span data-stu-id="445e8-394"><span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS\_PATCHEDGESTYLE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-395">Establece si los bordes de revisión usarán teselación de estilo float.</span><span class="sxs-lookup"><span data-stu-id="445e8-395">Sets whether patch edges will use float style tessellation.</span></span> <span data-ttu-id="445e8-396">El tipo enumerado [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) define los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="445e8-396">Possible values are defined by the [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) enumerated type.</span></span> <span data-ttu-id="445e8-397">El valor predeterminado es D3DPATCHEDGE \_ DISCRETE.</span><span class="sxs-lookup"><span data-stu-id="445e8-397">The default value is D3DPATCHEDGE\_DISCRETE.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-398"><span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS \_ DEBUGMONITORTOKEN**</span><span class="sxs-lookup"><span data-stu-id="445e8-398"><span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS\_DEBUGMONITORTOKEN**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-399">Establezca solo para depurar el monitor.</span><span class="sxs-lookup"><span data-stu-id="445e8-399">Set only for debugging the monitor.</span></span> <span data-ttu-id="445e8-400">El tipo enumerado [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) define los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="445e8-400">Possible values are defined by the [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) enumerated type.</span></span> <span data-ttu-id="445e8-401">Tenga en cuenta que si se establece D3DRS DEBUGMONITORTOKEN, la llamada se trata como pasar \_ un token al monitor de depuración.</span><span class="sxs-lookup"><span data-stu-id="445e8-401">Note that if D3DRS\_DEBUGMONITORTOKEN is set, the call is treated as passing a token to the debug monitor.</span></span> <span data-ttu-id="445e8-402">Por ejemplo, si después de pasar D3DDMT ENABLE o \_ D3DDMT DISABLE a \_ D3DRS DEBUGMONITORTOKEN, se pasan otros valores de token, el estado (habilitado o deshabilitado) del monitor de depuración se \_ conservará.</span><span class="sxs-lookup"><span data-stu-id="445e8-402">For example, if - after passing D3DDMT\_ENABLE or D3DDMT\_DISABLE to D3DRS\_DEBUGMONITORTOKEN - other token values are passed in, the state (enabled or disabled) of the debug monitor will still persist.</span></span>

<span data-ttu-id="445e8-403">Este estado solo es útil para las compilaciones de depuración.</span><span class="sxs-lookup"><span data-stu-id="445e8-403">This state is only useful for debug builds.</span></span> <span data-ttu-id="445e8-404">El monitor de depuración tiene como valor predeterminado D3DDMT \_ ENABLE.</span><span class="sxs-lookup"><span data-stu-id="445e8-404">The debug monitor defaults to D3DDMT\_ENABLE.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-405"><span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS \_ POINTSIZE \_ MAX**</span><span class="sxs-lookup"><span data-stu-id="445e8-405"><span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS\_POINTSIZE\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-406">Valor float que especifica el tamaño máximo al que se fijarán los sprites de punto.</span><span class="sxs-lookup"><span data-stu-id="445e8-406">A float value that specifies the maximum size to which point sprites will be clamped.</span></span> <span data-ttu-id="445e8-407">El valor debe ser menor o igual que el miembro MaxPointSize de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) y mayor o igual que D3DRS \_ POINTSIZE \_ MIN.</span><span class="sxs-lookup"><span data-stu-id="445e8-407">The value must be less than or equal to the MaxPointSize member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) and greater than or equal to D3DRS\_POINTSIZE\_MIN.</span></span> <span data-ttu-id="445e8-408">El valor predeterminado es 64.0.</span><span class="sxs-lookup"><span data-stu-id="445e8-408">The default value is 64.0.</span></span> <span data-ttu-id="445e8-409">Dado que [**el método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor, como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="445e8-409">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_PONTSIZE_MAX, *((DWORD*)&pointSizeMax));
```



</dd> <dt>

<span data-ttu-id="445e8-410"><span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS \_ INDEXEDVERTEXBLENDENABLE**</span><span class="sxs-lookup"><span data-stu-id="445e8-410"><span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS\_INDEXEDVERTEXBLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-411">valor bool que habilita o deshabilita la mezcla de vértices indexados.</span><span class="sxs-lookup"><span data-stu-id="445e8-411">bool value that enables or disables indexed vertex blending.</span></span> <span data-ttu-id="445e8-412">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="445e8-412">The default value is **FALSE**.</span></span> <span data-ttu-id="445e8-413">Cuando se establece en **TRUE,** se habilita la combinación de vértices indizados.</span><span class="sxs-lookup"><span data-stu-id="445e8-413">When set to **TRUE**, indexed vertex blending is enabled.</span></span> <span data-ttu-id="445e8-414">Cuando se establece en **FALSE,** la combinación de vértices indizados está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="445e8-414">When set to **FALSE**, indexed vertex blending is disabled.</span></span> <span data-ttu-id="445e8-415">Si este estado de representación está habilitado, el usuario debe pasar índices de matriz como DWORD empaquetadocon cada vértice.</span><span class="sxs-lookup"><span data-stu-id="445e8-415">If this render state is enabled, the user must pass matrix indices as a packed DWORDwith every vertex.</span></span> <span data-ttu-id="445e8-416">Cuando el estado de representación está deshabilitado y la fusión de vértices se habilita a través del estado VERTEXBLEND de D3DRS, es equivalente a tener índices de \_ matriz 0, 1, 2, 3 en cada vértice.</span><span class="sxs-lookup"><span data-stu-id="445e8-416">When the render state is disabled and vertex blending is enabled through the D3DRS\_VERTEXBLEND state, it is equivalent to having matrix indices 0, 1, 2, 3 in every vertex.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-417"><span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS \_ COLORWRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="445e8-417"><span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS\_COLORWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-418">Valor UINT que habilita una escritura por canal para el búfer de color de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="445e8-418">UINT value that enables a per-channel write for the render-target color buffer.</span></span> <span data-ttu-id="445e8-419">Un bit de conjunto da como resultado que el canal de color se actualice durante la representación en 3D.</span><span class="sxs-lookup"><span data-stu-id="445e8-419">A set bit results in the color channel being updated during 3D rendering.</span></span> <span data-ttu-id="445e8-420">Un bit claro da como resultado que el canal de color no se vería afectado.</span><span class="sxs-lookup"><span data-stu-id="445e8-420">A clear bit results in the color channel being unaffected.</span></span> <span data-ttu-id="445e8-421">Esta funcionalidad está disponible si el bit de funcionalidades COLORWRITEENABLE de D3DPMISCCAPS está establecido en el miembro PrimitiveMiscCaps de la estructura \_ [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="445e8-421">This functionality is available if the D3DPMISCCAPS\_COLORWRITEENABLE capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="445e8-422">Este estado de representación no afecta a la operación de borrar.</span><span class="sxs-lookup"><span data-stu-id="445e8-422">This render state does not affect the clear operation.</span></span> <span data-ttu-id="445e8-423">El valor predeterminado es 0x0000000F.</span><span class="sxs-lookup"><span data-stu-id="445e8-423">The default value is 0x0000000F.</span></span>

<span data-ttu-id="445e8-424">Los valores válidos para este estado de representación pueden ser cualquier combinación de las marcas D3DCOLORWRITEENABLE \_ ALPHA, D3DCOLORWRITEENABLE \_ BLUE, D3DCOLORWRITEENABLE GREEN o \_ D3DCOLORWRITEENABLE \_ RED.</span><span class="sxs-lookup"><span data-stu-id="445e8-424">Valid values for this render state can be any combination of the D3DCOLORWRITEENABLE\_ALPHA, D3DCOLORWRITEENABLE\_BLUE, D3DCOLORWRITEENABLE\_GREEN, or D3DCOLORWRITEENABLE\_RED flags.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-425"><span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS \_ TWEENFACTOR**</span><span class="sxs-lookup"><span data-stu-id="445e8-425"><span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS\_TWEENFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-426">Valor float que controla el factor de interpolación.</span><span class="sxs-lookup"><span data-stu-id="445e8-426">A float value that controls the tween factor.</span></span> <span data-ttu-id="445e8-427">El valor predeterminado es 0,0f.</span><span class="sxs-lookup"><span data-stu-id="445e8-427">The default value is 0.0f.</span></span> <span data-ttu-id="445e8-428">Dado que [**el método IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) acepta valores DWORD, la aplicación debe convertir una variable que contenga el valor , como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="445e8-428">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_TWEENFACTOR, *((DWORD*)&TweenFactor));
```



</dd> <dt>

<span data-ttu-id="445e8-429"><span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**BLENDOP de D3DRS \_**</span><span class="sxs-lookup"><span data-stu-id="445e8-429"><span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS\_BLENDOP**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-430">Valor utilizado para seleccionar la operación aritmética aplicada cuando el estado de representación de combinación alfa, D3DRS \_ ALPHABLENDENABLE, se establece en **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="445e8-430">Value used to select the arithmetic operation applied when the alpha blending render state, D3DRS\_ALPHABLENDENABLE, is set to **TRUE**.</span></span> <span data-ttu-id="445e8-431">El tipo enumerado [**D3DBLENDOP**](./d3dblendop.md) define los valores válidos.</span><span class="sxs-lookup"><span data-stu-id="445e8-431">Valid values are defined by the [**D3DBLENDOP**](./d3dblendop.md) enumerated type.</span></span> <span data-ttu-id="445e8-432">El valor predeterminado es D3DBLENDOP \_ ADD.</span><span class="sxs-lookup"><span data-stu-id="445e8-432">The default value is D3DBLENDOP\_ADD.</span></span>

<span data-ttu-id="445e8-433">Si no se admite la funcionalidad del dispositivo BLENDOP D3DPMISCCAPS, se \_ realiza D3DBLENDOP \_ ADD.</span><span class="sxs-lookup"><span data-stu-id="445e8-433">If the D3DPMISCCAPS\_BLENDOP device capability is not supported, then D3DBLENDOP\_ADD is performed.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-434"><span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS \_ POSITIONDEGREE**</span><span class="sxs-lookup"><span data-stu-id="445e8-434"><span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS\_POSITIONDEGREE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-435">Grado de interpolación de la posición de N revisiones.</span><span class="sxs-lookup"><span data-stu-id="445e8-435">N-patch position interpolation degree.</span></span> <span data-ttu-id="445e8-436">Los valores pueden ser D3DDEGREE \_ CUBIC (valor predeterminado) o D3DDEGREE \_ LINEAR.</span><span class="sxs-lookup"><span data-stu-id="445e8-436">The values can be D3DDEGREE\_CUBIC (default) or D3DDEGREE\_LINEAR.</span></span> <span data-ttu-id="445e8-437">Para obtener más información, [**vea D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="445e8-437">For more information, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="445e8-438"><span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS \_ NORMALDEGREE**</span><span class="sxs-lookup"><span data-stu-id="445e8-438"><span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS\_NORMALDEGREE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-439">Grado de interpolación normal de N revisiones.</span><span class="sxs-lookup"><span data-stu-id="445e8-439">N-patch normal interpolation degree.</span></span> <span data-ttu-id="445e8-440">Los valores pueden ser D3DDEGREE \_ LINEAR (valor predeterminado) o D3DDEGREE \_ QUADRATIC.</span><span class="sxs-lookup"><span data-stu-id="445e8-440">The values can be D3DDEGREE\_LINEAR (default) or D3DDEGREE\_QUADRATIC.</span></span> <span data-ttu-id="445e8-441">Para obtener más información, [**vea D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="445e8-441">For more information, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="445e8-442"><span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS \_ DESERCIÓNPRUEBATESTENABLE**</span><span class="sxs-lookup"><span data-stu-id="445e8-442"><span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS\_SCISSORTESTENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-443">**TRUE** para habilitar las pruebas de sitición **y FALSE** para deshabilitarla.</span><span class="sxs-lookup"><span data-stu-id="445e8-443">**TRUE** to enable scissor testing and **FALSE** to disable it.</span></span> <span data-ttu-id="445e8-444">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="445e8-444">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-445"><span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS \_ DESPEDAZCALEDEPTHBIAS**</span><span class="sxs-lookup"><span data-stu-id="445e8-445"><span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS\_SLOPESCALEDEPTHBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-446">Se usa para determinar la cantidad de sesgo que se puede aplicar a las primitivas planas para reducir la z-fighting.</span><span class="sxs-lookup"><span data-stu-id="445e8-446">Used to determine how much bias can be applied to co-planar primitives to reduce z-fighting.</span></span> <span data-ttu-id="445e8-447">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="445e8-447">The default value is 0.</span></span>

<span data-ttu-id="445e8-448">bias = (max \* D3DRS \_ CTRLEDEPTHBIAS) + D3DRS \_ DEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="445e8-448">bias = (max \* D3DRS\_SLOPESCALEDEPTHBIAS) + D3DRS\_DEPTHBIAS.</span></span>

<span data-ttu-id="445e8-449">donde max es la pendiente de profundidad máxima del triángulo que se representa.</span><span class="sxs-lookup"><span data-stu-id="445e8-449">where max is the maximum depth slope of the triangle being rendered.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-450"><span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS \_ ANTIALIASEDLINEENABLE**</span><span class="sxs-lookup"><span data-stu-id="445e8-450"><span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS\_ANTIALIASEDLINEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-451">**TRUE** para habilitar el suavizado de contorno de línea, **FALSE para** deshabilitar el suavizado de contorno de línea.</span><span class="sxs-lookup"><span data-stu-id="445e8-451">**TRUE** to enable line antialiasing, **FALSE** to disable line antialiasing.</span></span> <span data-ttu-id="445e8-452">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="445e8-452">The default value is **FALSE**.</span></span>

<span data-ttu-id="445e8-453">Al representar en un destino de representación multimuestreo, se omite D3DRS ANTIALIASEDLINEENABLE y todas las líneas se representan \_ con alias.</span><span class="sxs-lookup"><span data-stu-id="445e8-453">When rendering to a multisample render target, D3DRS\_ANTIALIASEDLINEENABLE is ignored and all lines are rendered aliased.</span></span> <span data-ttu-id="445e8-454">Use [**ID3DXLine para**](id3dxline.md) la representación de líneas suavizadas en un destino de representación multimuestreo.</span><span class="sxs-lookup"><span data-stu-id="445e8-454">Use [**ID3DXLine**](id3dxline.md) for antialiased line rendering in a multisample render target.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-455"><span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS \_ MINTESSELLATIONLEVEL**</span><span class="sxs-lookup"><span data-stu-id="445e8-455"><span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS\_MINTESSELLATIONLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-456">Nivel mínimo de teselación.</span><span class="sxs-lookup"><span data-stu-id="445e8-456">Minimum tessellation level.</span></span> <span data-ttu-id="445e8-457">El valor predeterminado es 1,0f.</span><span class="sxs-lookup"><span data-stu-id="445e8-457">The default value is 1.0f.</span></span> <span data-ttu-id="445e8-458">Vea [Teselación (Direct3D 9).](tessellation.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-458">See [Tessellation (Direct3D 9)](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="445e8-459"><span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS \_ MAXTESSELLATIONLEVEL**</span><span class="sxs-lookup"><span data-stu-id="445e8-459"><span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS\_MAXTESSELLATIONLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-460">Nivel máximo de teselación.</span><span class="sxs-lookup"><span data-stu-id="445e8-460">Maximum tessellation level.</span></span> <span data-ttu-id="445e8-461">El valor predeterminado es 1,0f.</span><span class="sxs-lookup"><span data-stu-id="445e8-461">The default value is 1.0f.</span></span> <span data-ttu-id="445e8-462">Vea [Teselación (Direct3D 9).](tessellation.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-462">See [Tessellation (Direct3D 9)](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="445e8-463"><span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS \_ ADAPTIVETESS \_ X**</span><span class="sxs-lookup"><span data-stu-id="445e8-463"><span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS\_ADAPTIVETESS\_X**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-464">Cantidad que se puede tesentar de forma adaptable, en la dirección x.</span><span class="sxs-lookup"><span data-stu-id="445e8-464">Amount to adaptively tessellate, in the x direction.</span></span> <span data-ttu-id="445e8-465">El valor predeterminado es 0,0f.</span><span class="sxs-lookup"><span data-stu-id="445e8-465">Default value is 0.0f.</span></span> <span data-ttu-id="445e8-466">Consulte [Tessellation adaptable.](tessellation.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-466">See [Adaptive Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="445e8-467"><span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS \_ ADAPTIVETESS \_ Y**</span><span class="sxs-lookup"><span data-stu-id="445e8-467"><span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS\_ADAPTIVETESS\_Y**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-468">Cantidad que se puede tesentar de forma adaptable, en la dirección y.</span><span class="sxs-lookup"><span data-stu-id="445e8-468">Amount to adaptively tessellate, in the y direction.</span></span> <span data-ttu-id="445e8-469">El valor predeterminado es 0,0f.</span><span class="sxs-lookup"><span data-stu-id="445e8-469">Default value is 0.0f.</span></span> <span data-ttu-id="445e8-470">Consulte [ \_ Tessellation adaptable.](tessellation.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-470">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="445e8-471"><span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS \_ ADAPTIVETESS \_ Z**</span><span class="sxs-lookup"><span data-stu-id="445e8-471"><span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS\_ADAPTIVETESS\_Z**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-472">Cantidad que se puede tesentar de forma adaptable, en la dirección z.</span><span class="sxs-lookup"><span data-stu-id="445e8-472">Amount to adaptively tessellate, in the z direction.</span></span> <span data-ttu-id="445e8-473">El valor predeterminado es 1,0f.</span><span class="sxs-lookup"><span data-stu-id="445e8-473">Default value is 1.0f.</span></span> <span data-ttu-id="445e8-474">Consulte [ \_ Tessellation adaptable.](tessellation.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-474">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="445e8-475"><span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS \_ ADAPTIVETESS \_ W**</span><span class="sxs-lookup"><span data-stu-id="445e8-475"><span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS\_ADAPTIVETESS\_W**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-476">Cantidad que se puede tesentar de forma adaptable, en la dirección w.</span><span class="sxs-lookup"><span data-stu-id="445e8-476">Amount to adaptively tessellate, in the w direction.</span></span> <span data-ttu-id="445e8-477">El valor predeterminado es 0,0f.</span><span class="sxs-lookup"><span data-stu-id="445e8-477">Default value is 0.0f.</span></span> <span data-ttu-id="445e8-478">Consulte [ \_ Tessellation adaptable.](tessellation.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-478">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="445e8-479"><span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS \_ ENABLEADAPTIVETESSELLATION**</span><span class="sxs-lookup"><span data-stu-id="445e8-479"><span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS\_ENABLEADAPTIVETESSELLATION**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-480">**TRUE** para habilitar la teselación adaptable, **FALSE** para deshabilitarla.</span><span class="sxs-lookup"><span data-stu-id="445e8-480">**TRUE** to enable adaptive tessellation, **FALSE** to disable it.</span></span> <span data-ttu-id="445e8-481">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="445e8-481">The default value is **FALSE**.</span></span> <span data-ttu-id="445e8-482">Consulte [ \_ Tessellation adaptable.](tessellation.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-482">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="445e8-483"><span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS \_ TWOSIDEDSTENCILMODE**</span><span class="sxs-lookup"><span data-stu-id="445e8-483"><span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS\_TWOSIDEDSTENCILMODE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-484">**TRUE** habilita la galería de símbolos de dos lados, **FALSE** la deshabilita.</span><span class="sxs-lookup"><span data-stu-id="445e8-484">**TRUE** enables two-sided stenciling, **FALSE** disables it.</span></span> <span data-ttu-id="445e8-485">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="445e8-485">The default value is **FALSE**.</span></span> <span data-ttu-id="445e8-486">La aplicación debe establecer D3DRS CULLMODE en D3DCULL NONE para habilitar el modo de \_ galería de símbolos de dos \_ lados.</span><span class="sxs-lookup"><span data-stu-id="445e8-486">The application should set D3DRS\_CULLMODE to D3DCULL\_NONE to enable two-sided stencil mode.</span></span> <span data-ttu-id="445e8-487">Si el orden de sinuoso del triángulo es en el sentido de las agujas del reloj, se usarán las operaciones D3DRS \_ STENCIL. \*</span><span class="sxs-lookup"><span data-stu-id="445e8-487">If the triangle winding order is clockwise, the D3DRS\_STENCIL\* operations will be used.</span></span> <span data-ttu-id="445e8-488">Si el orden de cierre es en sentido contrario a las agujas del reloj, se usarán las operaciones \_ STENCIL de CCW \_ D3DRS. \*</span><span class="sxs-lookup"><span data-stu-id="445e8-488">If the winding order is counterclockwise, the D3DRS\_CCW\_STENCIL\* operations will be used.</span></span>

<span data-ttu-id="445e8-489">Para ver si se admite la galería de símbolos de dos lados, compruebe el miembro StencilCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) para D3DSTENCILCAPS \_ TWOSIDED.</span><span class="sxs-lookup"><span data-stu-id="445e8-489">To see if two-sided stencil is supported, check the StencilCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) for D3DSTENCILCAPS\_TWOSIDED.</span></span> <span data-ttu-id="445e8-490">Vea también [D3DSTENCILCAPS](d3dstencilcaps.md).</span><span class="sxs-lookup"><span data-stu-id="445e8-490">See also [D3DSTENCILCAPS](d3dstencilcaps.md).</span></span>

</dd> <dt>

<span data-ttu-id="445e8-491"><span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS \_ CCW \_ STENCINCINCIIL**</span><span class="sxs-lookup"><span data-stu-id="445e8-491"><span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS\_CCW\_STENCILFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-492">Operación de galería de símbolos que se va a realizar si se produce un error en la prueba de galería de símbolos CCW.</span><span class="sxs-lookup"><span data-stu-id="445e8-492">Stencil operation to perform if CCW stencil test fails.</span></span> <span data-ttu-id="445e8-493">Los valores son del [**tipo enumerado D3DSTENCISTONE.**](./d3dstencilop.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-493">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="445e8-494">El valor predeterminado es D3DSTENCI \_ KEEP.</span><span class="sxs-lookup"><span data-stu-id="445e8-494">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-495"><span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS \_ CCW \_ STENCILZFAIL**</span><span class="sxs-lookup"><span data-stu-id="445e8-495"><span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS\_CCW\_STENCILZFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-496">Operación de galería de símbolos que se realizará si se supera la prueba de galería de símbolos CCW y se produce un error en la prueba z.</span><span class="sxs-lookup"><span data-stu-id="445e8-496">Stencil operation to perform if CCW stencil test passes and z-test fails.</span></span> <span data-ttu-id="445e8-497">Los valores son del [**tipo enumerado D3DSTENCISTONE.**](./d3dstencilop.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-497">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="445e8-498">El valor predeterminado es D3DSTENCI \_ KEEP.</span><span class="sxs-lookup"><span data-stu-id="445e8-498">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-499"><span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS \_ CCW \_ STENCILPASS**</span><span class="sxs-lookup"><span data-stu-id="445e8-499"><span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS\_CCW\_STENCILPASS**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-500">Operación de galería de símbolos que se va a realizar si se supera la galería de símbolos CCW y las pruebas z.</span><span class="sxs-lookup"><span data-stu-id="445e8-500">Stencil operation to perform if both CCW stencil and z-tests pass.</span></span> <span data-ttu-id="445e8-501">Los valores son del [**tipo enumerado D3DSTENCISTONE.**](./d3dstencilop.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-501">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="445e8-502">El valor predeterminado es D3DSTENCI \_ KEEP.</span><span class="sxs-lookup"><span data-stu-id="445e8-502">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-503"><span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS \_ CCW \_ STENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="445e8-503"><span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS\_CCW\_STENCILFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-504">Función de comparación.</span><span class="sxs-lookup"><span data-stu-id="445e8-504">The comparison function.</span></span> <span data-ttu-id="445e8-505">La prueba de galería de símbolos CCW pasa si la función de galería de símbolos ((ref & mask) (stencil & mask)) es **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="445e8-505">CCW stencil test passes if ((ref & mask) stencil function (stencil & mask)) is **TRUE**.</span></span> <span data-ttu-id="445e8-506">Los valores son del [**tipo enumerado D3DCMPFUNC.**](./d3dcmpfunc.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-506">Values are from the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="445e8-507">El valor predeterminado es D3DCMP \_ ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="445e8-507">The default value is D3DCMP\_ALWAYS.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-508"><span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS \_ COLORWRITEENABLE1**</span><span class="sxs-lookup"><span data-stu-id="445e8-508"><span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS\_COLORWRITEENABLE1**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-509">Valores adicionales de ColorWriteEnable para los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="445e8-509">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="445e8-510">Consulte D3DRS \_ COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="445e8-510">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="445e8-511">Esta funcionalidad está disponible si el bit de funcionalidades D3DPMISCCAPS INDEPENDENTWRITEMASKS se establece en el miembro PrimitiveMiscCaps de la estructura \_ [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="445e8-511">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="445e8-512">El valor predeterminado es 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="445e8-512">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-513"><span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS \_ COLORWRITEENABLE2**</span><span class="sxs-lookup"><span data-stu-id="445e8-513"><span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS\_COLORWRITEENABLE2**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-514">Valores adicionales de ColorWriteEnable para los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="445e8-514">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="445e8-515">Consulte D3DRS \_ COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="445e8-515">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="445e8-516">Esta funcionalidad está disponible si el bit de funcionalidades D3DPMISCCAPS INDEPENDENTWRITEMASKS se establece en el miembro PrimitiveMiscCaps de la estructura \_ [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="445e8-516">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="445e8-517">El valor predeterminado es 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="445e8-517">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-518"><span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS \_ COLORWRITEENABLE3**</span><span class="sxs-lookup"><span data-stu-id="445e8-518"><span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS\_COLORWRITEENABLE3**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-519">Valores adicionales de ColorWriteEnable para los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="445e8-519">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="445e8-520">Consulte D3DRS \_ COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="445e8-520">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="445e8-521">Esta funcionalidad está disponible si el bit de funcionalidades D3DPMISCCAPS INDEPENDENTWRITEMASKS se establece en el miembro PrimitiveMiscCaps de la estructura \_ [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="445e8-521">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="445e8-522">El valor predeterminado es 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="445e8-522">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-523"><span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS \_ BLENDFACTOR**</span><span class="sxs-lookup"><span data-stu-id="445e8-523"><span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS\_BLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-524">[**D3DCOLOR se**](d3dcolor.md) usa para un factor de mezcla constante durante la mezcla alfa.</span><span class="sxs-lookup"><span data-stu-id="445e8-524">[**D3DCOLOR**](d3dcolor.md) used for a constant blend-factor during alpha blending.</span></span> <span data-ttu-id="445e8-525">Esta funcionalidad está disponible si el bit de funcionalidades DE BLENDFACTOR D3DPBLENDCAPS se establece en el miembro \_ SrcBlendCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) o en el miembro DestBlendCaps de **D3DCAPS9.**</span><span class="sxs-lookup"><span data-stu-id="445e8-525">This functionality is available if the D3DPBLENDCAPS\_BLENDFACTOR capabilities bit is set in the SrcBlendCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) or the DestBlendCaps member of **D3DCAPS9**.</span></span> <span data-ttu-id="445e8-526">Vea [**D3DRENDERSTATETYPE.**]()</span><span class="sxs-lookup"><span data-stu-id="445e8-526">See [**D3DRENDERSTATETYPE**]().</span></span> <span data-ttu-id="445e8-527">El valor predeterminado es 0xffffffff.</span><span class="sxs-lookup"><span data-stu-id="445e8-527">The default value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-528"><span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS \_ SRGBWRITEENABLE**</span><span class="sxs-lookup"><span data-stu-id="445e8-528"><span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS\_SRGBWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-529">Habilite la corrección gamma de las escrituras de destino de representación en sRGB.</span><span class="sxs-lookup"><span data-stu-id="445e8-529">Enable render-target writes to be gamma corrected to sRGB.</span></span> <span data-ttu-id="445e8-530">El formato debe exponer D3DUSAGE \_ SRGBWRITE.</span><span class="sxs-lookup"><span data-stu-id="445e8-530">The format must expose D3DUSAGE\_SRGBWRITE.</span></span> <span data-ttu-id="445e8-531">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="445e8-531">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-532"><span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS \_ DEPTHBIAS**</span><span class="sxs-lookup"><span data-stu-id="445e8-532"><span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS\_DEPTHBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-533">Valor de punto flotante que se usa para la comparación de valores de profundidad.</span><span class="sxs-lookup"><span data-stu-id="445e8-533">A floating-point value that is used for comparison of depth values.</span></span> <span data-ttu-id="445e8-534">Consulte [Sesgo de profundidad (Direct3D 9).](depth-bias.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-534">See [Depth Bias (Direct3D 9)](depth-bias.md).</span></span> <span data-ttu-id="445e8-535">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="445e8-535">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-536"><span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS \_ WRAP8**</span><span class="sxs-lookup"><span data-stu-id="445e8-536"><span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS\_WRAP8**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-537">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="445e8-537">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-538"><span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS \_ WRAP9**</span><span class="sxs-lookup"><span data-stu-id="445e8-538"><span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS\_WRAP9**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-539">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="445e8-539">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-540"><span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS \_ WRAP10**</span><span class="sxs-lookup"><span data-stu-id="445e8-540"><span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS\_WRAP10**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-541">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="445e8-541">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-542"><span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS \_ WRAP11**</span><span class="sxs-lookup"><span data-stu-id="445e8-542"><span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS\_WRAP11**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-543">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="445e8-543">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-544"><span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS \_ WRAP12**</span><span class="sxs-lookup"><span data-stu-id="445e8-544"><span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS\_WRAP12**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-545">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="445e8-545">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-546"><span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS \_ WRAP13**</span><span class="sxs-lookup"><span data-stu-id="445e8-546"><span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS\_WRAP13**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-547">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="445e8-547">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-548"><span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS \_ WRAP14**</span><span class="sxs-lookup"><span data-stu-id="445e8-548"><span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS\_WRAP14**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-549">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="445e8-549">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-550"><span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS \_ WRAP15**</span><span class="sxs-lookup"><span data-stu-id="445e8-550"><span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS\_WRAP15**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-551">Consulte D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="445e8-551">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-552"><span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS \_ SEPARATEALPHABLENDENABLE**</span><span class="sxs-lookup"><span data-stu-id="445e8-552"><span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS\_SEPARATEALPHABLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-553">**TRUE** habilita el modo de mezcla independiente para el canal alfa.</span><span class="sxs-lookup"><span data-stu-id="445e8-553">**TRUE** enables the separate blend mode for the alpha channel.</span></span> <span data-ttu-id="445e8-554">El valor predeterminado es **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="445e8-554">The default value is **FALSE**.</span></span>

<span data-ttu-id="445e8-555">Cuando se establece en **FALSE**, los factores de combinación de destino de representación y las operaciones aplicadas a alfa se ven obligados a ser los mismos que los definidos para el color.</span><span class="sxs-lookup"><span data-stu-id="445e8-555">When set to **FALSE**, the render-target blending factors and operations applied to alpha are forced to be the same as those defined for color.</span></span> <span data-ttu-id="445e8-556">Este modo se establece de forma eficaz en **FALSE** en implementaciones que no establecen el límite D3DPMISCCAPS \_ SEPARATEALPHABLEND.</span><span class="sxs-lookup"><span data-stu-id="445e8-556">This mode is effectively hardwired to **FALSE** on implementations that don't set the cap D3DPMISCCAPS\_SEPARATEALPHABLEND.</span></span> <span data-ttu-id="445e8-557">Vea [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="445e8-557">See [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

<span data-ttu-id="445e8-558">El tipo de combinación alfa independiente viene determinado por los estados de representación D3DRS \_ SRCBLEPHA y D3DRS \_ DESTBLEPHA.</span><span class="sxs-lookup"><span data-stu-id="445e8-558">The type of separate alpha blending is determined by the D3DRS\_SRCBLENDALPHA and D3DRS\_DESTBLENDALPHA render states.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-559"><span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS \_ SRCBLEPHA**</span><span class="sxs-lookup"><span data-stu-id="445e8-559"><span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS\_SRCBLENDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-560">Un miembro del [**tipo enumerado D3DBLEND.**](./d3dblend.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-560">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="445e8-561">Este valor se omite a menos que D3DRS \_ SEPARATEALPHABLENDENABLE sea **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="445e8-561">This value is ignored unless D3DRS\_SEPARATEALPHABLENDENABLE is **TRUE**.</span></span> <span data-ttu-id="445e8-562">El valor predeterminado es D3DBLEND \_ ONE.</span><span class="sxs-lookup"><span data-stu-id="445e8-562">The default value is D3DBLEND\_ONE.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-563"><span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS \_ DESTBLEPHA**</span><span class="sxs-lookup"><span data-stu-id="445e8-563"><span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS\_DESTBLENDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-564">Un miembro del [**tipo enumerado D3DBLEND.**](./d3dblend.md)</span><span class="sxs-lookup"><span data-stu-id="445e8-564">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="445e8-565">Este valor se omite a menos que D3DRS \_ SEPARATEALPHABLENDENABLE sea **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="445e8-565">This value is ignored unless D3DRS\_SEPARATEALPHABLENDENABLE is **TRUE**.</span></span> <span data-ttu-id="445e8-566">El valor predeterminado es D3DBLEND \_ ZERO.</span><span class="sxs-lookup"><span data-stu-id="445e8-566">The default value is D3DBLEND\_ZERO.</span></span>

</dd> <dt>

<span data-ttu-id="445e8-567"><span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS \_ BLENDOPALPHA**</span><span class="sxs-lookup"><span data-stu-id="445e8-567"><span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS\_BLENDOPALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-568">Valor utilizado para seleccionar la operación aritmética aplicada a la combinación alfa independiente cuando el estado de representación, D3DRS \_ SEPARATEALPHABLENDENABLE, se establece en **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="445e8-568">Value used to select the arithmetic operation applied to separate alpha blending when the render state, D3DRS\_SEPARATEALPHABLENDENABLE, is set to **TRUE**.</span></span>

<span data-ttu-id="445e8-569">El tipo enumerado [**D3DBLENDOP**](./d3dblendop.md) define valores válidos.</span><span class="sxs-lookup"><span data-stu-id="445e8-569">Valid values are defined by the [**D3DBLENDOP**](./d3dblendop.md) enumerated type.</span></span> <span data-ttu-id="445e8-570">El valor predeterminado es D3DBLENDOP \_ ADD.</span><span class="sxs-lookup"><span data-stu-id="445e8-570">The default value is D3DBLENDOP\_ADD.</span></span>

<span data-ttu-id="445e8-571">Si no se admite la funcionalidad del dispositivo BLENDOP D3DPMISCCAPS, \_ se realiza D3DBLENDOP \_ ADD.</span><span class="sxs-lookup"><span data-stu-id="445e8-571">If the D3DPMISCCAPS\_BLENDOP device capability is not supported, then D3DBLENDOP\_ADD is performed.</span></span> <span data-ttu-id="445e8-572">Vea [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="445e8-572">See [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

</dd> <dt>

<span data-ttu-id="445e8-573"><span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS \_ FORCE \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="445e8-573"><span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="445e8-574">Fuerza esta enumeración a compilar hasta 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="445e8-574">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="445e8-575">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara con un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="445e8-575">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="445e8-576">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="445e8-576">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="445e8-577">Comentarios</span><span class="sxs-lookup"><span data-stu-id="445e8-577">Remarks</span></span>



| <span data-ttu-id="445e8-578">Estados de representación</span><span class="sxs-lookup"><span data-stu-id="445e8-578">Render states</span></span>        |   <span data-ttu-id="445e8-579">Muestreador de textura</span><span class="sxs-lookup"><span data-stu-id="445e8-579">Texture sampler</span></span>                 |
|----------------------|--------------------|
| <span data-ttu-id="445e8-580">ps \_ 1 \_ 1 to ps \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="445e8-580">ps\_1\_1 to ps\_1\_3</span></span> | <span data-ttu-id="445e8-581">4 muestreadores de textura</span><span class="sxs-lookup"><span data-stu-id="445e8-581">4 texture samplers</span></span> |



 

<span data-ttu-id="445e8-582">Direct3D define la constante D3DRENDERSTATE WRAPBIAS como comodidad para que las aplicaciones habiliten o deshabiliten el ajuste de textura, en función del entero de base cero de un conjunto de coordenadas de textura (en lugar de usar explícitamente uno de los valores de estado \_ D3DRS \_ WRAP n).</span><span class="sxs-lookup"><span data-stu-id="445e8-582">Direct3D defines the D3DRENDERSTATE\_WRAPBIAS constant as a convenience for applications to enable or disable texture wrapping, based on the zero-based integer of a texture coordinate set (rather than explicitly using one of the D3DRS\_WRAP n state values).</span></span> <span data-ttu-id="445e8-583">Agregue el valor D3DRENDERSTATE WRAPBIAS al índice de base cero de un conjunto de coordenadas de textura para calcular el valor D3DRS WRAP n que corresponde a ese índice, como se muestra en el \_ \_ ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="445e8-583">Add the D3DRENDERSTATE\_WRAPBIAS value to the zero-based index of a texture coordinate set to calculate the D3DRS\_WRAP n value that corresponds to that index, as shown in the following example.</span></span>


```
// Enable U/V wrapping for textures that use the texture 
// coordinate set at the index within the dwIndex variable
    
HRESULT hr = pd3dDevice->SetRenderState(
dwIndex + D3DRENDERSTATE_WRAPBIAS,  
D3DWRAPCOORD_0 | D3DWRAPCOORD_1);
     
// If dwIndex is 3, the value that results from 
// the addition equals D3DRS_WRAP3 (131)
```



## <a name="requirements"></a><span data-ttu-id="445e8-584">Requisitos</span><span class="sxs-lookup"><span data-stu-id="445e8-584">Requirements</span></span>



| <span data-ttu-id="445e8-585">Requisito</span><span class="sxs-lookup"><span data-stu-id="445e8-585">Requirement</span></span> | <span data-ttu-id="445e8-586">Value</span><span class="sxs-lookup"><span data-stu-id="445e8-586">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="445e8-587">Encabezado</span><span class="sxs-lookup"><span data-stu-id="445e8-587">Header</span></span><br/> | <dl> <span data-ttu-id="445e8-588"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="445e8-588"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="445e8-589">Vea también</span><span class="sxs-lookup"><span data-stu-id="445e8-589">See also</span></span>

<dl> <dt>

[<span data-ttu-id="445e8-590">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="445e8-590">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="445e8-591">**IDirect3DDevice9::GetRenderState**</span><span class="sxs-lookup"><span data-stu-id="445e8-591">**IDirect3DDevice9::GetRenderState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrenderstate)
</dt> <dt>

[<span data-ttu-id="445e8-592">**IDirect3DDevice9::SetRenderState**</span><span class="sxs-lookup"><span data-stu-id="445e8-592">**IDirect3DDevice9::SetRenderState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)
</dt> </dl>

 

 
