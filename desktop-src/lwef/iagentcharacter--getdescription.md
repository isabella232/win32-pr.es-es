---
title: IAgentCharacter GetDescription
description: IAgentCharacter GetDescription
ms.assetid: 729f54ac-1c60-4a7b-b993-5682a6ea2b3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23216f1a7b013a54de1e64351c2a9d3a3d3359d90e0516cd6852a003baa047c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716195"
---
# <a name="iagentcharactergetdescription"></a>IAgentCharacter::GetDescription

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetDescription(
   BSTR * pbszDescription   // address of buffer for character description
); 
```

Recupera la descripción del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbszDescription"></span><span id="pbszdescription"></span><span id="PBSZDESCRIPTION"></span>*pbszDescription*
</dt> <dd>

Dirección de un BSTR que recibe el valor de la descripción del carácter. La descripción de un carácter se define cuando se compila con el Editor de caracteres de Microsoft Agent. La configuración de descripción es opcional y no se puede proporcionar para todos los caracteres.

</dd> </dl>

 

 




