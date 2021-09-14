---
description: Los búferes de índice, representados por la interfaz IDirect3DIndexBuffer9, son búferes de memoria que contienen datos de índice.
ms.assetid: baa60cd1-a1f0-4dbe-b934-aeb1a5c6b784
title: Búferes de índice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7151fae6deb72a0c569d269c80e5b13bf946f9d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264487"
---
# <a name="index-buffers-direct3d-9"></a>Búferes de índice (Direct3D 9)

Los búferes de índice, representados por la [**interfaz IDirect3DIndexBuffer9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) son búferes de memoria que contienen datos de índice. Los datos de índice, o índices, son desplazamientos enteros en búferes de vértice y se usan para representar primitivas mediante el método [**IDirect3DDevice9::D rawIndexedPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)

Un búfer de vértices contiene vértices; por lo tanto, puede dibujar un búfer de vértices con o sin primitivas indizadas. Sin embargo, dado que un búfer de índice contiene índices, no se puede usar un búfer de índice sin un búfer de vértices correspondiente. (Como nota lateral, [**IDirect3DDevice9::D rawIndexedPrimitiveUP**](/windows/desktop/api) e [**IDirect3DDevice9::D rawPrimitiveUP**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup) son los únicos métodos de dibujo que se dibujan sin un índice o un búfer de vértices).

## <a name="index-buffer-description"></a>Descripción del búfer de índice

Un búfer de índice se describe en términos de sus funcionalidades, como dónde existe en la memoria, si admite lectura y escritura, y el tipo y el número de índices que puede contener. Estos rasgos se mantienen en una [**estructura D3DINDEXBUFFER \_ DESC.**](d3dindexbuffer-desc.md)

Las descripciones del búfer de índice le dicen a la aplicación cómo se creó un búfer existente. Proporcione una estructura de descripción vacía para que el sistema rellene las funcionalidades de un búfer de índice creado previamente.

-   El miembro Format describe el formato de superficie de los datos del búfer de índice.
-   El tipo identifica el tipo de recurso del búfer de índice.
-   El miembro usage structure contiene marcas de funcionalidad general. La marca D3DUSAGE SOFTWAREPROCESSING indica que el búfer de índice se va a usar con el procesamiento de \_ vértices de software. La presencia de la marca WRITEONLY de D3DUSAGE en Usage indica que la memoria del búfer de índice solo se usa \_ para las operaciones de escritura. Esto libera al controlador para colocar los datos de índice en la mejor ubicación de memoria para permitir un procesamiento y una representación rápidos. Si no se usa la marca WRITEONLY de D3DUSAGE, es menos probable que el controlador coloque los datos en una ubicación ineficaz para las operaciones \_ de lectura. Esto sacrifique algo de velocidad de procesamiento y representación. Si no se especifica esta marca, se supone que las aplicaciones realizan operaciones de lectura y escritura en los datos del búfer de índice.
-   Pool especifica la clase de memoria asignada para el búfer de índice. La marca SYSTEMMEM de D3DPOOL indica que el sistema creó el \_ búfer de índice en la memoria del sistema.
-   El miembro Size almacena el tamaño, en bytes, de los datos del búfer de vértices.
-   No se usa el último parámetro pSharedHandle. Esta establezca esta propiedad **en NULL.**

## <a name="index-processing-requirements"></a>Requisitos de procesamiento de índices

El rendimiento de las operaciones de procesamiento de índices depende en gran medida de dónde exista el búfer de índice en la memoria y del tipo de dispositivo de representación que se esté utilizando. Las aplicaciones controlan la asignación de memoria para los búferes de índice cuando se crean. Cuando se establece la marca de memoria D3DPOOL \_ SYSTEMMEM, el búfer de índice se crea en la memoria del sistema. Cuando se usa la marca de memoria D3DPOOL DEFAULT, el controlador de dispositivo determina dónde se asigna mejor la memoria para el búfer de índice, a menudo denominada memoria óptima para el \_ controlador. La memoria óptima del controlador puede ser memoria de vídeo local, memoria de vídeo no local o memoria del sistema.

Establecer la marca de comportamiento D3DUSAGE SOFTWAREPROCESSING al llamar al método \_ [**IDirect3DDevice9::CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) especifica que el búfer de índice se va a usar con el procesamiento de vértices de software. Esta marca es necesaria en el procesamiento de vértices en modo mixto (D3DCREATE \_ MIXED VERTEXPROCESSING) cuando se usa el procesamiento de \_ vértices de software.

La aplicación puede escribir directamente índices en un búfer de índice asignado en la memoria óptima del controlador. Esta técnica evita una operación de copia redundante más adelante. Esta técnica no funciona bien si la aplicación lee datos de nuevo desde un búfer de índice, ya que las operaciones de lectura realizadas por el host desde la memoria óptima del controlador pueden ser muy lentas. Por lo tanto, si la aplicación necesita leer durante el procesamiento o escribe datos en el búfer de forma errática, un búfer de índice de memoria del sistema es una mejor opción.

> [!Note]  
> Use siempre D3DPOOL DEFAULT, excepto cuando no desee usar memoria de vídeo o usar grandes cantidades de RAM bloqueada por página cuando el controlador coloca búferes de vértices o índices en la memoria \_ AGP.

 

## <a name="create-an-index-buffer"></a>Creación de un búfer de índice

Cree un objeto de búfer de índice llamando al método [**IDirect3DDevice9::CreateIndexBuffer,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) que acepta seis parámetros.

