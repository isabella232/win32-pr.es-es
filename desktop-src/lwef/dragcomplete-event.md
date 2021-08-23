---
title: Evento DragComplete
description: Evento DragComplete
ms.assetid: b48e7097-9d9d-4eab-9dfc-68dbc9793382
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df5ec931a8d5f303dbc1eff5c2f97c018486c4b2fa7326de3e70fbf47a949aef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976675"
---
# <a name="dragcomplete-event"></a>Evento DragComplete

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Se produce cuando el usuario completa el arrastre de un carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**Sub** *agent** \_ DragComplete* *  **(ByVal** *CharacterID*, **ByVal** *Button*, **ByVal** *Shift*, **ByVal** *X*, **ByVal** *Y):)**



| Parte          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter arrastrado como una cadena.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Botón*      | Devuelve un entero que identifica el botón que se presionó y soltó para provocar el evento. El argumento del botón es un campo de bits con bits correspondientes al botón izquierdo (bit 0), el botón derecho (bit 1) y el botón central (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. Solo se establece uno de los bits, lo que indica el botón que provocó el evento.                                                                                                                                                                                                                                                                                |
| *Shift*       | Devuelve un entero que corresponde al estado de las teclas MAYÚS, CTRL y ALT cuando se presiona o se libera el botón especificado en el argumento de botón. Se establece un bit si la clave está abajo. El argumento mayús es un campo de bits con los bits menos significativos correspondientes a la tecla MAYÚS (bit 0), la tecla CTRL (bit 1) y la tecla ALT (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. El argumento mayús indica el estado de estas claves. Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas. Por ejemplo, si se presionan CTRL y ALT, el valor de mayús sería 6. |
| *X,Y*         | Devuelve un entero que especifica la ubicación actual del puntero del mouse. Los valores X e Y siempre se expresan en píxeles, en relación con la esquina superior izquierda de la pantalla.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Comentarios

Este evento solo se envía al cliente activo de entrada de un carácter. Cuando el usuario arrastra un carácter sin cliente activo de entrada, el servidor establece su último cliente activo de entrada como el cliente activo de entrada actual, envía el evento [**ActivateInput**](activateinput-event.md) a ese cliente y, a continuación, envía los eventos [**DragStart**](dragstart-event.md) y **DragComplete.**

### <a name="see-also"></a>Consulte también

[**Evento DragStart**](dragstart-event.md)


 

 




