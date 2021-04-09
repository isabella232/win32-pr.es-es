---
title: IAgentCharacter GetExtraData
description: IAgentCharacter GetExtraData
ms.assetid: 83f69bae-0ae3-45c5-ba0d-71610993da60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea854479ab85630abc3d110c9c193716ddedd004
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148863"
---
# <a name="iagentcharactergetextradata"></a>IAgentCharacter::GetExtraData

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetExtraData(
   BSTR * pbszExtraData   // address of buffer for additional character data
); 
```

Recupera datos adicionales almacenados como parte del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pbszExtraData"></span><span id="pbszextradata"></span><span id="PBSZEXTRADATA"></span>*pbszExtraData*
</dt> <dd>

Dirección de un BSTR que recibe el valor de los datos adicionales para el carácter. Los datos adicionales de un carácter se definen cuando se compilan con el editor de caracteres del agente de Microsoft. Un desarrollador de caracteres puede proporcionar esta cadena editando. Archivo ACD para un carácter. La configuración es opcional y es posible que no se proporcione para todos los caracteres, ni se pueden definir o cambiar los datos en tiempo de ejecución. Además, el significado de los datos proporcionados lo define el desarrollador de caracteres.

</dd> </dl>

 

 




