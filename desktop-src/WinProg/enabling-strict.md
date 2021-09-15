---
title: Habilitación de STRICT
description: Al definir el símbolo STRICT, se habilitan las características que requieren más atención a la hora de declarar y usar tipos.
ms.assetid: 4029c7a7-108a-40cb-8600-eb23968e9d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0400b67025f11dc9c58553f6835b2a8e2b36b4c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360544"
---
# <a name="enabling-strict"></a>Habilitación de STRICT

Al definir el símbolo **STRICT,** se habilitan las características que requieren más cuidado en la declaración y el uso de tipos. Esto le ayuda a escribir código más portátil. Esta atención adicional también reducirá el tiempo de depuración. Al **habilitar STRICT** se redefinen determinados tipos de datos para que el compilador no permita la asignación de un tipo a otro sin una conversión explícita. Esto es especialmente útil con Windows código. Los errores al pasar tipos de datos se notifican en tiempo de compilación en lugar de provocar errores irreales en tiempo de ejecución.

Con Visual C++, **la comprobación de** tipos STRICT se define de forma predeterminada.

Para definir **STRICT** archivo a archivo, inserte una instrucción **\# define** antes de incluir Windows.h:


```C++
#define STRICT
#include <windows.h>
```



Cuando se define **STRICT,** [las definiciones de tipos](windows-data-types.md) de datos cambian de la siguiente manera:

-   Los tipos de identificador específicos se definen para que sean mutuamente excluyentes; Por ejemplo, no podrá pasar un **HWND** donde se requiera un argumento de tipo **HDC.** Sin **STRICT**, todos los identificadores se definen como **HANDLE**, por lo que el compilador no impide que use un tipo de identificador donde se espera otro tipo.
-   Todos los tipos de función de devolución de llamada (como procedimientos de diálogo, procedimientos de ventana y procedimientos de enlace) se definen con prototipos completos. Esto evita que declare funciones de devolución de llamada con listas de parámetros incorrectas.
-   Los tipos de parámetros y valores devueltos que deben usar un puntero genérico se declaran correctamente **como LPVOID** en lugar de como **LPSTR** u otro tipo de puntero.
-   La [**estructura COMSTAT**](/windows/desktop/api/winbase/ns-winbase-comstat) se declara según el estándar ANSI.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Deshabilitar STRICT](disabling-strict.md)
</dt> <dt>

[Cumplimiento strict](strict-compliance.md)
</dt> </dl>

 

 
