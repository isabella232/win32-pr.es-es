---
title: Deshabilitación de STRICT
description: Para deshabilitar la comprobación de tipos STRICT, defina el nombre de símbolo NO \_ STRICT. En Visual C/C++, también puede especificar esta definición en la línea de comandos o en un archivo Make especificando /DNO STRICT como \_ opción del compilador.
ms.assetid: 57b01d2e-1f64-4ac0-b4f0-624c241899d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bfdfef2aa7988576aa4c1e17f002639de98121
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360545"
---
# <a name="disabling-strict"></a>Deshabilitación de STRICT

Para deshabilitar la comprobación de tipos **STRICT,** defina el nombre de símbolo **NO \_ STRICT.** En Visual C/C++, también puede especificar esta definición en la línea de comandos o en un archivo Make especificando **/DNO \_ STRICT** como opción del compilador.

Para definir **NO \_ STRICT archivo** a archivo, inserte una instrucción **\# define** antes de incluir Windows.h:


```C++
#define NO_STRICT
#include <windows.h>
```



Para obtener mejores resultados, también debe establecer el nivel de advertencia para los mensajes de error en al menos **/W3**. Esto siempre es aconsejable con las aplicaciones para Windows, ya que una práctica de codificación que provoca una advertencia (por ejemplo, pasar un número incorrecto de parámetros) suele provocar un error grave en tiempo de ejecución si no se corrige.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Habilitación de STRICT](enabling-strict.md)
</dt> <dt>

[Cumplimiento strict](strict-compliance.md)
</dt> </dl>

 

 