-   El primer parámetro especifica la longitud del búfer de índice, en bytes.
-   El segundo parámetro es un conjunto de controles de uso. Entre otras cosas, su valor determina si los vértices a los que hacen referencia los índices pueden contener información de recorte. Para mejorar el rendimiento, especifique D3DUSAGE \_ DONOTCLIP cuando no sea necesario recortar.

    La marca D3DUSAGE SOFTWAREPROCESSING se puede establecer cuando el procesamiento de vértices de software o de modo mixto \_ (D3DCREATE \_ MIXED \_ VERTEXPROCESSING/D3DCREATE \_ SOFTWARE \_ VERTEXPROCESSING) está habilitado para ese dispositivo. D3DUSAGE SOFTWAREPROCESSING debe establecerse para que los búferes se usen con el procesamiento de vértices de software en modo mixto, pero no se debe establecer para obtener el mejor rendimiento posible cuando se usa el procesamiento de índices de hardware en modo mixto \_ (D3DCREATE \_ HARDWARE \_ VERTEXPROCESSING). Sin embargo, establecer D3DUSAGE SOFTWAREPROCESSING es la única opción cuando se usa un solo búfer con el procesamiento de \_ vértices de hardware y software. D3DUSAGE \_ SOFTWAREPROCESSING se permite para dispositivos mixtos y de software.

    Es posible forzar los búferes de vértices e índices en la memoria del sistema especificando D3DPOOL SYSTEMMEM, incluso cuando el procesamiento del índice se realiza \_ en hardware. Se trata de una manera de evitar grandes cantidades de memoria bloqueada por páginas cuando un controlador coloca estos búferes en la memoria de AGP.

-   El tercer parámetro es el miembro D3DFMT INDEX16 o D3DFMT INDEX32 del tipo enumerado \_ \_ [D3DFORMAT](d3dformat.md) que especifica el tamaño de cada índice.

-   El cuarto parámetro es un miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) que indica al sistema dónde se debe colocar en memoria el nuevo búfer de índice.

-   El parámetro final que [**acepta IDirect3DDevice9::CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) es la dirección de una variable que se rellena con un puntero a la nueva interfaz [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) del objeto de búfer de vértices, si la llamada se realiza correctamente.

En el siguiente ejemplo de código de C++ se muestra el aspecto que podría tener la creación de un búfer de índice en el código.


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



## <a name="access-an-index-buffer"></a>Acceso a un búfer de índice

Los objetos de búfer de índice permiten que las aplicaciones accedan directamente a la memoria asignada para los datos de índice. Puede recuperar un puntero a la memoria del búfer de índice llamando al método [**IDirect3DIndexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) y, a continuación, accediendo a la memoria según sea necesario para rellenar el búfer con nuevos datos de índice o para leer los datos que contiene. El método Lock acepta cuatro parámetros. El primero, *OffsetToLock*, es el desplazamiento en los datos de índice. El segundo parámetro es el tamaño, medido en bytes, de los datos de índice. El tercer parámetro aceptado por el método **IDirect3DIndexBuffer9::Lock,** *ppbData*, es la dirección de un puntero BYTE rellenado con un puntero a los datos del índice, si la llamada se realiza correctamente.

El último parámetro, *Flags*, indica al sistema cómo se debe bloquear la memoria. Puede usarlo para indicar cómo la aplicación accede a los datos del búfer. Especifique constantes para el *parámetro Flags* según la forma en que la aplicación tendrá acceso a los datos de índice. Esto permite al controlador bloquear la memoria y proporcionar el mejor rendimiento dado el tipo de acceso solicitado. Use la marca D3DLOCK \_ READONLY si la aplicación solo leerá desde la memoria del búfer de índice. La inclusión de esta marca permite a Direct3D optimizar sus procedimientos internos para mejorar la eficacia, dado que el acceso a la memoria será de solo lectura.

Después de rellenar o leer los datos del índice, llame al método [**IDirect3DIndexBuffer9::Unlock,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-unlock) como se muestra en el ejemplo de código siguiente.


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
> Si crea un búfer de índice con la marca WRITEONLY D3DUSAGE, no use la marca de bloqueo \_ D3DLOCK \_ READONLY. Use la marca D3DLOCK \_ READONLY si la aplicación solo leerá desde la memoria del búfer de índice. La inclusión de esta marca permite a Direct3D optimizar sus procedimientos internos para mejorar la eficacia, dado que el acceso a la memoria será de solo lectura.
>
> Para obtener información sobre el uso de D3DLOCK DISCARD o D3DLOCK NOOVERWRITE para el parámetro Flags del método \_ \_ [**IDirect3DIndexBuffer9::Lock,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) vea Optimizaciones de [rendimiento (Direct3D 9).](performance-optimizations.md) 

 

En C++, dado que accede directamente a la memoria asignada para el búfer de índice, asegúrese de que la aplicación accede correctamente a la memoria asignada. De lo contrario, corre el riesgo de representar esa memoria como no válida. Use el paso del formato de índice que usa la aplicación para pasar de un índice del búfer asignado a otro.

Recupere información sobre un búfer de índice llamando al [**método IDirect3DIndexBuffer9::GetDesc.**](/windows/desktop/api) Este método rellena los miembros de la estructura [**D3DINDEXBUFFER \_ DESC**](d3dindexbuffer-desc.md) con información sobre el búfer de índice.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos de Direct3D](direct3d-resources.md)
</dt> <dt>

[Representación a partir de búferes de vértice e índice (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> <dt>

[Búferes de vértices (Direct3D 9)](vertex-buffers.md)
</dt> </dl>

 

 
