---
description: Una excepción es un evento que se produce durante la ejecución de un programa y requiere la ejecución de código fuera del flujo normal de control.
ms.assetid: 6b6326d8-6875-4146-a4e3-7873f4e400cb
title: Control de excepciones estructurado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62069b5aed16869a3f56b644d522c368702251c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164621"
---
# <a name="structured-exception-handling"></a>Control de excepciones estructurado

Una *excepción* es un evento que se produce durante la ejecución de un programa y requiere la ejecución de código fuera del flujo normal de control. Hay dos tipos de excepciones: excepciones de hardware y excepciones de software. *La CPU inicia las* excepciones de hardware. Pueden ser el resultado de la ejecución de determinadas secuencias de instrucciones, como la división por cero o un intento de acceder a una dirección de memoria no válida. *Las aplicaciones o el* sistema operativo inician explícitamente las excepciones de software. Por ejemplo, el sistema puede detectar cuándo se especifica un valor de parámetro no válido.

*El control estructurado de excepciones* es un mecanismo para controlar las excepciones de hardware y software. Por lo tanto, el código controlará las excepciones de hardware y software de forma idéntica. El control estructurado de excepciones permite tener un control completo sobre el control de excepciones, proporciona compatibilidad con depuradores y se puede usar en todos los lenguajes de programación y máquinas. *El control de excepciones vectoriales* es una extensión para el control estructurado de excepciones.

El sistema también admite *el* control de terminación , que le permite asegurarse de que cada vez que se ejecuta un cuerpo de código guardado, también se ejecuta un bloque especificado de código de terminación. El código de terminación se ejecuta independientemente de cómo el flujo de control deje el cuerpo guardado. Por ejemplo, un controlador de terminación puede garantizar que se realicen tareas de limpieza incluso si se produce una excepción o algún otro error mientras se ejecuta el cuerpo de código guardado.

-   [Acerca del control estructurado de excepciones](about-structured-exception-handling.md)
-   [Uso del control estructurado de excepciones](using-structured-exception-handling.md)
-   [Referencia de control estructurado de excepciones](structured-exception-handling-reference.md)

 

 



