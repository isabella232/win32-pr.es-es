---
title: Códigos en FACILITY_ITF
description: Códigos en facil \_ ITF
ms.assetid: 1f9f7b2c-a4e4-41c0-9ba5-b8bbf722e077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc4375b5956502dbaee97057d347aff1da77e3a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994063"
---
# <a name="codes-in-facility_itf"></a>Códigos en facil \_ ITF

Los **resultados HRESULT** con recursos como Facility \_ y Facility \_ RPC tienen un significado universal porque se definen en un único origen: Microsoft. Sin embargo, los **HRESULT** s en \_ la utilidad ITF se determinan mediante la función o el método de interfaz desde el que se devuelven. Esto significa que el mismo valor de 32 bits en el \_ ITF de instalación devuelto de dos métodos de interfaz diferentes puede tener significados diferentes.

La razón por la que los **Valores HRESULT** de la utilidad \_ ITF pueden tener diferentes significados en distintas interfaces es que los **Valores HRESULT** se mantienen en un tamaño de tipo de datos eficaz de 32 bits. Desafortunadamente, 32 bits no es lo suficientemente grande como para el desarrollo de un sistema de asignación de códigos de error que evita los códigos en conflicto asignados por diferentes programadores en distintos momentos en distintos lugares (a diferencia del control de identificadores de interfaz y CLSIDs). Como resultado, el **HRESULT** de 32 bits está estructurado de modo que Microsoft pueda definir varios códigos de error universales, a la vez que permite que otros programadores definan nuevos códigos de error sin temor de conflicto. La Convención de código de estado es la siguiente:

-   Los códigos de estado de los servicios que no sean de \_ ITF solo pueden ser definidos por Microsoft.
-   Los códigos de estado de \_ la instalación de ITF se definen únicamente por el desarrollador de la interfaz o función que devuelve el código de estado. Para evitar conflictos de códigos de error, quien define la interfaz es responsable de coordinar y publicar los \_ códigos de estado ITF de las instalaciones asociadas a esa interfaz.

Todos los códigos ITF de la función definida por COM \_ tienen un valor de código en el intervalo de 0x0000-0x01FF. Aunque es legal usar cualquier código en \_ la ITF de servicio, se recomienda usar solo los valores de código en el intervalo de 0x0200-0xFFFF. Esta recomendación se realiza como un medio para reducir la confusión con los errores definidos por COM.

También se recomienda que los desarrolladores definan nuevas funciones e interfaces para devolver los códigos de error, tal y como se definen en COM y en otros medios distintos de la instalación de \_ ITF. En concreto, las interfaces que tienen la posibilidad de ser remotas con RPC en el futuro deben definir los códigos de RPC de los servicios \_ como válidos. E \_ inesperado es un código de error específico que la mayoría de los desarrolladores querrán convertir en universalmente legal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de errores en COM](error-handling-in-com.md)
</dt> </dl>

 

 




