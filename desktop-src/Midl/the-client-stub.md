---
title: El código auxiliar del cliente
description: El módulo de código auxiliar de cliente proporciona puntos de entrada suplentes en el cliente para cada una de las operaciones definidas en el archivo IDL de entrada.
ms.assetid: 6b16a4ef-fa18-4cd0-b483-1365b8c2528b
keywords:
- MIDL y RPC MIDL, interfaces, código auxiliar de cliente
- interfaces MIDL
- interfaces MIDL, MIDL y RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8254915a510e7d176ba315d7a92b049bd0b60926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357447"
---
# <a name="the-client-stub"></a>El código auxiliar del cliente

El módulo de código auxiliar de cliente proporciona puntos de entrada suplentes en el cliente para cada una de las operaciones definidas en el archivo IDL de entrada.

Cuando la aplicación cliente realiza una llamada al procedimiento remoto, su llamada pasa primero a la rutina suplente en el archivo de código auxiliar de cliente. La rutina de código auxiliar de cliente realiza las siguientes funciones:

-   Calcula las referencias de los argumentos. El código auxiliar de cliente empaqueta los argumentos de entrada en un formulario que se puede transmitir al servidor.
-   Llama a la biblioteca en tiempo de ejecución del cliente para transmitir argumentos al espacio de direcciones remoto e invoca el procedimiento remoto en el espacio de direcciones del servidor.
-   Anula las referencias de los argumentos de salida. El código auxiliar del cliente desempaqueta los argumentos de salida y vuelve al autor de la llamada.

El compilador MIDL cambia [**/Client**](-client.md), [**/cstub**](-cstub.md)y [**/out**](-out.md) afectan al archivo de código auxiliar del cliente.

 

 




