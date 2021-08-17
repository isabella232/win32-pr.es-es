---
description: A todos los desarrolladores que crean aplicaciones en tiempo real que usan gráficos 3D les preocupa la optimización del rendimiento. En esta sección se proporcionan instrucciones para obtener el mejor rendimiento del código.
ms.assetid: 074f848e-4a42-48a2-adf7-4026b8967413
title: Optimizaciones de rendimiento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e22ff22e3cde3673a1fc5ccd1da1bdccd95c6a094d670f59742178b28954773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520447"
---
# <a name="performance-optimizations-direct3d-9"></a>Optimizaciones de rendimiento (Direct3D 9)

A todos los desarrolladores que crean aplicaciones en tiempo real que usan gráficos 3D les preocupa la optimización del rendimiento. En esta sección se proporcionan instrucciones para obtener el mejor rendimiento del código.

-   [Rendimiento general Sugerencias](#general-performance-tips)
-   [Bases de datos y selección](#databases-and-culling)
-   [Primitivas de procesamiento por lotes](#batching-primitives)
-   [Iluminación Sugerencias](#lighting-tips)
-   [Tamaño de textura](#texture-size)
-   [Transformaciones de matriz](#matrix-transforms)
-   [Uso de texturas dinámicas](#using-dynamic-textures)
-   [Uso de búferes dinámicos de vértices e índices](#using-dynamic-vertex-and-index-buffers)
-   [Uso de mallas](#using-meshes)
-   [Rendimiento del búfer Z](#z-buffer-performance)

## <a name="general-performance-tips"></a>Rendimiento general Sugerencias

-   Borrar solo cuando sea necesario.
-   Minimice los cambios de estado y a agrupar los cambios de estado restantes.
-   Use texturas más pequeñas, si puede hacerlo.
-   Dibuje objetos en la escena de delante hacia atrás.
-   Use franjas de triángulo en lugar de listas y ventiladores. Para obtener un rendimiento óptimo de la caché de vértices, organice las franjas para reutilizar los vértices del triángulo antes, en lugar de hacerlo más tarde.
-   Degrada correctamente los efectos especiales que requieren una proporción desproporcionada de recursos del sistema.
-   Pruebe constantemente el rendimiento de la aplicación.
-   Minimice los conmutadores de búfer de vértices.
-   Use búferes de vértice estáticos siempre que sea posible.
-   Use un búfer de vértice estático grande por FVF para objetos estáticos, en lugar de uno por objeto.
-   Si la aplicación necesita acceso aleatorio al búfer de vértices en la memoria AGP, elija un tamaño de formato de vértice que sea un múltiplo de 32 bytes. De lo contrario, seleccione el formato más pequeño adecuado.
-   Dibuje mediante primitivas indizadas. Esto puede permitir un almacenamiento en caché de vértices más eficaz dentro del hardware.
-   Si el formato de búfer de profundidad contiene un canal de galería de símbolos, borre siempre los canales de profundidad y galería de símbolos al mismo tiempo.
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

La creación de una base de datos confiable de los objetos de su mundo es clave para un rendimiento excelente en Direct3D. Es más importante que las mejoras en la rasterización o el hardware.

Debe mantener el recuento de polígonos más bajo que pueda administrar. Diseñe un recuento de polígonos bajo mediante la creación de modelos de polígono bajo desde el principio. Agregue polígonos si puede hacerlo sin sacrificar el rendimiento más adelante en el proceso de desarrollo. Recuerde que los polígonos más rápidos son los que no se dibujan.

## <a name="batching-primitives"></a>Primitivas de procesamiento por lotes

Para obtener el mejor rendimiento de representación durante la ejecución, intente trabajar con primitivos en lotes y mantener el número de cambios de estado de representación lo más bajo posible. Por ejemplo, si tiene un objeto con dos texturas, a agrupar los triángulos que usan la primera textura y seguirlos con el estado de representación necesario para cambiar la textura. A continuación, a agrupar todos los triángulos que usan la segunda textura. Se llama a la compatibilidad de hardware más sencilla con Direct3D con lotes de estados de representación y lotes de primitivas a través de la capa de abstracción de hardware (HAN). Mientras más eficaz sea el procesamiento por lotes de las instrucciones, menor es la cantidad de llamadas DESA que se realizan durante la ejecución.

## <a name="lighting-tips"></a>Iluminación Sugerencias

Dado que las luces agregan un costo por vértice a cada fotograma representado, puede mejorar significativamente el rendimiento al tener cuidado con la forma en que las usa en la aplicación. La mayoría de las sugerencias siguientes derivan de la máxima, "el código más rápido es el código al que nunca se llama".

-   Use el menor número de fuentes de luz posible. Para aumentar el nivel de iluminación general, por ejemplo, use la luz ambiental en lugar de agregar una nueva fuente de luz.
-   Las luces direccionales son más eficaces que las luces puntuales o los focos destacados. En el caso de las luces direccionales, la dirección a la luz es fija y no es necesario calcularla por vértice.
-   Los focos pueden ser más eficaces que las luces puntuales, ya que el área fuera del cono de luz se calcula rápidamente. Si los focos son más eficaces o no, depende de la cantidad de escena que se enciende con el foco.
-   Use el parámetro range para limitar las luces solo a las partes de la escena que necesita para iluminación. Todos los tipos de luz salen bastante pronto cuando están fuera del intervalo.
-   El especular resalta casi el doble del costo de una luz. Úselos solo cuando sea necesario. Establezca el estado de representación SPECULARENABLE de D3DRS \_ en 0, el valor predeterminado, siempre que sea posible. Al definir materiales, debe establecer el valor de potencia especular en cero para desactivar los resaltados especulares para ese material; No basta con establecer el color especular en 0,0,0.

## <a name="texture-size"></a>Tamaño de textura

El rendimiento de la asignación de textura depende en gran medida de la velocidad de la memoria. Hay varias maneras de maximizar el rendimiento de la caché de las texturas de la aplicación.

-   Mantenga las texturas pequeñas. Cuanto más pequeñas sean las texturas, mayor será la probabilidad de que se mantengan en la caché secundaria de la CPU principal.
-   No cambie las texturas por primitiva. Intente mantener los polígonos agrupados en orden de las texturas que usan.
-   Use texturas cuadradas siempre que sea posible. Las texturas cuyas dimensiones son 256 x 256 son las más rápidas. Si la aplicación usa cuatro texturas de 128 x 128, por ejemplo, intente asegurarse de que usan la misma paleta y colócelas todas en una textura de 256 x 256. Esta técnica también reduce la cantidad de intercambio de textura. Por supuesto, no debe usar texturas de 256 x 256 a menos que la aplicación requiera tanto texto porque, como se mencionó, las texturas se deben mantener lo más pequeñas posible.

## <a name="matrix-transforms"></a>Transformaciones de matriz

Direct3D usa el mundo y ve las matrices que se establecen para configurar varias estructuras de datos internas. Cada vez que se establece un nuevo mundo o una matriz de vistas, el sistema vuelve a calcular las estructuras internas asociadas. Establecer estas matrices con frecuencia (por ejemplo, miles de veces por fotograma) lleva mucho tiempo. Puede minimizar el número de cálculos necesarios mediante la concatenación del mundo y la visualización de matrices en una matriz de vista mundial que establezca como matriz del mundo y, a continuación, establezca la matriz de vistas en la identidad. Mantenga copias almacenadas en caché de mundos individuales y vea matrices para poder modificar, concatenar y restablecer la matriz mundial según sea necesario. Para mayor claridad en esta documentación, los ejemplos de Direct3D rara vez emplean esta optimización.

## <a name="using-dynamic-textures"></a>Uso de texturas dinámicas

Para averiguar si el controlador admite texturas dinámicas, compruebe la marca D3DCAPS2 DYNAMICTEXTURES de la estructura \_ [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

Tenga en cuenta lo siguiente al trabajar con texturas dinámicas.

-   No se pueden administrar. Por ejemplo, su grupo no puede ser D3DPOOL \_ MANAGED.
-   Las texturas dinámicas se pueden bloquear, incluso si se crean en D3DPOOL \_ DEFAULT.
-   D3DLOCK \_ DISCARD es una marca de bloqueo válida para texturas dinámicas.

Es una buena idea crear solo una textura dinámica por formato y posiblemente por tamaño. No se recomiendan mapas mip dinámicos, cubos y volúmenes debido a la sobrecarga adicional al bloquear cada nivel. En el caso de los mapas mip, D3DLOCK \_ DISCARD solo se permite en el nivel superior. Todos los niveles se descartan bloqueando solo el nivel superior. Este comportamiento es el mismo para volúmenes y cubos. En el caso de los cubos, el nivel superior y la cara 0 están bloqueados.

El pseudocódigo siguiente muestra un ejemplo de uso de una textura dinámica.


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



## <a name="using-dynamic-vertex-and-index-buffers"></a>Uso de búferes dinámicos de vértices e índices

Bloquear un búfer de vértice estático mientras el procesador de gráficos usa el búfer puede tener una reducción significativa del rendimiento. La llamada de bloqueo debe esperar hasta que el procesador de gráficos termine de leer los datos de vértices o índices del búfer para poder volver a la aplicación que realiza la llamada, un retraso significativo. Bloquear y luego representar desde un búfer estático varias veces por fotograma también impide que el procesador de gráficos almacena en búfer los comandos de representación, ya que debe finalizar los comandos antes de devolver el puntero de bloqueo. Sin los comandos almacenados en búfer, el procesador de gráficos permanece inactivo hasta que la aplicación termina de rellenar el búfer de vértices o el búfer de índice y emite un comando de representación.

Idealmente, los datos de vértice o índice nunca cambiarían, pero esto no siempre es posible. Hay muchas situaciones en las que la aplicación necesita cambiar los datos de vértices o índices en cada fotograma, quizás incluso varias veces por fotograma. En estas situaciones, el vértice o búfer de índice se debe crear con D3DUSAGE \_ DYNAMIC. Esta marca de uso hace que Direct3D se optimice para las operaciones de bloqueo frecuentes. D3DUSAGE DYNAMIC solo es útil cuando el búfer se bloquea con frecuencia; los datos que permanecen constantes deben colocarse en un vértice estático o \_ búfer de índice.

Para recibir una mejora del rendimiento al usar búferes de vértice dinámicos, la aplicación debe llamar a [**IDirect3DVertexBuffer9::Lock**](/windows/desktop/api) o [**IDirect3DIndexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) con las marcas adecuadas. D3DLOCK DISCARD indica que la aplicación no necesita mantener los datos antiguos de vértice o \_ índice en el búfer. Si el procesador de gráficos sigue usando el búfer cuando se llama al bloqueo con D3DLOCK DISCARD, se devuelve un puntero a una nueva región de memoria en lugar de los datos antiguos \_ del búfer. Esto permite que el procesador de gráficos siga usando los datos antiguos mientras la aplicación coloca los datos en el nuevo búfer. No se requiere ninguna administración de memoria adicional en la aplicación; el búfer antiguo se reutiliza o destruye automáticamente cuando el procesador de gráficos termina con él. Tenga en cuenta que el bloqueo de un búfer con D3DLOCK DISCARD siempre descarta todo el búfer, especificando un desplazamiento distinto de cero o un campo de tamaño limitado no conserva la información en las áreas desbloqueadas del \_ búfer.

Hay casos en los que la cantidad de datos que la aplicación necesita almacenar por bloqueo es pequeña, como agregar cuatro vértices para representar un sprite. D3DLOCK NOOVERWRITE indica que la aplicación no sobrescribirá los datos que ya \_ se usan en el búfer dinámico. La llamada de bloqueo devolverá un puntero a los datos antiguos, lo que permite a la aplicación agregar nuevos datos en regiones no utilizadas del vértice o búfer de índice. La aplicación no debe modificar los vértices ni los índices usados en una operación de dibujo, ya que el procesador de gráficos podría seguir utilizando estos. A continuación, la aplicación debe usar D3DLOCK DISCARD después de que el búfer dinámico esté lleno para recibir una nueva región de memoria, descartando los datos de vértice o índice antiguos una vez finalizado el procesador de \_ gráficos.

El mecanismo de consulta asincrónica es útil para determinar si los vértices siguen siendo usados por el procesador de gráficos. Emita una consulta de tipo D3DQUERYTYPE EVENT después de la última \_ llamada a DrawPrimitive que usa los vértices. Los vértices ya no se usan cuando [**IDirect3DQuery9::GetData**](/windows/desktop/api) devuelve S \_ OK. Bloquear un búfer con D3DLOCK DISCARD o ninguna marca siempre garantizará que los vértices se sincronicen correctamente con el procesador de gráficos; sin embargo, el uso de bloqueos sin marcas incurrirá en la penalización de rendimiento descrita \_ anteriormente. Otras llamadas API como [**IDirect3DDevice9::BeginScene,**](/windows/desktop/api) [**IDirect3DDevice9::EndScene**](/windows/desktop/api)e [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) no garantizan que el procesador de gráficos haya terminado de usar vértices.

A continuación se muestran formas de usar búferes dinámicos y las marcas de bloqueo adecuadas.


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



## <a name="using-meshes"></a>Uso de mallas

Puede optimizar las mallas mediante triángulos indexados de Direct3D en lugar de franjas de triángulos indexados. El hardware detectará que el 95 % de los triángulos sucesivos forman realmente franjas y se ajustan en consecuencia. Muchos controladores también lo hacen para hardware anterior.

Los objetos de malla D3DX pueden tener cada triángulo, o cara, etiquetado con un DWORD, denominado atributo de esa cara. La semántica de DWORD está definida por el usuario. D3DX los usa para clasificar la malla en subconjuntos. La aplicación establece atributos por cara mediante la [**llamada ID3DXMesh::LockAttributeBuffer.**](id3dxmesh--lockattributebuffer.md) El [**método ID3DXMesh::Optimize**](id3dxmesh--optimize.md) tiene una opción para agrupar los vértices y las caras de la malla en atributos mediante la opción D3DXMESHOPT \_ ATTRSORT. Cuando esto se hace, el objeto de malla calcula una tabla de atributos que puede obtener la aplicación mediante una llamada a [**ID3DXBaseMesh::GetAttributeTable**](id3dxbasemesh--getattributetable.md). Esta llamada devuelve 0 si la malla no está ordenada por atributos. No hay ninguna manera de que una aplicación establezca una tabla de atributos porque la genera el **método ID3DXMesh::Optimize.** La ordenación de atributos distingue datos, por lo que si la aplicación sabe que una malla está ordenada por atributos, debe llamar a **ID3DXMesh::Optimize** para generar la tabla de atributos.

En los temas siguientes se describen los distintos atributos de una malla.

### <a name="attribute-id"></a>Id. de atributo

Un identificador de atributo es un valor que asocia un grupo de caras a un grupo de atributos. Este identificador describe qué subconjunto de caras [**ID3DXBaseMesh::D rawSubset**](id3dxbasemesh--drawsubset.md) debe dibujar. Los identificadores de atributo se especifican para las caras del búfer de atributo. Los valores reales de los identificadores de atributo pueden ser cualquier cosa que se ajuste en 32 bits, pero es habitual usar de 0 a n donde n es el número de atributos.

### <a name="attribute-buffer"></a>Búfer de atributos

El búfer de atributos es una matriz de DWORD (uno por cara) que especifica a qué grupo de atributos pertenece cada cara. Este búfer se inicializa en cero al crear una malla, pero lo rellenan las rutinas de carga o el usuario debe rellenarlo si se desea más de un atributo con el identificador 0. Este búfer contiene la información que se usa para ordenar la malla en función de los atributos de [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md). Si no hay ninguna tabla de atributos, [**ID3DXBaseMesh::D rawSubset**](id3dxbasemesh--drawsubset.md) examina este búfer para seleccionar las caras del atributo especificado que se va a dibujar.

### <a name="attribute-table"></a>Tabla de atributos

La tabla de atributos es una estructura que posee y mantiene la malla. La única manera de generar uno es mediante una llamada a [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) con la ordenación de atributos o una optimización más segura habilitada. La tabla de atributos se usa para iniciar rápidamente una única llamada primitiva de dibujo a [**ID3DXBaseMesh::D rawSubset**](id3dxbasemesh--drawsubset.md). El único uso es que las mallas de progreso también mantienen esta estructura, por lo que es posible ver qué caras y vértices están activos en el nivel de detalle actual.

## <a name="z-buffer-performance"></a>Rendimiento del búfer Z

Las aplicaciones pueden aumentar el rendimiento al usar el almacenamiento en búfer z y el texturing asegurándose de que las escenas se representan de delante hacia atrás. Las primitivas con búfer z con textura se prueban previamente en el búfer z en una línea de examen. Si un polígono representado previamente oculta una línea de examen, el sistema la rechaza de forma rápida y eficaz. El almacenamiento en búfer Z puede mejorar el rendimiento, pero la técnica es más útil cuando una escena dibuja los mismos píxeles más de una vez. Esto es difícil de calcular exactamente, pero a menudo se puede realizar una aproximación cercana. Si los mismos píxeles se dibujan menos de dos veces, puede lograr el mejor rendimiento desactivando el almacenamiento en búfer z y representando la escena de nuevo al frente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programación Sugerencias](programming-tips.md)
</dt> </dl>

 

 
