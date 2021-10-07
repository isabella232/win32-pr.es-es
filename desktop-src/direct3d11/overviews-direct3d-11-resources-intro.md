---
title: Introducción a un recurso en Direct3D 11
description: En este tema se presentan recursos de Direct3D, como búferes y texturas.
ms.assetid: 9e991ab0-9648-484a-9a2c-5391ee5abf20
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d20cc08ee291000c1a368561669867f923c18516
ms.sourcegitcommit: dd41f53d69561daf7841332db3f27428734d7342
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/06/2021
ms.locfileid: "129609873"
---
# <a name="introduction-to-a-resource-in-direct3d-11"></a>Introducción a un recurso en Direct3D 11

Los recursos son los bloques de creación de la escena. Contienen la mayoría de los datos que Usa Direct3D para interpretar y representar la escena. Los recursos son áreas en memoria a las que se puede acceder mediante la canalización de Direct3D. Los recursos contienen los siguientes tipos de datos: geometría, texturas, datos de sombreador. En este tema se presentan recursos de Direct3D, como búferes y texturas.

Puede crear recursos fuertemente tipos o sin tipo. puede controlar si los recursos tienen acceso de lectura y escritura. puede hacer que los recursos solo puedan acceder a la CPU, GPU o ambos. Se pueden activar hasta 128 recursos para cada fase de la canalización.

Direct3D garantiza que se devuelva cero para cualquier recurso al que se acceda fuera de los límites.

El ciclo de vida de un recurso de Direct3D es:

-   Cree un recurso mediante uno de los métodos de creación de la [**interfaz ID3D11Device.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)
-   Enlace un recurso a la canalización mediante un contexto y uno de los métodos establecidos de la [**interfaz ID3D11DeviceContext.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)
-   Desasigne un recurso mediante una llamada al [**método Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) de la interfaz de recurso.

Esta sección contiene los siguientes temas:

