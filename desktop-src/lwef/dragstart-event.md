---
title: Evento DragStart
description: Evento DragStart
ms.assetid: fef0ae05-1958-45c6-8260-107c47b5fa92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e382e77c87848226568755c06d2541ebb4db14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075699"
---
# <a name="dragstart-event"></a>Evento DragStart

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Se produce cuando el usuario comienza a arrastrar un carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

**Sub** *Agent * * * \_ DragStart* *  **(ByVal** *CharacterID*, **(** *botón* ByVal, **(ByVal** *Shift*, **(ByVal** *X*, **(ByVal** *Y ** * *)*



| Parte          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter en el que se hizo clic como una cadena.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Botón*      | Devuelve un entero que identifica el botón que se presionó y liberó para provocar el evento. El argumento del botón es un campo de bits que se corresponde con el botón izquierdo (bit 0), el botón derecho (bit 1) y el botón central (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. Solo se establece uno de los bits, que indica el botón que causó el evento.                                                                                                                                                                                                                                                                                |
| *Shift*       | Devuelve un entero que corresponde al estado de las teclas Mayús, CTRL y ALT cuando el botón especificado en el argumento de botón se presiona o se suelta. Un bit se establece si la tecla está presionada. El argumento Shift es un campo de bits con los bits menos significativos correspondientes a la tecla Mayús (bit 0), la tecla CTRL (bit 1) y la tecla ALT (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. El argumento Shift indica el estado de estas claves. Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas. Por ejemplo, si se presionó CTRL y ALT, el valor de Shift sería 6. |
| *X, Y*         | Devuelve un entero que especifica la ubicación actual del puntero del mouse. Los valores X e y se expresan siempre en píxeles, con respecto a la esquina superior izquierda de la pantalla.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

Este evento solo se envía al cliente de entrada-activo de un carácter. Cuando el usuario arrastra un carácter sin ningún cliente de entrada-activo, el servidor establece su último cliente de entrada-activo como el cliente de entrada-activo actual, enviando el evento [**ActivateInput**](activateinput-event.md) a ese cliente y, a continuación, enviando el evento **DragStart** .

### <a name="see-also"></a>Consulte también

[**Evento DragComplete**](dragcomplete-event.md)


 

 




