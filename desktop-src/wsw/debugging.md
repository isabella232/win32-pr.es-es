---
title: Depuración (Windows Web Services)
description: Un conjunto de funciones solo está disponible en la compilación DEBUG y está diseñado para pruebas y depuraciones.
ms.assetid: 23c01420-3f51-4c3f-9ee1-2614de3a278f
keywords:
- Depuración de servicios web para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 135f81ec45028df098679c91d750915005bfc64b3ff7d072b0494badc98159fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838685"
---
# <a name="debugging-windows-web-services"></a>Depuración (Windows Web Services)

Un conjunto de funciones solo está disponible en la compilación DEBUG y está diseñado para pruebas y depuraciones.


Hay una serie de funciones y variables de entorno disponibles solo en el modo DEBUG. Se pueden usar para ayudar con las pruebas y la depuración.

-   Si se establece WsTimeout=0, todos los tiempos de espera serán INFINITOs. Esto resulta útil al realizar una ejecución paso a paso por el depurador durante las operaciones sensibles al tiempo.
-   Establecer WsFailCount tiene el mismo efecto que llamar a WsSetAutoFail.
-   WsFlags permite establecer varias marcas que modifican el comportamiento en tiempo de ejecución. La sintaxis es WsFlags=a,b,c. Las marcas admitidas son ModifyTimestamp, ModifyInclusivePrefixes, ModifyTimestampDigest, ModifyToHeaderDigest y ModifySignatureValue.

Las siguientes funciones se usan con la depuración:

-   [**WsDumpMemory**](wsdumpmemory.md)
-   [**WsSetAutoFail**](wssetautofail.md)

 

 




