---
title: IAgentCharacter GetName
description: IAgentCharacter GetName
ms.assetid: 6c013a18-8c56-42a8-8723-31d83b3230cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107e6fdb6be3e79dee14177d9f56ee7d258f3455d578641e7d3a3b3cf044c741
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962284"
---
# <a name="iagentcharactergetname"></a>IAgentCharacter::GetName

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetName(
   BSTR * pbszName   // address of buffer for character name
);
```

Recupera el nombre del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*
</dt> <dd>

Dirección de un BSTR que recibe el valor del nombre del carácter.

</dd> </dl>

El nombre predeterminado de un carácter se define cuando se compila con el Editor de caracteres de Microsoft Agent. El nombre de un carácter puede variar en función del identificador de idioma del carácter. Los caracteres se pueden compilar con nombres diferentes para distintos idiomas.

También puede establecer el nombre del carácter **mediante IAgentCharacter:SetName**; sin embargo, esto cambia el nombre de todos los clientes actuales del carácter.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::SetName**](iagentcharacter--setname.md)


 

 




