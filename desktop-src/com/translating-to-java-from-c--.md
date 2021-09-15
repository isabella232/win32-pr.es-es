---
title: Traducción a Java desde C++
description: Con el lenguaje de programación C++, los desarrolladores pueden acceder directamente a la memoria que almacena una variable determinada. Los punteros de memoria proporcionan este acceso directo. En Java, los punteros se controlan por usted.
ms.assetid: 2c8de3d9-3410-4153-b612-4afab8a69a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf63754782cba82819479a7e26535b518835580b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360156"
---
# <a name="translating-to-java-from-c"></a>Traducción a Java desde C++

Con el lenguaje de programación C++, los desarrolladores pueden acceder directamente a la memoria que almacena una variable determinada. Los punteros de memoria proporcionan este acceso directo. En Java, los punteros se controlan por usted.

En Java, los tipos de datos compuestos **struct**, **union** y **typedef** se controlan exclusivamente mediante el uso de clases. Por ejemplo, el tipo de datos **VARIANT** de C++ se asigna a **com.ms.com.Variant** en Java.

En C++, las cadenas son una matriz de caracteres. En Java, las cadenas son objetos . Los métodos que actúan sobre cadenas tratan la cadena como un objeto completo.

Los métodos COM devuelven un valor conocido como **HRESULT**, que es un código de error de 32 bits. La compatibilidad de Java con Microsoft Internet Explorer define una clase, **com.ms.com.ComException**, que encapsula el código de error **HRESULT.**

Java no admite tipos de datos sin signo, excepto **char**, que es un entero de 16 bits sin signo. Los métodos que aceptan o devuelven otros tipos de datos sin signo no se pueden usar desde Java.

Java no admite matrices multidimensionales. Los métodos que aceptan o devuelven matrices multidimensionales no están disponibles en Java.

Los valores booleanos de Java no se pueden convertir a 0 y 1.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducción a Java](translating-to-java.md)
</dt> </dl>

 

 




