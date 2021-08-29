---
title: IAgentCharacter GetExtraData
description: IAgentCharacter GetExtraData
ms.assetid: 83f69bae-0ae3-45c5-ba0d-71610993da60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12032eb7d4587b4d9ccc7260699e5e11bd816e6239d4b49d3ad4692882e4827
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962315"
---
# <a name="iagentcharactergetextradata"></a>IAgentCharacter::GetExtraData

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetExtraData(
   BSTR * pbszExtraData   // address of buffer for additional character data
); 
```

Recupera datos adicionales almacenados como parte del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbszExtraData"></span><span id="pbszextradata"></span><span id="PBSZEXTRADATA"></span>*pbszExtraData*
</dt> <dd>

Dirección de un BSTR que recibe el valor de los datos adicionales para el carácter. Los datos adicionales de un carácter se definen cuando se compilan con el Editor de caracteres de Microsoft Agent. Un desarrollador de caracteres puede proporcionar esta cadena editando . Archivo ACD para un carácter. El valor es opcional y no se puede proporcionar para todos los caracteres, ni se pueden definir o cambiar los datos en tiempo de ejecución. Además, el desarrollador de caracteres define el significado de los datos proporcionados.

</dd> </dl>

 

 




