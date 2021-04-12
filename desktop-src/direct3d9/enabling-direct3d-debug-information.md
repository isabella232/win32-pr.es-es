---
description: ¿Está intentando obtener más información sobre los objetos de Direct3D durante la depuración? Por ejemplo, en la siguiente captura de pantalla se muestra lo que se ve normalmente al mirar una interfaz Direct3D en la ventana Inspección.
ms.assetid: 365451f8-e93e-4cc4-b688-2e668518c245
title: Habilitar la información de depuración de Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17bb46cf8658d0417d021faa6bdbefd10822d1dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151947"
---
# <a name="enabling-direct3d-debug-information-direct3d-9"></a>Habilitar la información de depuración de Direct3D (Direct3D 9)

¿Está intentando obtener más información sobre los objetos de Direct3D durante la depuración? Por ejemplo, en la siguiente captura de pantalla se muestra lo que se ve normalmente al mirar una interfaz Direct3D en la ventana Inspección.

![captura de pantalla de una interfaz Direct3D en la ventana Inspección](images/d3d-debug-info1.png)

Puede habilitar los objetos de depuración principales para que un objeto reflejado que contenga todas las propiedades del objeto se pueda ver en la ventana Inspección. Simplemente incluya la siguiente \# definición en el código antes del archivo D3D9. h:


```
#define D3D_DEBUG_INFO
```



Para habilitar la información de depuración, la \# definición se debe compilar antes que el archivo D3D9. h (cualquier programa que use DXUT habilitará automáticamente la \_ información de depuración D3D \_ cuando el programa se compile para depurar). Si está ejecutando un ejemplo de SDK, puede verlo en DXStdAfx. h (que afecta a todos los ejemplos de C++). También debe ejecutar el tiempo de ejecución de depuración de Direct3D (que se puede habilitar desde el panel de control si es necesario).

Este es un ejemplo en el que se usa el [ejemplo BasicHLSL](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx).

1.  Agregue la \# definición al archivo Dxstdafx. h antes de la línea 37.
2.  Compilar un proyecto de depuración.
3.  Establecer un punto de interrupción en la línea 307 en BasicHLSL. cpp
4.  Ejecutar el depurador.

En la captura de pantalla siguiente se muestra el tipo de información detallada que puede obtener sobre un objeto de textura de Direct3D desde la ventana Inspección.

![captura de pantalla de un objeto de textura de Direct3D en la ventana Inspección](images/d3d-debug-info2.png)

> [!Note]
>
> Los nombres de las propiedades del objeto son visibles y los valores solo son correctos cuando se habilita el tiempo de ejecución de depuración. Cuando se ejecuta en el Runtime de venta directa, los valores no son válidos.

 

## <a name="use-the-call-stack-for-extended-debug"></a>Usar la pila de llamadas para la depuración extendida

Con la depuración de Direct3D habilitada, también puede examinar una pila de llamadas cada vez que se crea un objeto. Esto hará que la aplicación sea muy lenta, pero se puede usar para comprobar si hay pérdidas de recursos. Para escribir la pila de llamadas, establezca la siguiente clave del registro en 1:


```
\\HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Direct3D\\
D3D9Debugging\\EnableCreationStack
```



Al compilar la aplicación con depuración habilitada, obtendrá acceso a esta variable adicional:


```
  LPCWSTR CreationCallStack;
```



Esta variable almacenará la pila de llamadas cada vez que se cree un objeto. Esto hará que la aplicación sea muy lenta, pero se puede usar para depurar pérdidas de recursos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sugerencias de programación](programming-tips.md)
</dt> </dl>

 

 



