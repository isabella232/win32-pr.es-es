---
title: Agregar método
description: Agregar método
ms.assetid: dd258294-33d6-45f5-a6a1-a3a56b12a7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ae6cc3cd0a39be8b293a6ae64a96859e5d4fcf6d23ff410439422676b3527e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976835"
---
# <a name="add-method"></a>Agregar método

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Agrega un [objeto Command](the-command-object.md) a la [colección Commands.](the-commands-collection-object.md)

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Commands.Add_ *  *Name*, *Caption*, *Voice*, *Enabled*, *Visible*



| Parte      | Descripción                                                                                                                                                                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Nombre*    | Obligatorio. Valor de cadena correspondiente al identificador que asigna para el comando.                                                                                                                                                                                                                                        |
| *Caption* | Opcional. Valor de cadena correspondiente al nombre que aparecerá en el menú emergente del carácter y en la ventana Comandos cuando la aplicación cliente esté activa en la entrada. Para obtener más información, vea la [propiedad Caption](the-command-object.md) del [objeto Command.](caption-property.md)                       |
| *Voz*   | Opcional. Valor de cadena correspondiente a las palabras o frases que va a usar el motor de voz para reconocer este comando. Para obtener más información sobre las alternativas de formato para la cadena, vea [la](the-command-object.md) propiedad Voice del [objeto](voice-property.md) Command.                                |
| *Habilitado* | Opcional. Valor booleano que indica si el comando está habilitado. El valor predeterminado es **True**. Para obtener más información, vea [la propiedad](the-command-object.md) Enabled del [objeto Command.](enabled-property.md)                                                                                              |
| *Visible* | Opcional. Valor booleano que indica si el comando está visible en el menú emergente del carácter cuando la aplicación cliente está activa en la entrada. El valor predeterminado es **True**. Para obtener más información, vea la [propiedad](the-command-object.md) Visible del [objeto](visible-property.md) Command. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

El valor de la [propiedad Name](the-command-object.md) de un [objeto Command](name-property.md) debe ser único dentro de su [colección Commands.](the-commands-collection-object.md) Debe quitar un comando para poder crear un nuevo comando con la misma configuración de la propiedad Name. Al intentar crear un comando con una propiedad Name que ya existe, se produce un error.

Este método también devuelve un [objeto Command.](the-command-object.md) Esto le permite declarar un objeto y asignarle un comando al llamar a Addmethod.


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

[**Método Remove**](remove-method.md)
</dt> </dl>

 

 




