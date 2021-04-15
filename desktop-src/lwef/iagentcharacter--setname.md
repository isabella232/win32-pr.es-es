---
title: IAgentCharacter SetName
description: IAgentCharacter SetName
ms.assetid: 4944f910-60e9-446b-82e9-2794f445789a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec058e338adfa8c998bf26a1223ae71f0c7de3d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714267"
---
# <a name="iagentcharactersetname"></a>IAgentCharacter:: SetName

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetName(
   BSTR bszName   // character name
);
```

Establece el nombre del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*
</dt> <dd>

BSTR que establece el nombre del carácter. El nombre predeterminado de un carácter se define cuando se compila con el editor de caracteres del agente de Microsoft. Puede cambiarlo mediante **IAgentCharacter:: setName**; sin embargo, esto cambia el nombre de carácter de todos los clientes actuales del carácter. Esta propiedad no es persistente (se almacena de forma permanente). El nombre del carácter vuelve a su nombre predeterminado cada vez que un cliente carga el carácter por primera vez.

El nombre del carácter también puede depender de su identificador de idioma. Los caracteres se pueden compilar con nombres diferentes para distintos idiomas.

El servidor usa la configuración de nombre del carácter en partes de la interfaz del agente de Microsoft, como el título de la ventana comandos de voz cuando el carácter es de entrada-activo y en el menú emergente de la barra de tareas del agente de Microsoft.

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentCharacter:: GetName**](iagentcharacter--getname.md)


 

 




