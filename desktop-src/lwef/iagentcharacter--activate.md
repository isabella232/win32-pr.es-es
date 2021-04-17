---
title: IAgentCharacter activar
description: IAgentCharacter activar
ms.assetid: a81eb62d-709b-46b4-9ff2-c9017f7f853e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e86d2c094da484f528750d433e0fb6608790e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532506"
---
# <a name="iagentcharacteractivate"></a>IAgentCharacter:: Activate

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Activate(
   short sState, // topmost character or client setting
);
```

Establece si un cliente está activo o un carácter es el nivel superior.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.
-   Devuelve S \_ false para indicar que la operación no se realizó correctamente.

<dl> <dt>

<span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*
</dt> <dd>

Puede especificar los siguientes valores para este parámetro:



| Value | Descripción                   |
|-------|-------------------------------|
| 0     | Se establece como no es el cliente activo. |
| 1     | Establezca como el cliente activo.     |
| 2     | Cree el carácter más alto.   |



 

</dd> </dl>

Cuando hay varios caracteres visibles, solo uno de los caracteres recibe la entrada de voz a la vez. Del mismo modo, cuando varias aplicaciones cliente comparten el mismo carácter, solo uno de los clientes recibe la entrada de mouse (por ejemplo, eventos de clic o arrastre de control del agente de Microsoft) a la vez. El juego de caracteres para recibir entrada de mouse y voz es el carácter más alto y el cliente que recibe la entrada es el cliente activo del carácter. (La ventana del carácter superior también aparece en la parte superior del orden z de la ventana de caracteres). Normalmente, el usuario determina qué carácter es el nivel superior seleccionándolo explícitamente. Sin embargo, la activación de nivel superior también cambia cuando se muestra o se oculta un carácter (el carácter se vuelve o ya no es más alto, respectivamente).

También puede usar este método para administrar explícitamente cuando el cliente recibe entradas dirigidas al carácter, como cuando la propia aplicación se activa. Por ejemplo, establecer el **Estado** en 2 hace que el carácter sea más alto y el cliente recibe todos los eventos de entrada del mouse y voz generados a partir de la interacción del usuario con el carácter. Por lo tanto, también convierte al cliente en el cliente de entrada y activo del carácter. Sin embargo, también puede establecer el cliente activo para un carácter sin hacer que el carácter sea más alto, estableciendo el **Estado** en 1. Esto permite que el cliente reciba entradas dirigidas a ese carácter cuando el carácter se vuelve más alto. Del mismo modo, puede configurar el cliente para que no sea el cliente activo (para no recibir entradas) cuando el carácter se convierta en el nivel más alto, estableciendo el **Estado** en 0. Puede determinar si un carácter tiene otros clientes actuales mediante [**IAgentCharacter:: HasOtherClients**](iagentcharacter--hasotherclients.md).

Evite llamar a este método directamente después de un método [**Show**](iagentcharacter--show.md) . **Mostrar** establece automáticamente el cliente de entrada-activo. Cuando se oculta el carácter, se puede producir un error en la llamada a **Activate** si se procesa antes de que se complete el método **Show** .

Se producirá un error al intentar llamar a este método con el parámetro de **Estado** establecido en 2 (si el carácter especificado está oculto). De forma similar, si establece **State** en 0 y la aplicación es el único cliente, se produce un error en esta llamada. Un carácter siempre debe tener un cliente superior.

> [!Note]  
> La llamada a este método con el **Estado** establecido en 1 no suele generar un evento [**AgentNotifySink:: ActivateInputState**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) a menos que no se hayan cargado otros caracteres o que la aplicación ya sea de entrada-activa.

 

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::HasOtherClients**](iagentcharacter--hasotherclients.md)


 

 




