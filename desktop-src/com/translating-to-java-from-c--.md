---
title: Traducir a Java desde C++
description: Mediante el lenguaje de programación C++, los desarrolladores pueden acceder directamente a la memoria que almacena una variable determinada. Los punteros de memoria proporcionan este acceso directo. En Java, los punteros se controlan automáticamente.
ms.assetid: 2c8de3d9-3410-4153-b612-4afab8a69a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf63754782cba82819479a7e26535b518835580b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418415"
---
# <a name="translating-to-java-from-c"></a>Traducir a Java desde C++

Mediante el lenguaje de programación C++, los desarrolladores pueden acceder directamente a la memoria que almacena una variable determinada. Los punteros de memoria proporcionan este acceso directo. En Java, los punteros se controlan automáticamente.

En Java, los tipos de datos compuestos **struct**, **Union** y **typedef** se controlan exclusivamente mediante el uso de clases. Por ejemplo, el tipo de datos **Variant** de C++ se asigna a **com. ms. com. Variant** en Java.

En C++, las cadenas son una matriz de caracteres. En Java, las cadenas son objetos. Los métodos que actúan en cadenas tratan la cadena como un objeto completo.

Los métodos COM devuelven un valor conocido como **HRESULT**, que es un código de error de 32 bits. La compatibilidad de Java con Microsoft Internet Explorer define una clase, **com. ms. com. COMException**, que contiene el código de error **HRESULT** .

Java no admite tipos de datos sin signo excepto **Char**, que es un entero sin signo de 16 bits. Los métodos que aceptan o devuelven otros tipos de datos sin signo no se pueden usar desde Java.

Java no admite matrices multidimensionales. Los métodos que aceptan o devuelven matrices multidimensionales no están disponibles en Java.

Los valores booleanos de Java no se pueden convertir a 0 y 1.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducir a Java](translating-to-java.md)
</dt> </dl>

 

 




