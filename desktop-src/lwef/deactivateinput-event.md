---
title: Evento DeactivateInput
description: Evento DeactivateInput
ms.assetid: 59747932-82be-45d5-8465-73798904e8a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b2fe1ff13b599fe5fbcf2dac22e548a0432f415
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072382"
---
# <a name="deactivateinput-event"></a>Evento DeactivateInput

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Se produce cuando un cliente se convierte en no activo de entrada.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**Sub** *agent: \_ DeactivateInput* *  **(ByVal** *CharacterID):)**



| Parte          | Descripción                                                                    |
|---------------|--------------------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter que hace que el cliente se convierta en no activo de entrada. |



 

</dd> </dl>

### <a name="remarks"></a>Observaciones

Un cliente que no es activo de entrada ya no recibe eventos de mouse o voz del servidor (a menos que se vuelva activo de entrada). El servidor envía este evento solo al cliente que se convierte en no activo de entrada.

Este evento se produce cuando la aplicación cliente está activa en la entrada y el usuario elige el título de otro cliente en el menú emergente de un carácter o en la ventana Comandos de voz o se llama al método [**Activate**](activate-method.md) y se establece el parámetro **State** en 0. También puede ocurrir cuando el usuario selecciona el nombre de otro carácter haciendo clic o hablando. También se obtiene este evento cuando el carácter está oculto u otro carácter se vuelve visible.

### <a name="see-also"></a>Consulte también

[**Evento ActivateInput**](activateinput-event.md)


 

 




