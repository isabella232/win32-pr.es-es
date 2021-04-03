---
description: Los búferes de índice, representados por la interfaz IDirect3DIndexBuffer9, son búferes de memoria que contienen datos de índice.
ms.assetid: baa60cd1-a1f0-4dbe-b934-aeb1a5c6b784
title: Búferes de índice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7151fae6deb72a0c569d269c80e5b13bf946f9d0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906440"
---
# <a name="index-buffers-direct3d-9"></a>Búferes de índice (Direct3D 9)

Los búferes de índice, representados por la interfaz [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) , son búferes de memoria que contienen datos de índice. Los datos de índice, o índices, son desplazamientos enteros en búferes de vértices y se usan para representar primitivas mediante el método [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) .

Un búfer de vértice contiene vértices; por lo tanto, puede dibujar un búfer de vértices con o sin primitivos indizados. Sin embargo, dado que un búfer de índice contiene índices, no se puede utilizar un búfer de índice sin un búfer de vértices correspondiente. (Como nota al margen, [**IDirect3DDevice9::D rawindexedprimitiveup**](/windows/desktop/api) y [**IDirect3DDevice9::D rawprimitiveup**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup) son los únicos métodos de dibujo que dibujan sin un índice o un búfer de vértice).

## <a name="index-buffer-description"></a>Descripción del búfer de índice

Un búfer de índice se describe en cuanto a sus capacidades, como dónde existe en la memoria, si admite lectura y escritura, y el tipo y el número de índices que puede contener. Estos rasgos se encuentran en una estructura [**D3DINDEXBUFFER \_ DESC**](d3dindexbuffer-desc.md) .

Las descripciones del búfer de índice indican a la aplicación cómo se creó un búfer existente. Proporciona una estructura de Descripción vacía para que el sistema rellene con las capacidades de un búfer de índice creado previamente.

-   El miembro Format describe el formato de superficie de los datos del búfer de índice.
-   El tipo identifica el tipo de recurso del búfer de índice.
-   El miembro de la estructura Usage contiene marcas de capacidad generales. La \_ marca D3DUSAGE SOFTWAREPROCESSING indica que el búfer de índice se va a usar con el procesamiento de vértices de software. La presencia de la \_ marca WRITEONLY de D3DUSAGE en uso indica que la memoria del búfer de índice solo se utiliza para las operaciones de escritura. Esto libera el controlador para colocar los datos de índice en la mejor ubicación de memoria para habilitar el procesamiento y la representación rápidos. Si \_ no se usa la marca WRITEONLY de D3DUSAGE, es menos probable que el controlador Coloque los datos en una ubicación que sea ineficaz para las operaciones de lectura. Esto sacrifica la velocidad de procesamiento y representación. Si no se especifica esta marca, se supone que las aplicaciones realizan operaciones de lectura y escritura en los datos del búfer de índice.
-   Grupo especifica la clase de memoria asignada para el búfer de índice. La \_ marca D3DPOOL SYSTEMMEM indica que el sistema creó el búfer de índice en la memoria del sistema.
-   El miembro size almacena el tamaño, en bytes, de los datos del búfer de vértices.
-   No se usa el último parámetro pSharedHandle. Establézcalo en **null**.

## <a name="index-processing-requirements"></a>Requisitos de procesamiento de índices

El rendimiento de las operaciones de procesamiento de índices depende en gran medida de dónde exista el búfer de índice en la memoria y qué tipo de dispositivo de representación se está usando. Las aplicaciones controlan la asignación de memoria para los búferes de índice cuando se crean. Cuando \_ se establece la marca de memoria D3DPOOL SYSTEMMEM, el búfer de índice se crea en la memoria del sistema. Cuando \_ se usa la marca de memoria predeterminada de D3DPOOL, el controlador de dispositivo determina dónde se asigna mejor la memoria para el búfer de índice, que a menudo se conoce como memoria óptima para el controlador. La memoria óptima del controlador puede ser la memoria de vídeo local, la memoria de vídeo no local o la memoria del sistema.

