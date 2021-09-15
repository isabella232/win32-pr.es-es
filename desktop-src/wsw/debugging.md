---
title: Depuración (Windows Web Services)
description: Un conjunto de funciones solo está disponible en la compilación debug y está diseñado para pruebas y depuración.
ms.assetid: 23c01420-3f51-4c3f-9ee1-2614de3a278f
keywords:
- Depuración de servicios web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cad0abe916e068408cfda48184aa86e40029203
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574240"
---
# <a name="debugging-windows-web-services"></a>Depuración (Windows Web Services)

Un conjunto de funciones solo está disponible en la compilación debug y está diseñado para pruebas y depuración.


Hay una serie de funciones y variables de entorno disponibles solo en el modo DEBUG. Se pueden usar para ayudar con las pruebas y la depuración.

-   Al establecer WsTimeout=0, todos los tiempos de espera serán INFINITOs. Esto resulta útil al pasar por el depurador durante las operaciones de tiempo confidencial.
-   Establecer WsFailCount tiene el mismo efecto que llamar a WsSetAutoFail.
-   WsFlags permite establecer varias marcas que modifican el comportamiento en tiempo de ejecución. La sintaxis es WsFlags=a,b,c. Las marcas admitidas son ModifyTimestamp, ModifyInclusivePrefixes, ModifyTimestampDigest, ModifyToHeaderDigest y ModifySignatureValue.

Las siguientes funciones se usan con la depuración:

-   [**WsDumpMemory**](wsdumpmemory.md)
-   [**WsSetAutoFail**](wssetautofail.md)

 

 




