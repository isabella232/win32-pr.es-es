---
title: Evento ActivateInput
description: Evento ActivateInput
ms.assetid: bc395750-5da0-4379-8eca-3195e936052c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db21d605a014002063a7c5aa42554a06adb1ed35296242944de789daeb3155c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610685"
---
# <a name="activateinput-event"></a>Evento ActivateInput

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Se produce cuando un cliente se convierte en activo de entrada.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**Sub** *agent* \_ ActivateInput **(ByVal** *CharacterID):)**



| Parte          | Descripción                                                                    |
|---------------|--------------------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter a través del cual el cliente se convierte en activo de entrada. |



 

</dd> </dl>

### <a name="remarks"></a>Comentarios

El cliente activo de entrada recibe eventos de entrada de mouse y voz proporcionados por el servidor. El servidor envía este evento solo al cliente que se convierte en activo de entrada.

Este evento puede producirse cuando el usuario cambia al objeto [Command,](the-command-object.md) por ejemplo, eligiendo la entrada del objeto Command en la ventana Comandos o en el menú emergente de un carácter. También puede ocurrir cuando el usuario selecciona un carácter (haciendo clic o hablando su nombre), cuando un carácter se vuelve visible y cuando el carácter de otra aplicación cliente se oculta. También puede llamar al método  [Activate](activate-method.md) (con el estado establecido en 2) para hacer que el carácter sea el más alto de forma explícita, lo que da lugar a que la aplicación cliente se convierta en entrada-activa y desencadena este evento. Sin embargo, este evento no se produce si se usa el método Activate Method solo para especificar si el cliente es el cliente activo del carácter.

### <a name="see-also"></a>Consulte también

[**Evento DeactivateInput,**](deactivateinput-event.md) [ **método Activate**](activate-method.md)


 

 




