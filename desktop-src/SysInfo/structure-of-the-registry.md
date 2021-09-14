---
description: El registro es una base de datos jerárquica que contiene datos que son críticos para el funcionamiento de Windows y las aplicaciones y servicios que se ejecutan en Windows.
ms.assetid: 4ed60563-73d8-4134-8cb2-8388734fb18d
title: Estructura del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bf104806b5e4e10b4be7387018e714a0db8bf37
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160675"
---
# <a name="structure-of-the-registry"></a>Estructura del Registro

El registro es una base de datos jerárquica que contiene datos que son críticos para el funcionamiento de Windows y las aplicaciones y servicios que se ejecutan en Windows. Los datos se estructuran en formato de árbol. Cada nodo del árbol se denomina *clave*. Cada clave puede contener *subclaves y* entradas de datos *denominadas valores*. A veces, la presencia de una clave son todos los datos que requiere una aplicación. otras veces, una aplicación abre una clave y usa los valores asociados a la clave. Una clave puede tener cualquier número de valores y los valores pueden estar en cualquier formato. Para obtener más información, vea [Tipos de valor del Registro y](registry-value-types.md) [Límites de tamaño de elemento del Registro.](registry-element-size-limits.md)

Cada clave tiene un nombre que consta de uno o varios caracteres imprimibles. Los nombres de clave no distinguen mayúsculas de minúsculas. Los nombres de clave no pueden incluir el carácter de barra diagonal inversa ( ), pero se puede usar cualquier otro \\ carácter imprimible. Los nombres de valor y los datos pueden incluir el carácter de barra diagonal inversa.

El nombre de cada subclave es único con respecto a la clave que está inmediatamente encima de ella en la jerarquía. Los nombres de clave no se localizan en otros idiomas, aunque los valores pueden ser .

La siguiente ilustración es una estructura de clave del Registro de ejemplo, tal como se muestra en el Editor del Registro.

![ventana del editor del registro](images/regtree.png)

Cada uno de los árboles **Mi PC** es una clave. La **clave HKEY \_ LOCAL \_ MACHINE** tiene las siguientes subclaves: **HARDWARE,** **SAM,** **SECURITY,** **SOFTWARE** y **SYSTEM**. Cada una de estas claves a su vez tiene subclaves. Por ejemplo, la **clave HARDWARE** tiene las subclaves **DESCRIPTION**, **DEVICEMAP** y **RESOURCEMAP**; La **clave DEVICEMAP** tiene varias subclaves, incluido **VIDEO**.

Cada valor consta de un nombre de valor y sus datos asociados, si los hay. **MaxObjectNumber** y **VgaCompatible son** valores que contienen datos en la **subclave VIDEO.**

Un árbol del Registro puede tener una profundidad de 512 niveles. Puede crear hasta 32 niveles a la vez a través de una única llamada API del registro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general de Windows Registry](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))
</dt> </dl>

 

 
