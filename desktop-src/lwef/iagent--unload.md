---
title: IAgent UnLoad
description: IAgent UnLoad
ms.assetid: 560301b3-c038-4c6e-b3f1-1203b618b67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e6e457e2acc33c5b34800b8378d82a50d5c4aa6a139366ca1c0d241f676f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610145"
---
# <a name="iagentunload"></a>IAgent::UnLoad

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT UnLoad(
   long * dwCharID  //character ID
);
```

Descarga los datos de caracteres para el carácter especificado de la [**colección**](/windows/desktop/lwef/the-characters-object) Characters.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador del carácter.

</dd> </dl>

Use este método cuando ya no necesite un carácter para liberar la memoria usada para almacenar información sobre el carácter. Si vuelve a tener acceso al carácter, use el [**método Load.**](load-method.md)

## <a name="see-also"></a>Consulte también

[**IAgent::Load**](iagent--load.md)


 

 