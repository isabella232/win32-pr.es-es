---
title: IAgentCommandsEx GetDefaultID
description: IAgentCommandsEx GetDefaultID
ms.assetid: 14079ae0-ad2c-4f38-9371-9914f8402e49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4dabfb1c957031b353303775921a352bf40d984ac5de1ee9c933f79a5e02cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105231"
---
# <a name="iagentcommandsexgetdefaultid"></a>IAgentCommandsEx::GetDefaultID

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetDefaultID(
   long * pdwID  // address of default command's ID
);
```

Recupera el identificador del comando predeterminado en una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*
</dt> <dd>

Dirección de una variable que recibe el identificador del conjunto [**de**](/windows/desktop/lwef/the-command-object) comandos como valor predeterminado.

</dd> </dl>

Esta propiedad devuelve el objeto [**Command**](/windows/desktop/lwef/the-command-object) predeterminado actual en la [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object) El comando predeterminado está en negrita en el menú emergente del carácter. Sin embargo, establecer el comando predeterminado no cambia el control de comandos ni los eventos de doble clic.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**IAgentCommandsEx::SetDefaultID**](iagentcommandsex--setdefaultid.md)


 

 