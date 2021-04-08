---
title: Type-Conversion y serialización de atributos ACF
description: Utilice estos atributos para controlar cómo se transmiten los datos a través de la red.
ms.assetid: 6af635f6-eeee-4fa6-85db-5d60434a1235
keywords:
- Los MIDL, atributos, conversión de tipos y serialización de tipo ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14367be3df97cc1185fca64e46aafe1d342f3526
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994475"
---
# <a name="type-conversion-and-marshaling-acf-attributes"></a>Type-Conversion y serialización de atributos ACF

Utilice estos atributos para controlar cómo se transmiten los datos a través de la red.



| Atributo                                        | Uso                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| descodificación de [**codificación**](encode.md)[](decode.md) | Indica a MIDL que exponga las rutinas de serialización de tipo o procedimiento (picking) que genera para el código auxiliar. La aplicación cliente puede llamar a esas rutinas para calcular las referencias de datos por valor.                                                                                                                                                                                                                                                                                  |
| [**representar \_ como**](represent-as.md)            | Especifica cómo se representará un tipo de datos en la conexión, cuando la naturaleza exacta del tipo de datos de un cliente no es importante para el servidor (porque solo necesita los datos en sí y no la estructura real), o bien el tipo de cliente real es desconocido para MIDL en tiempo de compilación. Por ejemplo, si la aplicación cliente usa una lista vinculada de números de punto flotante, podría especificar que la representación por cable de esa lista sea una matriz de tipo [**float**](float.md). |
| [**\_serialización de usuario**](user-marshal.md)            | Controla cómo se transmiten los datos a través de la conexión implementando sus propias rutinas de cálculo de referencias. Este atributo es útil si tiene un tipo de datos desconocido para MIDL o si va a pasar información entre plataformas big-endian y Little-Endian.                                                                                                                                                                                                                 |



 

Los atributos de serialización [**de DCE en \_ línea**](in-line.md) y [**fuera \_ de \_ línea**](out-of-line.md) no se implementan en Microsoft RPC. El compilador MIDL calcula automáticamente las referencias de tipos de datos complejos fuera de línea.

 

 




