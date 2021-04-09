---
title: Consideraciones sobre la programación de MGM
description: 'Al desarrollar clientes de administrador de grupo de multidifusión, siga las directrices siguientes:'
ms.assetid: 48451a76-81e0-4d60-acb3-c9ec55de32b4
keywords:
- Multidifusión, consideraciones de programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e442de1dcb2da5a8664648587a88f05feaee970
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903654"
---
# <a name="mgm-programming-considerations"></a>Consideraciones sobre la programación de MGM

Al desarrollar clientes de administrador de grupo de multidifusión, observe las siguientes directrices:

-   Las llamadas a funciones se deben realizar desde dentro del proceso del enrutador. Si se llama a las funciones desde otro proceso, sus resultados no serán válidos; el cliente no interactuará con el administrador del grupo de multidifusión.
-   Los clientes que usan la API MGM deben proporcionar su propia comprobación de errores, asegurándose de que solo se pasan datos válidos al administrador del grupo de multidifusión. Las funciones MGM no devuelven mensajes de error detallados sobre parámetros no válidos. el valor del parámetro de ERROR \_ no válido \_ se devuelve sin explicación.
-   Los clientes deben tener cuidado al utilizar los bloqueos mientras llaman a las funciones MGM. Si lo hace, puede evitar interbloqueos. Al llamar a las funciones MGM, los clientes no deben mantener los bloqueos que podrían mantenerse simultáneamente en una devolución de llamada del administrador del grupo de multidifusión.

 

 




