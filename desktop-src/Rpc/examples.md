---
title: Ejemplos (RPC)
description: Ejemplos que muestran los conceptos de llamada a procedimiento remoto (RPC).
ms.assetid: d5db3085-6df0-4539-a605-d60055f4f4ec
keywords:
- RPC (llamada a procedimiento remoto), ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e6a814d78afbfc7fefa979c890cbbb8c3d4ce0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105676527"
---
# <a name="examples-rpc"></a>Ejemplos (RPC)

El kit de desarrollo de software (SDK) de la plataforma incluye ejemplos que muestran una variedad de conceptos de llamada a procedimiento remoto (RPC), como se indica a continuación:

-   ASYNCRPC muestra la estructura de una aplicación RPC que usa llamadas a procedimientos remotos asincrónicas. También muestra varios métodos de notificación de la finalización de la llamada.
-   CLUUID muestra el uso del UUID de objeto de cliente para permitir que un cliente seleccione entre varias implementaciones de un procedimiento remoto.
-   El directorio de datos contiene cuatro programas: DUNION ilustra uniones discriminadas (no encapsuladas); Inout muestra los parámetros [ \[ in \] ](../midl/in.md), [ \[ out \] ](../midl/out-idl.md) ; REPAS muestra el atributo [representated \_ as](/windows/desktop/Midl/represent-as) ; TRANSMISIÓN muestra el atributo [transmitir \_ como](/windows/desktop/Midl/transmit-as) .
-   DYNEPT muestra una aplicación cliente que administra su conexión con el servidor a través de extremos dinámicos.
-   El directorio FILEREP contiene cuatro ejemplos que muestran cómo los desarrolladores pueden escribir un servicio simple de replicación de archivos, un servicio de replicación de archivos de varios usuarios, un servicio que admite características de seguridad y un servicio que usa canalizaciones asincrónicas de RPC.
-   El directorio HANDles contiene tres programas, AUTO, CXHNDL, USRDEF, que muestran el [ \_ identificador automático](/windows/desktop/Midl/auto-handle), el \[ identificador de contexto \_ y los \] identificadores genéricos (definidos por el usuario), respectivamente.
-   HELLO es una implementación de cliente/servidor de "Hello, World".
-   El directorio PICKLE contiene dos programas: PICKLP muestra la serialización del procedimiento de datos; La lista desplegable muestra la serialización del tipo de datos; ambos programas usan los atributos de [ \[ codificación \] ](../midl/encode.md) y [ \[ descodificación \] ](../midl/decode.md) .
-   CANALIZAciones muestra el uso del constructor de tipo de canalización.
-   RPCSVC muestra la implementación de un servicio con RPC.
-   STROUT muestra cómo asignar memoria en un servidor para un objeto bidimensional (una matriz de punteros) y devolverla al cliente como un \[ \] parámetro de solo salida. Después, el cliente libera la memoria. Esta técnica permite al código auxiliar llamar al servidor sin conocer de antemano la cantidad de datos que se devolverá.

    Este programa también permite al usuario compilar para Unicode o ANSI.

Todos los archivos de código fuente y los archivos make de estos programas se encuentran en el SDK de la plataforma.

Para obtener ejemplos básicos de desarrollo de aplicaciones RPC y más sencillos, consulte los temas del [tutorial](tutorial.md) .

 

 
