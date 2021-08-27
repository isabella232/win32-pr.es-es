---
title: IAgentCharacter Activate
description: IAgentCharacter Activate
ms.assetid: a81eb62d-709b-46b4-9ff2-c9017f7f853e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7256b1d155b051985c72120283e60896026218ea81d8b2b9c37dc94fb52bb63a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751001"
---
# <a name="iagentcharacteractivate"></a>IAgentCharacter::Activate

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Activate(
   short sState, // topmost character or client setting
);
```

Establece si un cliente está activo o si un carácter está en la parte superior.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.
-   Devuelve S \_ FALSE para indicar que la operación no se ha realizado correctamente.

<dl> <dt>

<span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*
</dt> <dd>

Puede especificar los siguientes valores para este parámetro:



| Value | Descripción                   |
|-------|-------------------------------|
| 0     | Establezca como no el cliente activo. |
| 1     | Establezca como el cliente activo.     |
| 2     | Haga el carácter superior.   |



 

</dd> </dl>

Cuando hay varios caracteres visibles, solo uno de los caracteres recibe la entrada de voz a la vez. De forma similar, cuando varias aplicaciones cliente comparten el mismo carácter, solo uno de los clientes recibe la entrada del mouse (por ejemplo, eventos de clic o arrastre del control de Microsoft Agent) a la vez. El juego de caracteres para recibir la entrada de mouse y voz es el carácter superior y el cliente que recibe la entrada es el cliente activo del carácter. (La ventana del carácter superior también aparece en la parte superior del orden Z de la ventana de caracteres). Normalmente, el usuario determina qué carácter está en la parte superior al seleccionarlo explícitamente. Sin embargo, la activación de nivel superior también cambia cuando se muestra u oculta un carácter (el carácter se convierte o ya no está en la parte superior, respectivamente).

También puede usar este método para administrar explícitamente cuando el cliente recibe entradas dirigidas al carácter, como cuando la propia aplicación se activa. Por ejemplo, establecer **Estado** en 2 hace que el carácter sea el más alto y el cliente recibe todos los eventos de entrada de voz y mouse generados a partir de la interacción del usuario con el carácter. Por lo tanto, también convierte al cliente en el cliente activo de entrada del carácter. Sin embargo, también puede establecer el cliente activo para un carácter sin hacer que el carácter sea superior; para ello, **establezca Estado** en 1. Esto permite que el cliente reciba la entrada dirigida a ese carácter cuando el carácter se convierte en el nivel superior. Del mismo modo, puede establecer el cliente para que no sea el cliente activo (para no recibir entrada) cuando el carácter se convierte en el nivel superior, estableciendo **Estado** en 0. Puede determinar si un carácter tiene otros clientes actuales [**mediante IAgentCharacter::HasOtherClients**](iagentcharacter--hasotherclients.md).

Evite llamar a este método directamente después de [**un método Show.**](iagentcharacter--show.md) **Mostrar** establece automáticamente el cliente activo de entrada. Cuando el carácter está oculto, se puede producir un error en la llamada a **Activate** si se procesa antes de que se complete el método **Show.**

Se producirá un error al intentar llamar a este método con el parámetro **State** establecido en 2 (cuando el carácter especificado está oculto). De forma similar, si establece **Estado** en 0 y la aplicación es el único cliente, se produce un error en esta llamada. Un carácter siempre debe tener un cliente de nivel superior.

> [!Note]  
> Llamar a este método con **State** establecido en 1 no suele generar un evento [**AgentNotifySink::ActivateInputState**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) a menos que no haya otros caracteres cargados o la aplicación ya esté activa en la entrada.

 

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::HasOtherClients**](iagentcharacter--hasotherclients.md)


 

 




