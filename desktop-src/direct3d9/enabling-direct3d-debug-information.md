---
description: ¿Está intentando obtener más información sobre los objetos de Direct3D durante la depuración? Por ejemplo, la siguiente captura de pantalla muestra lo que normalmente se ve cuando se observa una interfaz de Direct3D en la ventana de reloj.
ms.assetid: 365451f8-e93e-4cc4-b688-2e668518c245
title: Habilitar la información de depuración de Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88851c144c2e651e920d870618f66a38028207bc5503f513f45fb053e16bd2e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730175"
---
# <a name="enabling-direct3d-debug-information-direct3d-9"></a>Habilitar la información de depuración de Direct3D (Direct3D 9)

¿Está intentando obtener más información sobre los objetos de Direct3D durante la depuración? Por ejemplo, la siguiente captura de pantalla muestra lo que normalmente se ve cuando se observa una interfaz de Direct3D en la ventana de reloj.

![captura de pantalla de una interfaz direct3d en la ventana de reloj](images/d3d-debug-info1.png)

Puede habilitar los objetos de depuración principales para que un objeto reflejado que contiene todas las propiedades del objeto se pueda ver en la ventana de visualización. Simplemente incluya la siguiente \# definición en el código antes del archivo D3D9.h:


```
#define D3D_DEBUG_INFO
```



Para habilitar la información de depuración, la definición debe compilarse antes del archivo D3D9.h (cualquier programa que use DXUT habilitará automáticamente D3D DEBUG INFO cuando el programa se compile para la \# \_ \_ depuración). Si ejecuta un ejemplo de SDK, puede verlo en DXStdAfx.h (lo que afecta a todos los ejemplos de C++). También debe ejecutar el tiempo de ejecución de depuración de Direct3D (que se puede habilitar desde el Panel de control si es necesario).

Este es un ejemplo de uso del [ejemplo BasicHLSL](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx).

1.  Agregue la \# definición al archivo Dxstdafx.h antes de la línea 37.
2.  Compile un proyecto de depuración.
3.  Establecer un punto de interrupción en la línea 307 en BasicHLSL.cpp
4.  Ejecute el depurador.

En la siguiente captura de pantalla se muestra el tipo de información detallada que puede obtener sobre un objeto de textura de Direct3D desde la ventana de reloj.

![captura de pantalla de un objeto de textura direct3d en la ventana de reloj](images/d3d-debug-info2.png)

> [!Note]
>
> Los nombres de propiedad de objeto son visibles y los valores son correctos solo cuando el tiempo de ejecución de depuración está habilitado. Cuando se ejecuta en el entorno de ejecución comercial, los valores no son válidos.

 

## <a name="use-the-call-stack-for-extended-debug"></a>Usar la pila de llamadas para la depuración extendida

Con la depuración de Direct3D habilitada, también puede ver una pila de llamadas cada vez que se crea un objeto. Esto hará que la aplicación sea muy lenta, pero se puede usar para comprobar si hay fugas de recursos. Para escribir la pila de llamadas, establezca la siguiente clave del Registro en 1:


```
\\HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Direct3D\\
D3D9Debugging\\EnableCreationStack
```



La compilación de la aplicación con depuración habilitada le dará acceso a esta variable adicional:


```
  LPCWSTR CreationCallStack;
```



Esta variable almacenará la pila de llamadas cada vez que se cree un objeto. Esto hará que la aplicación sea muy lenta, pero se puede usar para depurar pérdidas de recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programación Sugerencias](programming-tips.md)
</dt> </dl>

 

 



