---
title: Consideraciones de programación de MGM
description: Al desarrollar clientes de administrador de grupos de multidifusión, observe las siguientes directrices.
ms.assetid: 48451a76-81e0-4d60-acb3-c9ec55de32b4
keywords:
- Multidifusión, consideraciones de programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76a749406384068cc7dce54fab237c261926149aaf9b2fbdca23327c7b75f3d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029635"
---
# <a name="mgm-programming-considerations"></a>Consideraciones de programación de MGM

Al desarrollar clientes de administrador de grupos de multidifusión, observe las siguientes directrices:

-   Las llamadas de función deben realizarse desde dentro del proceso del enrutador. Si se llama a funciones desde otro proceso, sus resultados no serán válidos; el cliente no interactuará con el administrador de grupos de multidifusión.
-   Los clientes que usan la API de MGM deben proporcionar su propia comprobación de errores, lo que garantiza que solo se pasan datos válidos al administrador de grupos de multidifusión. Las funciones MGM no devuelven mensajes de error detallados sobre parámetros no válidos; El valor ERROR \_ INVALID PARAMETER se devuelve sin \_ explicación.
-   Los clientes deben tener cuidado al usar bloqueos al llamar a funciones MGM. Si lo hace, puede evitar interbloqueos. Al llamar a funciones MGM, los clientes no deben contener bloqueos que se puedan mantener simultáneamente en una devolución de llamada del administrador de grupos de multidifusión.

 

 




