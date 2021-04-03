---
description: Una excepción es un evento que se produce durante la ejecución de un programa y requiere la ejecución de código fuera del flujo de control normal.
ms.assetid: 6b6326d8-6875-4146-a4e3-7873f4e400cb
title: Control de excepciones estructurado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62069b5aed16869a3f56b644d522c368702251c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907003"
---
# <a name="structured-exception-handling"></a>Control de excepciones estructurado

Una *excepción* es un evento que se produce durante la ejecución de un programa y requiere la ejecución de código fuera del flujo de control normal. Hay dos tipos de excepciones: excepciones de hardware y de software. La CPU inicia las *excepciones de hardware* . Pueden ser el resultado de la ejecución de ciertas secuencias de instrucciones, como la división por cero o un intento de obtener acceso a una dirección de memoria no válida. Las aplicaciones o el sistema operativo inician explícitamente las *excepciones de software* . Por ejemplo, el sistema puede detectar cuándo se especifica un valor de parámetro no válido.

El *control estructurado de excepciones* es un mecanismo para controlar las excepciones de hardware y software. Por lo tanto, el código controlará las excepciones de hardware y software de forma idéntica. El control de excepciones estructurado permite tener un control completo sobre el control de excepciones, proporciona compatibilidad con los depuradores y se puede usar en todos los lenguajes de programación y máquinas. El *control de excepciones vectoriales* es una extensión del control estructurado de excepciones.

El sistema también admite el *control de terminación*, lo que le permite asegurarse de que, siempre que se ejecute un cuerpo protegido de código, también se ejecute un bloque de código de terminación especificado. El código de finalización se ejecuta independientemente de cómo el flujo de control abandone el cuerpo protegido. Por ejemplo, un controlador de terminación puede garantizar que las tareas de limpieza se realicen incluso si se produce una excepción o algún otro error mientras se ejecuta el cuerpo protegido del código.

-   [Acerca del control estructurado de excepciones](about-structured-exception-handling.md)
-   [Usar el control de excepciones estructurado](using-structured-exception-handling.md)
-   [Referencia de control de excepciones estructurado](structured-exception-handling-reference.md)

 

 



