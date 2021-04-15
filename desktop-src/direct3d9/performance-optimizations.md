---
description: Cada desarrollador que crea aplicaciones en tiempo real que usan gráficos 3D se preocupa de la optimización del rendimiento. En esta sección se proporcionan instrucciones para obtener el mejor rendimiento del código.
ms.assetid: 074f848e-4a42-48a2-adf7-4026b8967413
title: Optimizaciones de rendimiento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d42be994522f0d83e36387b1a5866b3eee10df3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494272"
---
# <a name="performance-optimizations-direct3d-9"></a>Optimizaciones de rendimiento (Direct3D 9)

Cada desarrollador que crea aplicaciones en tiempo real que usan gráficos 3D se preocupa de la optimización del rendimiento. En esta sección se proporcionan instrucciones para obtener el mejor rendimiento del código.

-   [Sugerencias generales de rendimiento](#general-performance-tips)
-   [Bases de datos y selección](#databases-and-culling)
-   [Procesamiento por lotes de primitivas](#batching-primitives)
-   [Sugerencias de iluminación](#lighting-tips)
-   [Tamaño de textura](#texture-size)
-   [Transformaciones de matriz](#matrix-transforms)
-   [Usar texturas dinámicas](#using-dynamic-textures)
-   [Usar búferes dinámicos de vértices y de índices](#using-dynamic-vertex-and-index-buffers)
-   [Usar mallas](#using-meshes)
-   [Rendimiento del búfer Z](#z-buffer-performance)

## <a name="general-performance-tips"></a>Sugerencias generales de rendimiento

-   Desactive solo cuando sea necesario.
-   Minimizar los cambios de estado y agrupar los cambios de estado restantes.
-   Use texturas más pequeñas, si puede hacerlo.
-   Dibuje objetos de la escena de delante a atrás.
-   Use bandas de triángulo en lugar de listas y ventiladores. Para un rendimiento óptimo de la caché de vértices, organice las tiras para volver a usar los vértices de triángulo antes, en lugar de más adelante
-   Degradar correctamente los efectos especiales que requieren una cuota desproporcionada de recursos del sistema.
-   Pruebe constantemente el rendimiento de su aplicación.
-   Minimice los modificadores de búfer de vértices.
-   Use búferes de vértices estáticos siempre que sea posible.
-   Use un búfer de vértices estáticos grande por FVF para los objetos estáticos, en lugar de uno por cada objeto.
-   Si la aplicación necesita acceso aleatorio al búfer de vértices en la memoria AGP, elija un tamaño de formato de vértice que sea un múltiplo de 32 bytes. En caso contrario, seleccione el formato más pequeño adecuado.
-   Dibuje utilizando primitivos indizados. Esto puede permitir un almacenamiento en caché de vértices más eficaz en el hardware.
-   Si el formato de búfer de profundidad contiene un canal de estarcido, borre siempre los canales de profundidad y estarcido al mismo tiempo.
-   Combine la instrucción del sombreador y la salida de datos siempre que sea posible. Por ejemplo:
    ```
    // Rather than doing a multiply and add, and then output the data with 
    //   two instructions:
    mad r2, r1, v0, c0
    mov oD0, r2

    // Combine both in a single instruction, because this eliminates an  
    //   additional register copy.
    mad oD0, r1, v0, c0 
    ```

    

## <a name="databases-and-culling"></a>Bases de datos y selección

Crear una base de datos confiable de los objetos de su mundo es clave para un rendimiento excelente en Direct3D. Es más importante que las mejoras en la rasterización o el hardware.

Debe mantener el número de polígonos más bajo que puede administrar. Diseño para un número de polígonos bajos mediante la creación de modelos de poco polígono desde el principio. Agregue polígonos si puede hacerlo sin sacrificar el rendimiento más adelante en el proceso de desarrollo. Recuerde que los polígonos más rápidos son los que no dibuja.

## <a name="batching-primitives"></a>Procesamiento por lotes de primitivas

Para obtener el mejor rendimiento de representación durante la ejecución, intente trabajar con primitivas en lotes y mantenga el número de cambios de estado de representación lo más bajo posible. Por ejemplo, si tiene un objeto con dos texturas, agrupe los triángulos que usan la primera textura y siga con el estado de representación necesario para cambiar la textura. A continuación, agrupe todos los triángulos que usan la segunda textura. La compatibilidad de hardware más sencilla con Direct3D se llama con lotes de Estados de representación y lotes de primitivas a través de la capa de abstracción de hardware (HAL). Cuanto más eficaz es el procesamiento por lotes de las instrucciones, se realizan menos llamadas a HAL durante la ejecución.

## <a name="lighting-tips"></a>Sugerencias de iluminación

Dado que las luces agregan un costo por vértice a cada fotograma representado, puede mejorar significativamente el rendimiento si tiene cuidado al usarlos en la aplicación. La mayoría de las siguientes sugerencias se derivan de la maximización, "el código más rápido es código al que nunca se llama".

-   Use el menor número posible de fuentes de luz. Para aumentar el nivel de iluminación general, por ejemplo, use la luz ambiente en lugar de agregar una nueva fuente de luz.
-   Las luces direccionales son más eficaces que las luces de punto o los focos. En el caso de las luces direccionales, la dirección de la luz es fija y no tiene que calcularse por vértices.
-   Los focos pueden ser más eficaces que las luces puntuales, ya que el área fuera del cono de luz se calcula rápidamente. Si los focos son más eficientes o no dependen de la cantidad de la escena que está iluminada por el foco.
-   Use el parámetro de intervalo para limitar las luces a las partes de la escena que debe iluminar. Todos los tipos de luz salen bastante pronto cuando están fuera del intervalo.
-   Los reflejos especulares casi duplican el costo de una luz. Úselos solo cuando sea necesario. Establezca el estado de representación de SPECULARENABLE de D3DRS \_ en 0, el valor predeterminado, siempre que sea posible. Al definir materiales, debe establecer el valor de potencia especular en cero para desactivar las iluminaciones especulares para ese material. simplemente establecer el color especular en 0, 0, 0 no es suficiente.

## <a name="texture-size"></a>Tamaño de textura

El rendimiento de la asignación de texturas depende en gran medida de la velocidad de la memoria. Hay varias maneras de maximizar el rendimiento de la memoria caché de las texturas de la aplicación.

-   Mantenga las texturas reducidas. Cuanto más pequeñas sean las texturas, más posibilidades tendrán de mantenerse en la caché secundaria de la CPU principal.
-   No cambie las texturas por primitivos. Intente mantener los polígonos agrupados por orden de las texturas que usan.
-   Utilice texturas cuadradas siempre que sea posible. Las texturas cuyas dimensiones son 256x256 son las más rápidas. Si la aplicación usa cuatro texturas de 128x128, por ejemplo, intente asegurarse de que usan la misma paleta y colocarlas en una sola textura de 256x256. Esta técnica también reduce la cantidad de intercambio de textura. Por supuesto, no debe utilizar texturas de 256x256 a menos que la aplicación requiera una gran texturización porque, como se mencionó, las texturas deben mantenerse lo más pequeñas posible.

## <a name="matrix-transforms"></a>Transformaciones de matriz

Direct3D usa el mundo y las matrices de vistas que se establecen para configurar varias estructuras de datos internas. Cada vez que se establece un nuevo mundo o una matriz de vistas, el sistema vuelve a calcular las estructuras internas asociadas. Establecer estas matrices con frecuencia (por ejemplo, miles de veces por fotograma) es un proceso que consume mucho tiempo. Puede minimizar el número de cálculos necesarios concatenando el mundo y ver las matrices en una matriz de vista mundial que establezca como la matriz universal y, a continuación, estableciendo la matriz de la vista en la identidad. Mantenga copias en caché de matrices de todo el mundo y vistas para que pueda modificar, concatenar y restablecer la matriz universal según sea necesario. Para mayor claridad en esta documentación, los ejemplos de Direct3D raramente emplean esta optimización.

## <a name="using-dynamic-textures"></a>Usar texturas dinámicas

Para averiguar si el controlador admite texturas dinámicas, Compruebe la \_ marca de D3DCAPS2 DYNAMICTEXTURES de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .

Tenga en cuenta lo siguiente al trabajar con texturas dinámicas.

-   No se pueden administrar. Por ejemplo, el grupo no se puede \_ administrar D3DPOOL.
-   Las texturas dinámicas se pueden bloquear, incluso si se crean en el \_ valor predeterminado de D3DPOOL.
-   D3DLOCK \_ discard es una marca de bloqueo válida para las texturas dinámicas.

Es aconsejable crear solo una textura dinámica por formato y, posiblemente, por tamaño. No se recomiendan los mapas MIP, los cubos y los volúmenes dinámicos debido a la sobrecarga adicional en el bloqueo de todos los niveles. En el caso de los mapas MIP, D3DLOCK \_ solo se permite en el nivel superior. Todos los niveles se descartan bloqueando solo el nivel superior. Este comportamiento es el mismo para los volúmenes y los cubos. En el caso de los cubos, el nivel superior y la esfera 0 están bloqueados.

En el siguiente pseudocódigo se muestra un ejemplo del uso de una textura dinámica.


```
DrawProceduralTexture(pTex)
{
    // pTex should not be very small because overhead of 
    //   calling driver every D3DLOCK_DISCARD will not 
    //   justify the performance gain. Experimentation is encouraged.
    pTex->Lock(D3DLOCK_DISCARD);
    <Overwrite *entire* texture>
    pTex->Unlock();
    pDev->SetTexture();
    pDev->DrawPrimitive();
}
```



## <a name="using-dynamic-vertex-and-index-buffers"></a>Usar búferes dinámicos de vértices y de índices

Bloquear un búfer de vértices estático mientras el procesador de gráficos usa el búfer puede tener una penalización significativa del rendimiento. La llamada de bloqueo debe esperar hasta que el procesador de gráficos termine de leer los datos de vértices o índices del búfer antes de poder volver a la aplicación que realiza la llamada, un retraso significativo. El bloqueo y la representación de un búfer estático varias veces por fotograma también impide que el procesador de gráficos almacene en búfer comandos de representación, ya que debe finalizar los comandos antes de devolver el puntero de bloqueo. Sin comandos almacenados en búfer, el procesador de gráficos permanece inactivo hasta que la aplicación termina de llenar el búfer de vértices o el búfer de índice y emite un comando de representación.

Idealmente, los datos de vértices o índices nunca cambiarían, pero esto no siempre es posible. Hay muchas situaciones en las que la aplicación necesita cambiar los datos de vértices o índices en cada fotograma, quizás incluso varias veces por fotograma. En estas situaciones, se debe crear el búfer de vértice o de índice con D3DUSAGE \_ Dynamic. Esta marca de uso hace que Direct3D optimice las operaciones frecuentes de bloqueo. D3DUSAGE \_ Dynamic solo es útil cuando el búfer se bloquea con frecuencia; los datos que permanecen constantes deben colocarse en un vértice o en un búfer de índice estático.

Para obtener una mejora del rendimiento cuando se usan búferes de vértices dinámicos, la aplicación debe llamar a [**IDirect3DVertexBuffer9:: Lock**](/windows/desktop/api) o [**IDirect3DIndexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) con las marcas adecuadas. D3DLOCK \_ discard indica que la aplicación no necesita mantener los datos de índice o vértice antiguos en el búfer. Si el procesador de gráficos sigue usando el búfer cuando se llama a Lock con D3DLOCK \_ discard, se devuelve un puntero a una nueva región de memoria en lugar de los datos de búfer antiguos. Esto permite que el procesador de gráficos siga usando los datos antiguos mientras la aplicación coloca los datos en el nuevo búfer. No se requiere ninguna administración de memoria adicional en la aplicación; el búfer antiguo se reutiliza o se destruye automáticamente cuando el procesador de gráficos finaliza con él. Tenga en cuenta que el bloqueo de un búfer con D3DLOCK discard \_ siempre descarta todo el búfer, especificando un desplazamiento distinto de cero o un campo de tamaño limitado no conserva la información en las áreas desbloqueadas del búfer.

Hay casos en los que la cantidad de datos que la aplicación necesita almacenar por bloqueo es pequeña, como agregar cuatro vértices para representar un Sprite. D3DLOCK \_ NOOVERWRITE indica que la aplicación no sobrescribirá los datos que ya se estén usando en el búfer dinámico. La llamada de bloqueo devolverá un puntero a los datos antiguos, lo que permite a la aplicación agregar nuevos datos en regiones no utilizadas del búfer de vértice o de índice. La aplicación no debe modificar los vértices ni los índices usados en una operación de dibujo, ya que el procesador de gráficos aún podría usarlos. A continuación, la aplicación debe usar D3DLOCK \_ discard después de que el búfer dinámico esté lleno para recibir una nueva región de memoria, descartando los datos de vértice o de vértice antiguos una vez finalizado el procesador de gráficos.

El mecanismo de consulta asincrónico es útil para determinar si el procesador de gráficos sigue usando los vértices. Emita una consulta de tipo D3DQUERYTYPE \_ Event después de la última llamada a DrawPrimitive que usa los vértices. Los vértices ya no se usan cuando [**IDirect3DQuery9:: GetData**](/windows/desktop/api) devuelve S \_ correctos. Si se bloquea un búfer con D3DLOCK \_ discard o ninguna marca, siempre se garantiza que los vértices estén sincronizados correctamente con el procesador de gráficos; sin embargo, el uso de Lock sin marcas incurrirá en la penalización del rendimiento que se ha descrito anteriormente. Otras llamadas API como [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api), [**IDirect3DDevice9:: EndScene**](/windows/desktop/api)y [**IDirect3DDevice9::P reenviados**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) no garantizan que el procesador de gráficos termine de usar los vértices.

A continuación se muestran las formas de usar búferes dinámicos y las marcas de bloqueo apropiadas.


```
    // USAGE STYLE 1
    // Discard the entire vertex buffer and refill with thousands of vertices.
    // Might contain multiple objects and/or require multiple DrawPrimitive 
    //   calls separated by state changes, etc.
 
    // Determine the size of data to be moved into the vertex buffer.
    UINT nSizeOfData = nNumberOfVertices * m_nVertexStride;
 
    // Discard and refill the used portion of the vertex buffer.
    CONST DWORD dwLockFlags = D3DLOCK_DISCARD;
    
    // Lock the vertex buffer.
    BYTE* pBytes;
    if( FAILED( m_pVertexBuffer->Lock( 0, 0, &pBytes, dwLockFlags ) ) )
        return false;
    
    // Copy the vertices into the vertex buffer.
    memcpy( pBytes, pVertices, nSizeOfData );
    m_pVertexBuffer->Unlock();
 
    // Render the primitives.
    m_pDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, nNumberOfVertices/3)
```




```
    // USAGE STYLE 2
    // Reusing one vertex buffer for multiple objects
 
    // Determine the size of data to be moved into the vertex buffer.
    UINT nSizeOfData = nNumberOfVertices * m_nVertexStride;
 
    // No overwrite will be used if the vertices can fit into 
    //   the space remaining in the vertex buffer.
    DWORD dwLockFlags = D3DLOCK_NOOVERWRITE;
    
    // Check to see if the entire vertex buffer has been used up yet.
    if( m_nNextVertexData > m_nSizeOfVB - nSizeOfData )
    {
        // No space remains. Start over from the beginning 
        //   of the vertex buffer.
        dwLockFlags = D3DLOCK_DISCARD;
        m_nNextVertexData = 0;
    }
    
    // Lock the vertex buffer.
    BYTE* pBytes;
    if( FAILED( m_pVertexBuffer->Lock( (UINT)m_nNextVertexData, nSizeOfData, 
               &pBytes, dwLockFlags ) ) )
        return false;
    
    // Copy the vertices into the vertex buffer.
    memcpy( pBytes, pVertices, nSizeOfData );
    m_pVertexBuffer->Unlock();
 
    // Render the primitives.
    m_pDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 
               m_nNextVertexData/m_nVertexStride, nNumberOfVertices/3)
 
    // Advance to the next position in the vertex buffer.
    m_nNextVertexData += nSizeOfData;
```



## <a name="using-meshes"></a>Usar mallas

Puede optimizar las mallas mediante triángulos indizados de Direct3D en lugar de bandas triangulares indizadas. El hardware detectará que el 95 por ciento de triángulos sucesivos forman tiras y se ajustan en consecuencia. Muchos controladores lo hacen también para hardware más antiguo.

Los objetos de malla de D3DX pueden tener cada triángulo, o una esfera, etiquetada con un valor DWORD, denominado el atributo de esa superficie. La semántica del valor DWORD es definida por el usuario. D3DX los usa para clasificar la malla en subconjuntos. La aplicación establece atributos por caras mediante la llamada a [**ID3DXMesh:: LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md) . El método [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) tiene una opción para agrupar los vértices de malla y las caras en atributos mediante la opción D3DXMESHOPT de \_ ATTRSORT. Cuando se hace esto, el objeto de malla calcula una tabla de atributos que la aplicación puede obtener llamando a [**ID3DXBaseMesh:: GetAttributeTable**](id3dxbasemesh--getattributetable.md). Esta llamada devuelve 0 si la malla no está ordenada por atributos. No hay ninguna manera de que una aplicación establezca una tabla de atributos porque se genera mediante el método **ID3DXMesh:: Optimize** . El orden de los atributos distingue los datos, por lo que si la aplicación sabe que una malla está ordenada por atributos, sigue siendo necesario llamar a **ID3DXMesh:: Optimize** para generar la tabla de atributos.

En los temas siguientes se describen los distintos atributos de una malla.

### <a name="attribute-id"></a>IDENTIFICADOR de atributo

Un identificador de atributo es un valor que asocia un grupo de caras con un grupo de atributos. Este identificador describe el subconjunto de caras [**ID3DXBaseMesh::D rawsubset**](id3dxbasemesh--drawsubset.md) debe dibujar. Los identificadores de atributo se especifican para las caras en el búfer de atributo. Los valores reales de los identificadores de atributo pueden ser cualquier cosa que quepa en 32 bits, pero es habitual usar de 0 a n, donde n es el número de atributos.

### <a name="attribute-buffer"></a>Búfer de atributo

El búfer de atributo es una matriz de DWORDs (uno por cada tipo) que especifica a qué grupo de atributos pertenece cada una de ellas. Este búfer se inicializa en cero en la creación de una malla, pero se rellena con las rutinas de carga o debe ser rellenado por el usuario si se desea más de un atributo con el identificador 0. Este búfer contiene la información que se usa para ordenar la malla en función de los atributos de [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md). Si no hay ninguna tabla de atributos, [**ID3DXBaseMesh::D rawsubset**](id3dxbasemesh--drawsubset.md) examina este búfer para seleccionar las caras del atributo especificado que se van a dibujar.

### <a name="attribute-table"></a>Tabla de atributos

La tabla de atributos es una estructura que posee y mantiene la malla. La única manera de generar una es mediante una llamada a [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) con ordenación de atributos o una optimización más segura habilitada. La tabla de atributos se usa para iniciar rápidamente una única llamada primitiva de Draw a [**ID3DXBaseMesh::D rawsubset**](id3dxbasemesh--drawsubset.md). El único otro uso es que el progreso de las mallas también mantiene esta estructura, por lo que es posible ver qué caras y vértices están activos en el nivel de detalle actual.

## <a name="z-buffer-performance"></a>Rendimiento del búfer Z

Las aplicaciones pueden aumentar el rendimiento cuando se usa el almacenamiento en búfer z y el uso de texturas asegurándose de que las escenas se representan de delante a atrás. Las primitivas almacenadas en búfer de z con textura se comprueban en el búfer z en función de la línea de exploración. Si un polígono representado previamente oculta una línea de exploración, el sistema la rechaza de forma rápida y eficaz. El almacenamiento en búfer Z puede mejorar el rendimiento, pero la técnica es más útil cuando una escena dibuja los mismos píxeles más de una vez. Esto es difícil de calcular exactamente, pero a menudo puede hacer una aproximación aproximada. Si los mismos píxeles se dibujan menos de dos veces, puede lograr el mejor rendimiento si desactiva el almacenamiento en búfer z y representa la escena de vuelta al principio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sugerencias de programación](programming-tips.md)
</dt> </dl>

 

 
