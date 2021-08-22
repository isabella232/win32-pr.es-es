---
title: Habilitación de STRICT
description: Al definir el símbolo STRICT, se habilitan las características que requieren más atención a la hora de declarar y usar tipos.
ms.assetid: 4029c7a7-108a-40cb-8600-eb23968e9d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca6ca814d69910620b89095cc18be3b37601329dc053937d5772243097537c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561799"
---
# <a name="enabling-strict"></a>Habilitación de STRICT

Al definir el símbolo **STRICT,** se habilitan las características que requieren más atención a la hora de declarar y usar tipos. Esto le ayuda a escribir código más portátil. Esta atención adicional también reducirá el tiempo de depuración. Al **habilitar STRICT** se redefinen determinados tipos de datos para que el compilador no permita la asignación de un tipo a otro sin una conversión explícita. Esto es especialmente útil con Windows código. Los errores al pasar tipos de datos se notifican en tiempo de compilación en lugar de provocar errores irreales en tiempo de ejecución.

Con Visual C++, **la comprobación de** tipos STRICT se define de forma predeterminada.

Para definir **STRICT** archivo a archivo, inserte una instrucción **\# define** antes de incluir Windows.h:


```C++
#define STRICT
#include <windows.h>
```



Cuando se define **STRICT,** [las definiciones de tipos](windows-data-types.md) de datos cambian de la siguiente manera:

-   Los tipos de identificador específicos se definen para que sean mutuamente excluyentes; Por ejemplo, no podrá pasar un **HWND** donde se requiera un argumento de tipo **HDC.** Sin **STRICT,** todos los identificadores se definen como **HANDLE,** por lo que el compilador no impide que use un tipo de identificador donde se espera otro tipo.
-   Todos los tipos de función de devolución de llamada (como procedimientos de diálogo, procedimientos de ventana y procedimientos de enlace) se definen con prototipos completos. Esto evita que declare funciones de devolución de llamada con listas de parámetros incorrectas.
-   Los tipos de parámetros y valores devueltos que deben usar un puntero genérico se declaran correctamente como **LPVOID** en lugar de como **LPSTR** u otro tipo de puntero.
-   La [**estructura COMSTAT**](/windows/desktop/api/winbase/ns-winbase-comstat) se declara según el estándar ANSI.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Deshabilitación de STRICT](disabling-strict.md)
</dt> <dt>

[Cumplimiento strict](strict-compliance.md)
</dt> </dl>

 

 
