---
title: Depurar (servicios Web de Windows)
description: Un conjunto de funciones solo está disponible en la compilación de depuración y está pensada para probar y depurar.
ms.assetid: 23c01420-3f51-4c3f-9ee1-2614de3a278f
keywords:
- Depuración de servicios web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cad0abe916e068408cfda48184aa86e40029203
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105714517"
---
# <a name="debugging-windows-web-services"></a>Depurar (servicios Web de Windows)

Un conjunto de funciones solo está disponible en la compilación de depuración y está pensada para probar y depurar.


Solo hay una serie de funciones y variables de entorno disponibles en el modo de depuración. Se pueden usar para ayudar con las pruebas y la depuración.

-   Si se establece WsTimeout = 0, todos los tiempos de espera serán INFINITOs. Esto resulta útil cuando se recorre el depurador durante las operaciones que dependen del tiempo.
-   Establecer WsFailCount tiene el mismo efecto que llamar a WsSetAutoFail.
-   WsFlags permite establecer varias marcas que modifican el comportamiento de tiempo de ejecución. La sintaxis es WsFlags = a, b, c. Los marcadores admitidos son ModifyTimestamp, ModifyInclusivePrefixes, ModifyTimestampDigest, ModifyToHeaderDigest y ModifySignatureValue.

Las siguientes funciones se usan con la depuración:

-   [**WsDumpMemory**](wsdumpmemory.md)
-   [**WsSetAutoFail**](wssetautofail.md)

 

 




