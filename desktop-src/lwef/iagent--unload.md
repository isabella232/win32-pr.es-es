---
title: Descarga de IAgent
description: Descarga de IAgent
ms.assetid: 560301b3-c038-4c6e-b3f1-1203b618b67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc30d6c4c06c1d292a26a2f503477dcca651dd18
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358945"
---
# <a name="iagentunload"></a>IAgent:: Unload

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT UnLoad(
   long * dwCharID  //character ID
);
```

Descarga los datos de caracteres para el carácter especificado de la colección de [**caracteres**](/windows/desktop/lwef/the-characters-object) .

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

IDENTIFICADOR del carácter.

</dd> </dl>

Utilice este método cuando ya no necesite un carácter, para liberar memoria que se utiliza para almacenar información sobre el carácter. Si vuelve a tener acceso al carácter, utilice el método [**Load**](load-method.md) .

## <a name="see-also"></a>Consulte también

[**IAgent:: Load**](iagent--load.md)


 

 