-   [Escritura fuerte frente a débil](#strong-vs-weak-typing)
-   [Vistas de recursos](#resource-views)
-   [Vistas sin procesar de búferes](#raw-views-of-buffers)
-   [Temas relacionados](#related-topics)

## <a name="strong-vs-weak-typing"></a>Escritura fuerte frente a débil

Hay dos maneras de especificar completamente el diseño (o la superficie de memoria) de un recurso:

-   Con tipo: especifique completamente el tipo cuando se cree el recurso.
-   Sin tipo: especifique completamente el tipo cuando el recurso esté enlazado a la canalización.

La creación de un recurso totalmente tipo restringe el recurso al formato con el que se creó. Esto permite que el tiempo de ejecución optimice el acceso, especialmente si el recurso se crea con marcas que indican que la aplicación no puede asignarlo. Los recursos creados con un tipo específico no se pueden reinterpretar mediante el mecanismo de vista a menos que el recurso se haya creado con la marca D3D10 \_ DDI \_ BIND \_ PRESENT. Si se establece D3D10 DDI BIND PRESENT, se pueden crear vistas de recursos de destino de representación o sombreador en estos recursos mediante cualquiera de los miembros con tipo completo de la familia adecuada, incluso si el recurso original se creó como totalmente con \_ \_ \_ tipo.

En un recurso de tipo menos, el tipo de datos es desconocido cuando se crea el recurso por primera vez. La aplicación debe elegir entre el tipo disponible menos formatos (vea [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)). Debe especificar el tamaño de la memoria que se va a asignar y si el tiempo de ejecución tendrá que generar los subtextos en un mapa mip. Sin embargo, el formato de datos exacto (si la memoria se interpretará como enteros, valores de punto flotante, enteros sin signo, etc.) no se determina hasta que el recurso se enlaza [a](#resource-views)la canalización con una vista de recursos . A medida que el formato de textura sigue siendo flexible hasta que la textura se enlaza a la canalización, el recurso se conoce como almacenamiento con tipos débiles. El almacenamiento con tipos débiles tiene la ventaja de que se puede reutilizar o reinterpretar en otro formato, siempre y cuando el número de componentes y el número de bits de cada componente sean los mismos en ambos formatos.

Un único recurso se puede enlazar a varias fases de canalización, siempre y cuando cada una tenga una vista única, que califica totalmente los formatos en cada ubicación. Por ejemplo, un recurso creado con el formato DXGI \_ FORMAT \_ R32G32B32A32 TYPELESS podría usarse como \_ DXGI \_ FORMAT \_ R32G32B32A32 FLOAT y \_ DXGI FORMAT \_ \_ R32G32B32A32A32 \_ UINT en diferentes ubicaciones de la canalización simultáneamente.

## <a name="resource-views"></a>Vistas de recursos

Los recursos se pueden almacenar en formatos de memoria de uso general para que se puedan compartir en varias fases de canalización. Una fase de canalización interpreta los datos de recursos mediante una vista. Una vista de recursos es conceptualmente similar a convertir los datos de recursos para que se puedan usar en un contexto determinado.

Una vista se puede usar con un recurso sin tipo. Es decir, puede crear un recurso en tiempo de compilación y declarar el tipo de datos cuando el recurso está enlazado a la canalización. Una vista creada para un recurso sin tipo siempre tiene el mismo número de bits por componente; la forma en que se interpretan los datos depende del formato especificado. El formato especificado debe ser de la misma familia que el formato sin tipo utilizado al crear el recurso. Por ejemplo, un recurso creado con el formato TYPELESS R8G8B8A8 no se puede ver como un recurso FLOAT de R32 aunque ambos formatos puedan tener el mismo tamaño en \_ \_ memoria.

Una vista también expone otras funcionalidades, como la capacidad de leer las superficies de profundidad o galería de símbolos en un sombreador, generar un mapa de cubo dinámico en un solo paso y representar simultáneamente en varios segmentos de un volumen.



| Interfaz de recursos                                             | Descripción                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)       | Acceder a un recurso de textura durante las pruebas de galería de símbolos de profundidad.                                       |
| [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)       | Acceda a un recurso de textura que se usa como destino de representación.                                    |
| [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)   | Acceder a un recurso de sombreador, como un búfer constante, un búfer de textura, una textura o un muestreador. |
| [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) | Acceder a un recurso desordenado mediante un sombreador de píxeles o un sombreador de proceso.                        |



 

## <a name="raw-views-of-buffers"></a>Vistas sin procesar de búferes

Puede pensar en un búfer sin procesar, que también se puede denominar búfer de direcciones de [bytes,](direct3d-11-advanced-stages-cs-resources.md)como una bolsa de bits a la que desea acceder sin procesar, es decir, un búfer al que puede acceder cómodamente a través de fragmentos de uno a cuatro valores de dirección sin tipo de 32 bits. Indica que desea obtener acceso sin procesar a un búfer (o una vista sin procesar de un búfer) al llamar a uno de los métodos siguientes para crear una vista para el búfer:

-   Para crear una vista de recursos de sombreador (SRV) en el búfer, llame a [**ID3D11Device::CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview) con la marca [**D3D11 \_ BUFFEREX \_ SRV \_ FLAG \_ RAW**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bufferex_srv_flag). Esta marca se especifica en el **miembro Flags** de la estructura [**D3D11 \_ BUFFEREX \_ SRV.**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_bufferex_srv) Establezca **D3D11 \_ BUFFEREX \_ SRV** en el miembro **BufferEx** de la estructura [**D3D11 \_ SHADER RESOURCE VIEW \_ \_ \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) a la que apunta el parámetro *pDesc* de **ID3D11Device::CreateShaderResourceView.** También se establece el valor bufferex de dimensión [**\_ \_ \_ SRV D3D11**](/previous-versions/windows/desktop/legacy/ff476217(v=vs.85)) en el miembro **ViewDimension** de **D3D11 \_ SHADER RESOURCE VIEW \_ \_ \_ DESC** para indicar que el SRV es una vista sin formato.
-   Para crear una vista de acceso no ordenado (UAV) al búfer, llame a [**ID3D11Device::CreateUnorderedAccessView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createunorderedaccessview) con la marca [**D3D11 \_ BUFFER \_ UAV \_ FLAG \_ RAW**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_buffer_uav_flag). Esta marca se especifica en el **miembro Flags** de la estructura [**D3D11 \_ BUFFER \_ UAV.**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_uav) Establezca **D3D11 \_ BUFFER \_ UAV** en el miembro **Buffer** de la estructura [**D3D11 \_ UNORDERED \_ ACCESS VIEW \_ \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_unordered_access_view_desc) a la que apunta el parámetro *pDesc* de **ID3D11Device::CreateUnorderedAccessView.** También se establece el valor [**D3D11 \_ UAV \_ DIMENSION \_ BUFFER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_uav_dimension) en el miembro **ViewDimension** de **D3D11 \_ UNORDERED \_ ACCESS VIEW \_ \_ DESC** para indicar que el UAV es una vista sin formato.

Puede usar los tipos de objeto [**HLSL ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) y [**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) al trabajar con búferes sin procesar.

Para crear una vista sin procesar en un búfer, primero debe llamar a [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) con la marca [**\_ \_ MISC \_ BUFFER ALLOW RAW \_ \_ \_ VIEWS de D3D11 RESOURCE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) para crear el recurso de búfer subyacente. Esta marca se especifica en el miembro **MiscFlags** de la estructura [**D3D11 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) a la que apunta el parámetro *pDesc* de **ID3D11Device::CreateBuffer.** No se puede combinar la marca DE BÚFER MISC DE RECURSOS D3D11 PERMITIR VISTAS SIN PROCESAR con EL BÚFER MISC DEL RECURSO [**D3D11 \_ \_ \_ \_ ESTRUCTURADO.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) **\_ \_ \_ \_ \_ \_** Además, si especifica [**D3D11 \_ BIND CONSTANT \_ \_ BUFFER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) en **BindFlags** de **D3D11 \_ BUFFER \_ DESC,** no puede especificar también **D3D11 \_ RESOURCE \_ MISC BUFFER ALLOW RAW \_ \_ \_ \_ VIEWS** in **MiscFlags**. Esto no es una limitación de solo las vistas sin procesar porque los búferes constantes ya tienen una restricción que no se puede combinar con ninguna otra vista.

Aparte de los casos no válidos anteriores, al crear un búfer con [**D3D11 \_ RESOURCE \_ MISC \_ BUFFER ALLOW RAW \_ \_ \_ VIEWS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag), no se limita la funcionalidad frente a no establecer **D3D11 \_ RESOURCE \_ MISC BUFFER ALLOW RAW \_ \_ \_ \_ VIEWS**. Es decir, puede usar este tipo de búfer para el acceso sin procesar de cualquier manera que sea posible con Direct3D. Si especifica la marca **D3D11 \_ RESOURCE \_ MISC \_ BUFFER ALLOW \_ \_ RAW \_ VIEWS** , solo aumentará la funcionalidad disponible.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos](overviews-direct3d-11-resources.md)
</dt> <dt>

[Nuevos tipos de recursos](direct3d-11-advanced-stages-cs-resources.md)
</dt> </dl>

 

 
