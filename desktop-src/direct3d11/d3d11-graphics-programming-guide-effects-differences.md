---
title: Diferencias entre los efectos 10 y 11
description: En este tema se muestran las diferencias entre Efectos 10 y Efectos 11.
ms.assetid: c3e5e6bc-c544-49ee-b6d9-021ce87f9b12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29af1b9e7aec72f96a62e0f62668b81a6eec8367
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361300"
---
# <a name="differences-between-effects-10-and-effects-11"></a>Diferencias entre los efectos 10 y 11

En este tema se muestran las diferencias entre Efectos 10 y Efectos 11.

## <a name="device-contexts-threading-and-cloning"></a>Contextos de dispositivo, subprocesos y clonación

La interfaz ID3D10Device se ha dividido en dos interfaces en Direct3D 11: ID3D11Device e ID3D11DeviceContext. Puede crear varios ID3D11DeviceContexts para facilitar la ejecución simultánea en varios subprocesos. Efectos 11 amplía este concepto al marco de efectos.

El tiempo de ejecución de Effects 11 es de un solo subproceso. Por este motivo, no debe usar una sola instancia ID3DX11Effect con varios subprocesos simultáneamente.

Para usar el entorno de ejecución de Effects 11 en varias instancias, debe crear instancias ID3DX11Effect independientes. Dado que ID3D11DeviceContext también es de un solo subproceso, debe pasar distintas instancias de ID3D11DeviceContext a cada instancia de efecto en Aplicar. Puede usar estos contextos de dispositivo independientes para crear listas de comandos para que el subproceso de representación pueda aplicarlos en el contexto inmediato del dispositivo.

La manera más fácil de crear varios efectos que encapsulan la misma funcionalidad, para su uso en varios subprocesos, es crear un efecto y, a continuación, realizar copias clonadas. La clonación tiene las siguientes ventajas con respecto a la creación de varias copias desde cero:

1.  La rutina de clonación es más rápida que la rutina de creación.
2.  Los efectos clonados comparten sombreadores creados, bloques de estado e instancias de clase (por lo que no tienen que volver a crearse).
3.  Los efectos clonados pueden compartir búferes constantes.
4.  Los efectos clonados comienzan con un estado que coincide con el efecto actual (valores de variable, tanto si se ha optimizado como si no).

Consulte [Clonación de un efecto](d3d11-graphics-programming-guide-effects-cloning.md) para obtener más información.

## <a name="effect-pools-and-groups"></a>Grupos y grupos de efectos

Con diferencia, el uso más frecuente de los grupos de efectos en Direct3D 10 era para agrupar materiales. Los grupos de efectos se han quitado de Efectos 11 y se han agregado grupos, que es un método más eficaz de agrupación de materiales.

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



Puede lograr la misma funcionalidad en Efectos 11 mediante grupos:


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



## <a name="new-shader-stages"></a>Nuevas fases del sombreador

Hay tres nuevas fases del sombreador en Direct3D 11: el sombreador de casco, el sombreador de dominio y el sombreador de proceso. Los efectos 11 los controla de forma similar a los sombreadores de vértices, los sombreadores de geometría y los sombreadores de píxeles.

Se han agregado tres nuevos tipos de variables a Efectos 11:

-   HullShader
-   DomainShader
-   ComputeShader

Si usa estos sombreadores en una técnica, debe etiquetar esa técnica "técnica11" y no "técnica10". El sombreador de proceso no se puede establecer en el mismo paso que cualquier otro estado gráfico (otros sombreadores, bloques de estado o destinos de representación).

## <a name="new-texture-types"></a>Nuevos tipos de textura

Direct3D 11 admite los siguientes tipos de textura:

