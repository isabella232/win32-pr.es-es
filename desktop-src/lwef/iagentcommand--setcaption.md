---
title: IAgentCommand SetCaption
description: IAgentCommand SetCaption
ms.assetid: f4fdd37a-28b4-4e00-885c-58addedec659
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ffccf42a972ec9635c929fb954d58bfaff967af364d24ae505e1dbb2bd8772
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976365"
---
# <a name="iagentcommandsetcaption"></a>IAgentCommand::SetCaption

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Command
);
```

Establece el [**texto del**](caption-property.md) título que se muestra para un [**comando**](/windows/desktop/lwef/the-command-object).

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

BSTR que especifica el texto de la propiedad [**Caption**](caption-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Al establecer la [](/windows/desktop/lwef/the-command-object) propiedad [**Caption**](caption-property.md) de un comando, se define cómo aparecerá en el menú emergente del carácter cuando su propiedad [**Visible**](visible-property.md) esté establecida en **True** y la aplicación no sea el cliente activo de entrada. Para especificar una clave de acceso (mnemotécnica sin línea) para el título **,** incluya un carácter de yerba (&) antes de ese carácter. Para que se pueda seleccionar, su [**propiedad Enabled**](enabled-property.md) debe establecerse en **True.**

## <a name="see-also"></a>Consulte también

[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 