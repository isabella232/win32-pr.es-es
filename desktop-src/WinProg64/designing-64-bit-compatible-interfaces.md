---
title: Diseño de interfaces compatibles con 64 bits
description: Los problemas de compatibilidad con versiones anteriores surgen cuando se agregan nuevos tipos de datos o métodos a una interfaz, se cambian los tipos de datos antiguos o se usan los tipos de datos de forma inadecuada.
ms.assetid: 676affd8-a155-4ac2-9647-0c7352c87a31
keywords:
- compatibilidad con versiones anteriores de 64 bits programación de Windows
- interfaces compatibles con 64 bits de programación de Windows de 64 bits
- Guía de programación de Windows de 64 bits, programación de Windows de 64 bits, compatibilidad
- compatibilidad con la programación de Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebcde0e621d35cf216c2191f2e4b7da624dc274
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357056"
---
# <a name="designing-64-bit-compatible-interfaces"></a>Diseño de interfaces compatibles con 64 bits

La migración de Windows de 32 bits a Windows de 64 bits no debe, por sí misma, crear problemas para las aplicaciones distribuidas, independientemente de si usan llamadas a procedimiento remoto (RPC) directamente o a través de DCOM. El modelo de programación RPC especifica tamaños de datos bien definidos y tipos enteros que tienen el mismo tamaño en cada extremo de la conexión. Además, en el modelo de datos Abstract LLP64 desarrollado para Windows de 64 bits, solo los punteros se expanden a 64 bits, todos los demás tipos de datos enteros siguen siendo 32 bits. Dado que los punteros son locales para cada lado de la conexión cliente/servidor y normalmente se transmiten como marcadores **nulos** o no **nulos** , el motor de serialización puede administrar distintos tamaños de puntero en cualquier extremo de una conexión de forma transparente.

Sin embargo, surgen problemas de compatibilidad con versiones anteriores cuando se agregan nuevos tipos de datos o métodos a una interfaz, se cambian los tipos de datos antiguos o se usan los tipos de datos de forma inadecuada. En los temas siguientes se explica cómo evitar estas situaciones (cuando sea posible) y cómo diseñar soluciones sólidas cuando no es posible evitarlas.

## <a name="in-this-section"></a>En esta sección

-   [Cambiar una interfaz existente](changing-an-existing-interface.md)
-   [Evitar la ocultación de información](avoiding-information-hiding.md)
-   [Evitar el polimorfismo](avoiding-polymorphism.md)
-   [Usar nuevos tipos de datos en el archivo IDL](using-new-data-types-in-your-idl-file.md)
-   [Preparación de la aplicación para Windows de 64 bits](preparing-your-application-for-64-bit-windows.md)

## <a name="related-sections"></a>Secciones relacionadas

Si no está familiarizado con los nuevos tipos de datos, el entorno de trabajo y los cambios de API para Windows de 64 bits, consulte [preparación para Windows de 64](getting-ready-for-64-bit-windows.md)bits.

 

 




