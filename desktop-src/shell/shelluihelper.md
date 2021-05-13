---
description: Implementado por shell para ayudar a crear scripts y microsoft Visual Basic los desarrolladores usan algunas de las características disponibles en el shell. El objeto ShellUIHelper no tiene propiedades ni eventos. Se proporcionan métodos para agregar elementos al shell.
title: Objeto ShellUIHelper (Exdisp.h)
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
ms.openlocfilehash: b77d618c4c772859a9009f3cca761c59df83257a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842436"
---
# <a name="shelluihelper-object"></a>Objeto ShellUIHelper

Implementado por shell para ayudar a crear scripts y microsoft Visual Basic los desarrolladores usan algunas de las características disponibles en el shell. El **objeto ShellUIHelper** no tiene propiedades ni eventos. Se proporcionan métodos para agregar elementos al shell.

## <a name="members"></a>Members

El **objeto ShellUIHelper** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El **objeto ShellUIHelper** tiene estos métodos.



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
<td style="text-align: left;">Agrega un nuevo canal a la lista de <strong>canales</strong> del menú Internet Explorer Favoritos y a la barra <strong>Canal</strong> del escritorio.<br/>
<blockquote>
[!Note]<br />
Este método ya no se admite en Windows Vista. En ese sistema operativo, devuelve E_NOTIMPL.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></td>
<td style="text-align: left;">Agrega un elemento al Active Desktop.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></td>
<td style="text-align: left;">Muestra la interfaz de usuario predeterminada para crear un elemento favorito. La interfaz de usuario se inicializa en los parámetros especificados.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></td>
<td style="text-align: left;">Indica si se ha suscrito una dirección URL especificada.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Exdisp.h</dt> </dl>                            |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 




