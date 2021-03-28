---
title: Interfaces y clases en efectos
description: Hay muchas maneras de usar clases e interfaces en los efectos 11.
ms.assetid: 526d477b-fc1f-4bd0-a620-ce9b78147f68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b067b8e03b2d43ea44ccab6164424cbc84c7237
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420918"
---
# <a name="interfaces-and-classes-in-effects"></a><span data-ttu-id="7128b-103">Interfaces y clases en efectos</span><span class="sxs-lookup"><span data-stu-id="7128b-103">Interfaces and Classes in Effects</span></span>

<span data-ttu-id="7128b-104">Hay muchas maneras de usar clases e interfaces en los efectos 11.</span><span class="sxs-lookup"><span data-stu-id="7128b-104">There are many ways to use classes and interfaces in Effects 11.</span></span> <span data-ttu-id="7128b-105">Para ver la sintaxis de la interfaz y la clase, consulte [interfaces y clases](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span><span class="sxs-lookup"><span data-stu-id="7128b-105">For interface and class syntax, see [Interfaces and Classes](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span></span>

<span data-ttu-id="7128b-106">En las secciones siguientes se detalla cómo especificar instancias de clase en un sombreador que usa interfaces.</span><span class="sxs-lookup"><span data-stu-id="7128b-106">The following sections detail how to specify class instances to a shader which uses interfaces.</span></span> <span data-ttu-id="7128b-107">Usaremos la interfaz y las clases siguientes en los ejemplos:</span><span class="sxs-lookup"><span data-stu-id="7128b-107">We will use the following interface and classes in the examples:</span></span>


```
interface IColor
{
  float4 GetColor();
};

class CRed : IColor
{
  float4 GetColor() { return float4(1,0,0,1); }
};
class CGreen : IColor
{
  float4 GetColor() { return float4(0,1,0,1); }
};

CRed pRed;
CGreen pGreen;
IColor pIColor;
IColor pIColor2 = pRed;
```



<span data-ttu-id="7128b-108">Tenga en cuenta que las instancias de la interfaz se pueden inicializar en instancias de clase.</span><span class="sxs-lookup"><span data-stu-id="7128b-108">Note that interface instances can be initialized to class instances.</span></span> <span data-ttu-id="7128b-109">También se admiten matrices de instancias de clase e interfaz y se pueden inicializar como en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="7128b-109">Arrays of class and interface instances are also supported and they can be initialized as in the following example:</span></span>


```
CRed pRedArray[2];
IColor pIColor3 = pRedArray[1];
IColor pIColorArray[2] = {pRed, pGreen};
IColor pIColorArray2[2] = pRedArray;
```



## <a name="uniform-interface-parameters"></a><span data-ttu-id="7128b-110">Parámetros de interfaz uniformes</span><span class="sxs-lookup"><span data-stu-id="7128b-110">Uniform Interface Parameters</span></span>

<span data-ttu-id="7128b-111">Al igual que otros tipos de datos uniformes, se deben especificar parámetros de interfaz uniformes en la llamada a CompileShader.</span><span class="sxs-lookup"><span data-stu-id="7128b-111">Just like other uniform data types, uniform interface parameters must be specified in the CompileShader call.</span></span> <span data-ttu-id="7128b-112">Los parámetros de interfaz pueden asignarse a instancias de la interfaz global o a instancias de clase globales.</span><span class="sxs-lookup"><span data-stu-id="7128b-112">Interface parameters can be assigned to global interface instances or global class instances.</span></span> <span data-ttu-id="7128b-113">Cuando se asigna a una instancia de interfaz global, el sombreador tendrá una dependencia en la instancia de la interfaz, lo que significa que debe establecerse en una instancia de clase.</span><span class="sxs-lookup"><span data-stu-id="7128b-113">When assigned to a global interface instance, the shader will have a dependency on the interface instance, which means that it must be set to a class instance.</span></span> <span data-ttu-id="7128b-114">Cuando se asigna a instancias de clase global, el compilador especializa el sombreador (como con otros tipos de datos uniformes) para usar esa clase.</span><span class="sxs-lookup"><span data-stu-id="7128b-114">When assigned to global class instances, the compiler specializes the shader (as with other uniform data types) to use that class.</span></span> <span data-ttu-id="7128b-115">Esto es importante para dos escenarios:</span><span class="sxs-lookup"><span data-stu-id="7128b-115">This is important for two scenarios:</span></span>

1.  <span data-ttu-id="7128b-116">Los sombreadores con un \_ destino de 4 x pueden usar parámetros de interfaz si estos parámetros son uniformes y se asignan a instancias de clase global (por lo que no se usa ninguna vinculación dinámica).</span><span class="sxs-lookup"><span data-stu-id="7128b-116">Shaders with a 4\_x target can use interface parameters if these parameters are uniform and assigned to global class instances (so no dynamic linkage is used).</span></span>
2.  <span data-ttu-id="7128b-117">Los usuarios pueden decidir tener muchos sombreadores especializados y compilados sin vinculación dinámica o pocos sombreadores compilados con vinculación dinámica.</span><span class="sxs-lookup"><span data-stu-id="7128b-117">Users can decide to have many compiled, specialized shaders with no dynamic linkage or few compiled shaders with dynamic linkage.</span></span>


```
float4 PSUniform( uniform IColor color ) : SV_Target
{
  return color;
}

technique11
{
  pass
  {
    SetPixelShader( CompileShader( ps_4_0, PSUniform(pRed) ) );
  }
  pass
  {
    SetPixelShader( CompileShader( ps_5_0, PSUniform(pIColor2) ) );
  }
}
```



<span data-ttu-id="7128b-118">Si pIColor2 permanece sin cambios a través de la API, las dos pasadas anteriores son funcionalmente equivalentes, pero la primera usa un \_ \_ sombreador estático de PS 4 0 mientras que la segunda usa un \_ \_ sombreador de PS 5 0 con vinculación dinámica.</span><span class="sxs-lookup"><span data-stu-id="7128b-118">If pIColor2 remains unchanged through the API, then the previous two passes are functionally equivalent, but the first uses a ps\_4\_0 static shader while the second uses a ps\_5\_0 shader with dynamic linkage.</span></span> <span data-ttu-id="7128b-119">Si pIColor2 se cambia a través de la API de efectos (consulte Configuración de instancias de clase a continuación), el comportamiento del sombreador de píxeles en el segundo paso puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="7128b-119">If pIColor2 is changed through the effects API (see Setting Class Instances below), then the behavior of the pixel shader in the second pass may change.</span></span>

## <a name="non-uniform-interface-parameters"></a><span data-ttu-id="7128b-120">Parámetros de interfaz no uniformes</span><span class="sxs-lookup"><span data-stu-id="7128b-120">Non-Uniform Interface Parameters</span></span>

<span data-ttu-id="7128b-121">Los parámetros de interfaz no uniformes crean dependencias de interfaz para los sombreadores.</span><span class="sxs-lookup"><span data-stu-id="7128b-121">Non-uniform interface parameters create interface dependencies for the shaders.</span></span> <span data-ttu-id="7128b-122">Al aplicar un sombreador con parámetros de interfaz, estos parámetros se deben asignar en con la llamada a BindInterfaces.</span><span class="sxs-lookup"><span data-stu-id="7128b-122">When applying a shader with interface parameters, these parameters must be assigned in with the BindInterfaces call.</span></span> <span data-ttu-id="7128b-123">Las instancias de la interfaz global y las instancias de clases globales se pueden especificar en la llamada a BindInterfaces.</span><span class="sxs-lookup"><span data-stu-id="7128b-123">Global interface instances and global class instances can be specified in the BindInterfaces call.</span></span>


```
float4 PSAbstract( IColor color ) : SV_Target
{
  return color;
}

PixelShader pPSAbstract = CompileShader( ps_5_0, PSAbstract(pRed) );

technique11
{
  pass
  {
    SetPixelShader( BindInterfaces( pPSAbstract, pRed ) );
  }
  pass
  {
    SetPixelShader( BindInterfaces( pPSAbstract, pIColor2 ) );
  }
}
```



<span data-ttu-id="7128b-124">Si pIColor2 permanece inalterado a través de la API, las dos pasadas anteriores son funcionalmente equivalentes y usan la vinculación dinámica.</span><span class="sxs-lookup"><span data-stu-id="7128b-124">If pIColor2 remains unchanged through the API, then the previous two passes are functionally equivalent and both use dynamic linkage.</span></span> <span data-ttu-id="7128b-125">Si pIColor2 se cambia a través de la API de efectos (consulte Configuración de instancias de clase a continuación), el comportamiento del sombreador de píxeles en el segundo paso puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="7128b-125">If pIColor2 is changed through the effects API (see Setting Class Instances below), then the behavior of the pixel shader in the second pass may change.</span></span>

## <a name="setting-class-instances"></a><span data-ttu-id="7128b-126">Establecer instancias de clase</span><span class="sxs-lookup"><span data-stu-id="7128b-126">Setting Class Instances</span></span>

<span data-ttu-id="7128b-127">Al establecer un sombreador con vinculación dinámica del sombreador al dispositivo de Direct3D 11, también deben especificarse las instancias de clase.</span><span class="sxs-lookup"><span data-stu-id="7128b-127">When setting a shader with dynamic shader linkage to the Direct3D 11 device, class instances must also be specified.</span></span> <span data-ttu-id="7128b-128">Es un error establecer este tipo de sombreador con una instancia de clase **null** .</span><span class="sxs-lookup"><span data-stu-id="7128b-128">It is an error to set such a shader with a **NULL** class instance.</span></span> <span data-ttu-id="7128b-129">Por lo tanto, todas las instancias de interfaz a las que hace referencia un sombreador deben tener una instancia de clase asociada.</span><span class="sxs-lookup"><span data-stu-id="7128b-129">Therefore, all interface instances which a shader references must have an associated class instance.</span></span>

<span data-ttu-id="7128b-130">En el ejemplo siguiente se muestra cómo obtener una variable de instancia de clase de un efecto y establecerla en una variable de interfaz:</span><span class="sxs-lookup"><span data-stu-id="7128b-130">The following example shows how to get a class instance variable from an effect and set it to an interface variable:</span></span>


```
ID3DX11EffectPass* pPass = pEffect->GetTechniqueByIndex(0)->GetPassByIndex(1);

ID3DX11EffectInterfaceVariable* pIface = pEffect->GetVariableByName( "pIColor2" )->AsInterface();
ID3DX11EffectClassInstanceVariable* pCI = pEffect->GetVariableByName( "pGreen" )->AsClassInstance();
pIface->SetClassInstance( pCI );
pPass->Apply( 0, pDeviceContext );

// Apply the same pass with a different class instance
pCI = pEffect->GetVariableByName( "pRedArray" )->GetElement(1)->AsClassInstance();
pIface->SetClassInstance( pCI );
pPass->Apply( 0, pDeviceContext );
```



## <a name="related-topics"></a><span data-ttu-id="7128b-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7128b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7128b-132">Efectos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="7128b-132">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 