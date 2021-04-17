---
title: Método Activate
description: Método Activate
ms.assetid: 8111139d-1453-416e-8f08-38c06669ff4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21df1965abaeed35e9e440a0f559f5e12d68d6fe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105695580"
---
# <a name="activate-method"></a>Método Activate

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**Denominación**](../wmformat/description.md)
</dt> <dd>

Establece el cliente activo o el carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("*** CharacterID * *"). Activar* *  \[ *Estado*\]



| Parte    | Descripción                                                                                                                                                                           |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Estado* | Opcional. Puede especificar los siguientes valores para este parámetro: 0 no es el cliente activo.<br/> 1 el cliente activo. <br/> 2 (valor predeterminado) el carácter superior.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando hay varios caracteres visibles, solo uno de los caracteres recibe la entrada de voz a la vez. Del mismo modo, cuando varias aplicaciones cliente comparten el mismo carácter, solo uno de los clientes recibe la entrada del mouse (por ejemplo, eventos de clic o arrastre de control del agente de Microsoft). El juego de caracteres para recibir la entrada de mouse y voz es el carácter más alto y el cliente que recibe la entrada es el cliente activo de ese carácter. (La ventana del carácter superior también aparece en la parte superior del orden z de la ventana de caracteres). Normalmente, el usuario determina el carácter superior seleccionando explícitamente el carácter. Sin embargo, la activación de nivel superior también cambia cuando se muestra o se oculta un carácter (el carácter se vuelve o ya no es más alto, respectivamente).

También puede usar este método para administrar explícitamente cuando el cliente recibe entradas dirigidas al carácter como cuando la propia aplicación se activa. Por ejemplo, establecer el *Estado* en 2 hace que el carácter sea más alto y el cliente recibe todos los eventos de entrada de voz y del mouse generados a partir de la interacción del usuario con el carácter. Por lo tanto, también convierte al cliente en el cliente de entrada y activo del carácter.

Sin embargo, también puede establecer que sea el cliente activo para un carácter sin que el carácter sea más alto, estableciendo el *Estado* en 1. Esto permite que el cliente reciba entradas dirigidas a ese carácter cuando el carácter se vuelve más alto. Del mismo modo, puede configurar el cliente para que no sea el cliente activo (no para recibir la entrada) cuando el carácter se convierta en el nivel más alto, estableciendo el *Estado* en 0.

Evite llamar a este método directamente después de un método [**Show**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) . **Mostrar** establece automáticamente el cliente de entrada-activo. Cuando se oculta el carácter, se puede producir un error en la llamada a [**Activate**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) si se procesa antes de que se complete el método **Show** .

Si llama a este método para una función, devuelve un valor booleano que indica si el método se realizó correctamente. Se producirá un error al intentar llamar a este método con el parámetro de *Estado* establecido en 2 cuando se oculte el carácter especificado. De forma similar, si establece *State* en 0 y la aplicación es el único cliente, se produce un error en esta llamada porque un carácter debe tener siempre un cliente superior.


```
   Dim Genie as Object

   Sub FormLoad()

   Agent1.Characters.Load "Genie", "Genie.acs"

   Set Genie = Agent1.Characters ("Genie")

   If (Genie. Activate = True) Then
      'I'm active

   Else
      'I must be hidden or something

   End If 
   
   End Sub
```



> [!Note]  
> La llamada a este método con el *Estado* establecido en 1 no genera normalmente un evento [**ActivateInput**](https://www.bing.com/search?q=**ActivateInput**) a menos que no se cargue ningún otro carácter o que la aplicación ya sea de entrada-activa.

 

## <a name="see-also"></a>Consulte también

[**Evento ActivateInput**](activateinput-event.md), [ **evento DeactivateInput**](deactivateinput-event.md)


 

