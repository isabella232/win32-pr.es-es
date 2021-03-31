---
description: Copiar y obtener acceso a los datos de recursos (Direct3D 10)
ms.assetid: 34fd4d15-ee64-4acf-967d-a4afb6f26329
title: Copiar y obtener acceso a los datos de recursos (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38bd075585ee3123e163075a50b06b53a77a214c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807538"
---
# <a name="copying-and-accessing-resource-data-direct3d-10"></a>Copiar y obtener acceso a los datos de recursos (Direct3D 10)

Ya no es necesario pensar en los recursos que se crean en la memoria de vídeo o en la memoria del sistema. O si el tiempo de ejecución debe administrar la memoria. Gracias a la arquitectura del nuevo WDDM (modelo de controladores de pantalla de Windows), las aplicaciones ahora crean recursos de Direct3D 10 con diferentes marcas de [**uso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) para indicar el modo en que la aplicación pretende usar los datos de recursos. El nuevo modelo de controlador virtualiza la memoria que usan los recursos; después, se convierte en responsabilidad del sistema operativo/controlador/administrador de memoria para colocar recursos en el área de memoria más eficaz posible, dado el uso esperado.

El caso predeterminado es que los recursos estén disponibles para la GPU. Por supuesto, supongamos que hay ocasiones en las que los datos de recursos deben estar disponibles para la CPU. Copiar los datos de recursos para que el procesador adecuado pueda acceder a él sin afectar al rendimiento requiere cierto conocimiento de cómo funcionan los métodos de la API.

-   [Copiar datos de recursos](#copying-and-accessing-resource-data-direct3d-10)
-   [Acceso a los datos de recursos](#copying-and-accessing-resource-data-direct3d-10)

## <a name="copying-resource-data"></a>Copiar datos de recursos

Los recursos se crean en memoria cuando Direct3D ejecuta una llamada a Create. Se pueden crear en la memoria de vídeo, en la memoria del sistema o en cualquier otro tipo de memoria. Dado que el modelo de controlador WDDM virtualiza esta memoria, las aplicaciones ya no necesitan realizar un seguimiento del tipo de recursos de memoria que se crea en.

Lo ideal es que todos los recursos se encuentren en la memoria de vídeo para que la GPU pueda tener acceso inmediato a ellos. Sin embargo, a veces es necesario que la CPU Lea los datos de recursos o que la GPU tenga acceso a los datos de recursos en los que se ha escrito la CPU. Direct3D 10 controla estos escenarios diferentes solicitando a la aplicación que especifique un uso y, a continuación, ofrece varios métodos para copiar los datos de recursos cuando sea necesario.

En función de cómo se haya creado el recurso, no siempre es posible tener acceso directamente a los datos subyacentes. Esto puede significar que los datos de recursos se deben copiar desde el recurso de origen a otro recurso al que pueda acceder el procesador adecuado. En términos de Direct3D 10, los recursos predeterminados a los que se puede acceder directamente a través de la GPU, se puede acceder directamente a los recursos dinámicos y de ensayo mediante la CPU.

Una vez creado un recurso, no se puede cambiar su [**uso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) . En su lugar, copie el contenido de un recurso a otro recurso que se creó con un uso diferente. Direct3D 10 proporciona esta funcionalidad con tres métodos diferentes. Los dos primeros métodos ( [**ID3D10Device:: CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) y [**ID3D10Device:: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)) están diseñados para copiar los datos de recursos de un recurso a otro. El tercer método ([**ID3D10Device:: UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource)) está diseñado para copiar datos de la memoria en un recurso.

Hay dos tipos principales de recursos: asignable y no asignable. Los recursos creados con usos dinámicos o de almacenamiento provisional son asignables, mientras que los recursos creados con usos predeterminados o inmutables no son asignables.

La copia de datos entre recursos no asignables es muy rápida porque es el caso más común y se ha optimizado para que funcione correctamente. Dado que la CPU no puede acceder directamente a estos recursos, se optimizan para que la GPU pueda manipularlos rápidamente.

La copia de datos entre recursos que se van a asignar es más problemática porque el rendimiento dependerá del uso con el que se creó el recurso. Por ejemplo, la GPU puede leer un recurso dinámico bastante rápidamente, pero no puede escribir en ellos, y la GPU no puede leer ni escribir directamente en los recursos de ensayo.

Las aplicaciones que deseen copiar datos de un recurso con uso predeterminado en un recurso con uso de almacenamiento provisional (para permitir que la CPU Lea los datos, es decir, el problema de readback de GPU) deben hacerlo con precaución. Consulte [acceso a los datos de recursos](#copying-and-accessing-resource-data-direct3d-10) para obtener más información sobre este último caso.

## <a name="accessing-resource-data"></a>Acceso a los datos de recursos

El acceso a un recurso requiere la asignación del recurso; la asignación básicamente significa que la aplicación está intentando conceder a la CPU acceso a la memoria. El proceso de asignación de un recurso para que la CPU pueda acceder a la memoria subyacente puede producir cuellos de botella en el rendimiento y, por este motivo, se debe tener cuidado en cómo y cuándo realizar esta tarea.

El rendimiento puede triturarse en una detención si la aplicación intenta asignar un recurso en el momento equivocado. Si la aplicación intenta obtener acceso a los resultados de una operación antes de que finalice esa operación, se producirá una detención de canalización.

La realización de una operación de asignación en el momento equivocado podría provocar una caída importante del rendimiento al forzar la sincronización de la GPU y la CPU entre sí. Esta sincronización se realizará si la aplicación desea tener acceso a un recurso antes de que la GPU termine de copiarlo en un recurso que la CPU puede asignar.

La CPU solo puede leer los recursos creados con la \_ marca de \_ almacenamiento provisional uso de D3D10. Dado que los recursos creados con esta marca no se pueden establecer como salidas de la canalización, si la CPU desea leer los datos de un recurso generado por la GPU, se deben copiar los datos en un recurso creado con la marca de ensayo. Para ello, la aplicación puede usar los métodos [**ID3D10Device:: CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) o [**ID3D10Device:: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) para copiar el contenido de un recurso en otro. A continuación, la aplicación puede obtener acceso a este recurso mediante una llamada al método de asignación adecuado. Cuando ya no se necesita el acceso al recurso, la aplicación debe llamar al método de desasignación correspondiente. Por ejemplo, [**ID3D10Texture2D:: Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) y [**ID3D10Texture2D::**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-unmap)desasignar. Los diferentes métodos de asignación devuelven algunos valores específicos en función de las marcas de entrada. Para obtener más información, consulte la [**sección asignar comentarios**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture1d-map) .

> [!Note]  
> Cuando la aplicación llama al método Map, recibe un puntero a los datos de recursos a los que se tiene acceso. El tiempo de ejecución garantiza que el puntero tenga una alineación específica, en función del [nivel de característica](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md). En el [**nivel de característica de D3D \_ \_ \_ 10 \_ 0**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_feature_level) y superior, el puntero se alinea con 16 bytes. Para inferior al [**nivel de característica de D3D \_ \_ \_ 10 \_ 0**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_feature_level), el puntero se alinea con 4 bytes. La alineación de 16 bytes permite que la aplicación realice operaciones optimizadas para [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100))en los datos de forma nativa, sin necesidad de realinear ni copiar.

 

### <a name="performance-considerations"></a>Consideraciones de rendimiento

Es mejor pensar en un equipo como un equipo que se ejecuta como una arquitectura paralela con dos tipos principales de procesadores: una o más CPU y una o varias GPU. Como en cualquier arquitectura paralela, el mejor rendimiento se consigue cuando cada procesador está programado con suficientes tareas para evitar que se inactivo y cuando el trabajo de un procesador no está esperando el trabajo de otro.

El escenario del peor de los casos para el paralelismo de GPU/CPU es la necesidad de forzar a un procesador a esperar los resultados del trabajo realizado por otro. Direct3D 10 intenta quitar este costo al hacer que los métodos [**ID3D10Device:: CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) y [**ID3D10Device:: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) sean asíncronos; la copia no se ha ejecutado necesariamente en el momento en que el método vuelve. La ventaja de esto es que la aplicación no paga el costo de rendimiento de copiar realmente los datos hasta que la CPU tenga acceso a los datos, que es cuando se llama a Map. Si se llama al método de asignación después de que los datos se hayan copiado realmente, no se produce ninguna pérdida de rendimiento. Por otro lado, si se llama al método Map antes de que se copien los datos, se producirá una detención de la canalización.

Las llamadas asincrónicas en Direct3D 10 (que son la mayoría de los métodos, y especialmente las llamadas de representación) se almacenan en lo que se denomina un búfer de comandos. Este búfer es interno del controlador de gráficos y se usa para procesar por lotes las llamadas al hardware subyacente, de modo que el cambio costoso del modo de usuario al modo kernel en Microsoft Windows se produce lo más poco posible.

El búfer de comandos se vacía, con lo que se produce un cambio de modo de usuario/kernel en una de estas cuatro situaciones, que son las siguientes.

1.  Se llama a [**present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) .
2.  Se llama a [**ID3D10Device:: Flush**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-flush) .
3.  El búfer de comandos está lleno; su tamaño es dinámico y está controlado por el sistema operativo y el controlador de gráficos.
4.  La CPU requiere acceso a los resultados de un comando que espera para ejecutarse en el búfer de comandos.

De las cuatro situaciones anteriores, el número cuatro es el más importante para el rendimiento. Si la aplicación emite una llamada a [**ID3D10Device:: CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) o [**ID3D10Device:: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) , esta llamada se pone en cola en el búfer de comandos. Si la aplicación intenta asignar el recurso de almacenamiento provisional que era el destino de la llamada de copia antes de que se haya vaciado el búfer de comandos, se producirá una detención de canalización porque no solo se debe ejecutar la llamada al método de copia, pero también se deben ejecutar todos los demás comandos almacenados en búfer del búfer de comandos. Esto hará que la GPU y la CPU se sincronicen porque la CPU estará esperando para tener acceso al recurso de almacenamiento provisional mientras la GPU está vacía el búfer de comandos y, por último, rellenando el recurso que necesita la CPU. Una vez que la GPU finalice la copia, la CPU comenzará a acceder al recurso de almacenamiento provisional, pero durante este tiempo, la GPU estará inactiva.

Al hacerlo con frecuencia en tiempo de ejecución, se degradará considerablemente el rendimiento. Por ese motivo, la asignación de recursos creados con uso predeterminado debe realizarse con cuidado. La aplicación debe esperar el tiempo suficiente para que el búfer de comandos se vacíe y, por lo tanto, todos esos comandos terminen de ejecutarse antes de intentar asignar el recurso de almacenamiento provisional correspondiente. ¿Cuánto tiempo debe esperar la aplicación? Al menos dos fotogramas, ya que esto permitirá que el paralelismo entre las CPU y la GPU se aproveche de forma máxima. La forma en que funciona la GPU es que mientras la aplicación procesa el fotograma N mediante el envío de llamadas al búfer de comandos, la GPU está ocupada ejecutando las llamadas del fotograma anterior, N-1.

Por lo tanto, si una aplicación desea asignar un recurso que se origina en la memoria de vídeo y llama a [**ID3D10Device:: CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) o [**ID3D10Device:: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) en el fotograma n, esta llamada comenzará realmente a ejecutarse en el marco n + 1 cuando la aplicación envíe llamadas para el siguiente fotograma. La copia debe finalizar cuando la aplicación está procesando el fotograma N + 2.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Fotograma</th>
<th>Estado de la GPU/CPU</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>N</td>
<td><ul>
<li>Los problemas de CPU representan llamadas para el marco actual.</li>
</ul></td>
</tr>
<tr class="even">
<td>N + 1</td>
<td><ul>
<li>GPU que ejecuta llamadas enviadas desde la CPU durante el fotograma N.</li>
<li>Los problemas de CPU representan llamadas para el marco actual.</li>
</ul></td>
</tr>
<tr class="odd">
<td>N + 2</td>
<td><ul>
<li>GPU terminó de ejecutar llamadas enviadas desde la CPU durante el fotograma N. resultados listos.</li>
<li>GPU que ejecuta llamadas enviadas desde la CPU durante el fotograma N + 1.</li>
<li>Los problemas de CPU representan llamadas para el marco actual.</li>
</ul></td>
</tr>
<tr class="even">
<td>N + 3</td>
<td><ul>
<li>GPU terminó de ejecutar llamadas enviadas desde la CPU durante el fotograma N + 1. Resultados listos.</li>
<li>GPU que ejecuta llamadas enviadas desde la CPU durante el fotograma N + 2.</li>
<li>Los problemas de CPU representan llamadas para el marco actual.</li>
</ul></td>
</tr>
<tr class="odd">
<td>N + 4</td>
<td>...</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
