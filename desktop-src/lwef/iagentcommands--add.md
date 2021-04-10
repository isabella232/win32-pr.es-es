---
title: IAgentCommands agregar
description: IAgentCommands agregar
ms.assetid: f6be7773-77fa-4c59-8feb-c2ebf54fd2e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee56854c302a096143e58fe6c21ef75fedfbf59
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149194"
---
# <a name="iagentcommandsadd"></a>IAgentCommands:: Add

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Add(
   BSTR bszCaption,  // Caption setting for Command
   BSTR bszVoice,    // Voice setting for Command
   long bEnabled,    // Enabled setting for Command
   long bVisible,    // Visible setting for Command
   long * pdwID      // address for variable for ID
);
```

Agrega un [**comando**](/windows/desktop/lwef/the-command-object) a una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

BSTR que especifica el valor del texto de [**título**](caption-property.md) que se muestra para un [**comando**](/windows/desktop/lwef/the-command-object) en una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

BSTR que especifica el valor de la configuración del texto de la [**voz**](voice-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object) en una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Una expresión booleana que especifica el valor [**habilitado**](enabled-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object) en una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . Si el parámetro es **true**, el **comando** está habilitado y se puede seleccionar; Si es **false**, el **comando** está deshabilitado.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Una expresión booleana que especifica el valor [**visible**](visible-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object) en una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . Si el parámetro es **true**, el **comando** estará visible en el menú emergente del carácter (si también se establece la propiedad [**Caption**](caption-property.md) ).

</dd> <dt>

<span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID* 
</dt> <dd>

Dirección de una variable que recibe el identificador del [**comando**](/windows/desktop/lwef/the-command-object)agregado.

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentCommand:: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand:: setEnabled**](iagentcommand--setenabled.md), [**IAgentCommand:: setVisible**](iagentcommand--setvisible.md), [**IAgentCommand:: SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md), [**IAgentCommands:: Remove**](iagentcommands--remove.md), [**IAgentCommands:: RemoveAll**](iagentcommands--removeall.md)


 

 