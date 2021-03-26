---
title: Cambios de código de bytes en SM 5.1
description: SM 5.1 cambia el modo en que se declaran y se hace referencia a los registros de recursos en las instrucciones.
ms.assetid: ABECF705-67B8-4419-8D18-74B43B9DC3AF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d66db788b0012a1c3221e37d4c2dd4e41566c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357800"
---
# <a name="bytecode-changes-in-sm51"></a><span data-ttu-id="a5e98-103">Cambios de código de bytes en SM 5.1</span><span class="sxs-lookup"><span data-stu-id="a5e98-103">Bytecode changes in SM5.1</span></span>

<span data-ttu-id="a5e98-104">SM 5.1 cambia el modo en que se declaran y se hace referencia a los registros de recursos en las instrucciones.</span><span class="sxs-lookup"><span data-stu-id="a5e98-104">SM5.1 changes how resource registers are declared and referenced in instructions.</span></span>

<span data-ttu-id="a5e98-105">SM 5.1 pasa a declarar una "variable" de registro, de forma similar a como se hace para los registros de memoria compartida del grupo, que se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a5e98-105">SM5.1 moves towards declaring a register “variable”, similar to how it is done for group shared memory registers, illustrated by the following example:</span></span>

``` syntax
Texture2D<float4> tex0          : register(t5,  space0);
Texture2D<float4> tex1[][5][3]  : register(t10, space0);
Texture2D<float4> tex2[8]       : register(t0,  space1);
SamplerState samp0              : register(s5, space0);

float4 main(float4 coord : COORD) : SV_TARGET
{
    float4 r = coord;
    r += tex0.Sample(samp0, r.xy);
    r += tex2[r.x].Sample(samp0, r.xy);
    r += tex1[r.x][r.y][r.z].Sample(samp0, r.xy);
    return r;
}
```

<span data-ttu-id="a5e98-106">A continuación se muestra el desensamblado de este ejemplo:</span><span class="sxs-lookup"><span data-stu-id="a5e98-106">The disassembly of this example follows:</span></span>

``` syntax
// Resource Bindings:
//
// Name                                 Type  Format         Dim Space Slot  Elements
// ------------------------------ ---------- ------- ----------- ----- ---- ---------
// samp0                             sampler      NA          NA     0    5         1
// tex0                              texture  float4          2d     0    5         1
// tex1[0][5][3]                     texture  float4          2d     0   10 unbounded
// tex2[8]                           texture  float4          2d     1    0         8
//
//
//
// Input signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// COORD                    0   xyzw        0     NONE   float   xyzw
//
//
// Output signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// SV_TARGET                0   xyzw        0   TARGET   float   xyzw
//
ps_5_1
dcl_globalFlags refactoringAllowed
dcl_sampler s0[5:5], mode_default, space=0
dcl_resource_texture2d (float,float,float,float) t0[5:5], space=0
dcl_resource_texture2d (float,float,float,float) t1[10:*], space=0
dcl_resource_texture2d (float,float,float,float) t2[0:7], space=1
dcl_input_ps linear v0.xyzw
dcl_output o0.xyzw
dcl_temps 2
sample r0.xyzw, v0.xyxx, t0[0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, v0.xyzw
ftou r1.x, r0.x
sample r1.xyzw, r0.xyxx, t2[r1.x + 0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, r1.xyzw
ftou r1.xyz, r0.zyxz
imul null, r1.yz, r1.zzyz, l(0, 15, 3, 0)
iadd r1.y, r1.z, r1.y
iadd r1.x, r1.x, r1.y
sample r1.xyzw, r0.xyxx, t1[r1.x + 10].xyzw, s0[5]
add o0.xyzw, r0.xyzw, r1.xyzw
ret
// Approximately 12 instruction slots used
```

<span data-ttu-id="a5e98-107">Ahora cada intervalo de recursos del sombreador tiene un identificador (un nombre) en el código de bytes del sombreador.</span><span class="sxs-lookup"><span data-stu-id="a5e98-107">Each shader resource range now has an ID (a name) in the shader bytecode.</span></span> <span data-ttu-id="a5e98-108">Por ejemplo, la matriz de texturas de Tex1 se convierte en ' t 1 ' en el código de bytes del sombreador.</span><span class="sxs-lookup"><span data-stu-id="a5e98-108">For example, tex1 texture array becomes ‘t1’ in the shader byte code.</span></span> <span data-ttu-id="a5e98-109">Asignar identificadores únicos a cada intervalo de recursos permite dos cosas:</span><span class="sxs-lookup"><span data-stu-id="a5e98-109">Giving unique IDs to each resource range allows two things:</span></span>

-   <span data-ttu-id="a5e98-110">Identifique de forma inequívoca qué intervalo de recursos (consulte DCL \_ Resource \_ texture2d) se está indizando en una instrucción (vea la instrucción de ejemplo).</span><span class="sxs-lookup"><span data-stu-id="a5e98-110">Unambiguously identify which resource range (see dcl\_resource\_texture2d) is being indexed in an instruction (see sample instruction).</span></span>
-   <span data-ttu-id="a5e98-111">Adjunte un conjunto de atributos a la declaración, por ejemplo, tipo de elemento, tamaño de intervalo, modo de operación de trama, etc.</span><span class="sxs-lookup"><span data-stu-id="a5e98-111">Attach set of attributes to the declaration, e.g., element type, stride size, raster operation mode, etc..</span></span>

<span data-ttu-id="a5e98-112">Tenga en cuenta que el identificador del intervalo no está relacionado con la declaración de límite inferior de HLSL.</span><span class="sxs-lookup"><span data-stu-id="a5e98-112">Note that the ID of the range is not related to the HLSL lower bound declaration.</span></span>

