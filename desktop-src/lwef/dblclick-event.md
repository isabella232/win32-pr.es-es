---
title: Evento DblClick
description: Evento DblClick
ms.assetid: 81ed5396-a2dc-49fe-820f-61ca0935fe85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b900b8a8b79345c50749a4355deeb05fdc1220
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357373"
---
# <a name="dblclick-event"></a>Evento DblClick

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Se produce cuando el usuario hace doble clic en un carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

**Sub** *Agent * * * \_ DblClick* *  **(ByVal** *CharacterID*, **ByVal** *Button*, **ByVal** *Shift*, **ByVal** *X*, **ByVal** *Y * * *)**



| Parte          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter doble clic como una cadena.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| *Botón*      | Devuelve un entero que identifica el botón que se presionó y liberó para provocar el evento. El argumento del botón es un campo de bits que se corresponde con el botón izquierdo (bit 0), el botón derecho (bit 1) y el botón central (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. Solo se establece uno de los bits, que indica el botón que causó el evento. Si el carácter incluye un icono de la barra de tareas, si también se establece el bit 13, se produce el clic en el icono de la barra de tareas.                                                                                                                                                                       |
| *Shift*       | Devuelve un entero que corresponde al estado de las teclas Mayús, CTRL y ALT cuando el botón especificado en el argumento de botón se presiona o se suelta. Un bit se establece si la tecla está presionada. El argumento Shift es un campo de bits con los bits menos significativos correspondientes a la tecla Mayús (bit 0), la tecla CTRL (bit 1) y la tecla ALT (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. El argumento Shift indica el estado de estas claves. Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas. Por ejemplo, si se presionó CTRL y ALT, el valor de Shift sería 6. |
| *X, Y*         | Devuelve un entero que especifica la ubicación actual del puntero del mouse. Los valores X e y se expresan siempre en píxeles, con respecto a la esquina superior izquierda de la pantalla.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

Este evento solo se envía al cliente de entrada-activo de un carácter. Cuando el usuario hace doble clic en un carácter o en su icono de la barra de tareas sin ningún cliente de entrada-activo, el servidor envía el evento a su último cliente de entrada-activo. Si el carácter es visible ([visible](visible-property.md)  =  **true**), también establece el cliente activo como el cliente de entrada-activo actual, enviando el evento [**ActivateInput**](activateinput-event.md) a ese cliente y enviando después el evento **DblClick** . Si el carácter está oculto (visible = **false**) y el usuario hace doble clic en el icono de la barra de tareas del carácter con el botón 1, también muestra automáticamente el carácter.

 

 