Al establecer la \_ marca de comportamiento D3DUSAGE SOFTWAREPROCESSING cuando se llama al método [**IDirect3DDevice9:: CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) , se especifica que el búfer de índice se va a usar con el procesamiento de vértices de software. Esta marca es necesaria en el procesamiento de vértices en modo mixto (D3DCREATE \_ Mixed \_ VERTEXPROCESSING) cuando se usa el procesamiento de vértices de software.

La aplicación puede escribir directamente índices en un búfer de índice asignado en la memoria óptima del controlador. Esta técnica evita una operación de copia redundante más adelante. Esta técnica no funciona bien si la aplicación Lee los datos de un búfer de índice, porque las operaciones de lectura realizadas por el host desde la memoria óptima del controlador pueden ser muy lentas. Por lo tanto, si la aplicación necesita leer durante el procesamiento o escribe datos en el búfer de forma errática, un búfer de índice de la memoria del sistema es una opción mejor.

> [!Note]  
> Use siempre \_ el valor predeterminado de D3DPOOL, excepto si no desea usar memoria de vídeo o usar grandes cantidades de RAM con bloqueo de página cuando el controlador coloca los búferes de vértice o de índice en la memoria AGP.

 

## <a name="create-an-index-buffer"></a>Crear un búfer de índice

Cree un objeto de búfer de índice llamando al método [**IDirect3DDevice9:: CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) , que acepta seis parámetros.

-   El primer parámetro especifica la longitud del búfer de índice, en bytes.
-   El segundo parámetro es un conjunto de controles de uso. Entre otras cosas, su valor determina si los vértices a los que se hace referencia en los índices pueden contener información de recorte. Para mejorar el rendimiento, especifique D3DUSAGE \_ DONOTCLIP cuando no se recorte.

    La \_ marca D3DUSAGE SOFTWAREPROCESSING se puede establecer cuando el procesamiento de vértices de modo mixto o software (D3DCREATE \_ mixto \_ VERTEXPROCESSING/D3DCREATE \_ software \_ VERTEXPROCESSING) está habilitado para ese dispositivo. D3DUSAGE \_ SOFTWAREPROCESSING se debe establecer para que los búferes se usen con el procesamiento de vértices de software en modo mixto, pero no se debe establecer para el mejor rendimiento posible al usar el procesamiento de índices de hardware en modo mixto (D3DCREATE de \_ hardware \_ VERTEXPROCESSING). Sin embargo, el establecimiento de D3DUSAGE \_ SOFTWAREPROCESSING es la única opción cuando se usa un solo búfer con el procesamiento de vértices de hardware y software. D3DUSAGE \_ SOFTWAREPROCESSING se permite para dispositivos mixtos y de software.

    Es posible forzar búferes de vértices y de índices en la memoria del sistema mediante \_ la especificación de D3DPOOL SYSTEMMEM, incluso cuando el procesamiento de índices se realiza en el hardware. Se trata de una manera de evitar grandes cantidades excesivas de memoria bloqueada en páginas cuando un controlador coloca estos búferes en la memoria AGP.

-   El tercer parámetro es el miembro D3DFMT \_ INDEX16 o D3DFMT \_ INDEX32 del tipo enumerado [D3DFORMAT](d3dformat.md) que especifica el tamaño de cada índice.

-   El cuarto parámetro es un miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) que indica al sistema dónde colocar el nuevo búfer de índice en la memoria.

-   El último parámetro que [**IDirect3DDevice9:: CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) acepta es la dirección de una variable que se rellena con un puntero a la nueva interfaz [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) del objeto de búfer de vértices, si la llamada se realiza correctamente.

En el ejemplo de código de C++ siguiente se muestra cómo la creación de un búfer de índice podría ser similar en el código.


```
/*
 * For the purposes of this example, the d3dDevice variable is the 
 * address of an IDirect3DDevice9 interface exposed by a 
 * Direct3DDevice object, g_IB is a variable of type 
 * LPDIRECT3DINDEXBUFFER9.
 */

if( FAILED( d3dDevice->CreateIndexBuffer( 16384 *sizeof(WORD),
           D3DUSAGE_WRITEONLY, D3DFMT_INDEX16, D3DPOOL_DEFAULT, 
           &g_IB, NULL ) ) )
    return E_FAIL;
```



