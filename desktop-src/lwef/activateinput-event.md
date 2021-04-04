---
title: Evento ActivateInput
description: Evento ActivateInput
ms.assetid: bc395750-5da0-4379-8eca-3195e936052c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0b4fdf83256d58dd247dee85b639f5499f013e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076241"
---
# <a name="activateinput-event"></a>Evento ActivateInput

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Se produce cuando un cliente pasa a ser de entrada-activo.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

**Sub** *Agent* \_ ActivateInput **(ByVal** *CharacterID ** * *)*



| Parte          | Descripción                                                                    |
|---------------|--------------------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter a través del cual el cliente pasa a ser de entrada-activo. |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

El cliente de entrada-activo recibe los eventos de entrada de mouse y voz proporcionados por el servidor. El servidor envía este evento solo al cliente que pasa a ser de entrada-activo.

Este evento puede producirse cuando el usuario cambia al objeto de [comando](the-command-object.md) , por ejemplo, al elegir la entrada del objeto de comando en la ventana comandos o en el menú emergente de un carácter. También se puede producir cuando el usuario selecciona un carácter (al hacer clic o hablar su nombre), cuando se hace visible un carácter y cuando se oculta el carácter de otra aplicación cliente. También puede llamar al [método Activate](activate-method.md) (con el **Estado** establecido en 2) para crear explícitamente el carácter más alto, lo que hace que la aplicación cliente se convierta en entrada-activa y desencadene este evento. Sin embargo, este evento no se produce si se usa el método activar método únicamente para especificar si el cliente es el cliente activo del carácter.

### <a name="see-also"></a>Consulte también

[Evento **DeactivateInput**](deactivateinput-event.md), [método **Activate**](activate-method.md)


 

 




