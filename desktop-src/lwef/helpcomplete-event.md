---
title: Evento HelpComplete
description: Evento HelpComplete
ms.assetid: d805f089-154f-4b39-9d78-a02b732f87ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3984f4b67eaed6bc9226685e927c35e151c11e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105695593"
---
# <a name="helpcomplete-event"></a>Evento HelpComplete

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Indica que se ha salido del modo de ayuda contextual.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

**Sub** *Agent. * * * (ByVal* *  *CharacterID * *, ByVal* *  *nombre * * *, ByVal* *  *causa * * *)**



| Parte          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter en el que se hizo clic como una cadena.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *Nombre*        | Devuelve un valor de cadena que identifica el nombre (ID.) del comando.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| *Causa*       | Devuelve un valor que indica lo que hizo que se completara el modo de ayuda. 1 el usuario seleccionó un comando proporcionado por la aplicación.<br/> 2 el usuario seleccionó el objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) de otro cliente.<br/> 3 el usuario seleccionó el comando abrir comandos de voz.<br/> 4 el usuario seleccionó el comando cerrar comandos de voz.<br/> 5 el usuario seleccionó el comando show *nombredecarácter* .<br/> 6 el usuario seleccionó el comando ocultar *nombredecarácter* .<br/> 7 el usuario seleccionó (hizo clic en) el carácter.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

Normalmente, el modo de ayuda se completa cuando el usuario hace clic o arrastra el carácter o selecciona un comando en el menú emergente del carácter. Al hacer clic en otro carácter o en cualquier otro lugar de la pantalla, no se cancela el modo de ayuda. El cliente que establece el modo de ayuda para el carácter puede cancelar el modo de ayuda estableciendo [**HelpModeOn**](helpmodeon-property.md) en **false**. (Esto no desencadena el evento **HelpComplete** ).

Cuando el usuario selecciona un comando en el menú emergente del carácter en el modo de ayuda, el servidor quita el menú, llama a ayuda con el [**HelpContextID**](helpcontextid-property.md)especificado del comando y envía este evento. La información contextual (también conocida como esto?) La ventana de ayuda se muestra en la ubicación del puntero. Si el usuario selecciona el comando por entrada de voz, se muestra la ventana de ayuda sobre el carácter. Si el carácter está fuera de la pantalla, la ventana se muestra en la pantalla más cercana a la posición actual del carácter.

Si el servidor devuelve el nombre como una cadena vacía (""), indica que el usuario seleccionó un comando proporcionado por el servidor.

Este evento solo se envía a la aplicación cliente que coloca el carácter en modo de ayuda.

### <a name="see-also"></a>Consulte también

[**Propiedad HelpModeOn**](helpmodeon-property.md), [ **propiedad HelpContextID**](helpcontextid-property.md)


 

