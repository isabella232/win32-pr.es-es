---
description: Indexador de ASF
ms.assetid: 3f95b0ac-d70f-4bc2-8524-c7de1df34afa
title: Indexador de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adde38583d70bdbc23382e6d57316cc92b5fbd3963560a10960acbe29ea97624
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117881146"
---
# <a name="asf-indexer"></a>Indexador de ASF

El *indexador* ASF es un componente de capa WMContainer que se usa para leer o escribir objetos de índice en un archivo de formato de sistemas avanzados (ASF). Para obtener información sobre la estructura de un archivo ASF, vea [ASF File Structure](asf-file-structure.md).

Una aplicación puede usar el indexador para realizar búsquedas en función del tiempo de presentación o para generar nuevas entradas de índice para un archivo ASF. El indexador de ASF implementa la [**interfaz DEFFIndexer.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de índice</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Índice basado en tiempo de presentación</td>
<td>Proporciona indexación basada en tiempo de presentación para secuencias de audio y vídeo en bloques de índice para que la indexación sea más eficiente. Cada bloque de índice hace referencia a entradas de índice que contienen un desplazamiento de bytes. <br/> El desplazamiento es la posición del paquete de datos que se está buscando, en relación con el inicio del objeto de datos de ASF.<br/> GUID_NULL debe usarse como tipo GUID para el identificador de índice. Para obtener más información; vea Using the Indexer to Write a New Index ( Usar el <a href="using-the-indexer-to-write-a-new-index.md">indexador para escribir un nuevo índice).</a><br/></td>
</tr>
<tr class="even">
<td>Índice de código de tiempo</td>
<td>Facilita la búsqueda por código de tiempo en secuencias que contienen metadatos de código de tiempo. Los códigos de tiempo se ajustan a un formato SMPTE (<em>Hours:Minutes:Seconds:Frames</em>). Cada bloque de índice hace referencia a entradas de índice que contienen un desplazamiento de bytes. <br/> El desplazamiento es la posición del paquete de datos que se está buscando, en relación con el inicio del objeto de datos de ASF.<br/>
<blockquote>
[!Note]<br />
Los objetos de índice de código de tiempo no se admiten actualmente.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td>Índice basado en fotogramas</td>
<td>Proporciona indexación basada en fotogramas para secuencias de vídeo. Los índices del índice basado en fotogramas se refieren a números de fotograma, con el primer fotograma de una secuencia en el archivo ASF correspondiente a la entrada 0 en el objeto de índice basado en fotogramas. Cada bloque de índice hace referencia a entradas de índice que contienen un desplazamiento de bytes.<br/>
<blockquote>
[!Note]<br />
Actualmente no se admiten objetos de índice basados en fotogramas.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

Esta sección contiene los temas siguientes.



| Tema                                                                                | Descripción                                                                                                                      |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Creación y configuración del indexador](indexer-creation-and-configuration.md)         | Cómo crear un objeto de indexador y configurarlo para leer un índice existente o para escribir un nuevo objeto de índice de ASF para un archivo. |
| [Usar el indexador para buscar en un archivo](using-the-indexer-to-seek.md)                 | Cómo usar el indexador para buscar dentro de un archivo ASF.                                                                               |
| [Usar el indexador para escribir un nuevo índice](using-the-indexer-to-write-a-new-index.md) | Cómo usar el indexador para generar entradas de índice y escribir un nuevo objeto index para un archivo ASF.                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Componentes de ASF de WMContainer](wmcontainer-asf-components.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




