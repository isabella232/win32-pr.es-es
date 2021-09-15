---
title: Desempaquetar y empaquetar DXGI_FORMAT editar In-Place imágenes
description: El archivo D3DX DXGIFormatConvert.inl contiene funciones de conversión de formato en línea que puede usar en el sombreador de proceso o en el sombreador de píxeles \_ en hardware de Direct3D 11.
ms.assetid: 328c4488-9758-4359-a37b-ac50f20e2940
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 04f3729bbeda5b0677da9d52e595e621523ff2d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573773"
---
# <a name="unpacking-and-packing-dxgi_format-for-in-place-image-editing"></a>Desempaquetar y empaquetar DXGI \_ FORMAT para la edición In-Place imágenes

El archivo D3DX DXGIFormatConvert.inl contiene funciones de conversión de formato en línea que puede usar en el sombreador de proceso o en el sombreador de píxeles \_ en hardware de Direct3D 11. Puede usar estas funciones en la aplicación para leer y escribir simultáneamente en una textura. Es decir, puede realizar la edición de imágenes en contexto. Para usar estas funciones de conversión de formato insertadas, incluya el archivo D3DX \_ DXGIFormatConvert.inl en la aplicación.

> El encabezado D3DX \_ DXGIFormatConvert.inl se incluye en el SDK de DirectX heredado. También se incluye en el paquete de NuGet [Microsoft.DXSDK.D3DX.](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX)

La vista de acceso desordenado (UAV) de Direct3D 11 de un recurso Texture1D, Texture2D o Texture3D admite lecturas de acceso aleatorio y escrituras en la memoria desde un sombreador de proceso o sombreador de píxeles. Sin embargo, Direct3D 11 admite simultáneamente la lectura y escritura en solo el formato de textura UINT DXGI \_ FORMAT \_ R32. \_ Por ejemplo, Direct3D 11 no admite simultáneamente la lectura y escritura en otros formatos más útiles, como DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM. Solo puede usar un UAV para la escritura de acceso aleatorio a estos otros formatos, o puede usar solo un sombreador Vista de recursos (SRV) para leer el acceso aleatorio de estos otros formatos. El hardware de conversión de formato no está disponible para leer y escribir simultáneamente en otros formatos.

Sin embargo, puede leer y escribir simultáneamente en estos otros formatos si la textura se va a convertir al formato de textura UINT DXGI FORMAT R32 al crear un UAV, siempre que el formato original del recurso admita la conversión \_ \_ a \_ DXGI FORMAT \_ \_ R32 \_ UINT. La mayoría de los formatos de 32 bits por elemento admiten la conversión a DXGI \_ FORMAT \_ R32 \_ UINT. Al convertir la textura al formato de textura UINT DXGI FORMAT R32 al crear un UAV, puede realizar lecturas y \_ escrituras simultáneas en la textura siempre que el sombreador realice el desempaquete de formato manual al leer y empaquetar en la \_ \_ escritura.

La ventaja de convertir la textura al formato de textura UINT DXGI FORMAT R32 es que más adelante puede usar el formato adecuado \_ \_ \_ (por ejemplo, DXGI \_ FORMAT \_ R16G16 FLOAT) con otras vistas en la misma textura, como Vistas de destino de representación \_ (RTV) o SRV. Por lo tanto, el hardware puede realizar el desempaquete y empaquetado de formato automático típico, puede realizar el filtrado de texturas, y así sucesivamente cuando no hay limitaciones de hardware.

El siguiente escenario requiere que una aplicación realice la siguiente secuencia de acciones para realizar la edición de imágenes en contexto.

Supongamos que quiere crear una textura en la que puede usar un sombreador de píxeles o un sombreador de proceso para realizar la edición en contexto y desea que los datos de textura se almacenen en un formato que sea descendiente de uno de los siguientes formatos SIN TIPO:

-   FORMATO DXGI \_ \_ R10G10B10A2 \_ SIN TIPO
-   FORMATO DXGI \_ \_ R8G8B8A8 \_ SIN TIPO
-   FORMATO DXGI \_ \_ B8G8R8A8 \_ SIN TIPO
-   FORMATO DXGI \_ \_ B8G8R8X8 \_ SIN TIPO
-   FORMATO DXGI \_ \_ R16G16 \_ SIN TIPO

Por ejemplo, el formato DXGI \_ FORMAT \_ R10G10B10A2 UNORM es un descendiente del formato \_ DXGI \_ FORMAT \_ R10G10B10A2 \_ TYPELESS. Por lo tanto, DXGI \_ FORMAT \_ R10G10B10A2 UNORM admite el patrón de uso que se \_ describe en la secuencia siguiente. Los formatos que descienden de DXGI \_ FORMAT \_ R32 \_ TYPELESS, como DXGI FORMAT \_ \_ R32 \_ FLOAT, se admiten trivialmente sin necesidad de ninguna ayuda de conversión de formato que se describe en la secuencia siguiente.

**Para realizar la edición de imágenes en contexto**

