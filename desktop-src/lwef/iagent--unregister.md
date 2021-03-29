---
title: IAgent anular registro
description: IAgent anular registro
ms.assetid: d81cde72-f9ff-45aa-9dbf-faea9a478c3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796e033ac823ee7c79fe5312fab2c57dec36e694
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904598"
---
# <a name="iagentunregister"></a>IAgent:: unregister

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Unregister(
   long dwSinkID  //notification sink ID
);
```

Descarga los datos de caracteres para el carácter especificado de la colección de [**caracteres**](/windows/desktop/lwef/the-characters-object) .

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwSinkID*
</dt> <dd>

IDENTIFICADOR del receptor de notificaciones.

</dd> </dl>

Utilice este método cuando ya no necesite servicios del agente de Microsoft, como cuando se cierre la aplicación.

## <a name="see-also"></a>Consulte también

[**IAgent:: Register**](iagent--register.md)


 

 