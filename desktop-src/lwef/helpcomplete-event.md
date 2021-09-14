---
title: Evento HelpComplete
description: Evento HelpComplete
ms.assetid: d805f089-154f-4b39-9d78-a02b732f87ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3984f4b67eaed6bc9226685e927c35e151c11e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241257"
---
# <a name="helpcomplete-event"></a>Evento HelpComplete

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Indica que se ha salido del modo de Ayuda contextual.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**Sub** *agent.)(ByVal* *  *CharacterID,ByVal* *  *Name!", ByVal* *  *Cause).)**



| Parte          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter en el que se ha hecho clic como una cadena.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *Nombre*        | Devuelve un valor de cadena que identifica el nombre (id.) del comando.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| *Causa*       | Devuelve un valor que indica lo que hizo que se completara el modo de Ayuda. 1 El usuario seleccionó un comando proporcionado por la aplicación.<br/> 2 El usuario seleccionó el [**objeto Commands**](/windows/desktop/lwef/the-commands-collection-object) de otro cliente.<br/> 3 El usuario seleccionó el comando Abrir comandos de voz.<br/> 4 El usuario seleccionó el comando Cerrar comandos de voz.<br/> 5 El usuario seleccionó el comando *Mostrar nombrede* caracteres.<br/> 6 El usuario seleccionó el comando *Ocultar characterName.*<br/> 7 El usuario seleccionó (hizo clic) en el carácter.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

Normalmente, el modo de Ayuda se completa cuando el usuario hace clic o arrastra el carácter o selecciona un comando en el menú emergente del carácter. Al hacer clic en otro carácter o en otro lugar de la pantalla, no se cancela el modo de Ayuda. El cliente que establece el modo de Ayuda para el carácter puede cancelar el modo de Ayuda estableciendo [**HelpModeOn**](helpmodeon-property.md) en **False.** (Esto no desencadena el **evento HelpComplete).**

Cuando el usuario selecciona un comando en el menú emergente del carácter en modo ayuda, el servidor quita el menú, llama a la Ayuda con el [**HelpContextID**](helpcontextid-property.md)especificado del comando y envía este evento. Contextual (también conocido como What's This?) La ventana de Ayuda se muestra en la ubicación del puntero. Si el usuario selecciona el comando por entrada de voz, la ventana Ayuda se muestra sobre el carácter. Si el carácter está fuera de la pantalla, la ventana se muestra en la pantalla más cercana a la posición actual del carácter.

Si el servidor devuelve Name como una cadena vacía (""), indica que el usuario seleccionó un comando proporcionado por el servidor.

Este evento solo se envía a la aplicación cliente que coloca el carácter en modo de Ayuda.

### <a name="see-also"></a>Consulte también

[**Propiedad HelpModeOn**](helpmodeon-property.md), [ **propiedad HelpContextID**](helpcontextid-property.md)


 

