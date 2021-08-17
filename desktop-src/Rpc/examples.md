---
title: Ejemplos (RPC)
description: Ejemplos que muestran los conceptos de llamada a procedimiento remoto (RPC).
ms.assetid: d5db3085-6df0-4539-a605-d60055f4f4ec
keywords:
- Llamada a procedimiento remoto RPC, ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e75dca3866e325a4f10eb446d209b834b62ff0407e7edd19f92ec70ac700df85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930054"
---
# <a name="examples-rpc"></a>Ejemplos (RPC)

Platform Software Development Kit (SDK) incluye ejemplos que muestran una variedad de conceptos de llamada a procedimiento remoto (RPC), como se muestra a continuación:

-   ASYNCRPC muestra la estructura de una aplicación RPC que usa llamadas a procedimiento remoto asincrónicas. También muestra varios métodos de notificación de la finalización de la llamada.
-   CLUUID muestra el uso del UUID de objeto de cliente para permitir que un cliente seleccione entre varias implementaciones de un procedimiento remoto.
-   El directorio DATA contiene cuatro programas: DUNION muestra uniones discriminadas (no superadas); INOUT muestra en [ \[ los parámetros \] ](../midl/in.md), [ \[ out; \] ](../midl/out-idl.md) REPAS muestra la representación [ \_ como](/windows/desktop/Midl/represent-as) atributo; XMIT muestra la [transmisión \_ como](/windows/desktop/Midl/transmit-as) atributo.
-   D LDAPPT muestra una aplicación cliente que administra su conexión al servidor a través de puntos de conexión dinámicos.
-   El directorio FILEREP contiene cuatro ejemplos que ilustran cómo los desarrolladores pueden escribir un servicio de replicación de archivos simple, un servicio de replicación de archivos multiusutivo, un servicio que admite características de seguridad y un servicio mediante canalizaciones asincrónicas rpc.
-   El directorio HANDLES contiene tres programas, AUTO, CXHNDL y USRDEF, que muestran identificadores [automáticos, \_ ](/windows/desktop/Midl/auto-handle)identificadores de contexto y identificadores genéricos (definidos por el \[ \_ \] usuario), respectivamente.
-   HELLO es una implementación de cliente/servidor de "Hola mundo".
-   El directorio PICKLE contiene dos programas: PICKLP muestra la serialización de procedimientos de datos; PICKLT muestra la serialización de tipos de datos; ambos programas usan los [ \[ atributos de \] codificación](../midl/encode.md) [ \[ y descodificación. \] ](../midl/decode.md)
-   PIPES muestra el uso del constructor de tipo de canalización.
-   RPCSVC muestra la implementación de un servicio con RPC.
-   STROUT muestra cómo asignar memoria en un servidor para un objeto bidimensional (una matriz de punteros) y pasarla de vuelta al cliente como un \[ \] parámetro out -only. A continuación, el cliente libera la memoria. Esta técnica permite que el código auxiliar llame al servidor sin saber de antemano cuántos datos se devolverán.

    Este programa también permite al usuario compilar para UNICODE o ANSI.

Todos los archivos de origen y archivos Make de estos programas se encuentran en platform SDK.

Para ver el desarrollo básico de aplicaciones RPC y ejemplos más sencillos, consulte los [temas del tutorial.](tutorial.md)

 

 
