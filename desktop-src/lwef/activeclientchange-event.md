---
title: Evento ActiveClientChange
description: Evento ActiveClientChange
ms.assetid: 617b40e6-cafb-463e-8b36-2a12c468d3ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8137edd559d934fd1a478350cd1185885c7dc148
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268770"
---
# <a name="activeclientchange-event"></a>Evento ActiveClientChange

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Se produce cuando cambia el cliente activo del carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

 *Subagente.* ActiveClientChange (ByVal *CharacterID*, ByVal *activo* **)**



| Parte          | Descripción                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter para el que se produjo el evento.                                                                                                                                                                                                      |
| *Activo*      | Valor booleano que indica si el cliente se ha convertido en activo o no activo. **True** La aplicación cliente se convierte en el cliente activo del carácter. <br/> **False** La aplicación cliente ya no es el cliente activo del carácter.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

Cuando varias aplicaciones cliente comparten el mismo carácter, el cliente activo del carácter recibe la entrada del mouse (por ejemplo, eventos de clic o arrastre de control del agente de Microsoft). Del mismo modo, cuando se muestran varios caracteres, el cliente activo del carácter superior (también conocido como cliente de entrada-activo) recibe eventos de [comando](command-event.md) .

Cuando el cliente activo de un carácter cambia, este evento devuelve el identificador de ese carácter y **es true** si la aplicación se convierte en el cliente activo del carácter o en **false** si ya no es el cliente activo del carácter.

Una aplicación cliente puede recibir este evento cuando el usuario selecciona la entrada de una aplicación cliente en el menú emergente del carácter o mediante el comando de voz, cuando la aplicación cliente cambia su estado activo o cuando otra aplicación cliente cierra su conexión con el agente. El agente envía este evento solo a las aplicaciones cliente que se ven afectadas directamente; Esto se convierte en el cliente activo o se detiene en el cliente activo.

### <a name="see-also"></a>Consulte también

[* * * * ActivateInput * * Event *](activateinput-event.md)*, [* * * * Active * * Property * *](active-property.md), * * * * [DeactivateInput * * Event * *](deactivateinput-event.md), [* * * * Activate * * Method * *](activate-method.md)


 

 





