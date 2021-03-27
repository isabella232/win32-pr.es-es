---
title: Cómo indizar varios flujos de salida
description: En el modelo de sombreador 5, un sombreador de geometría puede admitir hasta 4 flujos independientes. Esto significa que un solo sombreador puede generar un resultado entre uno y cuatro flujos de salida, dependiendo del número de secuencias declaradas.
ms.assetid: 2ddde992-6746-4033-9190-bde7d7b14add
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8564917be9565e862043e370840f8ac7280f174
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075195"
---
# <a name="how-to-index-multiple-output-streams"></a>Cómo: indizar varios flujos de salida

En el modelo de sombreador 5, un sombreador de geometría puede admitir hasta 4 flujos independientes. Esto significa que un solo sombreador puede generar un resultado entre uno y cuatro flujos de salida, dependiendo del número de secuencias declaradas.

Para indizar varios flujos de salida

1.  Defina un flujo de datos mediante un tipo de plantilla de flujo.

    ```
        inout PointStream<OutVertex1> myStream1, 
    ```

    

2.  Defina un segundo flujo de datos mediante un tipo de plantilla de flujo.

    ```
        inout PointStream<OutVertex2> myStream2 )
    ```

    

3.  Los datos se envían a las secuencias (o ambas) mediante las funciones intrínsecas del objeto de salida de flujo (como Append o RestartStrip).

    ```
    void MyGS( 
        InVertex verts[2], 
        inout PointStream<OutVertex1> myStream1, 
        inout PointStream<OutVertex2> myStream2 )
    {
        OutVertex1 myVert1 = TransformVertex1( verts[0] );
        OutVertex2 myVert2 = TransformVertex2( verts[1] );
        myStream1.Append( myVert1 );
        myStream2.Append( myVert2 );
    }
    ```

    

Al usar un solo flujo de salida, puede emitir tiras de triángulo, tiras de líneas o listas de puntos. Cuando se almacenan bandas de triángulo y de línea en el búfer de flujo de salida, se expanden a listas de triángulos y líneas, respectivamente. También puede rasterizar una secuencia y no enviarla a un búfer de memoria.

Cuando se usan varios flujos de salida, todos los flujos deben contener puntos y hasta un flujo de salida se puede enviar al rasterizador. Lo más habitual es que una aplicación no rasterizará ningún flujo.

Después de transmitir los datos a un búfer, puede usar esos datos para representar cualquier tipo primitivo, no solo el tipo primitivo que usó para rellenar el búfer.

La salida total del sombreador de geometría está limitada a 1024 escalares. Cuando existen varias secuencias, el número de escalares se calcula a partir del tipo de flujo más grande multiplicado por el número máximo de vértices.



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Diferencias entre el modelo de sombreador 4 y el modelo de sombreador 5:<br/> Modelo de sombreador 4:<br/>
<ul>
<li>El número máximo de escalas para la salida de flujo es 64.</li>
<li>La máscara de registro por componente debe coincidir en el intervalo de índices.</li>
</ul>
Modelo de sombreador 5:<br/>
<ul>
<li>El número máximo de escalas para la salida de flujo es 128.</li>
<li>No es necesario que la máscara de registro por componente coincida en el intervalo de índices.</li>
<li>La indexación dinámica de salidas debe ser válida en todas las secuencias.</li>
<li>No es necesario que los modos de interpolación coincidan con las secuencias.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características del sombreador de geometría](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 





