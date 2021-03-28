---
title: Introducción a un recurso en Direct3D 11
description: En este tema se presentan recursos de Direct3D como búferes y texturas.
ms.assetid: 9e991ab0-9648-484a-9a2c-5391ee5abf20
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb466883991795a66eec0ba1b99f5c989fa33c1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421043"
---
# <a name="introduction-to-a-resource-in-direct3d-11"></a>Introducción a un recurso en Direct3D 11

Los recursos son los bloques de creación de la escena. Contienen la mayoría de los datos que usa Direct3D para interpretar y representar la escena. Los recursos son áreas de memoria a las que se puede tener acceso a través de la canalización de Direct3D. Los recursos contienen los siguientes tipos de datos: geometría, texturas, datos de sombreador. En este tema se presentan recursos de Direct3D como búferes y texturas.

Puede crear recursos fuertemente tipados o sin tipo. puede controlar si los recursos tienen acceso de lectura y escritura. puede hacer que los recursos sean accesibles solo para la CPU, la GPU o ambos. Se pueden activar hasta 128 recursos para cada fase de la canalización.

Direct3D garantiza que se devuelva cero para cualquier recurso al que se tenga acceso fuera de los límites.

El ciclo de vida de un recurso de Direct3D es:

-   Cree un recurso con uno de los métodos de creación de la interfaz [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .
-   Enlazar un recurso a la canalización mediante un contexto y uno de los métodos set de la interfaz [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .
-   Desasigne un recurso llamando al método [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) de la interfaz de recursos.

Esta sección contiene los siguientes temas:

-   [Sólida frente al establecimiento débil](#strong-vs-weak-typing)
-   [Vistas de recursos](#resource-views)
-   [Vistas sin procesar de búferes](#raw-views-of-buffers)
-   [Temas relacionados](#related-topics)

## <a name="strong-vs-weak-typing"></a>Sólida frente al establecimiento débil

Hay dos maneras de especificar por completo el diseño (o la superficie de memoria) de un recurso:

-   Typed: especifique completamente el tipo cuando se crea el recurso.
-   Sin tipo: especifique completamente el tipo cuando el recurso se enlaza a la canalización.

Al crear un recurso totalmente tipado, se restringe el recurso al formato con el que se creó. Esto permite al motor en tiempo de ejecución optimizar el acceso, especialmente si el recurso se crea con marcas que indican que la aplicación no puede asignarlo. Los recursos creados con un tipo específico no se pueden volver a interpretar con el mecanismo de vista a menos que el recurso se haya creado con la \_ marca de presentación de enlace DDI D3D10 \_ \_ . Si D3D10 \_ DDI \_ BIND \_ present es Set, se pueden crear vistas de recursos de sombreador o de representación en estos recursos mediante cualquiera de los miembros totalmente tipados de la familia adecuada, incluso si el recurso original se ha creado como un tipo completo.

En un recurso de tipo menos, se desconoce el tipo de datos cuando el recurso se crea por primera vez. La aplicación debe elegir entre los formatos de tipo disponibles menos ( [**consulte \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)). Debe especificar el tamaño de la memoria que se va a asignar y si el tiempo de ejecución necesitará generar las subtexturas en un mipmap. Sin embargo, el formato de datos exacto (si la memoria se interpreta como enteros, valores de punto flotante, enteros sin signo, etc.) no se determina hasta que el recurso se enlaza a la canalización con una [vista de recursos](#resource-views). Dado que el formato de textura sigue siendo flexible hasta que la textura se enlaza a la canalización, el recurso se denomina almacenamiento débilmente tipado. El almacenamiento débilmente tipado tiene la ventaja de que se puede reutilizar o reinterpretar en otro formato, siempre que el número de componentes y el recuento de bits de cada componente sea el mismo en ambos formatos.

Un solo recurso se puede enlazar a varias fases de canalización, siempre y cuando cada una tenga una vista única, que califique por completo los formatos en cada ubicación. Por ejemplo, un recurso creado con el formato DXGI \_ format \_ R32G32B32A32 \_ no puede usarse como un formato de \_ dxgi \_ R32G32B32A32 \_ float y un formato de dxgi \_ \_ R32G32B32A32 \_ uint en diferentes ubicaciones de la canalización simultáneamente.

## <a name="resource-views"></a>Vistas de recursos

Los recursos se pueden almacenar en formatos de memoria de uso general para que puedan compartirse en varias fases de canalización. Una fase de canalización interpreta los datos de recursos mediante una vista. Una vista de recursos es conceptualmente similar a la conversión de los datos de recursos para que se pueda usar en un contexto determinado.

Una vista se puede usar con un recurso sin tipo. Es decir, puede crear un recurso en tiempo de compilación y declarar el tipo de datos cuando el recurso se enlaza a la canalización. Una vista creada para un recurso sin tipo siempre tiene el mismo número de bits por componente; la forma en que se interpretan los datos depende del formato especificado. El formato especificado debe ser de la misma familia que el formato sin tipo utilizado al crear el recurso. Por ejemplo, un recurso creado con el \_ formato sin tipo R8G8B8A8 no se puede ver como un recurso Float de R32, aunque \_ ambos formatos tengan el mismo tamaño en la memoria.

Una vista también expone otras funciones, como la capacidad de leer las superficies de fondo o de la galería de símbolos en un sombreador, generar un mapa dinámico en un solo paso y representar simultáneamente en varios segmentos de un volumen.



| Interfaz de recursos                                             | Descripción                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)       | Acceder a un recurso de textura durante las pruebas de la galería de símbolos de profundidad.                                       |
| [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)       | Acceder a un recurso de textura que se usa como destino de representación.                                    |
| [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)   | Acceder a un recurso de sombreador como un búfer de constantes, un búfer de textura, una textura o una muestra. |
| [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) | Acceder a un recurso no ordenado mediante un sombreador de píxeles o un sombreador de cálculo.                        |



 

## <a name="raw-views-of-buffers"></a>Vistas sin procesar de búferes

Puede pensar en un búfer sin formato, que también se puede llamar [búfer de direcciones de bytes](direct3d-11-advanced-stages-cs-resources.md), como un contenedor de bits al que desea tener acceso sin formato, es decir, un búfer que puede acceder de forma cómoda a través de fragmentos de uno a valores de dirección sin tipo de 4 32 bits. Indica que desea tener acceso sin formato a un búfer (o una vista sin formato de un búfer) cuando se llama a uno de los métodos siguientes para crear una vista en el búfer:

-   Para crear una vista de recursos del sombreador (SRV) para el búfer, llame a [**ID3D11Device:: CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview) con la marca [**D3D11 \_ BUFFEREX \_ SRV \_ \_ sin formato**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bufferex_srv_flag). Esta marca se especifica en el miembro **Flags** de la estructura [**D3D11 \_ BUFFEREX \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_bufferex_srv) . Establezca **D3D11 \_ BUFFEREX \_ SRV** en el miembro **BUFFEREX** de la estructura [**DESC de la \_ \_ \_ vista de \_ recursos del sombreador D3D11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) en la que el parámetro *pDesc* de **ID3D11Device:: CreateShaderResourceView** . También se establece el valor BUFFEREX de la [**\_ \_ dimensión \_ D3D11 SRV**](/previous-versions/windows/desktop/legacy/ff476217(v=vs.85)) en el miembro **ViewDimension** de la **vista de \_ recursos del sombreador \_ \_ \_ D3D11** para indicar que el SRV es una vista sin formato.
-   Para crear una vista de acceso desordenado (UAV) en el búfer, llame a [**ID3D11Device:: CreateUnorderedAccessView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createunorderedaccessview) con la marca [**D3D11 \_ buffer \_ UAV \_ \_ raw**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_buffer_uav_flag). Esta marca se especifica en el miembro **Flags** de la estructura [**\_ \_ UAV del búfer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_uav) . El **búfer de \_ D3D11 \_** se establece en el miembro de **búfer** de la estructura de DESC de la [**\_ \_ vista de acceso \_ \_ desordenado de D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_unordered_access_view_desc) a la que apunta el parámetro *pDesc* de **ID3D11Device:: CreateUnorderedAccessView** . También se establece el valor del [**búfer de dimensiones de D3D11 \_ \_ \_ UAV**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_uav_dimension) en el miembro **ViewDimension** de **D3D11 \_ Unordered \_ Access \_ View \_ DESC** para indicar que UAV es una vista sin formato.

Puede usar los tipos de objeto [**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) y [**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) de HLSL al trabajar con búferes sin procesar.

Para crear una vista sin formato en un búfer, primero debe llamar a [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) con la marca [**D3D11 de \_ recurso \_ \_ adicional \_ permitir \_ \_ vistas sin formato**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) para crear el recurso de búfer subyacente. Esta marca se especifica en el miembro **MiscFlags** de la [**estructura \_ \_ DESC del búfer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) al que apunta el parámetro *pDesc* de **ID3D11Device:: CreateBuffer** . No se puede combinar la marca del **\_ búfer Misceláneo de recursos D3D11 \_ \_ \_ permitir \_ \_ vistas sin formato** con el [**\_ búfer Misceláneo de recursos D3D11 \_ \_ \_ estructurado**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag). Además, si especifica el [**\_ búfer de \_ constantes \_ de BIND de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) en **BindFlags** de la **\_ \_ Descripción del búfer de D3D11**, no puede especificar el búfer adicional de **D3D11 \_ recursos \_ misceláneos \_ \_ permitir \_ \_ vistas sin procesar** en **MiscFlags**. Esto no es una limitación de las vistas sin formato, ya que los búferes de constantes ya tienen una restricción que no se pueden combinar con ninguna otra vista.

Aparte de los casos no válidos anteriores, cuando se crea un búfer con el [**\_ búfer diverso del recurso D3D11 se \_ \_ \_ permite \_ \_ vistas sin formato**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag), no hay limitación en cuanto a la funcionalidad en lugar de establecer el **\_ búfer misceláneo del recurso D3D11 \_ \_ \_ permitir \_ \_ vistas sin procesar**. Es decir, puede usar este tipo de búfer para el acceso no sin formato de varias maneras posibles con Direct3D. Si especifica la marca **D3D11 \_ Resource \_ Misc ( \_ búfer adicional \_ permitir \_ \_ vistas sin formato** ), solo aumentará la funcionalidad disponible.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos](overviews-direct3d-11-resources.md)
</dt> <dt>

[Nuevos tipos de recursos](direct3d-11-advanced-stages-cs-resources.md)
</dt> </dl>

 

 