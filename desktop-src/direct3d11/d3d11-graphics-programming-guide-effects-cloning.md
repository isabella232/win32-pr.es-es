---
title: Clonar un efecto
description: La clonación de un efecto crea una segunda copia prácticamente idéntica del efecto.
ms.assetid: e3870363-5ee8-4fdc-a489-cdaeef8c9c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68607d3cc9f00a346fcfa65c255f3caa51dea384
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777239"
---
# <a name="cloning-an-effect"></a><span data-ttu-id="0b35e-103">Clonar un efecto</span><span class="sxs-lookup"><span data-stu-id="0b35e-103">Cloning an Effect</span></span>

<span data-ttu-id="0b35e-104">La clonación de un efecto crea una segunda copia prácticamente idéntica del efecto.</span><span class="sxs-lookup"><span data-stu-id="0b35e-104">Cloning an effect creates a second, almost identical copy of the effect.</span></span> <span data-ttu-id="0b35e-105">Vea el siguiente calificador único para obtener una explicación de por qué no es exacta.</span><span class="sxs-lookup"><span data-stu-id="0b35e-105">See the following single qualifier for an explanation of why it is not exact.</span></span> <span data-ttu-id="0b35e-106">Una segunda copia de un efecto es útil cuando se desea usar el marco de trabajo de efectos en varios subprocesos, ya que el tiempo de ejecución del efecto no es seguro para subprocesos para mantener un alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="0b35e-106">A second copy of an effect is useful when one wants to use the effects framework on multiple threads, since the effect runtime is not thread safe to maintain high performance.</span></span>

<span data-ttu-id="0b35e-107">Dado que los contextos de dispositivo también son no seguros para subprocesos, los distintos subprocesos deben pasar distintos contextos de dispositivo al método ID3DX11EffectPass:: Apply.</span><span class="sxs-lookup"><span data-stu-id="0b35e-107">Since device contexts are also non-thread-safe, different threads should pass different device contexts to the ID3DX11EffectPass::Apply method.</span></span>

<span data-ttu-id="0b35e-108">Un efecto se puede clonar con la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="0b35e-108">An effect can be cloned with the following syntax:</span></span>


```
ID3DX11Effect* pClonedEffect = NULL;
UINT Flags = D3DX11_EFFECT_CLONE_FORCE_NONSINGLE;
HRESULT hr = pEffect->CloneEffect( Flags, &pClonedEffect );
```



<span data-ttu-id="0b35e-109">En el ejemplo anterior, la copia clonada encapsulará el mismo estado que el efecto original, independientemente del estado en el que se encuentra el efecto original.</span><span class="sxs-lookup"><span data-stu-id="0b35e-109">In the above example, the cloned copy will encapsulate the same state as the original effect, regardless of what state the original effect is in.</span></span> <span data-ttu-id="0b35e-110">En concreto:</span><span class="sxs-lookup"><span data-stu-id="0b35e-110">In particular:</span></span>

1.  <span data-ttu-id="0b35e-111">Si pEffect está optimizado, se optimiza el efecto pCloned</span><span class="sxs-lookup"><span data-stu-id="0b35e-111">If pEffect is optimized, pCloned Effect is optimized</span></span>
2.  <span data-ttu-id="0b35e-112">Si pEffect tiene algunas variables administradas por el usuario, el efecto pCloned tendrá las mismas variables administradas por el usuario (vea la descripción única a continuación).</span><span class="sxs-lookup"><span data-stu-id="0b35e-112">If pEffect has some user-managed variables, pCloned Effect will have the same user-managed variables (see the single description below)</span></span>
3.  <span data-ttu-id="0b35e-113">Todas las actualizaciones de variables pendientes (hasta que se aplique una llamada a aplicar actualiza el estado del dispositivo) en pEffect estarán pendientes en pClonedEffect</span><span class="sxs-lookup"><span data-stu-id="0b35e-113">Any pending variable updates (until an Apply call updates device state) in pEffect will be pending in pClonedEffect</span></span>

