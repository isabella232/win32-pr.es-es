---
title: Evento de clic
description: Evento de clic
ms.assetid: 772029d5-97b6-49d8-a989-04f0fc429aca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3956d19e833a3e0a5f71192b2846ef9cb270ad10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418973"
---
# <a name="click-event"></a>Evento de clic

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Se produce cuando el usuario hace clic en un carácter o en el icono del carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

**Sub** *Agent * * * \_ click* *  **(ByVal** *CharacterID*, **ByVal** *Button*, **ByVal** *Shift*, **ByVal** *X*, **ByVal** *Y * * *)**



| Parte          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter en el que se hizo clic como una cadena.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Botón*      | Devuelve un entero que identifica el botón que se presionó y liberó para provocar el evento. El argumento del botón es un campo de bits que se corresponde con el botón izquierdo (bit 0), el botón derecho (bit 1) y el botón central (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. Solo se establece uno de los bits, que indica el botón que causó el evento. Si el carácter incluye un icono de la barra de tareas y también se establece el bit 13, se produce el clic en el icono de la barra de tareas.                                                                                                                                                                      |
| *Shift*       | Devuelve un entero que corresponde al estado de las teclas Mayús, CTRL y ALT cuando el botón especificado en el argumento de botón se presiona o se suelta. Un bit se establece si la tecla está presionada. El argumento Shift es un campo de bits con los bits menos significativos correspondientes a la tecla Mayús (bit 0), la tecla CTRL (bit 1) y la tecla ALT (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. El argumento Shift indica el estado de estas claves. Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas. Por ejemplo, si se presionó CTRL y ALT, el valor de Shift sería 6. |
| *X, Y*         | Devuelve un entero que especifica la ubicación actual del puntero del mouse. Los valores X e y se expresan siempre en píxeles, con respecto a la esquina superior izquierda de la pantalla.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

Este evento solo se envía al cliente de entrada-activo de un carácter. Cuando el usuario hace clic en un carácter o en el icono de la barra de tareas sin ningún cliente de entrada-activo, el servidor envía el evento a su cliente activo. Si el carácter es visible ([**visible**](visible-property.md)  =  **true**), la acción del usuario también establece el último cliente de entrada-activo del carácter como el cliente actual de entrada-activo, enviando el evento [**ActivateInput**](activateinput-event.md) a ese cliente y, a continuación, enviando el evento **click** . Si el carácter está oculto (**visible**  =  **false**) y el usuario hace clic en el icono de la barra de tareas del carácter con el botón 1, el carácter también se muestra automáticamente.

> [!Note]  
> Al hacer clic en un carácter, no se deshabilita el resto de caracteres (todos los caracteres). Sin embargo, si se presiona la tecla de escucha, se vacía la salida del carácter de entrada-activo y se desencadena el evento [**RequestComplete**](requestcomplete-event.md) , pasando una [solicitud. estado](status-property.md) que indica que se interrumpió la cola del cliente.

 

 

 




