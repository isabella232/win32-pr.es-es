---
title: Tipos base y predefinidos de MIDL
description: MIDL admite los siguientes tipos base y predefinidos.
ms.assetid: 72da24b6-253d-4032-ba0c-58b2542701fc
keywords:
- tipos de datos MIDL, predefinidos y base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ecbc76b3f680f0fffbabcff38e8562475e26be8ae4ac583a78c614d1651151
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067085"
---
# <a name="midl-predefined-and-base-types"></a>Tipos base y predefinidos de MIDL

MIDL admite los siguientes tipos base y predefinidos.



| Tipo de datos                                  | Descripción                                                                                                                                                                                             | Inicio de sesión predeterminado     |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|
| [**Booleana**](boolean.md)                 | 8 bits. No es compatible con [**las interfaces oleautomation;**](oleautomation.md) use VARIANT \_ BOOL en su lugar.                                                                                               | Sin signo         |
| [**Byte**](byte.md)                       | 8 bits.                                                                                                                                                                                                 | (no aplicable) |
| [**Char**](char-idl.md)                   | 8 bits.                                                                                                                                                                                                 | Sin signo         |
| [**Doble**](double.md)                   | Número de punto flotante de 64 bits.                                                                                                                                                                           | (no aplicable) |
| [**error \_ status \_ t**](error-status-t.md) | Entero de 32 bits sin signo para devolver valores de estado para el control de errores.                                                                                                                                 | Sin signo         |
| [**Flotador**](float.md)                     | Número de punto flotante de 32 bits.                                                                                                                                                                           | (no aplicable) |
| [**handle \_ t**](handle-t.md)              | Tipo de identificador primitivo para el enlace.                                                                                                                                                                      | (no aplicable) |
| [**hyper**](hyper.md)                     | Entero de 64 bits.                                                                                                                                                                                         | Firmado           |
| [**int**](int.md)                         | Entero de 32 bits. En plataformas de 16 bits, no puede aparecer en funciones remotas sin un calificador de tamaño como [**short**](short.md), [**small,**](small.md) [**long**](long.md) o [**hyper**](hyper.md). | Firmado           |
| **\_\_int8**                               | Entero de 8 bits. Equivalente a **pequeño**.                                                                                                                                                                 | Firmado           |
| **\_\_int16**                              | Entero de 16 bits. Equivalente a **corto.**                                                                                                                                                                | Firmado           |
| **\_\_int32**                              | Entero de 32 bits. Equivalente a [**long.**](long.md)                                                                                                                                                     | Firmado           |
| [**\_\_int3264**](--int3264.md)           | Entero de 32 bits en plataformas de 32 bits y de 64 bits en plataformas de 64 bits.                                                                                                                       | Firmado           |
| [**\_\_int64**](--int64.md)               | Entero de 64 bits. Equivalente a [**hyper**](hyper.md).                                                                                                                                                   | Firmado           |
| [**long**](long.md)                       | Entero de 32 bits.                                                                                                                                                                                         | Firmado           |
| [**short**](short.md)                     | Entero de 16 bt.                                                                                                                                                                                          | Firmado           |
| [**Pequeño**](small.md)                     | Entero de 8 bits.                                                                                                                                                                                          | Firmado           |
| [**void**](void.md)                       | Indica que el procedimiento no devuelve un valor.                                                                                                                                                   | (no aplicable) |
| **Vacío \***                                | Puntero de 32 bits solo para identificadores de contexto.                                                                                                                                                                | (no aplicable) |
| [**wchar \_ t**](wchar-t.md)                | Tipo predefinido de 16 bits para caracteres anchos.                                                                                                                                                             | Sin signo         |



 

 

 




