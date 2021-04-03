---
title: El entorno
description: Los desarrolladores que trabajan en aplicaciones para Windows de 64 bits encontrarán el entorno de desarrollo prácticamente idéntico al entorno de desarrollo de Windows de 32 bits.
ms.assetid: 49b2b952-f771-4721-a9b0-01eb67a98007
keywords:
- entorno de desarrollo de 64 programación de Windows de bits
- 'entorno de 64: programación de Windows de bits'
- Guía de programación de Windows de 64 bits guía de programación de Windows de 64 bits, entorno de desarrollo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104ea1bdacbb478eaa0abcf46d04c3d772540f26
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075391"
---
# <a name="the-environment"></a>El entorno

Los desarrolladores que trabajan en aplicaciones para Windows de 64 bits encontrarán el entorno de desarrollo prácticamente idéntico al entorno de desarrollo de Windows de 32 bits. Las API existentes se han modificado cuando sea necesario para que reflejen la precisión de la plataforma en la que se ejecutan. El resultado es una simplicidad y una curva de aprendizaje breve para el desarrollador; escribir código para Windows de 64 bits es igual que escribir código para Windows de 32 bits.

Los archivos de encabezado de Windows admiten nuevos tipos de datos que permiten que los punteros y las variables asociadas a puntero reflejen la precisión de la plataforma. Esto significa que los desarrolladores pueden compilar una base de origen única para ejecutarse de forma nativa en Windows de 32 bits o en Windows de 64 bits. Esta estrategia reduce el costo del desarrollo de aplicaciones que aprovechan el hardware de 64 bits, como procesadores AMD Opteron o Athlon64 o procesadores Intel Itanium.

Tendrá más tiempo para que las aplicaciones 64 de bits estén listas si adopta las nuevas convenciones de tipos de datos lo antes posible. Si va a cambiar el código, debe cambiar las definiciones de datos al mismo tiempo. Pruebe la aplicación en Windows de 32 bits, ejecútela a través del compilador de 64 bits (descrito en [las herramientas](the-tools.md)) y la aplicación estará lista para probarse cuando tenga el hardware de 64 bits adecuado.

 

 




