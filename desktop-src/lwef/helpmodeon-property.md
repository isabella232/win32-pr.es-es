---
title: Propiedad HelpModeOn
description: Propiedad HelpModeOn
ms.assetid: 4a9b5fd3-12e2-489b-8ce0-9b66b01f517a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 489de1893e96bf2d4cc38ef9e788a726db8b9fd4dfbdc9ae3cd1b60f9bc02f91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962745"
---
# <a name="helpmodeon-property"></a>Propiedad HelpModeOn

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece si el modo de Ayuda contextual está en para el carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent.***Caracteres("**_CharacterID_*_"). HelpModeOn_ *  \[  =  *booleano*\]



| Parte      | Descripción                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Expresión booleana que especifica si el modo de Ayuda contextual está en. **True** El modo de ayuda está en on. <br/> **False** (valor predeterminado) El modo de Ayuda está desactivado.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Al establecer esta propiedad en **True,** el puntero del mouse cambia a la imagen de Ayuda contextual cuando se mueve sobre el carácter o sobre el menú emergente del carácter. Cuando el usuario hace clic o arrastra el carácter o hace clic en un elemento del menú emergente del carácter, el servidor desencadena el evento [**HelpComplete**](helpcomplete-event.md) y sale del modo de Ayuda.

En el modo de Ayuda, el servidor no envía los eventos [**Click**](click-event.md), [**DragStart,**](dragstart-event.md) [**DragComplete**](dragcomplete-event.md)y [**Command,**](command-event.md) a menos que establezca la propiedad [**AutoPopupMenu**](autopopupmenu-property.md) en **True.** En ese caso, el servidor enviará el evento **Click** (no sale del modo de Ayuda), pero solo para que el botón derecho del mouse le permita mostrar el menú emergente.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**Evento HelpComplete**](helpcomplete-event.md)


 

 





