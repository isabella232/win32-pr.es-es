---
title: Agregar método
description: Agregar método
ms.assetid: dd258294-33d6-45f5-a6a1-a3a56b12a7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4527dec6014c93bb02b4f080e032266ea40159e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075610"
---
# <a name="add-method"></a>Agregar método

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Agrega un objeto [Command](the-command-object.md) a la colección [Commands](the-commands-collection-object.md) .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("*** CharacterID * *"). Comandos. agregar* *  *nombre*, *título*, *voz*, *habilitado*, *visible*



| Parte      | Descripción                                                                                                                                                                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Nombre*    | Obligatorio. Valor de cadena que corresponde al identificador que se asigna para el comando.                                                                                                                                                                                                                                        |
| *Caption* | Opcional. Un valor de cadena que corresponde al nombre que aparecerá en el menú emergente del carácter y en la ventana comandos cuando la aplicación cliente sea de entrada-activa. Para obtener más información, vea la propiedad [Caption](caption-property.md) del objeto [Command](the-command-object.md) .                       |
| *Voz*   | Opcional. Valor de cadena que corresponde a las palabras o la frase que va a usar el motor de voz para reconocer este comando. Para obtener más información sobre las alternativas de formato de la cadena, vea la propiedad [Voice](voice-property.md) del objeto [Command](the-command-object.md) .                                |
| *Enabled* | Opcional. Valor booleano que indica si el comando está habilitado. El valor predeterminado es **True**. Para obtener más información, vea la propiedad [Enabled](enabled-property.md) del objeto [Command](the-command-object.md) .                                                                                              |
| *Visible* | Opcional. Un valor booleano que indica si el comando está visible en el menú emergente del carácter para el carácter cuando la aplicación cliente es de entrada-activa. El valor predeterminado es **True**. Para obtener más información, vea la propiedad [visible](visible-property.md) del objeto de [comando](the-command-object.md) . |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

El valor de la propiedad [Name](name-property.md) de un objeto [Command](the-command-object.md) debe ser único dentro de su colección [Commands](the-commands-collection-object.md) . Debe quitar un comando para poder crear un nuevo comando con el mismo valor de la propiedad nombre. Al intentar crear un comando con una propiedad Name que ya existe, se produce un error.

Este método también devuelve un objeto [Command](the-command-object.md) . Esto permite declarar un objeto y asignarle un comando cuando se llama a addMethod.


```
   Dim Cmd1 as IAgentCtlCommandEx
   Set Cmd1 = Genie.Commands.Add ("my first command", "Test", "Test", True, True)
   Cmd1.VoiceCaption = "this is a test"
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Insert (método)**](insert-method.md)
</dt> <dt>

[**método RemoveAll**](removeall-method.md)
</dt> <dt>

[**Remove (método)**](remove-method.md)
</dt> </dl>

 

 




