---
title: Desempaquetar y empaquetar DXGI_FORMAT para la edición de In-Place imagen
description: El \_ archivo D3DX DXGIFormatConvert. INL contiene funciones de conversión de formato en línea que puede usar en el sombreador de cálculo o en el sombreador de píxeles en el hardware de Direct3D 11.
ms.assetid: 328c4488-9758-4359-a37b-ac50f20e2940
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c613a3f0068537733961b58a8a4c2b4528d21f25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356871"
---
# <a name="unpacking-and-packing-dxgi_format-for-in-place-image-editing"></a>Desempaquetar y empaquetar el \_ formato de DXGI para la edición de In-Place imagen

El \_ archivo D3DX DXGIFormatConvert. INL contiene funciones de conversión de formato en línea que puede usar en el sombreador de cálculo o en el sombreador de píxeles en el hardware de Direct3D 11. Puede usar estas funciones en la aplicación para leer y escribir simultáneamente en una textura. Es decir, puede realizar la edición en contexto de la imagen. Para usar estas funciones de conversión de formato en línea, incluya el \_ archivo D3DX DXGIFormatConvert. INL en la aplicación.

La vista de acceso desordenado de Direct3D 11 (UAV) de un recurso Texture1D, Texture2D o Texture3D admite lecturas y escrituras de acceso aleatorio en la memoria desde un sombreador de cálculo o un sombreador de píxeles. Sin embargo, Direct3D 11 admite simultáneamente la lectura y la escritura en el formato de estilo DXGI \_ \_ R32 \_ uint Texture. Por ejemplo, Direct3D 11 no admite simultáneamente la lectura y la escritura en otros formatos más útiles, como el formato de DXGI \_ \_ R8G8B8A8 \_ UNORM. Solo se puede usar un UAV para el acceso aleatorio de escritura a otros formatos, o solo se puede usar un sombreador Vista de recursos (SRV) para el acceso aleatorio leído de otros formatos. El hardware de conversión de formato no está disponible para leer y escribir en otros formatos simultáneamente.

Sin embargo, todavía puede leer simultáneamente y escribir en otros formatos mediante la conversión de la textura al \_ \_ formato dxgi R32 \_ uint Texture al crear un UAV, siempre que el formato original del recurso admita la conversión al \_ formato dxgi \_ R32 \_ uint. La mayoría de los formatos de elementos de 32 bits por elemento admiten la conversión al formato de DXGI \_ \_ R32 \_ uint. Al convertir la textura en el formato de DXGI \_ formato \_ R32 \_ uint cuando se crea un UAV, se pueden realizar de forma simultánea lecturas y escrituras en la textura siempre que el sombreador realice el desempaquetado manual de formato en la lectura y el empaquetado en la escritura.

La ventaja de convertir la textura en el formato de DXGI \_ \_ R32 \_ uint Texture es que, más adelante, puede usar el formato adecuado (por ejemplo, DXGI \_ format \_ R16G16 \_ float) con otras vistas en la misma textura, como vistas de destino de representación (RTVs) o SRVs. Por lo tanto, el hardware puede realizar el desempaquetado y paquete de formato automático típico, puede realizar el filtrado de texturas, y así sucesivamente donde no haya limitaciones de hardware.

En el escenario siguiente se requiere que una aplicación realice la siguiente secuencia de acciones para realizar la edición de imágenes en contexto.

Supongamos que desea crear una textura en la que puede usar un sombreador de píxeles o un sombreador de cálculo para realizar la edición en contexto y desea almacenar los datos de textura en un formato descendiente de uno de los siguientes formatos sin tipo:

-   \_Formato de \_ DXGI \_ sin tipo R10G10B10A2
-   \_Formato de \_ DXGI \_ sin tipo R8G8B8A8
-   \_Formato de \_ DXGI \_ sin tipo B8G8R8A8
-   \_Formato de \_ DXGI \_ sin tipo B8G8R8X8
-   \_Formato de \_ DXGI \_ sin tipo R16G16

Por ejemplo, el formato de DXGI \_ formato \_ R10G10B10A2 \_ UNORM es un descendiente del formato \_ dxgi \_ \_ sin tipo R10G10B10A2. Por lo tanto \_ , \_ el formato de DXGI R10G10B10A2 \_ UNORM admite el patrón de uso que se describe en la siguiente secuencia. Los formatos que descienden del formato de DXGI \_ \_ R32 \_ sin tipo, como dxgi \_ format \_ R32 \_ float, se admiten de forma trivial sin necesidad de ninguna ayuda de conversión de formato que se describe en la siguiente secuencia.

**Para realizar la edición de imágenes en contexto**

