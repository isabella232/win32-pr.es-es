---
description: Un recurso de textura es una colección estructurada de datos.
ms.assetid: 4c716be8-044e-4ed4-aeca-4379440826bd
title: Creación de recursos de textura (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eadee1af159d6a45624dfd1d7c17c61878b4eeedb69799010177fe879ad1d132
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895345"
---
# <a name="creating-texture-resources-direct3d-10"></a>Creación de recursos de textura (Direct3D 10)

Un [recurso de](d3d10-graphics-programming-guide-resources-types.md) textura es una colección estructurada de datos. Normalmente, los valores de color se almacenan en [](d3d10-graphics-programming-guide-pipeline-stages.md) texturas y la canalización accede durante la representación en varias fases para la entrada y la salida. Crear texturas y definir cómo se usarán es una parte importante de la representación de escenas interesantes en Direct3D 10.

Aunque las texturas normalmente contienen información de color, la creación de texturas con [**un formato DXGI \_ diferente**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) les permite almacenar diferentes tipos de datos. A continuación, la canalización de Direct3D 10 puede aprovechar estos datos de maneras no tradicionales.

Todas las texturas tienen límites sobre la cantidad de memoria que consumen y el número de elementos de textura que contienen. Estas constantes de recursos especifican estos [límites.](d3d10-graphics-reference-resource-constants.md)

-   [Crear una textura a partir de un archivo](#create-a-texture-from-a-file)
    -   [Crear textura y ver por separado](#create-texture-and-view-separately)
    -   [Crear textura y vista simultáneamente](#create-texture-and-view-simultaneously)
-   [Crear texturas vacías](#creating-empty-textures)
    -   [Representación en una textura](#rendering-to-a-texture)
    -   [Rellenar texturas manualmente](#filling-textures-manually)
-   [Varios destinos de representación](#multiple-rendertargets)
-   [Temas relacionados](#related-topics)

## <a name="create-a-texture-from-a-file"></a>Crear una textura a partir de un archivo

> [!Note]  
> La [biblioteca de utilidades D3DX](d3d10-graphics-reference-d3dx10.md) está en desuso Windows 8 y no se admite para Windows Store.

 

Al crear una textura en Direct3D 10, también debe crear una [vista](d3d10-graphics-programming-guide-resources-access-views.md). Una vista es un objeto que indica al dispositivo cómo se debe acceder a una textura durante la representación. La manera más común de acceder a una textura es leerla mediante un [sombreador](../direct3dhlsl/dx-graphics-hlsl.md). Una vista de recursos de sombreador le mostrará a un sombreador cómo leer desde una textura durante la representación. El tipo de vista que usará una textura debe especificarse al crearla.

La creación de una textura y la carga de sus datos iniciales se pueden realizar de dos maneras diferentes: crear una textura y una vista por separado, o bien crear la textura y la vista al mismo tiempo. La API proporciona ambas técnicas para que pueda elegir cuál se adapta mejor a sus necesidades.

### <a name="create-texture-and-view-separately"></a>Crear textura y ver por separado

La manera más fácil de crear una textura es cargarla desde un archivo de imagen. Para crear la textura, basta con rellenar una estructura y proporcionar el nombre de la textura a [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md).


```
ID3D10Device *pDevice = NULL;
// Initialize D3D10 device...

D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;

ID3D10Resource *pTexture = NULL;
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pTexture, NULL );
```



La función D3DX [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) hace tres cosas: en primer lugar, crea un objeto de textura Direct3D 10; en segundo lugar, lee el archivo de imagen de entrada; en tercer lugar, almacena los datos de la imagen en el objeto de textura. En el ejemplo anterior, se carga un archivo BMP, pero la función puede cargar una variedad de tipos de archivo.

La marca de enlace indica que la textura se creará como un recurso de sombreador que permite que una fase del sombreador lea de la textura durante la representación.

En el ejemplo anterior no se especifican todos los parámetros de carga. De hecho, a menudo resulta beneficioso simplemente cero los parámetros de carga, ya que esto permite a D3DX elegir los valores adecuados en función de la imagen de entrada. Si desea que la imagen de entrada determine todos los parámetros con los que se crea la textura, simplemente especifique **NULL** para el **parámetro loadInfo** de la siguiente manera:


```
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", NULL, NULL, &pTexture, NULL );
```



Especificar **NULL para** la información de carga es un acceso directo sencillo pero eficaz.

Ahora que se ha creado una textura, debe crear una vista de recursos de sombreador para que la textura se pueda enlazar como una entrada a un sombreador. Dado [**que D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) devuelve un puntero a un recurso y no un puntero a una textura, debe determinar el tipo exacto de recurso que se cargó y, a continuación, puede crear una vista de sombreador y recurso [**mediante CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).


```
D3D10_SHADER_RESOURCE_VIEW_DESC srvDesc;
D3D10_RESOURCE_DIMENSION type;
pTexture->GetType( &type );
switch( type )
{
    case D3D10_RESOURCE_DIMENSION_BUFFER:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE1D:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE2D:
    {
        D3D10_TEXTURE2D_DESC desc;
        ID3D10Texture2D *pTexture2D = (ID3D10Texture2D*)pTexture;
        pTexture2D->GetDesc( &desc );
        
        srvDesc.Format = desc.Format;
        srvDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Texture2D.MipLevels = desc.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = desc.MipLevels -1;

    }
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE3D:
    //...
    break;
    default:
    //...
    break;
}

ID3D10ShaderResourceView *pSRView = NULL;
pDevice->CreateShaderResourceView( pTexture, &srvDesc, &pSRView );
```



Aunque el ejemplo anterior crea una vista de recursos de sombreador 2D, el código para crear otros tipos de vista de recursos de sombreador es muy similar. Cualquier fase del sombreador ahora puede usar esta textura como entrada.

El [**uso de D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) y [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview) para crear una textura y su vista asociada es una manera de preparar una textura para enlazarla a una fase de sombreador. Otra manera de hacerlo es crear la textura y su vista al mismo tiempo, que se describe en la sección siguiente.

### <a name="create-texture-and-view-simultaneously"></a>Crear textura y vista simultáneamente

Direct3D 10 requiere una textura y una vista de recursos de sombreador para leer desde una textura durante el tiempo de ejecución. Dado que la creación de una textura y una vista de recursos de sombreador es una tarea común, D3DX proporciona [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) para hacerlo por usted.


```
D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;

ID3D10ShaderResourceView *pSRView = NULL;
D3DX10CreateShaderResourceViewFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pSRView, NULL );
```



Con una sola llamada D3DX, se crean la vista de textura y de recurso de sombreador. La funcionalidad del **parámetro loadInfo** no ha cambiado; puede usarlo para personalizar cómo se crea la textura o derivar los parámetros necesarios del archivo de entrada especificando **NULL para** el **parámetro loadInfo.**

El [**objeto ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview) devuelto por la función [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) se puede usar más adelante para recuperar la interfaz [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource) original si es necesario. Para ello, llame al [**método GetResource.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10view-getresource)

D3DX proporciona una sola función para crear una vista de textura y de recurso de sombreador como una conviencia. Es decisión del usuario decidir qué método para crear una textura y una vista se adapta mejor a las necesidades de la aplicación.

Ahora que sabe cómo crear una textura y su vista de recursos de sombreador, en la sección siguiente se muestra cómo puede muestrear (leer) desde esa textura mediante un sombreador.

## <a name="creating-empty-textures"></a>Crear texturas vacías

En ocasiones, las aplicaciones querrán crear una textura y calcular [](d3d10-graphics-programming-guide-pipeline-stages.md) los datos que se almacenarán en la textura, o usar la canalización de gráficos para representarla y, posteriormente, usar los resultados en otro procesamiento. Estas texturas se pueden actualizar mediante la canalización de gráficos [](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) o por la propia aplicación, en función del tipo de uso que se especificó para la textura cuando se creó.

### <a name="rendering-to-a-texture"></a>Representación en una textura

El caso más común de crear una textura vacía que se rellenará con datos durante el tiempo de ejecución es el caso en el que una aplicación quiere representarse en una textura y, a continuación, usar los resultados de la operación de representación en un paso posterior. Las texturas creadas con este propósito deben especificar el [**uso predeterminado.**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)

En el ejemplo de código siguiente se crea una textura vacía en la que se puede representar la canalización y, posteriormente, se usa como entrada para un [sombreador](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).


```
// Create the render target texture
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = 1;
desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R32G32B32A32_FLOAT;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;

ID3D10Texture2D *pRenderTarget = NULL;
pDevice->CreateTexture2D( &desc, NULL, &pRenderTarget );
```



La creación de la textura requiere que la aplicación especifique información sobre las propiedades que tendrá la textura. El ancho y alto de la textura en los elementos de textura se establece en 256. Para este destino de representación, solo necesitamos un nivel de mapa mipmap. Solo se requiere un destino de representación, por lo que el tamaño de la matriz se establece en 1. Cada texel contiene cuatro valores de punto flotante de 32 bits, que se pueden usar para almacenar información muy precisa (vea [**DXGI \_ FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)). Un ejemplo por píxel es todo lo que se necesita. El uso se establece en el valor predeterminado porque permite la colocación más eficaz del destino de representación en memoria. Por último, se especifica el hecho de que la textura se enlazará como un destino de representación y un recurso de sombreador en distintos puntos en el tiempo.

Las texturas no se pueden enlazar para representarse directamente en la canalización; use una vista de destino de representación como se muestra en el ejemplo de código siguiente.


```
D3D10_RENDER_TARGET_VIEW_DESC rtDesc;
rtDesc.Format = desc.Format;
rtDesc.ViewDimension = D3D10_RTV_DIMENSION_TEXTURE2D;
rtDesc.Texture2D.MipSlice = 0;

ID3D10RenderTargetView *pRenderTargetView = NULL;
pDevice->CreateRenderTargetView( pRenderTarget, &rtDesc, &pRenderTargetView );
```



El formato de la vista render-target simplemente se establece en el formato de la textura original. La información del recurso debe interpretarse como una textura 2D y solo queremos usar el primer nivel de mapa mip del destino de representación.

De forma similar a cómo se debe crear una vista de destino de representación para que el destino de representación se pueda enlazar para la salida a la canalización, se debe crear una vista de recursos de sombreador para que el destino de representación se pueda enlazar a la canalización como una entrada. En el ejemplo de código siguiente se muestra esto.


```
// Create the shader-resource view
D3D10_SHADER_RESOURCE_VIEW_DESC srDesc;
srDesc.Format = desc.Format;
srDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
srDesc.Texture2D.MostDetailedMip = 0;
srDesc.Texture2D.MipLevels = 1;

ID3D10ShaderResourceView *pShaderResView = NULL;
pDevice->CreateShaderResourceView( pRenderTarget, &srDesc, &pShaderResView );
```



Los parámetros de las descripciones de vista de recursos de sombreador son muy similares a los de las descripciones de vista de destino de representación y se han elegido por las mismas razones.

### <a name="filling-textures-manually"></a>Rellenar texturas manualmente

A veces, a las aplicaciones les gustaría calcular valores en tiempo [](d3d10-graphics-programming-guide-pipeline-stages.md) de ejecución, colocarlos en una textura manualmente y, a continuación, hacer que la canalización de gráficos use esta textura en operaciones de representación posteriores. Para ello, la aplicación debe crear una textura vacía de tal manera que permita que la CPU acceda a la memoria subyacente. Para ello, se crea una textura dinámica y se obtiene acceso a la memoria subyacente mediante una llamada a un método determinado. En el ejemplo de código siguiente se muestra cómo utilizar este recurso.


```
D3D10_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DYNAMIC;
desc.BindFlags = D3D10_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
ID3D10Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



Tenga en cuenta que el formato se establece en 32 bits por píxel, donde cada componente se define mediante 8 bits. El parámetro usage se establece en dynamic mientras que las marcas de enlace se establecen para especificar que un sombreador tendrá acceso a la textura. El resto de la descripción de textura es similar a la creación de un destino de representación.

Llamar [**a Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) permite que la aplicación acceda a la memoria subyacente de la textura. A continuación, el puntero recuperado se usa para rellenar la textura con datos. Esto se puede ver en el ejemplo de código siguiente.


```
D3D10_MAPPED_TEXTURE2D mappedTex;
pTexture->Map( D3D10CalcSubresource(0, 0, 1), D3D10_MAP_WRITE_DISCARD, 0, &mappedTex );

UCHAR* pTexels = (UCHAR*)mappedTex.pData;
for( UINT row = 0; row < desc.Height; row++ )
{
    UINT rowStart = row * mappedTex.RowPitch;
    for( UINT col = 0; col < desc.Width; col++ )
    {
        UINT colStart = col * 4;
        pTexels[rowStart + colStart + 0] = 255; // Red
        pTexels[rowStart + colStart + 1] = 128; // Green
        pTexels[rowStart + colStart + 2] = 64;  // Blue
        pTexels[rowStart + colStart + 3] = 32;  // Alpha
    }
}

pTexture->Unmap( D3D10CalcSubresource(0, 0, 1) );
```



## <a name="multiple-rendertargets"></a>Varios destinos de representación

Se pueden enlazar hasta ocho vistas de destino de representación a la canalización a la vez [**(con OMSetRenderTargets).**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets) Para cada píxel (o cada ejemplo si está habilitado el multimuestreo), la combinación se realiza de forma independiente para cada vista de destino de representación. Dos de las variables de estado de mezcla( BlendEnable y RenderTargetWriteMask) son matrices de ocho, cada miembro de la matriz corresponde a una vista de destino de representación. Cuando se usan varios destinos de [](d3d10-graphics-programming-guide-resources-types.md) representación, cada destino de representación debe ser el mismo tipo de recurso (búfer, textura 1D, matriz de texturas 2D, etc.) y debe tener la misma dimensión (ancho, alto, profundidad para texturas 3D y tamaño de matriz para matrices de texturas). Si los destinos de representación son multimuestreo, todos deben tener el mismo número de muestras por píxel.

Solo puede haber un búfer de galería de símbolos de profundidad activo, independientemente de cuántos destinos de representación estén activos. Cuando se usan matrices de textura como destinos de representación, todas las dimensiones de vista deben coincidir. Los destinos de representación no necesitan tener el mismo formato de textura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
