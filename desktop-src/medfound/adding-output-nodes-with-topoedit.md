---
description: Agregar nodos de salida con TopoEdit
ms.assetid: 23d60fc7-547b-4ef5-b334-5f1b38e58e92
title: Agregar nodos de salida con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84dc30631332e8138b35e4bbc0ccde75ec9b0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705561"
---
# <a name="adding-output-nodes-with-topoedit"></a>Agregar nodos de salida con TopoEdit

En una topología, un nodo de salida representa un receptor de medios que recibe los datos multimedia de un nodo de transformación y los presenta para la reproducción. El tipo de nodo de salida depende del tipo de medio del nodo de origen.

En la tabla siguiente se muestra el comando de menú/barra de herramientas para agregar un nodo de salida a la topología.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de medio de origen</th>
<th>Comando de menú/barra de herramientas</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Secuencia de audio</td>
<td>En el menú <strong>topología</strong> , haga clic en <strong>Agregar SAR</strong>.</td>
<td>Crea un nodo de salida para el representador de audio de streaming (SAR) que reproduce una secuencia de audio a través de un dispositivo de audio, como una tarjeta de sonido.</td>
</tr>
<tr class="even">
<td>Secuencia de vídeo</td>
<td>En el menú de <strong>topología</strong> , haga clic en <strong>Agregar EVR</strong>.</td>
<td>Crea un nodo de salida para el representador de vídeo mejorado (EVR) que muestra los fotogramas de una secuencia de vídeo.</td>
</tr>
<tr class="odd">
<td>Receptor de multimedia personalizado</td>
<td><ol>
<li>En el menú <strong>topología</strong> , haga clic en <strong>Agregar receptor personalizado</strong>.<br/> Se abre el cuadro de diálogo <strong>GUID personalizado de entrada</strong> .<br/></li>
<li><p>En el campo <strong>GUID:</strong> , escriba el GUID del receptor personalizado que desee agregar a la topología.<br/></p>
<blockquote>
[!Note]<br />
TopoEdit espera el GUID con el formato &quot; {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX} &quot; . De lo contrario, no se puede Agregar el nodo y se muestra un &quot; mensaje de error GUID no válido &quot; .
</blockquote>
<p><br/></p></li>
<li>Haga clic en <strong>OK</strong>.<br/></li>
</ol></td>
<td>Crea un nodo de salida para el receptor de flujo para un origen de multimedia personalizado.<br/> El receptor personalizado debe admitir <strong>CoCreateInstance</strong> para que el receptor pueda especificarse con un CLSID.<br/></td>
</tr>
</tbody>
</table>



 

TopoEdit crea el nodo de salida especificado. En el **Panel de topología** se muestra el nodo de salida como un cuadro verde que muestra el nombre del receptor de la secuencia.

Para obtener información sobre cómo agregar nodos de salida mediante programación usando Media Foundation API, vea [crear nodos de salida](creating-output-nodes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilar topologías mediante TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[Representador de audio de streaming](streaming-audio-renderer.md)
</dt> <dt>

[Representador de vídeo mejorado](enhanced-video-renderer.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 




