---
title: Deshabilitar STRICT
description: Para deshabilitar la comprobación estricta de tipos, defina el nombre del símbolo como NO \_ estricto. En Visual C/C++, también puede especificar esta definición en la línea de comandos o en un archivo make si especifica/DNO \_ STRICT como opción del compilador.
ms.assetid: 57b01d2e-1f64-4ac0-b4f0-624c241899d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bfdfef2aa7988576aa4c1e17f002639de98121
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777514"
---
# <a name="disabling-strict"></a>Deshabilitar STRICT

Para deshabilitar la comprobación **estricta** de tipos, defina el nombre del símbolo como **no \_ estricto**. En Visual C/C++, también puede especificar esta definición en la línea de comandos o en un archivo make si especifica **/DNO \_ STRICT** como opción del compilador.

Para no definir de forma **\_ estricta** cada archivo, inserte una instrucción de **\# definición** antes de incluir Windows. h:


```C++
#define NO_STRICT
#include <windows.h>
```



Para obtener los mejores resultados, también debe establecer el nivel de advertencia para los mensajes de error en al menos **/W3**. Esto siempre es aconsejable con las aplicaciones de Windows, ya que una práctica de codificación que genera una advertencia (por ejemplo, pasando el número incorrecto de parámetros) suele provocar un error irrecuperable en tiempo de ejecución si no se corrige.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Habilitar STRICT](enabling-strict.md)
</dt> <dt>

[Cumplimiento estricto](strict-compliance.md)
</dt> </dl>

 

 