1.  Cree una textura con el formato dependiente de TYPELESS adecuado que se especifica en el escenario anterior junto con las marcas de enlace necesarias, como D3D11 \_ BIND \_ UNORDERED \_ ACCESS \| D3D11 \_ BIND SHADER \_ \_ RESOURCE.
2.  Para la edición de imágenes en contexto, cree un UAV con el formato DXGI \_ FORMAT \_ R32 \_ UINT. La API de Direct3D 11 normalmente no permite la conversión entre "familias" de diferentes formatos. Sin embargo, la API de Direct3D 11 realiza una excepción con el formato UINT DXGI \_ FORMAT \_ R32. \_
3.  En el sombreador de proceso o el sombreador de píxeles, use el paquete de formato en línea adecuado y desempaquete las funciones que se proporcionan en el archivo D3DX \_ DXGIFormatConvert.inl. Por ejemplo, supongamos que el UAV DXGI FORMAT R32 UINT de la textura contiene realmente datos con formato \_ \_ \_ DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM. Una vez que la aplicación lee un uint del UAV en el sombreador, debe llamar a la siguiente función para desempaquetar el formato de textura:

    ```
    XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
    ```

    

    A continuación, para escribir en el UAV en el mismo sombreador, la aplicación llama a la función siguiente para empaquetar los datos del sombreador en un uint que la aplicación puede escribir en el UAV:

    ```
    UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
    ```

    

4.  A continuación, la aplicación puede crear otras vistas, como SRV, con el formato necesario. Por ejemplo, la aplicación puede crear un SRV con el formato DXGI FORMAT R10G10B10A2 UNORM si el recurso se creó como \_ \_ \_ DXGI \_ FORMAT \_ R10G10B10A2 \_ TYPELESS. Cuando un sombreador accede a ese SRV, el hardware puede realizar la conversión automática de tipos como de costumbre.

> [!Note]  
> Si el sombreador solo debe escribir en un UAV o leer como un SRV, no se necesita ninguno de este trabajo de conversión porque puede usar UAV o SRV totalmente escritos. Las funciones de conversión de formato proporcionadas en D3DX DXGIFormatConvert.inl son potencialmente útiles solo si desea realizar lecturas y escrituras simultáneas en un UAV de una \_ textura.

 

A continuación se muestra la lista de funciones de conversión de formato que se incluyen en el archivo D3DX \_ DXGIFormatConvert.inl. Estas funciones se clasifican por el formato DXGI \_ que desempaquetar y empaquetar. Cada uno de los formatos admitidos desciende de uno de los formatos SIN TIPO enumerados en el escenario anterior y admite la conversión a DXGI \_ FORMAT \_ R32 UINT como \_ UAV.

<dl> <dt>

<span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>FORMATO DXGI \_ \_ R10G10B10A2 \_ UINT
</dt> <dd>


```
XMUINT4 D3DX_R10G10B10A2_UINT_to_UINT4(UINT packedInput)
UINT    D3DX_UINT4_to_R10G10B10A2_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM \_ SRGB
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> La \_ función inexact-type usa instrucciones de sombreador que no tienen una precisión lo suficientemente alta como para dar la respuesta exacta. La función alternativa usa una tabla de búsqueda almacenada en el sombreador para proporcionar una conversión >float de SRGB.

 

</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>FORMATO DXGI \_ \_ R8G8B8A8 \_ UINT
</dt> <dd>


```
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(UINT packedInput)
XMUINT  D3DX_UINT4_to_R8G8B8A8_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>FORMATO DXGI \_ \_ R8G8B8A8 \_ SNORM
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_SNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_SNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>FORMATO DXGI \_ \_ R8G8B8A8 \_ SINT
</dt> <dd>


```
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(UINT packedInput)
UINT   D3DX_INT4_to_R8G8B8A8_SINT(XMINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_B8G8R8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM \_ SRGB
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> La \_ función inexact-type usa instrucciones de sombreador que no tienen una precisión lo suficientemente alta como para dar la respuesta exacta. La función alternativa usa una tabla de búsqueda almacenada en el sombreador para proporcionar una conversión >float de SRGB.

 

</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM(hlsl_precise XMFLOAT3 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>FORMATO DXGI \_ \_ B8G8R8X8 \_ UNORM \_ SRGB
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(UINT packedInput) *
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(hlsl_precise XMFLOAT3 unpackedInput)
```



> [!Note]  
> La \_ función inexact-type usa instrucciones de sombreador que no tienen una precisión lo suficientemente alta como para dar la respuesta exacta. La función alternativa usa una tabla de búsqueda almacenada en el sombreador para proporcionar una conversión >float de SRGB.

 

</dd> <dt>

<span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>DXGI \_ FORMAT \_ R16G16 \_ FLOAT
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_FLOAT(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>DXGI \_ FORMAT \_ R16G16 \_ UNORM
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_UNORM(hlsl_precise FLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>DXGI \_ FORMAT \_ R16G16 \_ UINT
</dt> <dd>


```
XMUINT2 D3DX_R16G16_UINT_to_UINT2(UINT packedInput)
UINT    D3DX_UINT2_to_R16G16_UINT(XMUINT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>DXGI \_ FORMAT \_ R16G16 \_ SNORM
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_SNORM(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>DXGI \_ FORMAT \_ R16G16 \_ SINT
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

 

 




