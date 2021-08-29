---
title: IAgentCharacter SetName
description: IAgentCharacter SetName
ms.assetid: 4944f910-60e9-446b-82e9-2794f445789a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46a2210b14519a0595f37786725559d363cddaceb62ae93b80a52deb839e0b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725295"
---
# <a name="iagentcharactersetname"></a>IAgentCharacter::SetName

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetName(
   BSTR bszName   // character name
);
```

Establece el nombre del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*
</dt> <dd>

BSTR que establece el nombre del carácter. El nombre predeterminado de un carácter se define cuando se compila con el Editor de caracteres de Microsoft Agent. Puede cambiarlo mediante **IAgentCharacter::SetName**; sin embargo, esto cambia el nombre del carácter para todos los clientes actuales del carácter. Esta propiedad no es persistente (se almacena de forma permanente). El nombre del carácter se revierte a su nombre predeterminado cada vez que un cliente carga por primera vez el carácter.

El nombre del carácter también puede depender de su identificador de idioma. Los caracteres se pueden compilar con nombres diferentes para distintos idiomas.

El servidor usa la configuración de nombre del carácter en partes de la interfaz del agente de Microsoft, como el título de la ventana Comandos de voz cuando el carácter está activo para la entrada y en el menú emergente de la barra de tareas de Microsoft Agent.

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::GetName**](iagentcharacter--getname.md)


 

 




