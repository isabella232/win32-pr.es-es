---
title: Dibujo indirecto
description: El dibujo indirecto permite mover parte del recorrido de la escena y la selección de la CPU a la GPU, lo que puede mejorar el rendimiento. La CPU o la GPU pueden generar el búfer de comandos.
ms.assetid: F8D6C88A-101E-4F66-999F-43206F6527B6
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa474a469d5789d4b31830400d981ea771db2e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072959"
---
# <a name="indirect-drawing"></a>Dibujo indirecto

El dibujo indirecto permite mover parte del recorrido de la escena y la selección de la CPU a la GPU, lo que puede mejorar el rendimiento. La CPU o la GPU pueden generar el búfer de comandos.

-   [Firmas de comandos](#command-signatures)
-   [Estructuras de búfer de argumentos indirectos](#indirect-argument-buffer-structures)
-   [Creación de firmas de comandos](#command-signature-creation)
    -   [Sin cambios en los argumentos](#no-argument-changes)
    -   [Constantes raíz y búferes de vértices](#root-constants-and-vertex-buffers)
-   [Temas relacionados](#related-topics)

## <a name="command-signatures"></a>Firmas de comandos

El objeto de firma de comando ([**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature)) permite a las aplicaciones especificar el dibujo indirecto, en particular estableciendo lo siguiente:

-   Formato de búfer de argumento indirecto.
-   Tipo de comando que se usará (de los [**métodos ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) [**DrawInstanced,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) [**DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)o [**Dispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)).
-   Conjunto de enlaces de recursos que cambiarán la llamada por comando frente al conjunto que se heredará.

En el inicio, una aplicación crea un pequeño conjunto de firmas **de comandos**. En tiempo de ejecución, la aplicación rellena un búfer con comandos (a través de cualquier medio que elija el desarrollador de la aplicación). Opcionalmente, los comandos que contienen el estado que se va a establecer para las vistas del búfer de vértices, las vistas de búfer de índice, las constantes raíz y los descriptores raíz (SRV/ UAV/CBV sin procesar o estructurados). Estos diseños de argumentos no son específicos del hardware, por lo que las aplicaciones pueden generar los búferes directamente. La firma de comando hereda el estado restante de la lista de comandos. A continuación, la aplicación llama a [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) para indicar a la GPU que interprete el contenido del búfer de argumento indirecto según el formato definido por una firma de comando determinada.

Si la firma del comando cambia los argumentos raíz, se almacena en la firma del comando como un subconjunto de una firma raíz.

Tenga en cuenta que ningún estado de firma de comando vuelve a la lista de comandos cuando se completa la ejecución.

Por ejemplo, suponga que un desarrollador de aplicaciones quiere que se especifique una constante raíz única por cada llamada a draw en el búfer de argumento indirecto. La aplicación crearía una firma de comando que permite al búfer de argumento indirecto especificar los parámetros siguientes por llamada a draw:

-   Valor de una constante raíz.
-   Argumentos de dibujo (recuento de vértices, recuento de instancias, etc.).

El búfer de argumento indirecto generado por la aplicación contendrá una matriz de registros de tamaño fijo. Cada estructura corresponde a una llamada draw. Cada estructura contiene los argumentos de dibujo y el valor de la constante raíz. El número de llamadas a draw se especifica en un búfer independiente visible para GPU.

A continuación se muestra un búfer de comandos de ejemplo generado por la aplicación:

![formato de búfer de comandos](images/indirect-drawing-command-buffer.png)

## <a name="indirect-argument-buffer-structures"></a>Estructuras de búfer de argumentos indirectos

Las estructuras siguientes definen cómo aparecen determinados argumentos en un búfer de argumento indirecto. Estas estructuras no aparecen en ninguna API D3D12. Las aplicaciones usan estas definiciones al escribir en un búfer de argumento indirecto (con la CPU o GPU):

-   [**D3D12 \_ DRAW \_ ARGUMENTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_arguments)
-   [**D3D12 \_ DRAW \_ INDEXED \_ ARGUMENTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_indexed_arguments)
-   [**ARGUMENTOS DE DISTRIBUCIÓN D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dispatch_arguments)
-   [**VISTA BÚFER DE VÉRTICES D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)
-   [**VISTA BÚFER DE ÍNDICE D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_index_buffer_view)
-   DIRECCIÓN VIRTUAL de GPU D3D12 \_ \_ \_ (sinónimo typedef'd de UINT64).
-   [**VISTA DE BÚFER CONSTANTE D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc)

## <a name="command-signature-creation"></a>Creación de firmas de comandos

Para crear una firma de comando, use los siguientes elementos de API:

-   [**ID3D12Device::CreateCommandSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandsignature) (genera un [**id3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature))
-   [**TIPO DE ARGUMENTO INDIRECTO D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_indirect_argument_type)
-   [**D3D12 \_ INDIRECT \_ ARGUMENT \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc)
-   [**FIRMA DESC DEL \_ COMANDO \_ D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc)

El orden de los argumentos dentro de un búfer de argumento indirecto se define para coincidir exactamente con el orden de los argumentos especificados en el *parámetro pArguments* de [**D3D12 \_ COMMAND SIGNATURE \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc). Todos los argumentos de una llamada draw (graphics)/dispatch (compute) dentro de un búfer de argumento indirecto están empaquetados estrechamente. Sin embargo, las aplicaciones pueden especificar un intervalo de bytes arbitrario entre los comandos draw/dispatch en un búfer de argumento indirecto.

La firma raíz debe especificarse si y solo si la firma del comando cambia uno de los argumentos raíz.

Para la raíz SRV/UAV/CBV, el tamaño especificado de la aplicación es en bytes. La capa de depuración validará las restricciones siguientes en la dirección:

-   CBV: la dirección debe ser un múltiplo de 256 bytes.
-   SRV/UAV sin formato: la dirección debe ser un múltiplo de 4 bytes.
-   SRV/UAV estructurado: la dirección debe ser un múltiplo del intervalo de bytes de estructura (declarado en el sombreador).

Una firma de comando determinada es una firma de comando draw o compute. Si una firma de comando contiene una operación de dibujo, es una firma de comando de gráficos. De lo contrario, la firma del comando debe contener una operación de envío y es una firma de comando de proceso.

En las secciones siguientes se muestran algunas firmas de comando de ejemplo.

### <a name="no-argument-changes"></a>Sin cambios en los argumentos

En este ejemplo, el búfer de argumento indirecto generado por la aplicación contiene una matriz de estructuras de 36 bytes. Cada estructura solo contiene los cinco parámetros pasados [**a DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) (más relleno).

A continuación se muestra el código para crear la descripción de la firma del comando:

``` syntax
D3D12_INDIRECT_ARGUMENT_DESC Args[1];
Args[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW_INDEXED;

D3D12_COMMAND_SIGNATURE_DESC ProgramDesc;
ProgramDesc.ByteStride = 36;
ProgramDesc.NumArgumentDescs = 1;
ProgramDesc.pArguments = Args;
```

El diseño de una sola estructura dentro de un búfer de argumento indirecto es:



| Bytes | Descripción           |
|-------|-----------------------|
| 0:3   | IndexCountPerInstance |
| 4:7   | InstanceCount         |
| 8:11  | StartIndexLocation    |
| 12:15 | BaseVertexLocation    |
| 16:19 | StartInstanceLocation |
| 20:35 | Relleno               |



 

### <a name="root-constants-and-vertex-buffers"></a>Constantes raíz y búferes de vértices

En este ejemplo, cada estructura de un búfer de argumento indirecto cambia dos constantes raíz, cambia un enlace de búfer de vértices y realiza una operación de dibujo no indizada. No hay relleno entre estructuras.

El código para crear la descripción de la firma del comando es:

``` syntax
D3D12_INDIRECT_ARGUMENT_DESC Args[4];
Args[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT;
Args[0].Constant.RootParameterIndex = 2;
Args[0].Constant.DestOffsetIn32BitValues = 0;
Args[0].Constant.Num32BitValuesToSet = 1;

Args[1].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT;
Args[1].Constant.RootParameterIndex = 6;
Args[1].Constant.DestOffsetIn32BitValues = 0;
Args[1].Constant.Num32BitValuesToSet = 1;

Args[2].Type = D3D12_INDIRECT_ARGUMENT_TYPE_VERTEX_BUFFER_VIEW;
Args[2].VertexBuffer.Slot = 3;

Args[3].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW;

D3D12_COMMAND_SIGNATURE_DESC ProgramDesc;
ProgramDesc.ByteStride = 40;
ProgramDesc.NumArgumentDescs = 4;
ProgramDesc.pArguments = Args;
```

El diseño de una sola estructura dentro del búfer de argumento indirecto es el siguiente:



| Bytes | Descripción                               |
|-------|-------------------------------------------|
| 0:3   | Datos para el índice de parámetros raíz 2           |
| 4:7   | Datos para el índice de parámetros raíz 6           |
| 8:15  | Dirección virtual de VB en la ranura 3 (64 bits)  |
| 16:19 | VB tamaño                                   |
| 20:23 | VB paso                                 |
| 24:27 | VertexCountPerInstance                    |
| 28:31 | InstanceCount                             |
| 32:35 | StartVertexLocation                       |
| 36:39 | StartInstanceLocation                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tutoriales de vídeo de aprendizaje avanzado de DirectX: Ejecución de la selección de GPU indirecta y asincrónica](https://www.youtube.com/watch?v=fKD-VKJeeds)
</dt> <dt>

[Dibujo indirecto y selección de GPU: recorrido del código](indirect-drawing-and-gpu-culling-.md)
</dt> <dt>

[Representación](rendering.md)
</dt> </dl>

 

 