1.  Cree una textura con el formato dependiente sin tipos que se especifica en el escenario anterior, junto con las marcas de enlace necesarias, como D3D11 \_ enlace \_ Unordered \_ Access \| D3D11 \_ Binder \_ \_ .
2.  Para la edición de imágenes en contexto, cree un UAV con el formato de DXGI \_ formato \_ R32 \_ uint. La API de Direct3D 11 normalmente no permite la conversión entre "familias" de formato diferente. Sin embargo, la API de Direct3D 11 realiza una excepción con el formato de DXGI \_ format \_ R32 \_ uint.
3.  En el sombreador de cálculo o el sombreador de píxeles, use las funciones adecuadas de paquete de formato insertado y desempaquetado que se proporcionan en el \_ archivo D3DX DXGIFormatConvert. INL. Por ejemplo, supongamos que el \_ formato \_ de dxgi R32 \_ uint UAV de la textura realmente contiene \_ \_ \_ datos con formato de dxgi R10G10B10A2 UNORM. Una vez que la aplicación Lee un uint de UAV en el sombreador, debe llamar a la función siguiente para desempaquetar el formato de textura:

    ```
    XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
    ```

    

    Después, para escribir en el UAV en el mismo sombreador, la aplicación llama a la función siguiente para empaquetar los datos del sombreador en un valor uint que la aplicación puede escribir en UAV:

    ```
    UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
    ```

    

4.  A continuación, la aplicación puede crear otras vistas, como SRVs, con el formato requerido. Por ejemplo, la aplicación puede crear un SRV con el formato de DXGI \_ formato \_ R10G10B10A2 \_ UNORM si el recurso se creó como \_ formato de dxgi \_ R10G10B10A2 \_ sin tipo. Cuando un sombreador accede a ese SRV, el hardware puede realizar la conversión automática de tipos como de costumbre.

> [!Note]  
> Si el sombreador debe escribir solo en un UAV o leer como un SRV, no es necesario ninguno de estos trabajos de conversión porque puede usar UAVs o SRVs totalmente tipados. Las funciones de conversión de formato proporcionadas en D3DX \_ DXGIFormatConvert. INL solo son útiles si desea realizar operaciones de lectura y escritura simultáneas en una UAV de una textura.

 

A continuación se muestra la lista de funciones de conversión de formato que se incluyen en el \_ archivo D3DX DXGIFormatConvert. INL. Estas funciones se clasifican por el formato de DXGI \_ que desempaquetan y empaquetan. Cada uno de los formatos admitidos desciende de uno de los formatos sin tipo enumerados en el escenario anterior y admite la conversión al formato de DXGI \_ \_ R32 \_ uint como UAV.

<dl> <dt>

<span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>Formato de DXGI \_ \_ R10G10B10A2 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>Formato de DXGI \_ \_ R10G10B10A2 \_ uint
</dt> <dd>


```
XMUINT4 D3DX_R10G10B10A2_UINT_to_UINT4(UINT packedInput)
UINT    D3DX_UINT4_to_R10G10B10A2_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>Formato de DXGI \_ \_ R8G8B8A8 \_ UNORM \_ sRGB
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> La \_ función de tipo inexacto usa instrucciones del sombreador que no tienen una precisión lo suficientemente alta como para proporcionar la respuesta exacta. La función alternativa utiliza una tabla de búsqueda almacenada en el sombreador para proporcionar una conversión de punto flotante de SRGB->exacta.

 

</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>Formato de DXGI \_ \_ R8G8B8A8 \_ uint
</dt> <dd>


```
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(UINT packedInput)
XMUINT  D3DX_UINT4_to_R8G8B8A8_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>Formato de DXGI \_ \_ R8G8B8A8 \_ SNORM
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_SNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_SNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>Formato de DXGI \_ \_ R8G8B8A8 \_ Sint
</dt> <dd>


```
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(UINT packedInput)
UINT   D3DX_INT4_to_R8G8B8A8_SINT(XMINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_B8G8R8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM \_ sRGB
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> La \_ función de tipo inexacto usa instrucciones del sombreador que no tienen una precisión lo suficientemente alta como para proporcionar la respuesta exacta. La función alternativa utiliza una tabla de búsqueda almacenada en el sombreador para proporcionar una conversión de punto flotante de SRGB->exacta.

 

</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>Formato de DXGI \_ \_ B8G8R8X8 \_ UNORM
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM(hlsl_precise XMFLOAT3 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>Formato de DXGI \_ \_ B8G8R8X8 \_ UNORM \_ sRGB
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(UINT packedInput) *
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(hlsl_precise XMFLOAT3 unpackedInput)
```



> [!Note]  
> La \_ función de tipo inexacto usa instrucciones del sombreador que no tienen una precisión lo suficientemente alta como para proporcionar la respuesta exacta. La función alternativa utiliza una tabla de búsqueda almacenada en el sombreador para proporcionar una conversión de punto flotante de SRGB->exacta.

 

</dd> <dt>

<span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>Formato de DXGI \_ \_ R16G16 \_ float
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_FLOAT(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>Formato de DXGI \_ \_ R16G16 \_ UNORM
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_UNORM(hlsl_precise FLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>Formato de DXGI \_ \_ R16G16 \_ uint
</dt> <dd>


```
XMUINT2 D3DX_R16G16_UINT_to_UINT2(UINT packedInput)
UINT    D3DX_UINT2_to_R16G16_UINT(XMUINT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>Formato de DXGI \_ \_ R16G16 \_ SNORM
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_SNORM(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>Formato de DXGI \_ \_ R16G16 \_ Sint
</dt> <dd>


```
XMINT2 D3DX_R16G16_SINT_to_INT2(UINT packedInput)
UINT   D3DX_INT2_to_R16G16_SINT(XMINT2 unpackedInput)
```



</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