<span data-ttu-id="0b35e-114">Los siguientes objetos de dispositivo de Direct3D 11 son inmutables o nunca actualizados por el marco de trabajo de Effects, por lo que el efecto clonado apuntará a los mismos objetos que el efecto original:</span><span class="sxs-lookup"><span data-stu-id="0b35e-114">The following Direct3D 11 device objects are immutable or never updated by the effects framework, so the cloned effect will point to the same objects as the original effect:</span></span>

1.  <span data-ttu-id="0b35e-115">Objetos de bloque de estado (ID3D11BlendState, ID3D11RasterizerState, ID3D11DepthStencilState, ID3D11SamplerState)</span><span class="sxs-lookup"><span data-stu-id="0b35e-115">State block objects (ID3D11BlendState, ID3D11RasterizerState, ID3D11DepthStencilState, ID3D11SamplerState)</span></span>
2.  <span data-ttu-id="0b35e-116">Sombreadores</span><span class="sxs-lookup"><span data-stu-id="0b35e-116">Shaders</span></span>
3.  <span data-ttu-id="0b35e-117">Instancias de clase</span><span class="sxs-lookup"><span data-stu-id="0b35e-117">Class instances</span></span>
4.  <span data-ttu-id="0b35e-118">Texturas (sin incluir los búferes de textura)</span><span class="sxs-lookup"><span data-stu-id="0b35e-118">Textures (not including texture buffers)</span></span>
5.  <span data-ttu-id="0b35e-119">Vistas de acceso desordenado</span><span class="sxs-lookup"><span data-stu-id="0b35e-119">Unordered access views</span></span>

<span data-ttu-id="0b35e-120">Los siguientes objetos de dispositivo de Direct3D 11 son inmutables y modificados por el tiempo de ejecución del efecto (a menos que sea administrado por el usuario o único en un efecto clonado). las nuevas copias de estos objetos se crean cuando no es Single:</span><span class="sxs-lookup"><span data-stu-id="0b35e-120">The following Direct3D 11 device objects are both immutable and modified by the effect runtime (unless user-managed or single in a cloned effect); new copies of these objects are created when non-single:</span></span>

1.  <span data-ttu-id="0b35e-121">Búferes de constantes</span><span class="sxs-lookup"><span data-stu-id="0b35e-121">Constant buffers</span></span>
2.  <span data-ttu-id="0b35e-122">Búferes de textura</span><span class="sxs-lookup"><span data-stu-id="0b35e-122">Texture Buffers</span></span>

## <a name="single-constant-buffers-and-texture-buffers"></a><span data-ttu-id="0b35e-123">Búferes de una sola constante y búferes de textura</span><span class="sxs-lookup"><span data-stu-id="0b35e-123">Single Constant Buffers and Texture Buffers</span></span>

<span data-ttu-id="0b35e-124">Tenga en cuenta que este debate se aplica tanto a los búferes de constantes como a las texturas, pero se supone que los búferes de constantes se pueden leer fácilmente.</span><span class="sxs-lookup"><span data-stu-id="0b35e-124">Note that this discussion applies to both constant buffers and textures, but constant buffers are assumed for ease of reading.</span></span>

<span data-ttu-id="0b35e-125">Puede haber casos en los que un búfer de constantes solo se actualice en un subproceso, pero el estado del dispositivo establecido por efectos clonados usará estos datos.</span><span class="sxs-lookup"><span data-stu-id="0b35e-125">There may be cases where a constant buffer is only updated by one thread, but device state set by cloned effects will use this data.</span></span> <span data-ttu-id="0b35e-126">Por ejemplo, el efecto principal puede actualizar el mundo y ver las matrices a las que se hace referencia desde los sombreadores en efectos clonados que no cambian el mundo y ven matrices.</span><span class="sxs-lookup"><span data-stu-id="0b35e-126">For example, the main effect may update the world and view matrices which are referenced from shaders in cloned effects which do not change the world and view matrices.</span></span> <span data-ttu-id="0b35e-127">En estos casos, los efectos clonados deben hacer referencia al búfer de constantes actual en lugar de volver a crear uno.</span><span class="sxs-lookup"><span data-stu-id="0b35e-127">In these cases, the cloned effects need to reference the current constant buffer instead of recreating one.</span></span>

