---
title: Tipos base y predefinidos de MIDL
description: MIDL admite los siguientes tipos base y predefinidos.
ms.assetid: 72da24b6-253d-4032-ba0c-58b2542701fc
keywords:
- tipos de datos MIDL, predefinidos y base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1afaa479969d65f162a9d57935aa7fbc539701
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075606"
---
# <a name="midl-predefined-and-base-types"></a>Tipos base y predefinidos de MIDL

MIDL admite los siguientes tipos base y predefinidos.



| Tipo de datos                                  | Descripción                                                                                                                                                                                             | Signo predeterminado     |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|
| [**boolean**](boolean.md)                 | 8 bits. No es compatible con las interfaces de [**oleautomation**](oleautomation.md) ; Use VARIANT \_ bool en su lugar.                                                                                               | Sin signo         |
| [**bytes**](byte.md)                       | 8 bits.                                                                                                                                                                                                 | (no aplicable) |
| [**char**](char-idl.md)                   | 8 bits.                                                                                                                                                                                                 | Sin signo         |
| [**double**](double.md)                   | número de punto flotante de bit 64.                                                                                                                                                                           | (no aplicable) |
| [**Estado de error \_ \_ t**](error-status-t.md) | entero de 32 bits sin signo para devolver valores de estado para el control de errores.                                                                                                                                 | Sin signo         |
| [**flot**](float.md)                     | número de punto flotante de bit 32.                                                                                                                                                                           | (no aplicable) |
| [**identificador \_ t**](handle-t.md)              | Tipo de identificador primitivo para el enlace.                                                                                                                                                                      | (no aplicable) |
| [**Thread**](hyper.md)                     | entero de 64 bits.                                                                                                                                                                                         | Firmado           |
| [**Inter**](int.md)                         | entero de 32 bits. En las plataformas de 16 bits, no puede aparecer en funciones remotas sin un calificador de tamaño como [**Short**](short.md), [**Small**](small.md), [**Long**](long.md) o [**Hyper**](hyper.md). | Firmado           |
| **\_\_int8**                               | entero de 8 bits. Equivalente a **pequeño**.                                                                                                                                                                 | Firmado           |
| **\_\_Int16**                              | entero de 16 bits. Equivalente a **Short**.                                                                                                                                                                | Firmado           |
| **\_\_Int32**                              | entero de 32 bits. Equivalente a [**Long**](long.md).                                                                                                                                                     | Firmado           |
| [**\_\_int3264**](--int3264.md)           | Entero de 32 bits en plataformas de 32 bits y es de 64 bits en plataformas de 64 bits.                                                                                                                       | Firmado           |
| [**\_\_Int64**](--int64.md)               | entero de 64 bits. Equivalente a [**Hyper**](hyper.md).                                                                                                                                                   | Firmado           |
| [**tal**](long.md)                       | entero de 32 bits.                                                                                                                                                                                         | Firmado           |
| [**short**](short.md)                     | entero de 16 bits BT.                                                                                                                                                                                          | Firmado           |
| [**pequeño**](small.md)                     | entero de 8 bits.                                                                                                                                                                                          | Firmado           |
| [**void**](void.md)                       | Indica que el procedimiento no devuelve un valor.                                                                                                                                                   | (no aplicable) |
| **hueco \***                                | puntero de 32 bits solo para los identificadores de contexto.                                                                                                                                                                | (no aplicable) |
| [**WCHAR \_ t**](wchar-t.md)                | tipo predefinido de 16 bits para caracteres anchos.                                                                                                                                                             | Sin signo         |



 

 

 




