---
title: Llamar a WDS desde la línea de comandos
description: Puede iniciar la interfaz de usuario de búsqueda de escritorio de Microsoft Windows (WDS) con un filtro, un almacén y una consulta específicos desde otra aplicación o una página web que use el objeto auxiliar de explorador (BHO) mediante el uso de la sintaxis de la línea de comandos de windowssearch.exe.
ms.assetid: fd62f7c9-08a9-4e05-b0bc-e2215cfff59e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efae7aebc13f578e9c5c32542b451d3600a93a2b
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2020
ms.locfileid: "103789160"
---
# <a name="calling-wds-from-the-command-line"></a>Llamar a WDS desde la línea de comandos

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.

Puede iniciar la interfaz de usuario de búsqueda de escritorio de Microsoft Windows (WDS) con un filtro, un almacén y una consulta específicos desde otra aplicación o una página web que use el objeto auxiliar de explorador (BHO) mediante el uso de la sintaxis de la línea de comandos de windowssearch.exe. Cuando se llama a WDS desde la línea de comandos, no se devuelve información sobre las acciones o la selección del usuario en la ventana de WDS a la aplicación o página web que realiza la llamada.

La ruta de instalación de WDS se especifica en la configuración del registro InstallDir en HKEY_LOCAL_MACHINE \\ software \\ Microsoft \\ Windows Desktop Search. La ruta de acceso predeterminada en la que se instala windowssearch.exe es archivos de programa de \\ Windows Desktop Search.

## <a name="command-line-syntax"></a>Sintaxis de la línea de comandos

La siguiente sintaxis se aplica a la interfaz de la línea de comandos de Windows Desktop Search 2. x.



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

<td>Inicializa la búsqueda en el escritorio de Windows</td>
</tr>
<tr class="even">
<td>/indexnow</td>

<td>Desactiva el retroceso de la indización y vuelve a examinar todas las ubicaciones de los índices</td>
</tr>
<tr class="odd">
<td>/showstatus</td>

<td>Muestra la ventana de estado de indización</td>
</tr>
<tr class="even">
<td>/launchsearchwindow o/URL</td>

<td>Abre una ventana de WDS con una consulta vacía</td>
</tr>
<tr class="odd">
<td>/URL</td>
<td>buscar: [tienda | Mostrar | consulta] cadena de consulta</td>
<td>Abre una ventana de WDS con una consulta y un filtro en función de los parámetros siguientes:
<ul>
<li><p>almacén: especifica el origen de datos que se va a consultar: archivos, Outlook, outlookexpress. Si no se especifica, se buscará en todos los almacenes. <br/></p>
<blockquote>
[!Note]<br />
Aunque la sintaxis de consulta avanzada admite hacer referencia a Microsoft Outlook como ' OE ', el parámetro Store de la línea de comandos debe ser ' outlookexpress '.
</blockquote>
<p><br/></p></li>
<li><p>Show: especifica el tipo de resultados percibido que se va a devolver. Vea <a href="-search-2x-wds-perceivedtype.md">tipos percibidos</a> para obtener una lista completa de tipos. Si no se especifica, se devolverán todos los tipos. <br/></p>
<blockquote>
[!Note]<br />
Hay tres diferencias entre los valores de tipo percibidos y los valores de show. Para <code>show</code> , use ' Documents ' en lugar de ' doc ', ' Pictures ' en lugar de ' pics ' y ' textdocuments ' en lugar de ' text '.
</blockquote>
<p><br/></p></li>
<li>consulta: especifica los criterios de búsqueda. Este valor admite parámetros de <a href="-search-2x-wds-aqsreference.md">Sintaxis de consulta avanzada</a> para refinar los resultados. El parámetro de consulta debe ser el último parámetro de la dirección URL.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="example"></a>Ejemplo

Por ejemplo, para buscar imágenes que coincidan con los criterios ' papel tapiz ', use el siguiente comando:

`WindowsSearch.exe /url search:store=files&show=pictures&query=wallpaper`

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Sintaxis de consulta avanzada](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Tipos percibidos](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Llamar a WDS desde páginas web](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





