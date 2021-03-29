---
title: Propiedad HelpModeOn
description: Propiedad HelpModeOn
ms.assetid: 4a9b5fd3-12e2-489b-8ce0-9b66b01f517a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43662469c6461e92186a92daddb505b851f8740a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776459"
---
# <a name="helpmodeon-property"></a>Propiedad HelpModeOn

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece si el modo de ayuda contextual está activado para el carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente. ***Caracteres ("*** CharacterID * *"). HelpModeOn* *  \[  =  *booleano*\]



| Parte      | Descripción                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Expresión booleana que especifica si el modo de ayuda contextual está activado. **True** El modo de ayuda está activado. <br/> **False** (valor predeterminado) el modo de ayuda está desactivado.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando se establece esta propiedad en **true**, el puntero del mouse cambia a la imagen de ayuda contextual cuando se mueve sobre el carácter o sobre el menú emergente del carácter. Cuando el usuario hace clic o arrastra el carácter o hace clic en un elemento del menú emergente del carácter, el servidor desencadena el evento [**HelpComplete**](helpcomplete-event.md) y sale del modo de ayuda.

En el modo de ayuda, el servidor no envía los eventos [**click**](click-event.md), [**DragStart**](dragstart-event.md), [**DragComplete**](dragcomplete-event.md)y [**Command**](command-event.md) , a menos que establezca la propiedad [**AutoPopupMenu**](autopopupmenu-property.md) en **true**. En ese caso, el servidor enviará el evento de **clic** (no saldrá del modo de ayuda), sino solo el botón secundario del mouse para que pueda mostrar el menú emergente.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**Evento HelpComplete**](helpcomplete-event.md)


 

 





