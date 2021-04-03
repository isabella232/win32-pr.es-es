---
title: El código auxiliar del servidor
description: El código auxiliar de servidor proporciona puntos de entrada suplentes en el servidor para cada una de las operaciones definidas en el archivo IDL de entrada.
ms.assetid: e3263543-e78b-40a8-aafa-4315850112a8
keywords:
- MIDL del compilador MIDL, MIDL y RPC MIDL, interfaces, código auxiliar de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b351c53fa9e1d1716e1240ddf4febdccdadda46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076156"
---
# <a name="the-server-stub"></a>El código auxiliar del servidor

El código auxiliar de servidor proporciona puntos de entrada suplentes en el servidor para cada una de las operaciones definidas en el archivo IDL de entrada.

Cuando la biblioteca en tiempo de ejecución de RPC invoca una rutina de código auxiliar de servidor, realiza las siguientes funciones:

-   Anula las referencias de los argumentos de entrada (desempaqueta los argumentos de los formatos transmitidos).
-   Llama a la implementación real del procedimiento en el servidor.
-   Calcula las referencias de los argumentos de salida (empaqueta los argumentos en los formularios transmitidos).

El compilador MIDL cambia [**/Server**](-server.md), [**/sstub**](-sstub.md)y [**/out**](-out.md) afectan al archivo de código auxiliar del servidor.

 

 




