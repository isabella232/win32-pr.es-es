---
description: Implementado por el Shell para ayudar a crear scripts y Microsoft Visual Basic los desarrolladores usan algunas de las características disponibles en el shell. El objeto ShellUIHelper no tiene propiedades ni eventos. Se proporcionan métodos para agregar elementos al shell.
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
ms.openlocfilehash: f254bd218024b3d1df15a826da701b1f010ae616
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473331"
---
# <a name="shelluihelper-object"></a>Objeto ShellUIHelper

Implementado por el Shell para ayudar a crear scripts y Microsoft Visual Basic los desarrolladores usan algunas de las características disponibles en el shell. El **objeto ShellUIHelper** no tiene propiedades ni eventos. Se proporcionan métodos para agregar elementos al shell.

## <a name="members"></a>Miembros

El **objeto ShellUIHelper** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El **objeto ShellUIHelper** tiene estos métodos.




| Método | Descripción | 
|--------|-------------|
| <a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a> | Agrega un nuevo canal a la lista de <strong>canales</strong> del menú Internet Explorer Favoritos y a la barra <strong>Canal</strong> del escritorio.<br /><blockquote>[!Note]<br />Este método ya no se admite en Windows Vista. En ese sistema operativo, devuelve E_NOTIMPL.</blockquote><br /> | 
| <a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a> | Agrega un elemento al Active Desktop.<br /> | 
| <a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a> | Muestra la interfaz de usuario predeterminada para crear un elemento favorito. La interfaz de usuario se inicializa con los parámetros especificados.<br /> | 
| <a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a> | Indica si se ha suscrito a una dirección URL especificada.<br /> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows solo aplicaciones de \[ escritorio XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Exdisp.h</dt> </dl>                            |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 