## <a name="access-an-index-buffer"></a>Acceder a un búfer de índice

Los objetos de búfer de índice permiten a las aplicaciones tener acceso directamente a la memoria asignada para los datos de índice. Puede recuperar un puntero a la memoria del búfer de índice llamando al método [**IDirect3DIndexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) y, a continuación, accediendo a la memoria según sea necesario para rellenar el búfer con nuevos datos de índice o para leer los datos que contiene. El método lock acepta cuatro parámetros. El primero, *OffsetToLock*, es el desplazamiento en los datos del índice. El segundo parámetro es el tamaño, medido en bytes, de los datos del índice. El tercer parámetro aceptado por el método **IDirect3DIndexBuffer9:: Lock** , *ppbData*, es la dirección de un puntero de bytes rellenado con un puntero a los datos del índice, si la llamada se realiza correctamente.

El último parámetro, *Flags*, indica al sistema cómo debe bloquearse la memoria. Puede utilizarlo para indicar el modo en que la aplicación tiene acceso a los datos en el búfer. Especifique las constantes del parámetro *Flags* según la forma en que la aplicación tendrá acceso a los datos del índice. Esto permite que el controlador bloquee la memoria y proporcione el mejor rendimiento según el tipo de acceso solicitado. Use \_ la marca ReadOnly de D3DLOCK si la aplicación solo va a leer desde la memoria del búfer de índice. La inclusión de esta marca permite a Direct3D optimizar sus procedimientos internos para mejorar la eficacia, dado que el acceso a la memoria será de solo lectura.

Después de rellenar o leer los datos del índice, llame al método [**IDirect3DIndexBuffer9:: Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-unlock) , tal como se muestra en el ejemplo de código siguiente.


```
// This code example assumes the m_pIndexBuffer is a variable of type 
// LPDIRECT3DINDEXBUFFER9 and that g_Indices has been properly 
// initialized with indices.

// To fill the index buffer, you must lock the buffer to gain 
// access to the indices. This mechanism is required because index
// buffers may be in device memory.

VOID* pIndices;

if( FAILED( m_pIndexBuffer->Lock( 
      0,                 // Fill from start of the buffer
      sizeof(g_Indices), // Size of the data to load
      BYTE**)&pIndices,  // Returned index data
      0 ) ) )            // Send default flags to the lock
{
    SAFE_RELEASE(m_pIndexBuffer);
    return E_FAIL;
}

memcpy( pIndices, g_Indices, sizeof(g_Indices) );
m_pIndexBuffer->Unlock();
```



> [!Note]
>
> Si crea un búfer de índice con la \_ marca WRITEONLY de D3DUSAGE, no use la \_ marca de bloqueo de solo lectura D3DLOCK. Use la \_ marca ReadOnly de D3DLOCK si la aplicación solo va a leer desde la memoria del búfer de índice. La inclusión de esta marca permite a Direct3D optimizar sus procedimientos internos para mejorar la eficacia, dado que el acceso a la memoria será de solo lectura.
>
> Para obtener información sobre el uso de D3DLOCK \_ discard o D3DLOCK \_ NOOVERWRITE para el parámetro *Flags* del método [**IDirect3DIndexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) , vea [optimizaciones de rendimiento (Direct3D 9)](performance-optimizations.md).

 

En C++, dado que tiene acceso directo a la memoria asignada para el búfer de índice, asegúrese de que la aplicación tenga acceso correctamente a la memoria asignada. De lo contrario, se arriesga a representar que la memoria no es válida. Use el paso del formato de índice que utiliza la aplicación para pasar de un índice del búfer asignado a otro.

Recupere información sobre un búfer de índice mediante una llamada al método [**IDirect3DIndexBuffer9:: GetDesc**](/windows/desktop/api) . Este método rellena los miembros de la estructura [**D3DINDEXBUFFER \_ DESC**](d3dindexbuffer-desc.md) con información sobre el búfer de índice.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos de Direct3D](direct3d-resources.md)
</dt> <dt>

[Representación de búferes de vértices y de índices (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> <dt>

[Búferes de vértices (Direct3D 9)](vertex-buffers.md)
</dt> </dl>

 

 
