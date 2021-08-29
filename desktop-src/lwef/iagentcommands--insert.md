---
title: Inserción de IAgentCommands
description: Inserción de IAgentCommands
ms.assetid: f450aae4-db6f-4326-ae14-ddb68ab0953a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d249a64e3c04d396cea263429cf4ee7b51d536ae8c691761e169a9a52415130d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114695"
---
# <a name="iagentcommandsinsert"></a>IAgentCommands::Insert

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

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

Inserta un objeto [**Command**](/windows/desktop/lwef/the-command-object) en una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

BSTR que especifica el valor del texto [**del**](caption-property.md) título que se muestra para el [**comando**](/windows/desktop/lwef/the-command-object).

</dd> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

BSTR que especifica el valor de la configuración de [**texto**](voice-property.md) de voz para un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Expresión booleana que especifica el valor [**Habilitado**](enabled-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object). Si el parámetro es **True**, el **comando** está habilitado y se puede seleccionar; si **es False**, el **comando** está deshabilitado.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Expresión booleana que especifica el valor [**Visible**](visible-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object). Si el parámetro es **True**, **el** comando estará visible en el menú emergente del carácter (si también se establece la propiedad [**Caption).**](caption-property.md)

</dd> <dt>

<span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*dwRefID*
</dt> <dd>

Identificador de un [**comando usado**](/windows/desktop/lwef/the-command-object) como referencia para la inserción relativa del nuevo **comando**.

</dd> <dt>

<span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*dBefore*
</dt> <dd>

Expresión booleana que especifica dónde colocar el [**comando**](/windows/desktop/lwef/the-command-object). Si este parámetro es **True**, el nuevo **comando se** inserta antes del comando al que se **hace referencia**; si **es False**, el nuevo comando **se** coloca después del comando al que se **hace referencia.**

</dd> <dt>

<span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID* 
</dt> <dd>

Dirección de una variable que recibe el identificador del comando [**insertado.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Remove**](iagentcommands--remove.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)


 

 