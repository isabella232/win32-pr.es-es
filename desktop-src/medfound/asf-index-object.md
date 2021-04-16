---
description: Indexador ASF
ms.assetid: 3f95b0ac-d70f-4bc2-8524-c7de1df34afa
title: Indexador ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c729b547339149ee578a90283c570ec8460b0c57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696186"
---
# <a name="asf-indexer"></a>Indexador ASF

El *indexador* ASF es un componente de nivel WMContainer que se usa para leer o escribir objetos de índice en un archivo de formato de sistema avanzado (ASF). Para obtener información acerca de la estructura de un archivo ASF, consulte [ASF File Structure](asf-file-structure.md).

Una aplicación puede utilizar el indexador para realizar búsquedas en función del tiempo de presentación o para generar nuevas entradas de índice para un archivo ASF. El indizador ASF implementa la interfaz [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) .



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
<td>Proporciona una indización basada en el tiempo de presentación para secuencias de audio y vídeo en bloques de índice para que la indización tenga más espacio eficaz. Cada bloque de índice hace referencia a las entradas de índice que contienen un desplazamiento de bytes. <br/> El desplazamiento es la posición del paquete de datos en el que se realiza la búsqueda, en relación con el inicio del objeto de datos ASF.<br/> GUID_NULL debe usarse como el tipo GUID para el identificador de índice. Para obtener más información, consulte <a href="using-the-indexer-to-write-a-new-index.md">uso del indexador para escribir un nuevo índice</a>.<br/></td>
</tr>
<tr class="even">
<td>Índice de código de tiempo</td>
<td>Facilita la búsqueda por código de tiempo en secuencias que contienen metadatos de código de tiempo. Los códigos de tiempo se ajustan a un formato SMPTE (<em>horas: minutos: segundos: fotogramas</em>). Cada bloque de índice hace referencia a las entradas de índice que contienen un desplazamiento de bytes. <br/> El desplazamiento es la posición del paquete de datos en el que se realiza la búsqueda, en relación con el inicio del objeto de datos ASF.<br/>
<blockquote>
[!Note]<br />
Los objetos de índice de código de tiempo no se admiten actualmente.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td>Índice basado en marco</td>
<td>Proporciona índices basados en marcos para las secuencias de vídeo. Los índices en el índice basado en fotogramas están en términos de números de fotogramas, con el primer fotograma de una secuencia en el archivo ASF correspondiente a la entrada 0 en el objeto de índice basado en marco. Cada bloque de índice hace referencia a las entradas de índice que contienen un desplazamiento de bytes.<br/>
<blockquote>
[!Note]<br />
Actualmente no se admiten objetos de índice basados en marcos.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

Esta sección contiene los temas siguientes.



| Tema                                                                                | Descripción                                                                                                                      |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Creación y configuración de indexador](indexer-creation-and-configuration.md)         | Cómo crear un objeto de indexador y configurarlo para leer un índice existente o para escribir un nuevo objeto de índice ASF para un archivo. |
| [Usar el indexador para buscar en un archivo](using-the-indexer-to-seek.md)                 | Cómo usar el indizador para buscar en un archivo ASF.                                                                               |
| [Usar el indexador para escribir un nuevo índice](using-the-indexer-to-write-a-new-index.md) | Cómo usar el indexador para generar entradas de índice y escribir un nuevo objeto index para un archivo ASF.                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Componentes de WMContainer ASF](wmcontainer-asf-components.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




