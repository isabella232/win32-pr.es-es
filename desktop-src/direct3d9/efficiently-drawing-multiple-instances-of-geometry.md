---
description: Dada una escena que contiene muchos objetos que usan la misma geometría, puede dibujar muchas instancias de esa geometría en diferentes orientaciones, tamaños, colores, y así sucesivamente con un rendimiento considerablemente mejor al reducir la cantidad de datos que necesita proporcionar al representador.
ms.assetid: d8d9b0c8-b1c4-406d-bf2a-9716d725aec7
title: Dibujo eficaz de varias instancias de geometry (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9981dff913b704fca5e6b211b57e3647fddd28c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964956"
---
# <a name="efficiently-drawing-multiple-instances-of-geometry-direct3d-9"></a>Dibujo eficaz de varias instancias de geometry (Direct3D 9)

Dada una escena que contiene muchos objetos que usan la misma geometría, puede dibujar muchas instancias de esa geometría en diferentes orientaciones, tamaños, colores, y así sucesivamente con un rendimiento considerablemente mejor al reducir la cantidad de datos que necesita proporcionar al representador.

Esto se puede lograr mediante el uso de dos técnicas: la primera para dibujar geometría indexada y la segunda para la geometría no indexada. Ambas técnicas usan dos búferes de vértices: uno para proporcionar datos de geometría y otro para proporcionar datos de instancia por objeto. Los datos de instancia pueden ser una amplia variedad de información, como una transformación, datos de color o datos de iluminación, básicamente cualquier cosa que se pueda describir en una declaración de vértice. Dibujar muchas instancias de geometry con estas técnicas puede reducir drásticamente la cantidad de datos enviados al representador.

-   [Dibujar geometría indizada](#drawing-indexed-geometry)
    -   [Comparación de rendimiento de geometría indizada](#indexed-geometry-performance-comparison)
-   [Dibujar geometría no indizada](#drawing-non-indexed-geometry)
    -   [Comparación de rendimiento de geometría no indexada](#non-indexed-geometry-performance-comparison)
-   [Temas relacionados](#related-topics)

## <a name="drawing-indexed-geometry"></a>Dibujar geometría indizada

El búfer de vértice contiene datos por vértice definidos por una declaración de vértice. Supongamos que parte de cada vértice contiene datos de geometría y que parte de cada vértice contiene datos de instancia por objeto, como se muestra en el diagrama siguiente.

![diagrama de un búfer de vértices para geometría indizada](images/drawingmultipleinstances.png)

Esta técnica requiere un dispositivo que admita el modelo de sombreador de vértices \_ 3 0. Esta técnica funciona con cualquier sombreador programable, pero no con la canalización de función fija.

Para los búferes de vértices mostrados anteriormente, estas son las declaraciones de búfer de vértice correspondientes:


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



Estas declaraciones definen dos búferes de vértice. La primera declaración (para la secuencia 0, indicada por los ceros de la columna 1) define los datos de geometría que constan de: datos de coordenadas de posición, normal, tangente, binormal y textura.

La segunda declaración (para el flujo 1, indicada por los de la columna 1) define los datos de instancia por objeto. Cada instancia se define mediante cuatro números de punto flotante de cuatro componentes y un color de cuatro componentes. Los cuatro primeros valores se podrían usar para inicializar una matriz de 4x4, lo que significa que estos datos tendrán un tamaño, una posición y un giro únicos de cada instancia de la geometría. Los cuatro primeros componentes usan una semántica de coordenadas de textura que, en este caso, significa "se trata de un número general de cuatro componentes". Cuando use datos arbitrarios en una declaración de vértice, use una semántica de coordenadas de textura para marcarla. El último elemento de la secuencia se usa para los datos de color. Esto se podría aplicar en el sombreador de vértices para proporcionar a cada instancia un color único.

Antes de la representación, debe llamar a [**SetStreamSourceFreq para**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) enlazar los flujos de búfer de vértices al dispositivo. Este es un ejemplo que enlaza ambos búferes de vértice:


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



[**SetStreamSourceFreq usa**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) [D3DSTREAMSOURCE \_ INDEXEDDATA para](other-direct3d-constants.md) identificar los datos de geometría indizados. En este caso, el flujo 0 contiene los datos indexados que describen la geometría del objeto. Este valor se combina lógicamente con el número de instancias de la geometría que se va a dibujar.

Tenga en cuenta que D3DSTREAMSOURCE INDEXEDDATA y el número de instancias que se deben dibujar siempre deben \_ establecerse en el flujo cero.

En la segunda llamada, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) usa [D3DSTREAMSOURCE \_ INSTANCEDATA](other-direct3d-constants.md) para identificar la secuencia que contiene los datos de instancia. Este valor se combina lógicamente con 1, ya que cada vértice contiene un conjunto de datos de instancia.

Las dos últimas llamadas a [**SetStreamSource enlazan**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) los punteros del búfer de vértices al dispositivo.

Cuando haya terminado de representar los datos de instancia, asegúrese de restablecer la frecuencia de flujo de vértices a su estado predeterminado (que no usa la creación de instancias). Dado que en este ejemplo se han usado dos secuencias, establezca ambas secuencias como se muestra a continuación:


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="indexed-geometry-performance-comparison"></a>Comparación de rendimiento de geometría indizada

Aunque no es posible realizar una sola conclusión sobre cuánto podría reducir esta técnica el tiempo de representación en cada aplicación, tenga en cuenta la diferencia en la cantidad de datos transmitidos al tiempo de ejecución y el número de cambios de estado que se reducirán si se usa la técnica de creación de instancias. Esta secuencia de representación aprovecha el dibujo de varias instancias de la misma geometría:


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



Observe que se llama al bucle de representación una vez, los datos de geometry se transmiten una vez y n instancias se transmiten una vez. Esta siguiente secuencia de representación es idéntica en funcionalidad, pero no aprovecha las ventajas de la creación de instancias:


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



Observe que todo el bucle de representación está encapsulado por un segundo bucle para dibujar cada objeto. Ahora los datos de geometría se transmiten al representador n veces (en lugar de una vez) y cualquier estado de canalización también se puede establecer de forma redundante para cada objeto dibujado. Es muy probable que esta secuencia de representación sea significativamente más lenta. Observe también que los parámetros [**de DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) no han cambiado entre los dos bucles de representación.

## <a name="drawing-non-indexed-geometry"></a>Dibujar geometría no indizada

En [Dibujar geometría indexada,](#drawing-indexed-geometry)los búferes de vértice se configuraron para dibujar varias instancias de geometría indexada con mayor eficacia. También puede usar [**SetStreamSourceFreq para**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) dibujar geometría no indizada. Esto requiere un diseño de búfer de vértices diferente y tiene restricciones diferentes. Para dibujar geometría no indexada, prepare los búferes de vértices como en el diagrama siguiente.

![diagrama de un búfer de vértices para geometría no indexada](images/olderstyleinstancing.png)

Esta técnica no es compatible con la aceleración de hardware en ningún dispositivo. Solo es compatible con el procesamiento de vértices de software y solo funcionará con sombreadores frente a [ \_ \_ 3 0.](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md)

Dado que esta técnica funciona con geometría no indexada, no hay ningún búfer de índice. Como se muestra en el diagrama, el búfer de vértices que contiene geometría contiene n copias de los datos de geometría. Para cada instancia dibujada, los datos de geometría se leen desde el primer búfer de vértices y los datos de instancia se leen desde el segundo búfer de vértices.

Estas son las declaraciones de búfer de vértices correspondientes:


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



Estas declaraciones son idénticas a las declaraciones realizadas en el ejemplo de geometría indizada. Una vez más, la primera declaración (para la secuencia 0) define los datos geometry y la segunda declaración (para el flujo 1) define los datos de instancia por objeto. Al crear el primer búfer de vértices, asegúrese de cargarlo con el número de instancias de los datos de geometría que va a dibujar.

Antes de la representación, debe configurar el divisor que indica al tiempo de ejecución cómo dividir el primer búfer de vértices en n instancias. A continuación, establezca el divisor [**mediante SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) de la siguiente forma:


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



La primera llamada a [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) indica que el flujo 0 contiene n instancias de m vértices. [**A continuación, SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) enlaza el flujo 0 al búfer de vértices de geometría.

En la segunda llamada, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) identifica el flujo 1 como el origen de los datos de instancia. El segundo parámetro es el número de vértices de cada objeto (m). Recuerde que el flujo de datos de instancia siempre debe declararse como la segunda secuencia. [**A continuación, SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) enlaza el flujo 1 al búfer de vértices que contiene los datos de instancia.

Cuando haya terminado de representar los datos de instancia, asegúrese de restablecer la frecuencia de flujo de vértices a su estado predeterminado. Dado que en este ejemplo se han usado dos secuencias, establezca ambas secuencias como se muestra a continuación:


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="non-indexed-geometry-performance-comparison"></a>Comparación de rendimiento de geometría no indexada

La principal ventaja de este estilo de creación de instancias es que se puede usar en geometría no indizada. Aunque no es posible realizar una sola conclusión sobre cuánto podría reducir esta técnica el tiempo de representación en cada aplicación, tenga en cuenta la diferencia en la cantidad de datos transmitidos al tiempo de ejecución y el número de cambios de estado que se reducirán para la siguiente secuencia de representación:


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



Observe que se llama al bucle de representación una vez. Los datos de geometría se transmiten una vez, aunque no hay instancias de la geometría que se transmite. Los datos del búfer del vértice de instancia se transmiten una vez. Esta siguiente secuencia de representación es idéntica en funcionalidad, pero no aprovecha las ventajas de la creación de instancias:


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



Sin la creación de instancias, el bucle de representación debe ajustarse mediante un segundo bucle para dibujar cada objeto. Al eliminar el segundo bucle de representación, debería esperar un mejor rendimiento debido a menos cambios de estado de representación a los que se llama dentro del bucle.

En general, es razonable esperar que la técnica indexada (dibujar geometría[indizada)](#drawing-indexed-geometry)se realice mejor que la técnica no indexada[(dibujar](#drawing-non-indexed-geometry)geometría no indizada), ya que la técnica indizada solo transmite una copia de los datos de geometría. Observe que los parámetros [**de DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) no han cambiado para ninguna de las secuencias de representación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas avanzados](advanced-topics.md)
</dt> <dt>

[Ejemplo de creación de instancias](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)
</dt> </dl>

 

 
