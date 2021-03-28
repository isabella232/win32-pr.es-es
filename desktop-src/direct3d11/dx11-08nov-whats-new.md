---
title: Novedades de la versión de noviembre de 2008 de Direct3D 11 Tech Preview
description: Esta versión de Direct3D 11 contiene nuevas características, herramientas y documentación.
ms.assetid: 7d259764-b826-4609-b415-2093cc6df874
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a49529882eafaf092a866d1b172de62fe15c8e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420765"
---
# <a name="whats-new-in-the-nov-2008-direct3d-11-tech-preview"></a>Novedades de la versión de noviembre de 2008 de Direct3D 11 Tech Preview

Esta versión de Direct3D 11 contiene nuevas características, herramientas y documentación.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>Tesela<br/></td>
<td>Direct3D 11 proporciona fases de canalización adicionales para admitir <a href="direct3d-11-advanced-stages-tessellation.md">la teselación en tiempo real</a> de primitivas de orden superior. Gracias a las capacidades de programación exhaustivas, esta característica permite muchos métodos diferentes para evaluar superficies de orden superior, incluidas las superficies de subdivisión mediante técnicas de aproximación, revisiones de Bézier, Teselación adaptativa y asignación de desplazamiento. Esta característica solo estará disponible en el hardware de clase de Direct3D 11, por lo que para evaluar esta característica tendrá que usar el rasterizador de referencia. Para obtener una demostración de teselación en acción, consulte el ejemplo <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">SubD11</a> disponible en el explorador de ejemplo.<br/></td>
</tr>
<tr class="even">
<td><span id="Compute_Shader"></span><span id="compute_shader"></span><span id="COMPUTE_SHADER"></span>Sombreador de cálculo<br/></td>
<td>El <a href="direct3d-11-advanced-stages-compute-shader.md">sombreador de cálculo</a> es una fase adicional independiente de la canalización de Direct3D 11 que habilita la informática de uso general en la GPU. Además de todas las características de sombreador proporcionadas por el núcleo del sombreador unificado, el sombreador de cálculo también admite lecturas y escrituras distribuidas en los recursos a través de vistas de acceso desordenado, un grupo de memoria compartido dentro de un grupo de subprocesos en ejecución, primitivas de sincronización, operadores atómicos y muchas otras características avanzadas de datos en paralelo. En esta versión, se ha habilitado una variante del sombreador de cálculo de Direct3D 11, que puede funcionar en hardware de clase de Direct3D 10. Por lo tanto, es posible desarrollar sombreadores de cálculo en hardware real, pero se requiere un controlador actualizado. La funcionalidad completa del sombreador de cálculo de Direct3D 11 está destinada a la compatibilidad con el hardware de clase de Direct3D 11, por lo que para evaluar la funcionalidad completa, tendrá que usar el rasterizador de referencia hasta que dicho hardware esté disponible. Para obtener una demostración del sombreador de cálculo en acción, consulte el ejemplo <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">HDRToneMappingCS11</a> disponible en el explorador de ejemplo.<br/></td>
</tr>
<tr class="odd">
<td><span id="Multithreaded_Rendering"></span><span id="multithreaded_rendering"></span><span id="MULTITHREADED_RENDERING"></span>Representación multiproceso<br/></td>
<td>La diferencia clave de API de Direct3D 10 en Direct3D 11 es la adición de <a href="overviews-direct3d-11-render-multi-thread.md">contextos aplazados</a>, que permite la ejecución escalable de comandos de Direct3D distribuidos en varios núcleos. Un contexto diferido captura y ensambla acciones, como los cambios de estado, y dibuja envíos que se pueden ejecutar en el dispositivo real en un momento posterior. Mediante el uso de contextos diferidos en varios subprocesos, una aplicación puede distribuir la sobrecarga de CPU necesaria en el tiempo de ejecución de Direct3D 11 y el controlador a varios núcleos, lo que permite un mejor uso de la configuración de la máquina del usuario final. Esta característica está disponible para su uso en el hardware actual de Direct3D 10, así como en el rasterizador de referencia. Para obtener una demostración del uso de la API, consulte el ejemplo de <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">MultithreadedRendering11</a> disponible en el explorador de ejemplo.<br/></td>
</tr>
<tr class="even">
<td><span id="Dynamic_Shader_Linkage_"></span><span id="dynamic_shader_linkage_"></span><span id="DYNAMIC_SHADER_LINKAGE_"></span>Vinculación dinámica del sombreador <br/></td>
<td>Para solucionar el problema de explosión de la combinatoria que se ve en los sombreadores especializados para el rendimiento, Direct3D 11 presenta una forma limitada de <a href="/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking">vinculación del sombreador</a> en tiempo de ejecución que permite una especialización de sombreador casi óptima durante la ejecución de una aplicación. Esto se consigue especificando las implementaciones de funciones específicas en el código del sombreador cuando se asigna el sombreador a la canalización, lo que permite al controlador insertar instrucciones de sombreador nativas rápidamente en lugar de forzar al controlador a volver a compilar el lenguaje intermedio en instrucciones nativas con la nueva configuración. El desarrollo del sombreador se expone a través de la introducción de clases e interfaces a HLSL. Para obtener una demostración, consulte el ejemplo de <a href="https://msdn.microsoft.com/library/Ee416565(v=VS.85).aspx">vinculación dinámica de sombreador 11</a> disponible a través del explorador de ejemplo.<br/></td>
</tr>
<tr class="odd">
<td><span id="Windows_Advanced_Rasterizer__WARP_"></span><span id="windows_advanced_rasterizer__warp_"></span><span id="WINDOWS_ADVANCED_RASTERIZER__WARP_"></span>Rasterizador avanzado de Windows (WARP)<br/></td>
<td>Disponible en este SDK a través de Direct3D 11 y, a la larga, también a través de Direct3D 10,1, WARP es un rasterizador de escalado rápido de varios núcleos totalmente compatible con Direct3D 10,1. Usar esta tecnología es tan sencillo como pasar la marca D3D_DRIVER_TYPE_WARP en la creación del dispositivo.<br/></td>
</tr>
<tr class="even">
<td><span id="Direct3D_10_and_Direct3D_11_on_Direct3D_9_Hardware__D3D10_Level_9_"></span><span id="direct3d_10_and_direct3d_11_on_direct3d_9_hardware__d3d10_level_9_"></span><span id="DIRECT3D_10_AND_DIRECT3D_11_ON_DIRECT3D_9_HARDWARE__D3D10_LEVEL_9_"></span>Direct3D 10 y Direct3D 11 en hardware de Direct3D 9 (D3D10 nivel 9)<br/></td>
<td>Disponible en este SDK a través de Direct3D 11 y, a la larga, también a través de Direct3D 10,1, la API de Direct3D puede tener como destino la mayoría del hardware de Direct3D 9, así como el hardware de Direct3D 10, Direct3D 10,1 y Direct3D 11. Esto se consigue proporcionando el mecanismo de nivel de característica, que agrupa el hardware en seis categorías en función de la funcionalidad: 9_1, 9_2, 9_3, 10_0, 10_1 y 11_0. Una tarjeta solo cumple un nivel de característica si es totalmente compatible con ese nivel, y cada nivel es un supraconjunto estricto de los siguientes. La funcionalidad se emula mínimamente para garantizar que no se encuentren acantilados de rendimiento inesperados. Por lo tanto, las características como los sombreadores de geometría no están disponibles para los destinos de nivel de Direct3D 9. <br/></td>
</tr>
<tr class="odd">
<td><span id="Runtime_Binaries"></span><span id="runtime_binaries"></span><span id="RUNTIME_BINARIES"></span>Binarios en tiempo de ejecución<br/></td>
<td>Todos los archivos binarios en tiempo de ejecución proporcionados en Direct3D 11 Tech Preview que estarán disponibles en Windows 7 y Windows Vista SP1 se instalan con el SDK y se etiquetan como &quot; &quot; componentes beta (es decir, D3D11_beta.DLL). Todos los componentes con etiqueta beta tienen un tiempo limitado. Para crear proyectos para evaluar estos nuevos componentes, debe vincular a sus bibliotecas de importación de etiquetas de la versión beta equivalentes (es decir, D3D11_beta. lib). Si tiene una copia de PDC de Windows 7, los encabezados, las bibliotecas y los PDB proporcionados en la Windows SDK con la compilación son adecuados para el desarrollo con los componentes de Direct3D 11 que proporcionan en Windows 7. Reserve el uso de los encabezados, las bibliotecas y los PDB de este SDK a los componentes beta que se proporcionan aquí.<br/></td>
</tr>
<tr class="even">
<td><span id="D3DX11"></span><span id="d3dx11"></span>D3DX11<br/></td>
<td>D3DX11 admite actualmente la carga de texturas, la compilación del sombreador, la carga de datos y las funciones de subproceso de trabajo para los recursos de Direct3D 11. En el futuro, este componente proporcionará más tecnologías disponibles en D3DX10. La funcionalidad de compilación del sombreador también se proporciona directamente a través del componente del compilador de Direct3D, que se describe a continuación.<br/></td>
</tr>
<tr class="odd">
<td><span id="HLSL_and_Direct3D_Compiler"></span><span id="hlsl_and_direct3d_compiler"></span><span id="HLSL_AND_DIRECT3D_COMPILER"></span>HLSL y el compilador de Direct3D<br/></td>
<td>El compilador de HLSL tiene varias características nuevas para admitir las nuevas tecnologías disponibles en Direct3D 11. Esto incluye la programación orientada a objetos a través de interfaces y clases, una sintaxis de indización directa para las cargas de recursos y la palabra clave "precise" para garantizar que todas las operaciones realizadas con una variable específica cumplan las reglas de punto flotante estrictas. Casi todas las características lingüísticas nuevas tienen una funcionalidad válida en destinos de sombreador existentes. Además de admitir todos los sombreadores de Direct3D 9, Direct3D 10, Direct3D 10,1 y Direct3D 11, el compilador de HLSL también admite los destinos especiales necesarios para escribir sombreadores para los destinos de nivel 9 de Direct3D 10. Ahora, el compilador D3D es accesible directamente fuera de D3DX10 y D3DX11 a través de D3DCompiler. H y D3DCompiler. lib. Con estos nuevos archivos, no es necesario que una aplicación vincule a D3DX para realizar la compilación en tiempo de ejecución, y no es necesario que una aplicación incluya el compilador si solo se necesita la funcionalidad de D3DX.<br/></td>
</tr>
<tr class="even">
<td><span id="D3D11_Reference_Rasterizer"></span><span id="d3d11_reference_rasterizer"></span><span id="D3D11_REFERENCE_RASTERIZER"></span>Rasterizador de referencia de D3D11<br/></td>
<td>El rasterizador de referencia proporciona una implementación de rasterización estándar Gold para la evaluación de características de Direct3D 11 que todavía no están disponibles en el hardware. El rasterizador de referencia también se proporciona como una manera de comprobar la precisión de una implementación de hardware específica en el estándar de rasterización. El rasterizador de referencia está diseñado para que sea correcto, no el rendimiento. Para crear un dispositivo de referencia, solo tiene que pasar la marca D3D_DRIVER_TYPE_REFERENCE en la creación del dispositivo. <br/></td>
</tr>
<tr class="odd">
<td><span id="D3D11_SDK_Layers"></span><span id="d3d11_sdk_layers"></span><span id="D3D11_SDK_LAYERS"></span>Capas de SDK de D3D11<br/></td>
<td>Los niveles del SDK de Direct3D 11 proporcionan un mecanismo para realizar el seguimiento del funcionamiento del tiempo de ejecución de Direct3D 11 durante el desarrollo. Actualmente se usa para proporcionar información de depuración útil, que no solo incluye errores de uso inadecuado, sino también advertencias que recomiendan el uso de los procedimientos recomendados del tiempo de ejecución y, a menudo, proporcionan información detallada y útil para la depuración. Se recomienda encarecidamente que la salida de depuración de las capas del SDK de D3D11 esté activada en todo momento durante el desarrollo y que una aplicación no genere una salida de depuración durante la ejecución antes de que se libere o use con PIX para Windows para la generación de perfiles. Habilitar la capa de depuración es tan sencillo como pasar la marca D3D11_CREATE_DEVICE_DEBUG en el momento de la creación del dispositivo. Se recomienda encarecidamente a los desarrolladores que utilicen capas en las compilaciones de depuración. No se recomienda el uso de capas en compilaciones de versión o de perfil.<br/></td>
</tr>
<tr class="even">
<td><span id="New_Samples"></span><span id="new_samples"></span><span id="NEW_SAMPLES"></span>Nuevos ejemplos<br/></td>
<td>Esta versión tiene cuatro ejemplos nuevos.<br/>
<ul>
<li>En el ejemplo de <a href="https://msdn.microsoft.com/library/Ee416565(v=VS.85).aspx">vinculación dinámica del sombreador 11</a> se muestra el uso de interfaces del sombreador del modelo de sombreador 5 y la compatibilidad con Direct3D 11 para vincular los métodos de interfaz de sombreador en tiempo de ejecución.</li>
<li>En el ejemplo <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">HDRToneMappingCS11</a> se muestra cómo configurar y ejecutar el sombreador de cálculo (CS para abreviar más adelante), que es una de las nuevas características más interesantes de Direct3D 11. Aunque el ejemplo solo use el CS para implementar la asignación de tono HDR, el concepto debe extenderse fácilmente a otros algoritmos posteriores al procesamiento, así como a cálculos más generales.</li>
<li>En el ejemplo <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">MultithreadedRendering11</a> se muestra cómo dividir la representación entre varios subprocesos, con una sobrecarga muy baja.</li>
<li>El nuevo ejemplo de <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">SubD11</a> es muy similar al ejemplo SubD10 en el SDK de DirectX, salvo que se ha mejorado para aprovechar tres nuevas fases de canalización de Direct3D 11: el sombreador de casco, el del teselador y el sombreador de dominios.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características introducidas en versiones anteriores](d3d11-features-introduced-previous-releases.md)
</dt> </dl>

 

