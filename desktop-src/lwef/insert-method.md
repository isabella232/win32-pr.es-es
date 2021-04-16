---
title: Insert (método)
description: Insert (método)
ms.assetid: d58cfe50-ace7-4b0f-8539-c2e13a180c96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74eb6d76c1be9b83b7742255ee5a771ed93c64d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105685704"
---
# <a name="insert-method"></a>Insert (método)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Inserta un objeto **Command** en la colección **Commands** .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("*** CharacterID * *"). Commands. Insert* *  *Name*, *RefName*, *Before*\_

*Título*, *voz, habilitado, visible*



| Parte      | Descripción                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Nombre*    | Obligatorio. Valor de cadena que corresponde al identificador que se asigna al [**comando**](/windows/desktop/lwef/the-command-object).                                                                                                                                                                                               |
| *RefName* | Obligatorio. Un valor de cadena que corresponde al nombre (ID.) del comando justo encima o debajo del lugar en el que desea insertar el nuevo comando.                                                                                                                                                                 |
| *Antes*  | Opcional. Valor booleano que indica si se va a insertar el nuevo comando antes del comando especificado por *RefName*. **True** (valor predeterminado). El nuevo comando se insertará antes del comando al que se hace referencia.<br/> **False** El nuevo comando se insertará después del comando al que se hace referencia.<br/> |
| *Caption* | Opcional. Un valor de cadena que corresponde al nombre que aparecerá en el menú emergente del carácter y en la ventana comandos cuando la aplicación cliente sea de entrada-activa. Para obtener más información, vea la propiedad [**Caption**](caption-property.md)del objeto [**Command**](/windows/desktop/lwef/the-command-object) .    |
| *Voz*   | Opcional. Valor de cadena que corresponde a las palabras o la frase que va a usar el motor de voz para reconocer este comando. Para obtener más información sobre las alternativas de formato de la cadena, vea la propiedad **Voice** del objeto [**Command**](/windows/desktop/lwef/the-command-object) .                                  |
| *Enabled* | Opcional. Valor booleano que indica si el comando está habilitado. El valor predeterminado es **True**. Para obtener más información, vea la propiedad **Enabled** del objeto [**Command**](/windows/desktop/lwef/the-command-object) .                                                                                                  |
| *Visible* | Opcional. Un valor booleano que indica si el comando está visible en la ventana comandos cuando la aplicación cliente es de entrada-activa. El valor predeterminado es **True**. Para obtener más información, vea la propiedad [**visible**](visible-property.md) del objeto de [**comando**](/windows/desktop/lwef/the-command-object) .       |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

El valor de la propiedad [**Name**](name-property.md) de un objeto [**Command**](/windows/desktop/lwef/the-command-object) debe ser único dentro de su colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) . Debe quitar un **comando** para poder crear un nuevo **comando** con el mismo valor de la propiedad **nombre** . Al intentar crear un **comando** con una propiedad **Name** que ya existe, se produce un error.

Este método también devuelve un objeto [**Command**](/windows/desktop/lwef/the-command-object) . Esto permite declarar un objeto y asignarle un **comando** cuando se llama al método **Insert** .


```
   Dim Cmd2 as IAgentCtlCommandEx
   Set Cmd2 = Genie.Commands.Insert ("my second command", "my first command",_ True, "Test", "Test", True, True)
   Cmd2.VoiceCaption = "this is a test"
```



## <a name="see-also"></a>Consulte también

[**Método Add**](add-method.md), [**Remove Method**](remove-method.md), [**RemoveAll Method**](removeall-method.md)


 

