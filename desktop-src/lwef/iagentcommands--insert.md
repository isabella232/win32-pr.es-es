---
title: IAgentCommands insertar
description: IAgentCommands insertar
ms.assetid: f450aae4-db6f-4326-ae14-ddb68ab0953a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65f15df0c24e16a7554881cf3d0e6c41c4ee42b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420617"
---
# <a name="iagentcommandsinsert"></a>IAgentCommands:: Insert

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Insert(
   BSTR bszCaption,  // Caption setting for Command
   BSTR bszVoice,    // Voice setting for Command
   long bEnabled,    // Enabled setting for Command
   long bVisible,    // Visible setting for Command
   long dwRefID,     // reference Command for insertion
   long dBefore,     // insertion position flag
   long * pdwID      // address for variable for Command ID
);
```

Inserta un objeto [**Command**](/windows/desktop/lwef/the-command-object) en una colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

BSTR que especifica el valor del texto de [**título**](caption-property.md) que se muestra para el [**comando**](/windows/desktop/lwef/the-command-object).

</dd> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

BSTR que especifica el valor de la configuración del texto de la [**voz**](voice-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Una expresión booleana que especifica el valor [**habilitado**](enabled-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object). Si el parámetro es **true**, el **comando** está habilitado y se puede seleccionar; Si es **false**, el **comando** está deshabilitado.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Una expresión booleana que especifica el valor [**visible**](visible-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object). Si el parámetro es **true**, el **comando** estará visible en el menú emergente del carácter (si también se establece la propiedad [**Caption**](caption-property.md) ).

</dd> <dt>

<span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*dwRefID*
</dt> <dd>

IDENTIFICADOR de un [**comando**](/windows/desktop/lwef/the-command-object) que se usa como referencia para la inserción relativa del nuevo **comando**.

</dd> <dt>

<span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*dBefore*
</dt> <dd>

Expresión booleana que especifica dónde se debe colocar el [**comando**](/windows/desktop/lwef/the-command-object). Si este parámetro es **true**, el nuevo **comando** se inserta antes del **comando** al que se hace referencia; Si es **false**, el nuevo **comando** se coloca después del **comando** al que se hace referencia.

</dd> <dt>

<span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID* 
</dt> <dd>

Dirección de una variable que recibe el identificador del [**comando**](/windows/desktop/lwef/the-command-object)insertado.

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Remove**](iagentcommands--remove.md), [**IAgentCommands:: RemoveAll**](iagentcommands--removeall.md)


 

 