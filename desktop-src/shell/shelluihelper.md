---
description: Implementado por el shell para ayudar a los programadores de script y Microsoft Visual Basic a usar algunas de las características disponibles en el shell. El objeto ShellUIHelper no tiene propiedades ni eventos. Se proporcionan métodos para agregar elementos al shell.
title: Objeto ShellUIHelper (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9fffebc8-29b9-4064-b60c-c8c63690a79e
ms.openlocfilehash: f0df3b02624a802c19663b67cbcab508c3e0e487
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986019"
---
# <a name="shelluihelper-object"></a>Objeto ShellUIHelper

Implementado por el shell para ayudar a los programadores de script y Microsoft Visual Basic a usar algunas de las características disponibles en el shell. El objeto **ShellUIHelper** no tiene propiedades ni eventos. Se proporcionan métodos para agregar elementos al shell.

## <a name="members"></a>Miembros

El objeto **ShellUIHelper** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El objeto **ShellUIHelper** tiene estos métodos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Método</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></td>
<td style="text-align: left;">Agrega un nuevo canal a la lista de canales en el menú <strong>Favoritos</strong> de Internet Explorer y en la barra de <strong>canales</strong> del escritorio.<br/>
<blockquote>
[!Note]<br />
Este método ya no se admite en Windows Vista. En ese sistema operativo, devuelve E_NOTIMPL.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></td>
<td style="text-align: left;">Agrega un elemento al escritorio activo.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></td>
<td style="text-align: left;">Muestra la interfaz de usuario predeterminada para crear un elemento favorito. La interfaz de usuario se inicializa con los parámetros especificados.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></td>
<td style="text-align: left;">Indica si se ha suscrito a una dirección URL especificada.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Exdisp. h</dt> </dl>                            |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,71 o posterior)</dt> </dl> |



 

 




