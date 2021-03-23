---
title: Configuración del entorno de programación de Direct3D 12
description: Describe la instalación, las herramientas y las bibliotecas admitidas que componen un entorno de desarrollo de Direct3D 12 productivo.
ms.assetid: B2288866-E95F-46B8-A7A1-19888F029C03
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e6af0d0a93d55f700478ec839f3864ee0efbcd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549179"
---
# <a name="direct3d-12-programming-environment-setup"></a>Configuración del entorno de programación de Direct3D 12

Describe la instalación, las herramientas y las bibliotecas admitidas que componen un entorno de desarrollo de Direct3D 12 productivo.

-   [Entorno de desarrollo](#development-environment)
-   [Idiomas admitidos](#supported-languages)
-   [Estructuras auxiliares](#helper-structures)
-   [Biblioteca de administración de memoria](#memory-management-library)
-   [Herramientas y bibliotecas compatibles](#supported-tools-and-libraries)
-   [Muestras](#samples)
-   [Nivel de depuración](#debug-layer)
-   [Vídeos educativos](#educational-videos)
-   [Temas relacionados](#related-topics)

## <a name="development-environment"></a>Entorno de desarrollo

Los encabezados y las bibliotecas de Direct3D 12 forman parte del SDK de Windows 10. No se requiere ninguna descarga o instalación independiente para usar Direct3D 12.

Después de instalar el software del SDK de Windows 10 y Visual Studio, se completa la configuración del entorno de programación de Direct3D 12. Se recomienda Visual Studio 2019, ya que incluirá las herramientas de depuración de gráficos de D3D12, pero las versiones anteriores de Visual Studio funcionarán para el desarrollo de programas.

Para usar la [API de Direct3D 12](direct3d-12-reference.md), incluya D3d12. h y vincule a D3d12. lib, o bien consulte los puntos de entrada directamente en D3d12.dll.

Están disponibles los siguientes encabezados y bibliotecas. La ubicación de las bibliotecas estáticas depende de la versión (32 bits o 64 bits) de Windows 10 que se ejecuta en el equipo.



| Nombre del archivo de encabezado o biblioteca | Descripción                         | Ubicación de instalación      |
|-----------------------------|-------------------------------------|-----------------------|
| D3d12. h                     | Encabezado de API de Direct3D 12              | % WindowsSdkDir \\ incluir \% WindowsSDKVersion% \\ \um |
| D3d12. lib                   | Biblioteca estática de código auxiliar de API de Direct3D 12 | % WindowsSdkDir \\ lib \% WindowsSDKVersion% \\ \um\arch |
| D3d12.dll                   | Biblioteca dinámica de Direct3D 12 API     | % WINDIR% \\ system32    |
| D3d12SDKLayers. h            | Encabezado de depuración de Direct3D 12            | % WindowsSdkDir \\ incluir \% WindowsSDKVersion% \\ \um |
| D3d12SDKLayers.dll          | Biblioteca de depuración dinámica de Direct3D 12   | % WINDIR% \\ system32    |



## <a name="supported-languages"></a>Idiomas compatibles

C++ es el único lenguaje compatible con el desarrollo de Direct3D 12, C# y otros lenguajes .NET no se admiten.

## <a name="helper-structures"></a>Estructuras auxiliares

Hay una serie de estructuras auxiliares que, en concreto, facilitan la inicialización de un número de estructuras D3D12. Estas estructuras y algunas funciones de utilidad se encuentran en el encabezado D3dx12. h. Este encabezado es de código abierto y puede ser modificado por un desarrollador según sea necesario. descárguelo de [la biblioteca auxiliar de D3D12](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12) y consulte [las estructuras y funciones auxiliares para D3D12](helper-structures-and-functions-for-d3d12.md).

## <a name="memory-management-library"></a>Biblioteca de administración de memoria

Hay disponible una biblioteca auxiliar de administración de memoria para su descarga que se puede integrar en la aplicación para que coincida mejor con el comportamiento de la administración de memoria de D3D11. Como biblioteca de administración de estilo D3D11, es más eficaz con las aplicaciones que siguen usando una estrategia de asignación de estilo de *recursos confirmados* . En particular, la biblioteca debe considerarse como una piedra de paso que le ayudará a la mayor parte de la manera de volver a la administración de memoria del rendimiento de D3D11 cuando se encuentran en escenarios con restricción de memoria (por ejemplo, tarjetas de memoria de low-end, 4k, configuración de ultra, etc.). Las API de D3D12 permiten técnicas que permiten obtener una mayor eficacia de la memoria con respecto a D3D11, aunque estas técnicas pueden suponer un reto y mucho tiempo de implementación.

Tenga en cuenta que esta biblioteca es un trabajo en curso y puede cambiar con el tiempo. Use los vínculos siguientes para obtener acceso a la biblioteca y ejemplos.

-   [La biblioteca de inicio de residencia de D3D12](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries)

## <a name="supported-tools-and-libraries"></a>Herramientas y bibliotecas compatibles

Se pueden usar las siguientes bibliotecas con Direct3D 12.



|                                                                                  |                                                                                                                                                                                                                                                                        |                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| **Library**                                                                      | **Propósito**                                                                                                                                                                                                                                                            | **Documentación**                                                                                          |
| [Kit de herramientas de DirectX para DirectX 12](https://github.com/Microsoft/DirectXTK12) | Colección sustancial de clases auxiliares para escribir código de C++ de Direct3D 12 para aplicaciones Plataforma universal de Windows (UWP), aplicaciones de escritorio de Win32 para Windows 10 y aplicaciones de Xbox One exclusivas.                                                                         | [DirectX12TK wiki](https://github.com/Microsoft/DirectXTK12/wiki)                                          |
| [DirectXTex](https://github.com/Microsoft/DirectXTex)                      | Úselo para leer y escribir archivos DDS, y para realizar diversas operaciones de procesamiento de contenido de texturas, como el cambio de tamaño, la conversión de formato, la generación de mapas de MIP, la compresión de bloques para los recursos de textura en tiempo de ejecución de Direct3D y el mapa de bits a la conversión de asignación normal. | [DirectXTex wiki](https://github.com/Microsoft/DirectXTex/wiki)                                            |
| [DirectXMesh](https://github.com/Microsoft/DirectXMesh)                   | Úselo para realizar diversas operaciones de procesamiento de contenido de geometría, incluida la generación de tramas normales y tangentes, cálculos de adyacencia de triangulación y optimización de la caché de vértices.                                                                                | [DirectXMesh wiki](https://github.com/Microsoft/DirectXMesh/wiki)                                          |
| [DirectXMath](https://github.com/Microsoft/DirectXMath)                     | Un gran número de métodos y clases auxiliares para admitir vectores, escalares, matrices, cuaterniones y muchas otras operaciones matemáticas.                                                                                                                               | [Documentación de DirectXMath en MSDN](/windows/desktop/dxmath/ovw-xnamath-progguide) |
| [UVAtlas](https://github.com/Microsoft/UVAtlas)                         | Úselo para crear y empaquetar un Atlas de texturas isográfico.                                                                                                                                                                                                           | [UVAtlas wiki](https://github.com/Microsoft/UVAtlas/wiki)                                                  |



 

## <a name="samples"></a>Ejemplos

Para obtener una lista de ejemplos de D3D12 de trabajo y cómo localizarlos y ejecutarlos, consulte los [ejemplos de trabajo](working-samples.md).

Para ver Tutoriales sobre cómo agregar código para habilitar características concretas, consulte [tutoriales de código D3D12](d3d12-code-walk-throughs.md).

## <a name="debug-layer"></a>Nivel de depuración

La capa de depuración proporciona un amplio parámetro adicional y una validación de coherencia (como la validación de la vinculación del sombreador y el enlace de recursos, la validación de la coherencia de los parámetros y la notificación de descripciones

> [!Note]  
> En Windows 10, para crear un dispositivo que admita la capa de depuración, habilite la característica opcional "herramientas de gráficos". Vaya al panel de configuración, en sistema, aplicaciones & características, administrar características opcionales, agregar una característica y, a continuación, busque "herramientas de gráficos".

El encabezado necesario para admitir la capa de depuración, D3D12SDKLayers. h, se incluye de forma predeterminada en d3d12. h.

Cuando la capa de depuración enumera las pérdidas de memoria, genera una lista de punteros de interfaz de objetos junto con sus nombres descriptivos. El nombre descriptivo predeterminado es "sin &lt; nombre &gt; ". Puede establecer el nombre descriptivo mediante el método [**ID3D12Object:: setName**](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname) . Normalmente, debe compilar estas llamadas fuera de la versión de producción.

Se recomienda usar la capa de depuración para depurar las aplicaciones con el fin de asegurarse de que están limpias de errores y advertencias. La capa de depuración le ayuda a escribir código de Direct3D 12. Además, la productividad puede aumentar al usar la capa de depuración, ya que puede ver inmediatamente las causas de los errores de representación ocultos o incluso las pantallas negras en su origen. El nivel de depuración proporciona advertencias para muchos problemas. Por ejemplo:

-   Olvidó establecer una textura pero leerla en el sombreador de píxeles.
-   Profundidad de salida, pero no tiene ningún límite de estado de estarcido de profundidad.
-   Error de creación de textura con INVALIDARG.

Establezca el compilador definir D3DCOMPILE \_ Debug para indicar al compilador de HLSL que incluya información de depuración en el BLOB del sombreador.

``` syntax
#define D3DCOMPILE_DEBUG 1
```

Para obtener detalles de todas las interfaces y métodos de depuración, consulte la referencia de la [capa de depuración](direct3d-12-sdklayers-reference.md).

Para obtener información general sobre el uso de la capa de depuración, consulte [Descripción de la capa de depuración D3D12](understanding-the-d3d12-debug-layer.md).

## <a name="educational-videos"></a>Vídeos educativos

Hay una serie de vídeos relacionados con Direct3D 12 y Windows 10 en los [tutoriales de vídeo de aprendizaje avanzado de DirectX](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA), incluidos los vídeos sobre las herramientas de depuración de gráficos y la generación de informes de errores de gráficos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descripción de Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 