<span data-ttu-id="0b35e-128">Hay dos maneras de lograr este resultado deseado:</span><span class="sxs-lookup"><span data-stu-id="0b35e-128">There are two ways to achieve this desired result:</span></span>

1.  <span data-ttu-id="0b35e-129">Use ID3DX11EffectConstantBuffer:: SetConstantBuffer en el efecto clonado para que sea administrado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="0b35e-129">Use ID3DX11EffectConstantBuffer::SetConstantBuffer on the cloned effect to make it user-managed</span></span>
2.  <span data-ttu-id="0b35e-130">Marcar el búfer de constantes como "único" en el código HLSL, forzando al tiempo de ejecución de efecto a tratar es como administrado por el usuario después de la clonación</span><span class="sxs-lookup"><span data-stu-id="0b35e-130">Mark the constant buffer as "single" in the HLSL code, forcing the effect runtime to treat is as user-managed after cloning</span></span>

<span data-ttu-id="0b35e-131">Hay dos diferencias entre los dos métodos anteriores.</span><span class="sxs-lookup"><span data-stu-id="0b35e-131">There are two differences between the two methods above.</span></span> <span data-ttu-id="0b35e-132">En primer lugar, en el método 1 se creará un nuevo ID3D11Buffer y se llamará al usuario antes de SetConstantBuffer.</span><span class="sxs-lookup"><span data-stu-id="0b35e-132">First, in method 1, a new ID3D11Buffer will be created and user before SetConstantBuffer is called.</span></span> <span data-ttu-id="0b35e-133">Además, después de llamar a UndoSetConstantBuffer en el efecto clonado, la variable del método 1will apunta al búfer recién creado (que los efectos actualizarán al aplicarse) mientras que la variable del método 2 continuará señalando al búfer original (no se actualizará en la aplicación).</span><span class="sxs-lookup"><span data-stu-id="0b35e-133">Also, after calling UndoSetConstantBuffer in the cloned effect, the variable in method 1will point to the newly-created buffer (which effects will update on Apply) while the variable in method 2 will continue to point to the original buffer (not updating it on Apply).</span></span>

<span data-ttu-id="0b35e-134">Vea el ejemplo siguiente en HLSL:</span><span class="sxs-lookup"><span data-stu-id="0b35e-134">See the following example in HLSL:</span></span>


```
cbuffer ObjectData
{
    float4 Position;
};
single cbuffer ViewData
{
    float4x4 ViewMatrix;
};
```



<span data-ttu-id="0b35e-135">Durante la clonación, el efecto clonado creará un nuevo ID3D11Buffer para ObjectData y rellenará su contenido en Apply, pero hará referencia al ID3D11Buffer original para ViewData.</span><span class="sxs-lookup"><span data-stu-id="0b35e-135">While cloning, the cloned effect will create a new ID3D11Buffer for ObjectData, and fill its contents on Apply, but reference the original ID3D11Buffer for ViewData.</span></span> <span data-ttu-id="0b35e-136">El calificador único se puede pasar por alto en el proceso de clonación estableciendo la marca de la \_ fuerza de clonación del efecto de D3DX11 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0b35e-136">The single qualifier can be ignored in the cloning process by setting the D3DX11\_EFFECT\_CLONE\_FORCE\_NONSINGLE flag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b35e-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0b35e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b35e-138">Efectos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="0b35e-138">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




