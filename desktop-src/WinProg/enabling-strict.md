---
title: Habilitar STRICT
description: Al definir el símbolo STRICT, se habilitan las características que requieren más atención en la declaración y el uso de tipos.
ms.assetid: 4029c7a7-108a-40cb-8600-eb23968e9d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0400b67025f11dc9c58553f6835b2a8e2b36b4c
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/09/2021
ms.locfileid: "105707503"
---
# <a name="enabling-strict"></a>Habilitar STRICT

Al definir el símbolo **STRICT** , se habilitan las características que requieren más atención en la declaración y el uso de tipos. Esto le ayuda a escribir código más portable. Este cuidado adicional también reducirá el tiempo de depuración. Al habilitar **STRICT** , se redefinen determinados tipos de datos para que el compilador no permita la asignación de un tipo a otro sin una conversión explícita. Esto es especialmente útil con el código de Windows. Los errores al pasar tipos de datos se informan en tiempo de compilación en lugar de producir errores irrecuperables en tiempo de ejecución.

Con Visual C++, la comprobación **estricta** de tipos se define de forma predeterminada.

Para definir **STRICT** cada archivo, inserte una instrucción de **\# definición** antes de incluir Windows. h:


```C++
#define STRICT
#include <windows.h>
```



Cuando se define **STRICT** , las definiciones de [tipos de datos](windows-data-types.md) cambian como se indica a continuación:

-   Los tipos de identificador específicos se definen para ser mutuamente excluyentes; por ejemplo, no podrá pasar un **hWnd** en el que sea necesario un argumento de tipo **HDC** . Sin **STRICT**, todos los identificadores se definen como **Handle**, por lo que el compilador no impide usar un tipo de identificador donde se espera otro tipo.
-   Todos los tipos de función de devolución de llamada (como procedimientos de diálogo, procedimientos de ventana y procedimientos de enlace) se definen con prototipos completos. Esto evita que se declaren funciones de devolución de llamada con listas de parámetros incorrectas.
-   Los tipos de parámetro y valor devuelto que deben usar un puntero genérico se declaran correctamente como **LPVOID** en lugar de como **LPSTR** u otro tipo de puntero.
-   La estructura [**comstat**](/windows/desktop/api/winbase/ns-winbase-comstat) se declara según el estándar ANSI.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Deshabilitar STRICT](disabling-strict.md)
</dt> <dt>

[Cumplimiento estricto](strict-compliance.md)
</dt> </dl>

 

 