<span data-ttu-id="a5e98-113">El orden de los enlaces de recursos de reflexión y las instrucciones de declaración del sombreador es el mismo para ayudar a identificar la correspondencia entre las variables de HLSL y los ID. de código de bytes.</span><span class="sxs-lookup"><span data-stu-id="a5e98-113">The order of reflection resource bindings and shader declaration instructions is the same to aid in identifying the correspondence between HLSL variables and bytecode IDs.</span></span>

<span data-ttu-id="a5e98-114">Cada instrucción de declaración en SM 5.1 usa un operando 3D para definir: ID. de intervalo, límites inferior y superior.</span><span class="sxs-lookup"><span data-stu-id="a5e98-114">Each declaration instruction in SM5.1 uses a 3D operand to define: range ID, lower and upper bounds.</span></span> <span data-ttu-id="a5e98-115">Se emite un token adicional para especificar el espacio de registro.</span><span class="sxs-lookup"><span data-stu-id="a5e98-115">An additional token is emitted to specify the register space.</span></span> <span data-ttu-id="a5e98-116">También se pueden emitir otros tokens para transmitir propiedades adicionales del intervalo; por ejemplo, CBuffer o la instrucción de declaración de búfer estructurado emite el tamaño de la CBuffer o la estructura.</span><span class="sxs-lookup"><span data-stu-id="a5e98-116">Other tokens may be emitted as well to convey additional properties of the range, e.g., cbuffer or structured buffer declaration instruction emits the size of the cbuffer or structure.</span></span> <span data-ttu-id="a5e98-117">Los detalles exactos de la codificación se pueden encontrar en d3d12TokenizedProgramFormat. h y D3D10ShaderBinary:: CShaderCodeParser.</span><span class="sxs-lookup"><span data-stu-id="a5e98-117">The exact details of encoding can be found in d3d12TokenizedProgramFormat.h and D3D10ShaderBinary::CShaderCodeParser.</span></span>

<span data-ttu-id="a5e98-118">Las instrucciones de SM 5.1 no emitirán información adicional del operando de recursos como parte de la instrucción (como en SM 5.0).</span><span class="sxs-lookup"><span data-stu-id="a5e98-118">SM5.1 instructions will not emit additional resource operand information as part of the instruction (as in SM5.0).</span></span> <span data-ttu-id="a5e98-119">Esta información se mueve ahora a las instrucciones de declaración.</span><span class="sxs-lookup"><span data-stu-id="a5e98-119">This information is now moved to the declaration instructions.</span></span> <span data-ttu-id="a5e98-120">En SM 5.0, instrucciones que indexan los recursos de recursos necesarios para describirse en tokens de código de operación extendidos, ya que la indización ofuscaba la asociación con la declaración.</span><span class="sxs-lookup"><span data-stu-id="a5e98-120">In SM5.0, instructions indexing resources required resource attributes to be described in extended opcode tokens, since indexing obfuscated the association to the declaration.</span></span> <span data-ttu-id="a5e98-121">En SM 5.1, cada identificador (por ejemplo, ' t 1 ') está asociado de forma no ambigua a una única declaración que describe la información de recursos necesaria.</span><span class="sxs-lookup"><span data-stu-id="a5e98-121">In SM5.1 each ID (such as ‘t1’) is unambiguously associated with a single declaration that describes the required resource information.</span></span> <span data-ttu-id="a5e98-122">Por lo tanto, los tokens de código de operación extendidos usados en las instrucciones para describir la información de recursos ya no se emiten.</span><span class="sxs-lookup"><span data-stu-id="a5e98-122">Therefore, the extended opcode tokens used on instructions to describe resource information are no longer emitted.</span></span>

<span data-ttu-id="a5e98-123">En las instrucciones que no son de declaración, un operando de recursos para muestreadores, SRVs y UAVs es un operando 2D.</span><span class="sxs-lookup"><span data-stu-id="a5e98-123">In non-declaration instructions, a resource operand for samplers, SRVs, and UAVs is a 2D operand.</span></span> <span data-ttu-id="a5e98-124">El primer índice es una constante literal que especifica el identificador del intervalo.</span><span class="sxs-lookup"><span data-stu-id="a5e98-124">The first index is a literal constant that specifies the range ID.</span></span> <span data-ttu-id="a5e98-125">El segundo índice representa el valor de linealización del índice.</span><span class="sxs-lookup"><span data-stu-id="a5e98-125">The second index represents the linearized value of the index.</span></span> <span data-ttu-id="a5e98-126">El valor se calcula en relación con el principio del espacio de registro correspondiente (no con respecto al principio del intervalo lógico) para correlacionar mejor con la firma raíz y reducir la carga del compilador de controladores para ajustar el índice.</span><span class="sxs-lookup"><span data-stu-id="a5e98-126">The value is computed relative to the beginning of the corresponding register space (not relative to the beginning of the logical range) to better correlate with the root signature and to reduce the driver compiler burden of adjusting the index.</span></span>

<span data-ttu-id="a5e98-127">Un operando de recurso para CBVs es un operando 3D: el identificador literal del intervalo, el índice del CBuffer, el desplazamiento en la instancia concreta de CBuffer.</span><span class="sxs-lookup"><span data-stu-id="a5e98-127">A resource operand for CBVs is a 3D operand: literal ID of the range, index of the cbuffer, offset into the particular instance of cbuffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5e98-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a5e98-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5e98-129">Características del modelo de sombreador de HLSL 5,1 para Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="a5e98-129">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="a5e98-130">Modelo de sombreador 5,1</span><span class="sxs-lookup"><span data-stu-id="a5e98-130">Shader Model 5.1</span></span>](shader-model-5-1.md)
</dt> </dl>

 

 




