---
description: Dada una escena que contiene muchos objetos que usan la misma geometría, puede dibujar muchas instancias de esa geometría en distintas orientaciones, tamaños, colores, etc., con un rendimiento mucho mejor, reduciendo la cantidad de datos que necesita proporcionar al representador.
ms.assetid: d8d9b0c8-b1c4-406d-bf2a-9716d725aec7
title: Dibujo eficaz de varias instancias de Geometry (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9981dff913b704fca5e6b211b57e3647fddd28c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906444"
---
# <a name="efficiently-drawing-multiple-instances-of-geometry-direct3d-9"></a>Dibujo eficaz de varias instancias de Geometry (Direct3D 9)

Dada una escena que contiene muchos objetos que usan la misma geometría, puede dibujar muchas instancias de esa geometría en distintas orientaciones, tamaños, colores, etc., con un rendimiento mucho mejor, reduciendo la cantidad de datos que necesita proporcionar al representador.

Esto se puede lograr mediante el uso de dos técnicas: la primera para dibujar geometría indizada y la segunda para geometría no indizada. Ambas técnicas usan dos búferes de vértices: uno para proporcionar datos de geometría y otro para proporcionar datos de instancia por objeto. Los datos de instancia pueden ser una gran variedad de información, como una transformación, datos de color o datos de iluminación, básicamente todo lo que se puede describir en una declaración de vértice. Dibujar muchas instancias de Geometry con estas técnicas puede reducir drásticamente la cantidad de datos que se envían al representador.

-   [Dibujar geometría indizada](#drawing-indexed-geometry)
    -   [Comparación de rendimiento de geometría indizada](#indexed-geometry-performance-comparison)
-   [Dibujo de geometría no indizada](#drawing-non-indexed-geometry)
    -   [Comparación de rendimiento de geometría no indizada](#non-indexed-geometry-performance-comparison)
-   [Temas relacionados](#related-topics)

## <a name="drawing-indexed-geometry"></a>Dibujar geometría indizada

El búfer de vértice contiene datos por vértice que se definen mediante una declaración de vértice. Supongamos que parte de cada vértice contiene datos de geometría y que parte de cada vértice contiene datos de instancia por objeto, tal y como se muestra en el diagrama siguiente.

![diagrama de un búfer de vértices para geometría indizada](images/drawingmultipleinstances.png)

Esta técnica requiere un dispositivo que admita el \_ modelo de sombreador de vértices 3 0. Esta técnica funciona con cualquier sombreador programable, pero no con la canalización de funciones fijas.

En el caso de los búferes de vértices mostrados anteriormente, estas son las declaraciones de búfer de vértice correspondientes:


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



Estas declaraciones definen dos búferes de vértices. La primera declaración (para la secuencia 0, indicada por los ceros de la columna 1) define los datos de geometría que se componen de: posición, normal, tangente, binormalización y datos de coordenadas de textura.

La segunda declaración (para la secuencia 1, indicada por las de la columna 1) define los datos de instancia por objeto. Cada instancia se define mediante números de punto flotante del componente 4 4 y un color de cuatro componentes. Los primeros cuatro valores se pueden usar para inicializar una matriz 4x4, lo que significa que estos datos dimensionarán, posicionarán y girarán de forma exclusiva cada instancia de la geometría. Los primeros cuatro componentes usan una semántica de coordenadas de textura que, en este caso, significa "Esto es un número de cuatro componentes general". Cuando se usan datos arbitrarios en una declaración de vértice, se usa una semántica de coordenadas de textura para marcarlo. El último elemento de la secuencia se utiliza para los datos de color. Esto se podría aplicar en el sombreador de vértices para asignar a cada instancia un color único.

Antes de la representación, debe llamar a [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) para enlazar las secuencias del búfer de vértices al dispositivo. Este es un ejemplo en el que se enlazan ambos búferes de vértice:


```
// Set up the geometry data stream
pd3dDevice->SetStreamSourceFreq(0,
    (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
    D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1,
    (D3DSTREAMSOURCE_INSTANCEDATA | 1));
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
    D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



[**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) usa [D3DSTREAMSOURCE \_ INDEXEDDATA](other-direct3d-constants.md) para identificar los datos de geometría indexados. En este caso, stream 0 contiene los datos indizados que describen la geometría del objeto. Este valor se combina lógicamente con el número de instancias de la geometría que se va a dibujar.

Tenga en cuenta que D3DSTREAMSOURCE \_ INDEXEDDATA y el número de instancias que se van a dibujar siempre se deben establecer en el flujo cero.

En la segunda llamada, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) usa [D3DSTREAMSOURCE \_ INSTANCEDATA](other-direct3d-constants.md) para identificar la secuencia que contiene los datos de la instancia. Este valor se combina lógicamente con 1 porque cada vértice contiene un conjunto de datos de instancia.

Las dos últimas llamadas a [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) enlazan los punteros de búfer de vértices al dispositivo.

Cuando haya terminado de representar los datos de la instancia, asegúrese de restablecer la frecuencia del flujo de vértices a su estado predeterminado (que no usa la creación de instancias). Dado que en este ejemplo se usan dos flujos, establezca ambos flujos como se muestra a continuación:


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="indexed-geometry-performance-comparison"></a>Comparación de rendimiento de geometría indizada

Aunque no es posible realizar una conclusión única sobre el grado en que esta técnica puede reducir el tiempo de representación en cada aplicación, tenga en cuenta la diferencia en la cantidad de datos transmitidos en el tiempo de ejecución y el número de cambios de estado que se reducirán si usa la técnica de creación de instancias. Esta secuencia de representación aprovecha las ventajas de dibujar varias instancias de la misma geometría:


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set up the geometry data stream
    pd3dDevice->SetStreamSourceFreq(0,
                (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1,
                (D3DSTREAMSOURCE_INSTANCEDATA | 1));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



Observe que el bucle de representación se llama una vez, los datos de geometría se transmiten una vez y n instancias se transmiten una vez. Esta secuencia de representación siguiente es idéntica en la funcionalidad, pero no aprovecha las ventajas de la creación de instancias:


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));


        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }                             
    
    pd3dDevice->EndScene();
}
```



Observe que el bucle de representación completo está incluido en un segundo bucle para dibujar cada objeto. Ahora los datos de geometría se transmiten en el representador n veces (en lugar de una vez) y cualquier estado de canalización también se puede establecer de forma redundante para cada objeto dibujado. Es muy probable que esta secuencia de representación sea mucho más lenta. Observe también que los parámetros de [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) no han cambiado entre los dos bucles de representación.

## <a name="drawing-non-indexed-geometry"></a>Dibujo de geometría no indizada

En el [dibujo de geometría indizada](#drawing-indexed-geometry), los búferes de vértices se configuraron para dibujar varias instancias de geometría indizada con mayor eficacia. También puede usar [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) para dibujar geometría no indizada. Esto requiere un diseño de búfer de vértices diferente y tiene distintas restricciones. Para dibujar geometría no indizada, prepare los búferes de vértices como el diagrama siguiente.

![diagrama de un búfer de vértices para geometría no indizada](images/olderstyleinstancing.png)

Esta técnica no es compatible con la aceleración de hardware en cualquier dispositivo. Solo se admite en el procesamiento de vértices de software y solo funcionará con los sombreadores de [vs \_ 3 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md) .

Dado que esta técnica funciona con geometría no indizada, no hay ningún búfer de índice. Como se muestra en el diagrama, el búfer de vértices que contiene Geometry contiene n copias de los datos de geometría. Para cada instancia dibujada, los datos de geometría se leen desde el primer búfer de vértices y los datos de instancia se leen desde el segundo búfer de vértices.

Estas son las declaraciones de búfer de vértice correspondientes:


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



Estas declaraciones son idénticas a las declaraciones realizadas en el ejemplo de geometría indizada. Una vez más, la primera declaración (para Stream 0) define los datos de geometría y la segunda declaración (para Stream 1) define los datos de instancia por objeto. Al crear el primer búfer de vértices, asegúrese de cargarlo con el número de instancias de los datos de geometría que va a dibujar.

Antes de la representación, debe configurar el divisor, que indica al tiempo de ejecución cómo dividir el primer búfer de vértices en n instancias. A continuación, establezca el divisor con [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) de la siguiente manera:


```
// Set the divider
pd3dDevice->SetStreamSourceFreq(0, 1);
// Bind the stream to the vertex buffer
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
        D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance);
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
        D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



La primera llamada a [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) indica que el flujo 0 contiene n instancias de los vértices m. A continuación, [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) enlaza el flujo 0 al búfer de vértices de geometría.

En la segunda llamada, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) identifica la secuencia 1 como el origen de los datos de instancia. El segundo parámetro es el número de vértices de cada objeto (m). Recuerde que el flujo de datos de instancia siempre se debe declarar como la segunda secuencia. A continuación, [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) enlaza el flujo 1 al búfer de vértices que contiene los datos de instancia.

Cuando haya terminado de representar los datos de la instancia, asegúrese de restablecer la frecuencia del flujo de vértices a su estado predeterminado. Dado que en este ejemplo se usan dos flujos, establezca ambos flujos como se muestra a continuación:


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="non-indexed-geometry-performance-comparison"></a>Comparación de rendimiento de geometría no indizada

La principal ventaja de este estilo de creación de instancias es que se puede usar en geometría no indizada. Aunque no es posible realizar una conclusión única sobre el grado en que esta técnica puede reducir el tiempo de representación en cada aplicación, tenga en cuenta la diferencia en la cantidad de datos transmitidos en el tiempo de ejecución y el número de cambios de estado que se reducirán para la siguiente secuencia de representación:


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set the divider
    pd3dDevice->SetStreamSourceFreq(0, 1);
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



Observe que el bucle de representación se llama una vez. Los datos de geometría se transmiten una vez, aunque hay n instancias de la geometría que se transmite. Los datos del búfer de vértice de instancia se transmiten una vez. Esta secuencia de representación siguiente es idéntica en la funcionalidad, pero no aprovecha las ventajas de la creación de instancias:


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }
    
    pd3dDevice->EndScene();
}
```



Sin creación de instancias, el bucle de representación debe estar incluido en un segundo bucle para dibujar cada objeto. Al eliminar el segundo bucle de representación, debería esperar un mejor rendimiento debido a menos cambios en el estado de representación a los que se llama dentro del bucle.

En general, es razonable esperar que la técnica indizada ([dibujo de geometría indizada](#drawing-indexed-geometry)) funcione mejor que la técnica no indizada ([dibujo de geometría no indizada](#drawing-non-indexed-geometry)) porque la técnica indizada solo transmite una copia de los datos de geometría. Observe que los parámetros de [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) no han cambiado en ninguna de las secuencias de representación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas avanzados](advanced-topics.md)
</dt> <dt>

[Ejemplo de creación de instancias](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)
</dt> </dl>

 

 
