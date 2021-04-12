---
title: IAgentCharacter GetName
description: IAgentCharacter GetName
ms.assetid: 6c013a18-8c56-42a8-8723-31d83b3230cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33679577cfb5179a799ee61207f7ecd9b2be8a21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357794"
---
# <a name="iagentcharactergetname"></a>IAgentCharacter:: GetName

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetName(
   BSTR * pbszName   // address of buffer for character name
);
```

Recupera el nombre del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*
</dt> <dd>

Dirección de un BSTR que recibe el valor del nombre del carácter.

</dd> </dl>

El nombre predeterminado de un carácter se define cuando se compila con el editor de caracteres del agente de Microsoft. El nombre de un carácter puede variar en función del identificador de idioma del carácter. Los caracteres se pueden compilar con nombres diferentes para distintos idiomas.

También puede establecer el nombre del carácter mediante **IAgentCharacter: setName**; sin embargo, esto cambia el nombre de todos los clientes actuales del carácter.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter:: SetName**](iagentcharacter--setname.md)


 

 




