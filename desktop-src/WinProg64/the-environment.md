---
title: El entorno
description: Los desarrolladores que trabajan en aplicaciones para aplicaciones de 64 Windows encontrarán el entorno de desarrollo prácticamente idéntico al entorno de desarrollo para aplicaciones de 32 Windows.
ms.assetid: 49b2b952-f771-4721-a9b0-01eb67a98007
keywords:
- entorno de desarrollo de 64 bits Windows programación
- programación de entorno de 64 Windows bits
- Guía de programación de 64 Windows de programación de 64 Windows programación, entorno de desarrollo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104ea1bdacbb478eaa0abcf46d04c3d772540f26
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476123"
---
# <a name="the-environment"></a>El entorno

Los desarrolladores que trabajan en aplicaciones para aplicaciones de 64 Windows encontrarán el entorno de desarrollo prácticamente idéntico al entorno de desarrollo para aplicaciones de 32 Windows. Las API existentes se han modificado cuando es necesario para permitirles reflejar la precisión de la plataforma en la que se ejecutan. El resultado es simplicidad y una curva de aprendizaje corta para el desarrollador: escribir código para archivos de 64 bits Windows es igual que escribir código para archivos de 32 Windows.

Los Windows de encabezado admiten nuevos tipos de datos que permiten que los punteros y las variables asociadas al puntero reflejen la precisión de la plataforma. Esto significa que los desarrolladores pueden compilar una base de origen única para ejecutarse de forma nativa en archivos de 32 Windows o de 64 Windows. Esta estrategia reduce el costo de desarrollar aplicaciones que aprovechan hardware de 64 bits, como procesadores AMD Opteron o Athlon64 o procesadores Intel Itanium.

Tendrá más tiempo para preparar las aplicaciones de 64 bits si adopta las nuevas convenciones de tipo de datos lo antes posible. Si va a cambiar el código, debe cambiar las definiciones de datos al mismo tiempo. Pruebe la aplicación en un Windows de 32 bits, ejecute el compilador de 64 bits (descrito en [Las](the-tools.md)herramientas) y la aplicación estará lista para probarse cuando tenga el hardware de 64 bits adecuado.

 

 




