---
title: Dibujo indirecto
description: El dibujo indirecto permite que algunos recorridos de escena y selección de ubicación se muevan de la CPU a la GPU, lo que puede mejorar el rendimiento. La CPU o la GPU pueden generar el búfer de comandos.
ms.assetid: F8D6C88A-101E-4F66-999F-43206F6527B6
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7731a662bc6064e635d68942e6b0b222adf1eda8
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/19/2020
ms.locfileid: "104549081"
---
# <a name="indirect-drawing"></a>Dibujo indirecto

El dibujo indirecto permite que algunos recorridos de escena y selección de ubicación se muevan de la CPU a la GPU, lo que puede mejorar el rendimiento. La CPU o la GPU pueden generar el búfer de comandos.

-   [Firmas de comandos](#command-signatures)
-   [Estructuras de búfer de argumentos indirectos](#indirect-argument-buffer-structures)
-   [Creación de la firma de comandos](#command-signature-creation)
    -   [Ningún cambio de argumento](#no-argument-changes)
    -   [Constantes raíz y búferes de vértices](#root-constants-and-vertex-buffers)
-   [Temas relacionados](#related-topics)

## <a name="command-signatures"></a>Firmas de comandos

El objeto de firma de comando ([**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature)) permite que las aplicaciones especifiquen dibujos indirectos, en particular estableciendo lo siguiente:

-   El formato de búfer de argumento indirecto.
-   El tipo de comando que se usará (de los [](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) métodos ID3D12GraphicsCommandList [**DrawInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced), [**DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)o [**Dispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)).
-   Conjunto de enlaces de recursos que cambiarán la llamada por comando frente al conjunto que se va a heredar.

Al iniciarse, una aplicación crea un pequeño conjunto de **firmas de comandos**. En tiempo de ejecución, la aplicación rellena un búfer con comandos (a través de cualquier medio que elija el desarrollador de la aplicación). Comandos que contienen opcionalmente el estado que se establece para las vistas de búfer de vértices, las vistas de búfer de índice, las constantes raíz y los descriptores de raíz (RAW o Structured SRV/UAV/CBVs). Estos diseños de argumentos no son específicos de hardware, por lo que las aplicaciones pueden generar los búferes directamente. La firma del comando hereda el estado restante de la lista de comandos. A continuación, la aplicación llama a [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) para indicar a la GPU que interprete el contenido del búfer de argumentos indirectos según el formato definido por una firma de comando determinada.

Si la firma del comando cambia algún argumento raíz, se almacena en la firma del comando como un subconjunto de una firma raíz.

Tenga en cuenta que el estado de la firma de comandos no se filtra de nuevo a la lista de comandos cuando se completa la ejecución.

Por ejemplo, supongamos que un desarrollador de aplicaciones desea especificar una constante raíz única para cada llamada a Draw en el búfer de argumentos indirecto. La aplicación crearía una firma de comando que permite al búfer de argumentos indirecto especificar los siguientes parámetros por llamada a Draw:

-   Valor de una constante raíz.
-   Los argumentos de dibujo (número de vértices, recuento de instancias, etc.).

El búfer de argumentos indirectos generado por la aplicación contiene una matriz de registros de tamaño fijo. Cada estructura corresponde a una llamada a Draw. Cada estructura contiene los argumentos de dibujo y el valor de la constante raíz. El número de llamadas a Draw se especifica en un búfer independiente visible para GPU.

A continuación se muestra un búfer de comandos de ejemplo generado por la aplicación:

![formato de búfer de comandos](images/indirect-drawing-command-buffer.png)

## <a name="indirect-argument-buffer-structures"></a>Estructuras de búfer de argumentos indirectos

Las siguientes estructuras definen el modo en que los argumentos concretos aparecen en un búfer de argumentos indirecto. Estas estructuras no aparecen en ninguna API de D3D12. Las aplicaciones usan estas definiciones al escribir en un búfer de argumentos indirectos (con la CPU o la GPU):

-   [**Argumentos de D3D12 \_ Draw \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_arguments)
-   [**D3D12 \_ dibujar \_ argumentos indexados \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_indexed_arguments)
-   [**\_Argumentos de envío de D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dispatch_arguments)
-   [**D3D12 \_ \_ vista de búfer de vértices \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)
-   [**\_Vista de \_ búfer de índice de D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_index_buffer_view)
-   \_ \_ Dirección virtual de GPU D3D12 \_ (sinónimo de definición de tipo de tipo UINT64).
-   [**\_Vista de \_ búfer de constantes de D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc)

## <a name="command-signature-creation"></a>Creación de la firma de comandos

Para crear una firma de comando, use los siguientes elementos de API:

-   [**ID3D12Device:: CreateCommandSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandsignature) (genera una [**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature))
-   [**D3D12 \_ \_ tipo de argumento indirecto \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_indirect_argument_type)
-   [**D3D12 \_ argumento indirecto \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc)
-   [**Descripción de la \_ firma del comando D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc)

El orden de los argumentos dentro de un búfer de argumentos indirectos se define de forma que coincida exactamente con el orden de los argumentos especificados en el parámetro *pArguments* de la [**firma del \_ comando \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc). Todos los argumentos de una llamada a Draw (Graphics)/dispatch (Compute) dentro de un búfer de argumentos indirecto están estrechamente empaquetados. Sin embargo, las aplicaciones pueden especificar un intervalo de bytes arbitrario entre los comandos Draw/Dispatch en un búfer de argumentos indirecto.

La firma raíz debe especificarse solo si la firma del comando cambia uno de los argumentos raíz.

En el caso de la raíz SRV/UAV/CBV, el tamaño especificado de la aplicación se encuentra en bytes. El nivel de depuración validará las siguientes restricciones en la dirección:

-   CBV: la dirección debe ser un múltiplo de 256 bytes.
-   SRV/UAV sin formato: la dirección debe ser un múltiplo de 4 bytes.
-   SRV/UAV estructurado: la dirección debe ser un múltiplo del intervalo de bytes de la estructura (declarado en el sombreador).

Una firma de comando determinada es una firma de comando Draw o Compute. Si una firma de comando contiene una operación de dibujo, se trata de una firma de comando de gráficos. De lo contrario, la firma del comando debe contener una operación de envío y se trata de una firma de comando de proceso.

En las secciones siguientes se muestran algunas firmas de comandos de ejemplo.

### <a name="no-argument-changes"></a>Ningún cambio de argumento

En este ejemplo, el búfer de argumentos indirectos generado por la aplicación contiene una matriz de estructuras de 36 bytes. Cada estructura solo contiene los cinco parámetros pasados a [**DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) (más el relleno).

A continuación se muestra el código para crear la descripción de la firma del comando:

``` syntax
D3D12_INDIRECT_ARGUMENT_DESC Args[1];
Args[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW_INDEXED;

D3D12_COMMAND_SIGNATURE_DESC ProgramDesc;
ProgramDesc.ByteStride = 36;
ProgramDesc.NumArgumentDescs = 1;
ProgramDesc.pArguments = Args;
```

El diseño de una única estructura dentro de un búfer de argumentos indirecto es:



| Bytes | Descripción           |
|-------|-----------------------|
| 0:3   | IndexCountPerInstance |
| 4:7   | InstanceCount         |
| 8:11  | StartIndexLocation    |
| 12:15 | BaseVertexLocation    |
| 16:19 | StartInstanceLocation |
| 20:35 | Relleno               |



 

### <a name="root-constants-and-vertex-buffers"></a>Constantes raíz y búferes de vértices

En este ejemplo, cada estructura de un búfer de argumentos indirectos cambia dos constantes raíz, cambia un enlace de búfer de vértice y realiza una operación de dibujo no indizada. No hay ningún relleno entre las estructuras.

El código para crear la descripción de la firma del comando es:

``` syntax
D3D12_INDIRECT_ARGUMENT_DESC Args[4];
Args[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT;
Args[0].Constant.RootParameterIndex = 2;

Args[1].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT;
Args[1].Constant.RootParameterIndex = 6;

Args[2].Type = D3D12_INDIRECT_ARGUMENT_TYPE_VERTEX_BUFFER_VIEW;
Args[2].VertexBuffer.VBSlot = 3;

Args[3].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW_INSTANCED;

D3D12_COMMAND_SIGNATURE_DESC ProgramDesc;
ProgramDesc.ByteStride = 40;
ProgramDesc.NumArgumentDescs = 4;
ProgramDesc.pArguments = Args;
```

El diseño de una única estructura dentro del búfer de argumentos indirecto es el siguiente:



| Bytes | Descripción                     |
|-------|---------------------------------|
| 0:3   | Datos del índice 2 del parámetro raíz |
| 4:7   | Datos del índice de parámetro raíz 6 |
| 8:15  | Dirección virtual de VB (64 bits)  |
| 16:19 | Tamaño de VB                         |
| 20:23 | Intervalo de VB                       |
| 24:27 | VertexCountPerInstance          |
| 28:31 | InstanceCount                   |
| 32:35 | StartVertexLocation             |
| 36:39 | StartInstanceLocation           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tutoriales de vídeo de aprendizaje avanzado de DirectX: ejecutar la selección de GPU indirecta y asincrónica](https://www.youtube.com/watch?v=fKD-VKJeeds)
</dt> <dt>

[Dibujo indirecto y selección de GPU: tutorial de código](indirect-drawing-and-gpu-culling-.md)
</dt> <dt>

[Representación](rendering.md)
</dt> </dl>

 

 