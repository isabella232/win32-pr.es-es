---
title: Cómo indexar varias salidas Secuencias
description: En el modelo de sombreador 5, un sombreador de geometría puede admitir hasta 4 secuencias independientes. Esto significa que un solo sombreador puede generar entre uno y cuatro flujos de salida, dependiendo del número de secuencias declaradas.
ms.assetid: 2ddde992-6746-4033-9190-bde7d7b14add
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37aefd8b7cdcab05515bda6f81fa6c679751dc95
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473401"
---
# <a name="how-to-index-multiple-output-streams"></a>Cómo: Indexar varias salidas Secuencias

En el modelo de sombreador 5, un sombreador de geometría puede admitir hasta 4 secuencias independientes. Esto significa que un solo sombreador puede generar entre uno y cuatro flujos de salida, dependiendo del número de secuencias declaradas.

Para indexar varios flujos de salida

1.  Defina un flujo de datos mediante un tipo de plantilla de flujo.

    ```
        inout PointStream<OutVertex1> myStream1, 
    ```

    

2.  Defina un segundo flujo de datos mediante un tipo de plantilla de flujo.

    ```
        inout PointStream<OutVertex2> myStream2 )
    ```

    

3.  Salida de datos a secuencias (o a ambas) mediante las funciones intrínsecas del objeto de salida de secuencia (como Append o RestartStrip).

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

    

Al usar un único flujo de salida, puede emitir franjas de triángulo, franjas de líneas o listas de puntos. Cuando se almacenan franjas de triángulo y de línea en el búfer de transmisión por secuencias, se expanden a listas de triángulos y líneas, respectivamente. También puede rasterizar una secuencia y no enviarla a un búfer de memoria.

Cuando se usan varios flujos de salida, todas las secuencias deben contener puntos y se puede enviar hasta un flujo de salida al rasterizador. Más comúnmente, una aplicación no rasterizará ninguna secuencia.

Después de transmitir datos a un búfer, puede usar estos datos para representar cualquier tipo primitivo, no solo el tipo primitivo que usó para rellenar el búfer.

La salida total del sombreador de geometría se limita a 1024 escalares. Cuando existen varias secuencias, el número de escalares se calcula a partir del tipo de secuencia más grande multiplicado por el número máximo de vértices.




| | | Diferencias entre el modelo de sombreador 4 y el modelo de sombreador 5:<br /> Modelo de sombreador 4:<br /><ul><li>El número máximo de escalares para la salida del flujo es 64.</li><li>La máscara de registro por componente debe coincidir en el intervalo de índice.</li></ul>Modelo de sombreador 5:<br /><ul><li>El número máximo de escalares para la salida del flujo es 128.</li><li>No es necesario que la máscara de registro por componente coincida en el intervalo de índice.</li><li>La indexación dinámica de salidas debe ser legal en todas las secuencias.</li><li>No es necesario que los modos de interpolación coincidan con los flujos.</li></ul> | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Características del sombreador de geometría](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 





