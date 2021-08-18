---
title: Método Insert
description: Método Insert
ms.assetid: d58cfe50-ace7-4b0f-8539-c2e13a180c96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94b63da0477ee048239afa34ff57475dcce8f0d1129f4574d6b7b6543d75e49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114635"
---
# <a name="insert-method"></a>Método Insert

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Inserta un objeto **Command** en la **colección Commands.**

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Commands.Insert_ *  *Name*, *RefName*, *Before*\_

*Título,* *Voz, Habilitado, Visible*



| Parte      | Descripción                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Nombre*    | Obligatorio. Valor de cadena correspondiente al identificador que asigna al [**comando**](/windows/desktop/lwef/the-command-object).                                                                                                                                                                                               |
| *RefName* | Obligatorio. Valor de cadena correspondiente al nombre (id.) del comando justo encima o debajo de donde desea insertar el nuevo comando.                                                                                                                                                                 |
| *Antes*  | Opcional. Valor booleano que indica si se debe insertar el nuevo comando antes del comando especificado por *RefName*. **True** (valor predeterminado). El nuevo comando se insertará antes que el comando al que se hace referencia.<br/> **False** El nuevo comando se insertará después del comando al que se hace referencia.<br/> |
| *Caption* | Opcional. Valor de cadena correspondiente al nombre que aparecerá en el menú emergente del carácter y en la ventana Comandos cuando la aplicación cliente esté activa en la entrada. Para obtener más información, vea la [**propiedad Caption**](/windows/desktop/lwef/the-command-object) del [**objeto Command.**](caption-property.md)    |
| *Voz*   | Opcional. Valor de cadena correspondiente a las palabras o frases que va a usar el motor de voz para reconocer este comando. Para obtener más información sobre las alternativas de formato para la cadena, vea [**la**](/windows/desktop/lwef/the-command-object) propiedad Voice del **objeto** Command.                                  |
| *Habilitado* | Opcional. Valor booleano que indica si el comando está habilitado. El valor predeterminado es **True**. Para obtener más información, vea [**la propiedad**](/windows/desktop/lwef/the-command-object) Enabled del **objeto Command.**                                                                                                  |
| *Visible* | Opcional. Valor booleano que indica si el comando está visible en la ventana Comandos cuando la aplicación cliente está activa en la entrada. El valor predeterminado es **True**. Para obtener más información, vea la [**propiedad**](/windows/desktop/lwef/the-command-object) Visible del [**objeto**](visible-property.md) Command.       |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

El valor de [**la propiedad Name**](/windows/desktop/lwef/the-command-object) de un objeto [**Command**](name-property.md) debe ser único dentro de su [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object) Debe quitar un comando **para** poder crear un nuevo **comando** con la misma configuración **de la** propiedad Name. Al intentar crear un **comando con** una **propiedad Name** que ya existe, se produce un error.

Este método también devuelve un [**objeto Command.**](/windows/desktop/lwef/the-command-object) Esto le permite declarar un objeto y asignarle un **comando** al llamar al **método Insert.**


```
   Dim Cmd2 as IAgentCtlCommandEx
   Set Cmd2 = Genie.Commands.Insert ("my second command", "my first command",_ True, "Test", "Test", True, True)
   Cmd2.VoiceCaption = "this is a test"
```



## <a name="see-also"></a>Consulte también

[**Add method**](add-method.md), [**Remove method**](remove-method.md), [**RemoveAll method**](removeall-method.md)


 

