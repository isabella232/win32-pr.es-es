---
title: Configuración del entorno de programación de Direct3D 12
description: Describe la instalación, las herramientas y las bibliotecas admitidas que son un entorno de desarrollo productivo de Direct3D 12.
ms.assetid: B2288866-E95F-46B8-A7A1-19888F029C03
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee39dc1f99f2c99f911a52b211075b7d210b698
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813046"
---
# <a name="direct3d-12-programming-environment-setup"></a>Configuración del entorno de programación de Direct3D 12

Describe la instalación, las herramientas y las bibliotecas admitidas que son un entorno de desarrollo productivo de Direct3D 12.

-   [Entorno de desarrollo](#development-environment)
-   [Idiomas admitidos](#supported-languages)
-   [Estructuras auxiliares](#helper-structures)
-   [Biblioteca de administración de memoria](#memory-management-library)
-   [Herramientas y bibliotecas admitidas](#supported-tools-and-libraries)
-   [Ejemplos](#samples)
-   [Capa de depuración](#debug-layer)
-   [Vídeos educativos](#educational-videos)
-   [Temas relacionados](#related-topics)

## <a name="development-environment"></a>Entorno de desarrollo

Los encabezados y bibliotecas de Direct3D 12 forman parte del SDK Windows 10. No se requiere ninguna descarga o instalación independiente para usar Direct3D 12.

Después de instalar el software Windows 10 SDK y Visual Studio, se completa la configuración del entorno de programación de Direct3D 12. Visual Studio se recomienda 2019, ya que incluirá las herramientas de depuración de gráficos D3D12, pero las versiones anteriores de Visual Studio funcionarán para el desarrollo de programas.

Para usar la API de [Direct3D 12,](direct3d-12-reference.md)incluya D3d12.h y el vínculo a D3d12.lib, o consulte los puntos de entrada directamente en D3d12.dll.

Están disponibles los siguientes encabezados y bibliotecas. La ubicación de las bibliotecas estáticas depende de la versión (de 32 o 64 bits) de Windows 10 que se ejecuta en el equipo.



| Nombre de archivo de encabezado o biblioteca | Descripción                         | Ubicación de instalación      |
|-----------------------------|-------------------------------------|-----------------------|
| D3d12.h                     | Encabezado de API de Direct3D 12              | %WindowsSdkDir \\ Incluir \% WindowsSDKVersion% \\ \um |
| D3d12.lib                   | Biblioteca estática de código auxiliar de LA API de Direct3D 12 | %WindowsSdkDir \\ Lib \% WindowsSDKVersion% \\ \um\arch |
| D3d12.dll                   | Biblioteca de API dinámica de Direct3D 12     | %WINDIR% \\ System32    |
| D3d12SDKLayers.h            | Encabezado de depuración de Direct3D 12            | %WindowsSdkDir \\ Incluir \% WindowsSDKVersion% \\ \um |
| D3d12SDKLayers.dll          | Biblioteca de depuración dinámica de Direct3D 12   | %WINDIR% \\ System32    |



## <a name="supported-languages"></a>Idiomas compatibles

C++ es el único lenguaje admitido para el desarrollo de Direct3D 12, no se admiteN C# ni otros lenguajes .NET.

## <a name="helper-structures"></a>Estructuras auxiliares

Hay una serie de estructuras auxiliares que, en particular, hacen que sea fácil inicializar una serie de estructuras D3D12. Estas estructuras y algunas funciones de utilidad se encuentran en el encabezado D3dx12.h. Este encabezado es de código abierto y un desarrollador puede modificarlo según sea necesario: descárbalo de la biblioteca auxiliar [D3D12](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) y consulte Estructuras y funciones auxiliares para [D3D12.](helper-structures-and-functions-for-d3d12.md)

## <a name="memory-management-library"></a>Biblioteca de administración de memoria

Hay disponible una biblioteca auxiliar de administración de memoria para su descarga que puede integrar en la aplicación para que coincida más estrechamente con el comportamiento de administración de memoria D3D11. Como biblioteca de administración de estilo D3D11, es más  eficaz con aplicaciones que siguen usando una estrategia de asignación de estilo de recursos confirmado. En concreto, la biblioteca debe considerarse un paso a paso que le permitirá volver en gran medida a la administración de memoria eficaz de D3D11 cuando se encuentra en escenarios con restricciones de memoria (por ejemplo, tarjetas de memoria de gama baja, 4k, configuración ultra, entre otros). Las API de D3D12 habilitan técnicas que permiten obtener una eficacia de memoria aún mejor que D3D11, aunque estas técnicas pueden ser difíciles y llevar mucho tiempo en implementarse.

Tenga en cuenta que esta biblioteca es un trabajo en curso y puede cambiar con el tiempo. Use los vínculos siguientes para acceder a la biblioteca y a los ejemplos.

-   [Biblioteca de inicio de residencia de D3D12](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries)

## <a name="supported-tools-and-libraries"></a>Herramientas y bibliotecas admitidas

Todas las bibliotecas siguientes se pueden usar con Direct3D 12.



| Biblioteca                                                                                 |  Propósito                                                                                                                                                                                                                                                                      | Documentación                                                                                                           |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Kit de herramientas de DirectX para DirectX 12](https://github.com/Microsoft/DirectXTK12) | Una colección sustancial de clases auxiliares para escribir código de C++ de Direct3D 12 para aplicaciones de plataforma universal de Windows (UWP), aplicaciones de escritorio Win32 para Windows 10 y Xbox One aplicaciones exclusivas.                                                                         | [Wiki de DirectX12TK](https://github.com/Microsoft/DirectXTK12/wiki)                                          |
| [DirectXTex](https://github.com/Microsoft/DirectXTex)                      | Use esto para leer y escribir archivos DDS y realizar varias operaciones de procesamiento de contenido de textura, como cambiar el tamaño, conversión de formato, generación de mapa mip, compresión de bloques para recursos de textura en tiempo de ejecución de Direct3D y conversión de mapa de alto a mapa normal. | [Wiki de DirectXTex](https://github.com/Microsoft/DirectXTex/wiki)                                            |
| [DirectXMesh](https://github.com/Microsoft/DirectXMesh)                   | Úsalo para realizar varias operaciones de procesamiento de contenido de geometría, como la generación de normales y fotogramas tangentes, cálculos de adyacencia de triángulos y optimización de caché de vértices.                                                                                | [Wiki de DirectXMesh](https://github.com/Microsoft/DirectXMesh/wiki)                                          |
| [DirectXMath](https://github.com/Microsoft/DirectXMath)                     | Un gran número de clases y métodos auxiliares para admitir vectores, escalares, matrices, cuaterniones y muchas otras operaciones matemáticas.                                                                                                                               | [Documentación de DirectXMath en MSDN](/windows/desktop/dxmath/ovw-xnamath-progguide) |
| [UVAtlas](https://github.com/Microsoft/UVAtlas)                         | Úsese esto para crear y empaquetar un atlas de textura de isochart.                                                                                                                                                                                                           | [Wiki de UVAtlas](https://github.com/Microsoft/UVAtlas/wiki)                                                  |



 

## <a name="samples"></a>Ejemplos

Para obtener una lista de ejemplos de D3D12 en funcionamiento y cómo buscarlos y ejecutarlos, consulte [Ejemplos de trabajo.](working-samples.md)

Para obtener información general sobre cómo agregar código para habilitar características concretas, consulte Los recorridos de código [D3D12](d3d12-code-walk-throughs.md).

## <a name="debug-layer"></a>Capa de depuración

La capa de depuración proporciona una amplia validación adicional de parámetros y coherencia (como validar la vinculación del sombreador y el enlace de recursos, validar la coherencia de los parámetros y notificar descripciones de errores).

> [!Note]  
> Por Windows 10, para crear un dispositivo que admita la capa de depuración, habilite la característica opcional "Herramientas de gráficos". Vaya al panel Configuración, en Sistema, Aplicaciones & características, Administrar características opcionales, Agregar una característica y, a continuación, busque "Herramientas de gráficos".

El encabezado necesario para admitir la capa de depuración, D3D12SDKLayers.h, se incluye de forma predeterminada desde d3d12.h.

Cuando la capa de depuración enumera pérdidas de memoria, genera una lista de punteros de interfaz de objeto junto con sus nombres descriptivos. El nombre descriptivo predeterminado es " &lt; sin nombre &gt; ". Puede establecer el nombre descriptivo mediante el [**método ID3D12Object::SetName.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname) Normalmente, debe compilar estas llamadas fuera de la versión de producción.

Se recomienda usar la capa de depuración para depurar las aplicaciones para asegurarse de que están limpias de errores y advertencias. La capa de depuración le ayuda a escribir código de Direct3D 12. Además, la productividad puede aumentar cuando se usa la capa de depuración porque puede ver inmediatamente las causas de errores de representación oscuros o incluso pantallas en negro en su origen. La capa de depuración proporciona advertencias para muchos problemas. Por ejemplo:

-   Se olvidó de establecer una textura, pero leía de ella en el sombreador de píxeles.
-   Profundidad de salida, pero no tienen ningún estado de galería de símbolos de profundidad enlazado.
-   Error al crear la textura con INVALIDARG.

Establezca el compilador para definir D3DCOMPILE DEBUG para que le diga al compilador HLSL que incluya información \_ de depuración en el blob del sombreador.

``` syntax
#define D3DCOMPILE_DEBUG 1
```

Para obtener más información sobre todas las interfaces y métodos de depuración, consulte la referencia [de la capa de depuración.](direct3d-12-sdklayers-reference.md)

Para obtener información general sobre el uso de la capa de depuración, consulte Descripción de la capa de depuración [D3D12](understanding-the-d3d12-debug-layer.md).

## <a name="educational-videos"></a>Vídeos educativos

Hay una serie de vídeos relacionados con Direct3D 12 y Windows 10 en tutoriales de vídeo de aprendizaje avanzado de [DirectX, incluidos](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)vídeos sobre herramientas de depuración de gráficos e informes de errores de gráficos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descripción de Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 