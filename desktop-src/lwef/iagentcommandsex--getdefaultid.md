---
title: IAgentCommandsEx GetDefaultID
description: IAgentCommandsEx GetDefaultID
ms.assetid: 14079ae0-ad2c-4f38-9371-9914f8402e49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e4380eca62a65758979a94fb23511348b11acdf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420713"
---
# <a name="iagentcommandsexgetdefaultid"></a>IAgentCommandsEx::GetDefaultID

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetDefaultID(
   long * pdwID  // address of default command's ID
);
```

Recupera el identificador del comando predeterminado en una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*
</dt> <dd>

Dirección de una variable que recibe el identificador del conjunto de [**comandos**](/windows/desktop/lwef/the-command-object) como valor predeterminado.

</dd> </dl>

Esta propiedad devuelve el objeto de [**comando**](/windows/desktop/lwef/the-command-object) predeterminado actual en la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . El comando predeterminado está en negrita en el menú emergente del carácter. Sin embargo, el establecimiento del comando predeterminado no cambia el control de los comandos ni los eventos de doble clic.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**IAgentCommandsEx::SetDefaultID**](iagentcommandsex--setdefaultid.md)


 

 