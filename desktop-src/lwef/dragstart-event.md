---
title: Evento DragStart
description: Evento DragStart
ms.assetid: fef0ae05-1958-45c6-8260-107c47b5fa92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 835ffc22e23643d306b361977a4bbe8b04e6481f8a577c3c2cef959b4be46ea7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963095"
---
# <a name="dragstart-event"></a>Evento DragStart

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Se produce cuando el usuario comienza a arrastrar un carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**Sub** *agent** \_ DragStart* *  **(ByVal** *CharacterID*, **(ByVal** *Button*, **(ByVal** *Shift*, **(ByVal** *X*, **(ByVal** *Y"))**



| Parte          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter en el que se ha hecho clic como una cadena.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Botón*      | Devuelve un entero que identifica el botón que se presionó y soltó para provocar el evento. El argumento del botón es un campo de bits con bits correspondientes al botón izquierdo (bit 0), el botón derecho (bit 1) y el botón central (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. Solo se establece uno de los bits, lo que indica el botón que provocó el evento.                                                                                                                                                                                                                                                                                |
| *Shift*       | Devuelve un entero que corresponde al estado de las teclas MAYÚS, CTRL y ALT cuando se presiona o se libera el botón especificado en el argumento de botón. Se establece un bit si la clave está abajo. El argumento mayús es un campo de bits con los bits menos significativos correspondientes a la tecla MAYÚS (bit 0), la tecla CTRL (bit 1) y la tecla ALT (bit 2). Estos bits corresponden a los valores 1, 2 y 4, respectivamente. El argumento mayús indica el estado de estas claves. Se pueden establecer algunos, todos o ninguno de los bits, lo que indica que se presionan algunas, todas o ninguna de las teclas. Por ejemplo, si se presionan CTRL y ALT, el valor de mayús sería 6. |
| *X,Y*         | Devuelve un entero que especifica la ubicación actual del puntero del mouse. Los valores X e Y siempre se expresan en píxeles, en relación con la esquina superior izquierda de la pantalla.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Comentarios

Este evento solo se envía al cliente activo de entrada de un carácter. Cuando el usuario arrastra un carácter sin cliente activo de entrada, el servidor establece su último cliente activo de entrada como el cliente activo de entrada actual, envía el evento [**ActivateInput**](activateinput-event.md) a ese cliente y, a continuación, envía el **evento DragStart.**

### <a name="see-also"></a>Consulte también

[**Evento DragComplete**](dragcomplete-event.md)


 

 




