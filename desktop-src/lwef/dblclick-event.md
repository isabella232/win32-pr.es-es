---
title: Evento DblClick
description: Evento DblClick
ms.assetid: 81ed5396-a2dc-49fe-820f-61ca0935fe85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f48e5b4574f8378930001e1cea3916d12904fcc317b3b00ff14c436fb4912574
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117693779"
---
# <a name="dblclick-event"></a>Evento DblClick

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Se produce cuando el usuario hace doble clic en un carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**Sub** *agent(" \_ DblClick* *  **(ByVal** *CharacterID*, **ByVal** *Button*, **ByVal** *Shift*, **ByVal** *X*, **ByVal** *Y"))**



| Parte          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter con doble clic como una cadena.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| *Botón*      | Devuelve un entero que identifica el botón que se presionó y soltó para provocar el evento. El argumento del botón es un campo de bits con bits correspondientes al botón izquierdo (bit 0), el botón derecho (bit 1) y el botón central (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. Solo se establece uno de los bits, lo que indica el botón que provocó el evento. Si el carácter incluye un icono de barra de tareas, si también se establece el bit 13, se ha hecho clic en el icono de la barra de tareas.                                                                                                                                                                       |
| *Shift*       | Devuelve un entero que corresponde al estado de las teclas MAYÚS, CTRL y ALT cuando se presiona o se libera el botón especificado en el argumento de botón. Se establece un bit si la clave está abajo. El argumento mayús es un campo de bits con los bits menos significativos correspondientes a la tecla MAYÚS (bit 0), la tecla CTRL (bit 1) y la tecla ALT (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. El argumento mayús indica el estado de estas claves. Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas. Por ejemplo, si se presionan CTRL y ALT, el valor de mayús sería 6. |
| *X,Y*         | Devuelve un entero que especifica la ubicación actual del puntero del mouse. Los valores X e Y siempre se expresan en píxeles, en relación con la esquina superior izquierda de la pantalla.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Comentarios

Este evento solo se envía al cliente activo de entrada de un carácter. Cuando el usuario hace doble clic en un carácter o en su icono de barra de tareas sin cliente activo de entrada, el servidor envía el evento a su último cliente activo de entrada. Si el carácter está visible [(Visible](visible-property.md)True), también establece el cliente activo como el cliente activo de entrada actual, enviando el evento ActivateInput a ese cliente y, a continuación, enviando el  =   **evento DblClick.** [](activateinput-event.md) Si el carácter está oculto (Visible = **False)** y el usuario hace doble clic en el icono de la barra de tareas del carácter mediante el botón 1, también muestra automáticamente el carácter.

 

 




