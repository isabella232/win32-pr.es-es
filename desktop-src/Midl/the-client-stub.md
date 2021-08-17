---
title: Código auxiliar de cliente
description: El módulo de código auxiliar de cliente proporciona puntos de entrada suplentes en el cliente para cada una de las operaciones definidas en el archivo IDL de entrada.
ms.assetid: 6b16a4ef-fa18-4cd0-b483-1365b8c2528b
keywords:
- MIDL y RPC MIDL, interfaces, código auxiliar de cliente
- interfaces MIDL
- interfaces MIDL, MIDL y RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260c718f0910c2e6834c93409b6d8cd4969e3d2bbe9c53c65821dc0fe0eb19ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146228"
---
# <a name="the-client-stub"></a>Código auxiliar de cliente

El módulo de código auxiliar de cliente proporciona puntos de entrada suplentes en el cliente para cada una de las operaciones definidas en el archivo IDL de entrada.

Cuando la aplicación cliente realiza una llamada al procedimiento remoto, su llamada primero va a la rutina suplente en el archivo de código auxiliar del cliente. La rutina de código auxiliar de cliente realiza las siguientes funciones:

-   Serializa argumentos. El código auxiliar de cliente empaqueta los argumentos de entrada en un formulario que se puede transmitir al servidor.
-   Llama a la biblioteca en tiempo de ejecución del cliente para transmitir argumentos al espacio de direcciones remotas e invoca el procedimiento remoto en el espacio de direcciones del servidor.
-   Desmarshals los argumentos de salida. El código auxiliar del cliente desempaquete los argumentos de salida y vuelve al autor de la llamada.

Los modificadores del compilador [**MIDL /client**](-client.md), [**/cstub**](-cstub.md)y [**/out**](-out.md) afectan al archivo de código auxiliar de cliente.

 

 




