---
title: IAgentCommand GetEnabled
description: IAgentCommand GetEnabled
ms.assetid: b4ec25d2-b2e0-4b1b-8dc5-10fbb44149b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7118fa06fc895729755a36872a6d092d962d2416f81ac50e5c528cf9d69f5312
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477660"
---
# <a name="iagentcommandgetenabled"></a>IAgentCommand::GetEnabled

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetEnabled(
   long * pbEnabled  // address of Enabled setting for Command
);
```

Recupera el valor de la [**propiedad Enabled**](enabled-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object).

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

Dirección de una variable que recibe **True** si [**el comando**](/windows/desktop/lwef/the-command-object) está habilitado o **False** si está deshabilitado. No se **puede seleccionar un** comando deshabilitado.

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 