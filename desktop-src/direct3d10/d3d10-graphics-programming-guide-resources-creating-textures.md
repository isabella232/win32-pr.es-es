---
description: Un recurso de textura es una colección estructurada de datos.
ms.assetid: 4c716be8-044e-4ed4-aeca-4379440826bd
title: Crear recursos de textura (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81f2ca200b566d17b02af56c48cb1227c41106ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000632"
---
# <a name="creating-texture-resources-direct3d-10"></a>Crear recursos de textura (Direct3D 10)

Un recurso de [textura](d3d10-graphics-programming-guide-resources-types.md) es una colección estructurada de datos. Normalmente, los valores de color se almacenan en texturas y se obtiene acceso a ellos durante la representación por parte de la [canalización](d3d10-graphics-programming-guide-pipeline-stages.md) en varias fases para la entrada y la salida. Crear texturas y definir cómo se usarán es una parte importante de la representación de escenas de aspecto interesante en Direct3D 10.

Aunque las texturas suelen contener información de color, la creación de texturas con un [**\_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) diferente les permite almacenar diferentes tipos de datos. Estos datos pueden ser aprovechados por la canalización de Direct3D 10 de formas no tradicionales.

Todas las texturas tienen límites en la cantidad de memoria que consumen y el número de textura que contienen. Estos límites se especifican mediante [constantes de recursos](d3d10-graphics-reference-resource-constants.md).

-   [Crear una textura a partir de un archivo](#create-a-texture-from-a-file)
    -   [Crear textura y vista por separado](#create-texture-and-view-separately)
    -   [Crear textura y ver simultáneamente](#create-texture-and-view-simultaneously)
-   [Crear texturas vacías](#creating-empty-textures)
    -   [Representar una textura](#rendering-to-a-texture)
    -   [Rellenar las texturas manualmente](#filling-textures-manually)
-   [Varios Rendertargets](#multiple-rendertargets)
-   [Temas relacionados](#related-topics)

## <a name="create-a-texture-from-a-file"></a>Crear una textura a partir de un archivo

> [!Note]  
> La [biblioteca de utilidades de D3DX](d3d10-graphics-reference-d3dx10.md) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.

 

Al crear una textura en Direct3D 10, también debe crear una [vista](d3d10-graphics-programming-guide-resources-access-views.md). Una vista es un objeto que indica al dispositivo cómo se debe tener acceso a una textura durante la representación. La forma más común de obtener acceso a una textura es leer desde ella mediante un [sombreador](../direct3dhlsl/dx-graphics-hlsl.md). Una vista de recursos de sombreador indicará a un sombreador cómo leer de una textura durante la representación. El tipo de vista que utilizará una textura debe especificarse al crearla.

La creación de una textura y la carga de los datos iniciales se pueden realizar de dos maneras diferentes: crear una textura y una vista por separado, o bien crear la textura y la vista al mismo tiempo. La API proporciona ambas técnicas para que pueda elegir lo que mejor se adapte a sus necesidades.

### <a name="create-texture-and-view-separately"></a>Crear textura y vista por separado

La forma más fácil de crear una textura es cargarla desde un archivo de imagen. Para crear la textura, solo tiene que rellenar una estructura y proporcionar el nombre de la textura a [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md).


```
ID3D10Device *pDevice = NULL;
// Initialize D3D10 device...

D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;

ID3D10Resource *pTexture = NULL;
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pTexture, NULL );
```



La función de D3DX [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) realiza tres cosas: en primer lugar, crea un objeto de textura de Direct3D 10. en segundo lugar, lee el archivo de imagen de entrada; en tercer lugar, almacena los datos de la imagen en el objeto de textura. En el ejemplo anterior, se carga un archivo BMP, pero la función puede cargar diversos tipos de archivo.

La marca de enlace indica que la textura se creará como un recurso de sombreador que permite que una fase del sombreador Lea la textura durante la representación.

En el ejemplo anterior no se especifican todos los parámetros de carga. De hecho, a menudo es beneficioso simplemente quitar los parámetros de carga, ya que permite a D3DX elegir los valores adecuados en función de la imagen de entrada. Si desea que la imagen de entrada determine todos los parámetros con los que se crea la textura, simplemente especifique **null** para el parámetro **loadInfo** de la siguiente manera:


```
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", NULL, NULL, &pTexture, NULL );
```



Especificar **null** para la información de carga es un método abreviado sencillo pero eficaz.

Ahora que se ha creado una textura, debe crear una vista de recursos de sombreador para que la textura se pueda enlazar como entrada a un sombreador. Puesto que [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) devuelve un puntero a un recurso y no un puntero a una textura, tiene que determinar el tipo exacto de recurso que se ha cargado y, a continuación, puede crear una vista de recursos del sombreador mediante [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).


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



Aunque en el ejemplo anterior se crea una vista de recursos de sombreador 2D, el código para crear otros tipos de vista de recursos de sombreador es muy similar. Cualquier fase del sombreador ahora puede utilizar esta textura como entrada.

El uso de [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) y [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview) para crear una textura y su vista asociada es una manera de preparar una textura que se va a enlazar a una fase de sombreador. Otra forma de hacerlo es crear tanto la textura como su vista al mismo tiempo, que se describe en la sección siguiente.

### <a name="create-texture-and-view-simultaneously"></a>Crear textura y ver simultáneamente

Direct3D 10 requiere una textura y una vista de recursos del sombreador para leer de una textura durante el tiempo de ejecución. Dado que la creación de una textura y una vista de recursos del sombreador es una tarea común, D3DX proporciona el [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) para que lo haga.


```
D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;

ID3D10ShaderResourceView *pSRView = NULL;
D3DX10CreateShaderResourceViewFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pSRView, NULL );
```



Con una única llamada de D3DX, se crean la vista de recursos y la textura. La funcionalidad del parámetro **loadInfo** no cambia; puede usarlo para personalizar cómo se crea la textura, o para derivar los parámetros necesarios del archivo de entrada especificando **null** para el parámetro **loadInfo** .

El objeto [**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview) devuelto por la función [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) se puede usar más adelante para recuperar la interfaz [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource) original si es necesario. Esto se puede hacer llamando al método [**getResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10view-getresource) .

D3DX proporciona una sola función para crear una vista de textura y de un sombreador de recursos como convienience; depende de usted decidir qué método de creación de una textura y vista se adapta mejor a las necesidades de la aplicación.

Ahora que sabe cómo crear una textura y su vista de recursos del sombreador, en la siguiente sección se muestra cómo se puede muestrear (leer) de esa textura mediante un sombreador.

## <a name="creating-empty-textures"></a>Crear texturas vacías

A veces, las aplicaciones querrán crear una textura y calcular los datos que se van a almacenar en la textura, o usar la [canalización](d3d10-graphics-programming-guide-pipeline-stages.md) de gráficos para representar esta textura y, posteriormente, usar los resultados en otro procesamiento. Estas texturas se pueden actualizar mediante la canalización de gráficos o la propia aplicación, en función del tipo de [**uso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) especificado para la textura cuando se creó.

### <a name="rendering-to-a-texture"></a>Representar una textura

El caso más común de crear una textura vacía que se rellenará con datos durante el tiempo de ejecución es el caso en el que una aplicación desea representar en una textura y, a continuación, utilizar los resultados de la operación de representación en un paso posterior. Las texturas creadas con este propósito deben especificar el [**uso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)predeterminado.

En el ejemplo de código siguiente se crea una textura vacía que la canalización puede representar y que posteriormente se usa como entrada para un [sombreador](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).


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



La creación de la textura requiere que la aplicación especifique información sobre las propiedades que tendrá la textura. El ancho y el alto de la textura en textura se establece en 256. Para este destino de representación, solo se necesita un único nivel de mipmap. Solo se requiere un destino de representación para que el tamaño de la matriz se establezca en 1. Cada textura contiene valores de punto flotante de 4 32 bits, que se pueden usar para almacenar información muy precisa ( [**consulte \_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)). Una muestra por píxel es todo lo que se necesitará. El uso se establece en el valor predeterminado porque permite la colocación más eficaz del destino de representación en la memoria. Por último, el hecho de que la textura se enlace como destino de representación y se especifica un recurso de sombreador en distintos puntos en el tiempo.

Las texturas no se pueden enlazar directamente a la representación de la canalización. Use una vista de representación y destino como se muestra en el ejemplo de código siguiente.


```
D3D10_RENDER_TARGET_VIEW_DESC rtDesc;
rtDesc.Format = desc.Format;
rtDesc.ViewDimension = D3D10_RTV_DIMENSION_TEXTURE2D;
rtDesc.Texture2D.MipSlice = 0;

ID3D10RenderTargetView *pRenderTargetView = NULL;
pDevice->CreateRenderTargetView( pRenderTarget, &rtDesc, &pRenderTargetView );
```



El formato de la vista de representación-destino se establece simplemente en el formato de la textura original. La información del recurso debe interpretarse como una textura 2D y solo queremos usar el primer nivel de mipmap del destino de representación.

De forma similar al modo en que se debe crear una vista de representación y destino para que el destino de representación se pueda enlazar para la salida a la canalización, se debe crear una vista de recursos del sombreador para que el destino de representación se pueda enlazar a la canalización como entrada. En el ejemplo de código siguiente se muestra esto.


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



Los parámetros de las descripciones de la vista de recursos y del sombreador son muy similares a los de las descripciones de vista de destino de representación y se eligieron por las mismas razones.

### <a name="filling-textures-manually"></a>Rellenar las texturas manualmente

A veces, las aplicaciones desean calcular valores en tiempo de ejecución, colocarlos en una textura manualmente y, a continuación, hacer que la [canalización](d3d10-graphics-programming-guide-pipeline-stages.md) de gráficos use esta textura en operaciones de representación posteriores. Para ello, la aplicación debe crear una textura vacía de tal forma que permita que la CPU tenga acceso a la memoria subyacente. Esto se hace creando una textura dinámica y obteniendo acceso a la memoria subyacente llamando a un método determinado. En el ejemplo de código siguiente se muestra cómo utilizar este recurso.


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



Tenga en cuenta que el formato se establece en 32 bits por píxel, donde cada componente se define mediante 8 bits. El parámetro Usage se establece en Dynamic mientras que las marcas de enlace se establecen para especificar que un sombreador tendrá acceso a la textura. El resto de la descripción de la textura es similar a crear un destino de representación.

La llamada a [**map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) permite que la aplicación tenga acceso a la memoria subyacente de la textura. A continuación, el puntero recuperado se usa para rellenar la textura con datos. Esto puede verse en el ejemplo de código siguiente.


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



## <a name="multiple-rendertargets"></a>Varios Rendertargets

Se pueden enlazar hasta ocho vistas de destino de representación a la canalización a la vez (con [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)). Para cada píxel (o cada ejemplo si el muestreo múltiple está habilitado), la combinación se realiza de forma independiente para cada vista de destino de representación. Dos de las variables de estado de Blend-BlendEnable y RenderTargetWriteMask-son matrices de ocho, cada miembro de la matriz corresponde a una vista de representación-destino. Cuando se usan varios destinos de representación, cada destino de representación debe ser del mismo [tipo de recurso](d3d10-graphics-programming-guide-resources-types.md) (búfer, textura 1D, matriz de textura 2D, etc.) y debe tener la misma dimensión (ancho, alto, profundidad para las texturas 3D y tamaño de la matriz para las matrices de texturas). Si los destinos de representación tienen varias muestras, todos deben tener el mismo número de muestras por píxel.

Solo puede haber un búfer de estarcido de profundidad activo, independientemente del número de destinos de representación que estén activos. Al usar matrices de textura como destinos de representación, todas las dimensiones de la vista deben coincidir. No es necesario que los destinos de representación tengan el mismo formato de textura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
