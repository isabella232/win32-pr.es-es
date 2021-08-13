---
title: Llamada a WDS desde la línea de comandos
description: Puede iniciar la interfaz de usuario de Microsoft Windows Desktop Search (WDS) con un filtro específico, almacenar y consultar desde otra aplicación o página web que use el objeto del asistente de explorador (BHO) mediante la sintaxis de línea de comandos windowssearch.exe.
ms.assetid: fd62f7c9-08a9-4e05-b0bc-e2215cfff59e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ba9fa8310af43340ef71c5d7e574f1b95addca86a4f90051dc85f593f43302
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753221"
---
# <a name="calling-wds-from-the-command-line"></a>Llamada a WDS desde la línea de comandos

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use [Windows Search en](../search/-search-3x-wds-overview.md) su lugar.

Puede iniciar la interfaz de usuario de Microsoft Windows Desktop Search (WDS) con un filtro específico, almacenar y consultar desde otra aplicación o página web que use el objeto del asistente de explorador (BHO) mediante la sintaxis de línea de comandos windowssearch.exe. Al llamar a WDS desde la línea de comandos, no se devuelve información sobre las acciones o la selección del usuario en la ventana WDS a la aplicación o página web que realiza la llamada.

La ruta de instalación de WDS se especifica en la configuración del Registro InstallDir en HKEY_LOCAL_MACHINE \\ Software Microsoft Windows Desktop \\ \\ Search. La ruta de acceso predeterminada windowssearch.exe está instalada en es Archivos de \\ programa Windows Desktop Search.

## <a name="command-line-syntax"></a>Sintaxis de la línea de comandos

La sintaxis siguiente se aplica a Windows interfaz de la línea de comandos de Desktop Search 2.x.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Opciones</th>
<th>Parámetro</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>/startup</td>

<td>Inicializa Windows Desktop Search</td>
</tr>
<tr class="even">
<td>/indexnow</td>

<td>Desactiva la desactivación de la indexación y vuelve a examinar todas las ubicaciones de índice.</td>
</tr>
<tr class="odd">
<td>/showstatus</td>

<td>Muestra la ventana de estado de indexación</td>
</tr>
<tr class="even">
<td>/launchsearchwindow o /url</td>

<td>Abre una ventana wds con una consulta vacía</td>
</tr>
<tr class="odd">
<td>/url</td>
<td>cadena de consulta search:[store|show|query]</td>
<td>Abre una ventana de WDS con una consulta y un filtro basados en los parámetros siguientes:
<ul>
<li><p>store: especifica el origen de datos que se va a consultar: files, outlook, outlookexpress. Si no se especifica, se buscarán todos los almacenes. <br/></p>
<blockquote>
[!Note]<br />
Aunque la sintaxis de consulta avanzada admite la referencia a Microsoft Outlook como "oe", el parámetro store de la línea de comandos debe ser "outlookexpress".
</blockquote>
<p><br/></p></li>
<li><p>show: especifica qué tipo de resultados se va a devolver. Vea <a href="-search-2x-wds-perceivedtype.md">Perceived Types (Tipos percibidos)</a> para obtener una lista completa de tipos. Si no se especifica, se devolverán todos los tipos. <br/></p>
<blockquote>
[!Note]<br />
Hay tres diferencias entre los valores de tipo percibidos y los valores de show. Para , use "documents" en lugar de <code>show</code> "doc", "pictures" en lugar de "pics" y "textdocuments" en lugar de "text".
</blockquote>
<p><br/></p></li>
<li>query: especifica los criterios de búsqueda. Este valor admite parámetros <a href="-search-2x-wds-aqsreference.md">de sintaxis de consulta</a> avanzada para refinar los resultados. El parámetro de consulta debe ser el último parámetro de la dirección URL.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="example"></a>Ejemplo

Por ejemplo, para buscar en todos los archivos imágenes que coincidan con los criterios "papel tapiz", use el siguiente comando:

`WindowsSearch.exe /url search:store=files&show=pictures&query=wallpaper`

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Sintaxis de consulta avanzada](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Tipos percibidos](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Llamada a WDS desde Páginas web](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





