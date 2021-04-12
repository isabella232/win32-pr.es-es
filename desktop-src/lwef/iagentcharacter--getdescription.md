---
title: IAgentCharacter GetDescription
description: IAgentCharacter GetDescription
ms.assetid: 729f54ac-1c60-4a7b-b993-5682a6ea2b3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423cd1f5c799cc1f0177f6d3d7922d5d14de1dbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419207"
---
# <a name="iagentcharactergetdescription"></a>IAgentCharacter:: GetDescription

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetDescription(
   BSTR * pbszDescription   // address of buffer for character description
); 
```

Recupera la descripción del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pbszDescription"></span><span id="pbszdescription"></span><span id="PBSZDESCRIPTION"></span>*pbszDescription*
</dt> <dd>

Dirección de un BSTR que recibe el valor de la descripción del carácter. La descripción de un carácter se define cuando se compila con el editor de caracteres del agente de Microsoft. La configuración de la descripción es opcional y es posible que no se proporcione para todos los caracteres.

</dd> </dl>

 

 