-   [AppendStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [ByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer)
-   [ConsumeStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)
-   [StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer)

## <a name="unordered-access-views"></a>Vistas de acceso sin ordenar

Efectos 11 admite la obtención y configuración de los nuevos tipos de vistas de acceso no ordenados. Esto funciona de forma similar a las texturas.

Considere este ejemplo de HLSL de efectos:


```
  
RWTexture1D<float> myUAV;
```



Puede establecer esta variable en C++ como se muestra a continuación:


```
  
ID3D11UnorderedAccessView* pUAVTexture1D = NULL;
ID3DX11EffectUnorderedAccessViewVariable* pUAVVar;
pUAVVar = pEffect->GetVariableByName("myUAV")->AsUnorderedAccessView();
pUAVVar->SetUnorderedAccessView( pUAVTexture1D );
```



Direct3D 11 admite los siguientes tipos de vistas de acceso sin ordenar:

-   RWBuffer
-   RWByteAddressBuffer
-   RWStructuredBuffer
-   RWTexture1D
-   RWTexture1DArray
-   RWTexture2D
-   RWTexture2DArray
-   RWTexture3D

## <a name="interfaces-and-class-instances"></a>Interfaces e instancias de clase

Para obtener la sintaxis de interfaz y clase, [vea Interfaces y clases](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).

Para usar interfaces y clases en efectos, vea [Interfaces y clases en efectos](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md).

## <a name="addressable-stream-out"></a>Secuencias direccionables

En Direct3D 10, los sombreadores de geometría podrían generar un flujo de datos a la unidad de salida del flujo y a la unidad rasterizadora. En Direct3D11, los sombreadores de geometría pueden generar hasta cuatro flujos de datos a la unidad de salida del flujo y, como máximo, una de esas secuencias a la unidad rasterizadora. La **función intrínseca ConstructGSWithSO** se ha actualizado para reflejar esta nueva funcionalidad.

Consulte [Sintaxis de stream out](d3d11-graphics-reference-effect-streamout.md) para obtener más información.

## <a name="setting-and-unsetting-device-state"></a>Configuración y desajuste del estado del dispositivo

En Efectos 10, podría crear búferes constantes y búferes de textura administrados por el usuario mediante las funciones [**ID3D10EffectConstantBuffer::SetConstantBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) y [**SetTextureBuffer.**](id3dx11effectconstantbuffer-settexturebuffer.md) Después de llamar a estas funciones, el tiempo de ejecución de Effects 10 ya no administra el búfer constante o el búfer de textura y el usuario debe rellenar los datos mediante la interfaz ID3D10Device.

En Efectos 11, también puede hacer que los bloques de estado (estado de mezcla, estado de rasterizador, estado de galería de símbolos de profundidad y estado de muestreador) estén administrados por el usuario mediante las llamadas siguientes:

-   [**ID3DX11EffectBlendVariable::SetBlendState**](id3dx11effectblendvariable-setblendstate.md)
-   [**ID3DX11EffectRasterizerVariable::SetRasterizerState**](id3dx11effectrasterizervariable-setrasterizerstate.md)
-   [**ID3DX11EffectDepthStencilVariable::SetDepthStencilState**](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)
-   [**ID3DX11EffectSamplerVariable::SetSampler**](id3dx11effectsamplervariable-setsampler.md)

Después de llamar a estas funciones, el tiempo de ejecución de Efectos 11 ya no administra las variables de bloque de estado y los valores permanecerán sin cambios. Tenga en cuenta que, dado que los bloques de estado son inmutables, el usuario debe establecer un nuevo bloque de estado para cambiar los valores.

También puede revertir búferes constantes, búferes de textura y bloques de estado al estado administrado que no es de usuario. Si desasoye estas variables, el tiempo de ejecución de Efectos 11 seguirá actualícándolos cuando sea necesario. Puede usar las siguientes llamadas para deshacer la configuración de variables administradas por el usuario:

-   [**ID3DX11EffectConstantBuffer::UndoSetConstantBuffer**](id3dx11effectconstantbuffer-undosetconstantbuffer.md)
-   [**ID3DX11EffectConstantBuffer::UndoSetTextureBuffer**](id3dx11effectconstantbuffer-undosettexturebuffer.md)
-   [**ID3DX11EffectBlendVariable::UndoSetBlendState**](id3dx11effectblendvariable-undosetblendstate.md)
-   [**ID3DX11EffectRasterizerVariable::UndoSetRasterizerState**](id3dx11effectrasterizervariable-undosetrasterizerstate.md)
-   [**ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState**](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md)
-   [**ID3DX11EffectSamplerVariable::UndoSetSampler**](id3dx11effectsamplervariable-undosetsampler.md)

## <a name="effects-virtual-machine"></a>Máquina virtual de efectos

Se ha quitado la máquina virtual de efectos, que evaluó expresiones complejas fuera de las funciones.

No se admiten los siguientes ejemplos de expresiones complejas:

1.  SetPixelShader( myPSArray( i \* 3 + j ) );
2.  SetPixelShader( myPSArray( (float)i );
3.  FILTER = i + 2;

Se admiten los siguientes ejemplos de expresiones no complejas:

1.  SetPixelShader( myPS );
2.  SetPixelShader( myPS \[ i \] );
3.  SetPixelShader( myPS \[ uIndex \] ); // uIndex es una variable uint
4.  FILTER = i;
5.  FILTER = ANISOTROPIC;

Estas expresiones podrían aparecer en expresiones de bloque de estado (como FILTER) y expresiones de paso (como SetPixelShader).

## <a name="source-availability-and-location"></a>Disponibilidad y ubicación de origen

Los efectos 10 se distribuyeron en D3D10.dll. Los efectos 11 se distribuyen como origen, con las Visual Studio correspondientes para compilarlo. Al crear aplicaciones de tipo de efectos, se recomienda incluir el origen Effects 11 directamente en esas aplicaciones.

Puede obtener Effects 11 en [Effects for Direct3D 11 Update (Efectos para direct3D 11 Update).](https://github.com/Microsoft/FX11)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 