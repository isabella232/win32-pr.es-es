---
title: Diferencias entre efectos 10 y efectos 11
description: En este tema se muestran las diferencias entre los efectos 10 y 11.
ms.assetid: c3e5e6bc-c544-49ee-b6d9-021ce87f9b12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29af1b9e7aec72f96a62e0f62668b81a6eec8367
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792322"
---
# <a name="differences-between-effects-10-and-effects-11"></a>Diferencias entre efectos 10 y efectos 11

En este tema se muestran las diferencias entre los efectos 10 y 11.

## <a name="device-contexts-threading-and-cloning"></a>Contextos de dispositivo, subprocesos y clonación

La interfaz ID3D10Device se ha dividido en dos interfaces en Direct3D 11: ID3D11Device y ID3D11DeviceContext. Puede crear varios ID3D11DeviceContexts para facilitar la ejecución simultánea en varios subprocesos. Effects 11 extiende este concepto al marco de trabajo de efectos.

Los efectos 11 en tiempo de ejecución son de un solo subproceso. Por esta razón, no debe utilizar una única instancia de ID3DX11Effect con varios subprocesos simultáneamente.

Para usar el tiempo de ejecución de Effects 11 en varias instancias, debe crear instancias de ID3DX11Effect independientes. Dado que ID3D11DeviceContext también es de subproceso único, debe pasar instancias de ID3D11DeviceContext diferentes a cada instancia de Effect en Apply. Puede usar estos contextos de dispositivo independientes para crear listas de comandos de forma que el subproceso de representación pueda aplicarlos en el contexto de dispositivo inmediato.

La forma más fácil de crear varios efectos que encapsulan la misma funcionalidad, para su uso en varios subprocesos, es crear un efecto y luego hacer copias clonadas. La clonación presenta las siguientes ventajas en comparación con la creación de varias copias desde cero:

1.  La rutina de clonación es más rápida que la rutina de creación.
2.  Los efectos clonados comparten los sombreadores creados, los bloques de estado y las instancias de clase (por lo que no es necesario volver a crearlos).
3.  Los efectos clonados pueden compartir búferes de constantes.
4.  Los efectos clonados comienzan con el estado que coincide con el efecto actual (valores de variable, tanto si se ha optimizado como si no).

Consulte [clonar un efecto](d3d11-graphics-programming-guide-effects-cloning.md) para obtener más información.

## <a name="effect-pools-and-groups"></a>Grupos de efectos y grupos

Con diferencia el uso más frecuente de los grupos de efectos en Direct3D 10 era para agrupar materiales. Los grupos de efectos se han quitado de los efectos 11 y se han agregado grupos, que es un método más eficaz de agrupación de materiales.

Un grupo de efectos es simplemente un conjunto de técnicas. Consulte [Sintaxis de grupo de efectos (Direct3D 11)](d3d11-effect-group-syntax.md) para obtener más información.

Considere la siguiente jerarquía de efectos con cuatro efectos secundarios y un grupo de efectos:


```
// Effect Pool
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

// Effect Child 1
#include "EffectPool.fx"
technique10 GrassMaterialLowSpec { ... }

// Effect Child 2
#include "EffectPool.fx"
technique10 GrassMaterialHighSpec { ... }

// Effect Child 3
#include "EffectPool.fx"
technique10 WaterMaterialLowSpec { ... }

// Effect Child 4
#include "EffectPool.fx"
technique10 WaterMaterialHighSpec { ... }
```



Puede lograr la misma funcionalidad en Effects 11 mediante el uso de grupos:


```
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

fxgroup GrassMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}

fxgroup WaterMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}
```



## <a name="new-shader-stages"></a>Nuevas etapas del sombreador

Hay tres nuevas fases del sombreador en Direct3D 11: el sombreador de casco, el sombreador de dominios y el sombreador de proceso. Los efectos 11 lo controlan de manera similar a los sombreadores de vértices, los sombreadores de geometría y los sombreadores de píxeles.

Se han agregado tres nuevos tipos de variables a Effects 11:

-   HullShader
-   DomainShader
-   ComputeShader

Si usa estos sombreadores en una técnica, debe etiquetar esa técnica "technique11" y no "technique10". El sombreador de cálculo no se puede establecer en el mismo paso que cualquier otro estado de gráficos (otros sombreadores, bloques de estado o destinos de representación).

## <a name="new-texture-types"></a>Nuevos tipos de textura

Direct3D 11 admite los siguientes tipos de textura:

