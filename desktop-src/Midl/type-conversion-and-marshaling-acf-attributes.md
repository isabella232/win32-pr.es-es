---
title: Type-Conversion y serialización de atributos ACF
description: Use estos atributos para controlar cómo se transmiten los datos a través de la red.
ms.assetid: 6af635f6-eeee-4fa6-85db-5d60434a1235
keywords:
- MIDL de ACF, atributos, conversión de tipos y serialización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14367be3df97cc1185fca64e46aafe1d342f3526
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159346"
---
# <a name="type-conversion-and-marshaling-acf-attributes"></a>Type-Conversion y serialización de atributos ACF

Use estos atributos para controlar cómo se transmiten los datos a través de la red.



| Atributo                                        | Uso                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**codificar**](encode.md)[**descodificación**](decode.md) | Indica a MIDL que exponga las rutinas de serialización de tipo o procedimiento (pickling) que genera para los códigos auxiliares. La aplicación cliente puede llamar a esas rutinas para serializar los datos por valor.                                                                                                                                                                                                                                                                                  |
| [**representar \_ como**](represent-as.md)            | Especifica cómo se representará un tipo de datos en la conexión, cuando la naturaleza exacta del tipo de datos de un cliente no es importante para el servidor (porque solo necesita los datos en sí y no la estructura real) o el tipo de cliente real es desconocido para MIDL en tiempo de compilación. Por ejemplo, si la aplicación cliente usa una lista vinculada de números de punto flotante, podría especificar que la representación de conexión de esa lista sea una matriz de tipo [**float**](float.md). |
| [**serialización \_ de usuario**](user-marshal.md)            | Controla cómo se transmiten los datos a través de la conexión mediante la implementación de sus propias rutinas de serialización. Este atributo es útil si tiene un tipo de datos desconocido para MIDL o si pasa información entre plataformas big-endian y little-endian.                                                                                                                                                                                                                 |



 

Los atributos de serialización de DCE [**\_ en línea**](in-line.md) y fuera de línea no se implementan en RPC de Microsoft. [**\_ \_**](out-of-line.md) El compilador MIDL serializa automáticamente tipos de datos complejos fuera de línea.

 

 




