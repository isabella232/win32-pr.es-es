---
title: Método Activate
description: Método Activate
ms.assetid: 8111139d-1453-416e-8f08-38c06669ff4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5032c7c7f2faf7ec53028a0cc0ce55847fe300864bb531968fc8190b4e00d164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753164"
---
# <a name="activate-method"></a>Método Activate

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**Descripción**](../wmformat/description.md)
</dt> <dd>

Establece el cliente o carácter activo.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Activar_ *  \[ *estado*\]



| Parte    | Descripción                                                                                                                                                                           |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Estado* | Opcional. Puede especificar los siguientes valores para este parámetro: 0 No es el cliente activo.<br/> 1 Cliente activo. <br/> 2 (valor predeterminado) Carácter superior.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Cuando hay varios caracteres visibles, solo uno de los caracteres recibe la entrada de voz a la vez. De forma similar, cuando varias aplicaciones cliente comparten el mismo carácter, solo uno de los clientes recibe la entrada del mouse (por ejemplo, eventos de clic o arrastre del control de Microsoft Agent). El juego de caracteres para recibir la entrada de mouse y voz es el carácter superior y el cliente que recibe la entrada es el cliente activo de ese carácter. (La ventana del carácter superior también aparece en la parte superior del orden Z de la ventana de caracteres). Normalmente, el usuario determina el carácter superior seleccionando explícitamente el carácter. Sin embargo, la activación de nivel superior también cambia cuando se muestra u oculta un carácter (el carácter se convierte o ya no está en la parte superior, respectivamente).

También puede usar este método para administrar explícitamente cuando el cliente recibe entradas dirigidas al carácter, como cuando la propia aplicación se activa. Por ejemplo, si establece *Estado* en 2, el carácter se convierte en el nivel superior y el cliente recibe todos los eventos de entrada de mouse y voz generados a partir de la interacción del usuario con el carácter. Por lo tanto, también convierte al cliente en el cliente activo de entrada del carácter.

Sin embargo, también puede establecerse como el cliente activo para un carácter sin hacer que el carácter sea el más alto; para ello, establezca *Estado* en 1. Esto permite que el cliente reciba la entrada dirigida a ese carácter cuando el carácter se convierte en el nivel superior. Del mismo modo, puede establecer el cliente para que no sea el cliente activo (no para recibir la entrada) cuando el carácter se convierte en el nivel superior; para ello, establezca *Estado* en 0.

Evite llamar a este método directamente después de [**un método Show.**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) **Mostrar** establece automáticamente el cliente activo de entrada. Cuando el carácter está oculto, se puede producir un error en la llamada a [**Activate**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) si se procesa antes de que se complete el método **Show.**

Si llama a este método a una función, devuelve un valor booleano que indica si el método se ha hecho correctamente. Se producirá un error al intentar llamar a este método con el parámetro *State* establecido en 2 cuando se oculta el carácter especificado. De forma similar, si establece *Estado* en 0 y la aplicación es el único cliente, se produce un error en esta llamada porque un carácter siempre debe tener un cliente de nivel superior.


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
> Llamar a este método *con Estado* establecido en 1 no suele generar un evento [**ActivateInput**](https://www.bing.com/search?q=**ActivateInput**) a menos que no haya otros caracteres cargados o la aplicación ya esté activa en la entrada.

 

## <a name="see-also"></a>Consulte también

[**Evento ActivateInput**](activateinput-event.md), [ **evento DeactivateInput**](deactivateinput-event.md)


 