-   [AppendStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [ByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer)
-   [ConsumeStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)
-   [StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer)

## <a name="unordered-access-views"></a>Vistas de acceso desordenado

Effects 11 permite obtener y establecer los nuevos tipos de vistas de acceso desordenado. Esto funciona de forma similar a las texturas.

Considere este ejemplo de efectos HLSL:


```
  
RWTexture1D<float> myUAV;
```



Puede establecer esta variable en C++ de la siguiente manera:


```
  
ID3D11UnorderedAccessView* pUAVTexture1D = NULL;
ID3DX11EffectUnorderedAccessViewVariable* pUAVVar;
pUAVVar = pEffect->GetVariableByName("myUAV")->AsUnorderedAccessView();
pUAVVar->SetUnorderedAccessView( pUAVTexture1D );
```



Direct3D 11 admite los siguientes tipos de vistas de acceso desordenado:

-   RWBuffer
-   RWByteAddressBuffer
-   RWStructuredBuffer
-   RWTexture1D
-   RWTexture1DArray
-   RWTexture2D
-   RWTexture2DArray
-   RWTexture3D

## <a name="interfaces-and-class-instances"></a>Interfaces e instancias de clase

Para ver la sintaxis de la interfaz y la clase, consulte [interfaces y clases](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).

Para usar interfaces y clases en efectos, vea [interfaces y clases en efectos](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md).

## <a name="addressable-stream-out"></a>Transmisión por secuencias direccionable

En Direct3D 10, los sombreadores de geometría pueden generar un flujo de datos a la unidad de salida de la secuencia y la unidad de rasterizador. En Direct3D 11, los sombreadores de geometría pueden generar hasta cuatro flujos de datos en la unidad de salida de flujo y, como máximo, uno de esos flujos en la unidad de rasterizador. El intrínseco **ConstructGSWithSO** se ha actualizado para reflejar esta nueva funcionalidad.

Consulte [Sintaxis de Stream out](d3d11-graphics-reference-effect-streamout.md) para obtener más información.

## <a name="setting-and-unsetting-device-state"></a>Establecer y desconfigurar el estado del dispositivo

En los efectos 10, podría crear búferes de constantes y búferes de texturas administrados por el usuario mediante las funciones [**ID3D10EffectConstantBuffer:: SetConstantBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) y [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md) . Después de llamar a estas funciones, el tiempo de ejecución de los efectos 10 deja de administrar el búfer de constantes o el búfer de textura y el usuario debe rellenar los datos mediante la interfaz ID3D10Device.

En Effects 11, también puede hacer que los bloques de estado (estado de Blend, estado de rasterizador, estado de estarcido de profundidad y estado de muestra) se administren mediante el uso de las siguientes llamadas:

-   [**ID3DX11EffectBlendVariable::SetBlendState**](id3dx11effectblendvariable-setblendstate.md)
-   [**ID3DX11EffectRasterizerVariable::SetRasterizerState**](id3dx11effectrasterizervariable-setrasterizerstate.md)
-   [**ID3DX11EffectDepthStencilVariable::SetDepthStencilState**](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)
-   [**ID3DX11EffectSamplerVariable::SetSampler**](id3dx11effectsamplervariable-setsampler.md)

Después de llamar a estas funciones, el tiempo de ejecución de Effects 11 ya no administra las variables de bloque de estado y los valores permanecerán sin cambios. Tenga en cuenta que, dado que los bloques de estado son inmutables, el usuario debe establecer un nuevo bloque de estado para cambiar los valores.

También puede revertir los búferes de constantes, los búferes de textura y los bloques de estado al estado no administrado por el usuario. Si no establece estas variables, el tiempo de ejecución de Effects 11 continuará actualizarlas cuando sea necesario. Puede utilizar las siguientes llamadas para no establecer las variables administradas por el usuario:

-   [**ID3DX11EffectConstantBuffer::UndoSetConstantBuffer**](id3dx11effectconstantbuffer-undosetconstantbuffer.md)
-   [**ID3DX11EffectConstantBuffer::UndoSetTextureBuffer**](id3dx11effectconstantbuffer-undosettexturebuffer.md)
-   [**ID3DX11EffectBlendVariable::UndoSetBlendState**](id3dx11effectblendvariable-undosetblendstate.md)
-   [**ID3DX11EffectRasterizerVariable::UndoSetRasterizerState**](id3dx11effectrasterizervariable-undosetrasterizerstate.md)
-   [**ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState**](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md)
-   [**ID3DX11EffectSamplerVariable::UndoSetSampler**](id3dx11effectsamplervariable-undosetsampler.md)

## <a name="effects-virtual-machine"></a>Efectos de la máquina virtual

Se ha quitado la máquina virtual de efectos, que evaluó expresiones complejas fuera de las funciones.

No se admiten los siguientes ejemplos de expresiones complejas:

1.  SetPixelShader (myPSArray (i \* 3 + j));
2.  SetPixelShader (myPSArray ((float) i);
3.  FILTRO = i + 2;

Se admiten los siguientes ejemplos de expresiones no complejas:

1.  SetPixelShader( myPS );
2.  SetPixelShader (myPS \[ i \] );
3.  SetPixelShader (myPS \[ uIndex \] );//uIndex es una variable uint
4.  FILTRO = i;
5.  FILTER = ANISOTRÓPICO;

Estas expresiones pueden aparecer en expresiones de bloque de estado (como FILTER) y expresiones Pass (como SetPixelShader).

## <a name="source-availability-and-location"></a>Disponibilidad y ubicación de origen

Los efectos 10 se distribuyeron en D3D10.dll. Effects 11 se distribuye como Source, con las soluciones de Visual Studio correspondientes para compilarlo. Al crear aplicaciones de tipo Effects, se recomienda incluir directamente los efectos 11 en esas aplicaciones.

Puede obtener los efectos 11 de [Effects para la actualización de Direct3D 11](https://github.com/Microsoft/FX11).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 