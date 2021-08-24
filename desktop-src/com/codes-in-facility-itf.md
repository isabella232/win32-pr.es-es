---
title: Códigos en FACILITY_ITF
description: Códigos en FACILITY \_ ITF
ms.assetid: 1f9f7b2c-a4e4-41c0-9ba5-b8bbf722e077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2a16d051c352c353376865265c0451014f6110fbcde326914c3cc244a36223
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793795"
---
# <a name="codes-in-facility_itf"></a>Códigos en FACILITY \_ ITF

**Los HRESULT** con instalaciones como FACILITY NULL y FACILITY RPC tienen un significado universal porque se definen \_ en un único \_ origen: Microsoft. Sin embargo, **los HRESULT** de FACILITY ITF están determinados por la función o el método de interfaz \_ desde los que se devuelven. Esto significa que el mismo valor de 32 bits en FACILITY ITF devuelto por dos métodos de interfaz \_ diferentes podría tener significados diferentes.

El motivo por el que **los HRESULT** de FACILITY ITF pueden tener significados diferentes en distintas interfaces es que los HRESULT se mantienen en un tamaño de tipo de datos eficaz de \_ 32 bits. Desafortunadamente, 32 bits no son lo suficientemente grandes para el desarrollo de un sistema de asignación de código de error que evita códigos en conflicto asignados por distintos programadores en distintos momentos en distintos lugares (a diferencia del control de identificadores de interfaz y CLID). Como resultado, el **HRESULT** de 32 bits está estructurado de forma que Microsoft puede definir varios códigos de error universales, al tiempo que permite que otros programadores definan nuevos códigos de error sin miedo a conflictos. La convención de código de estado es la siguiente:

-   Microsoft solo puede definir códigos de estado en instalaciones que no sean FACILITY \_ ITF.
-   Los códigos de estado de facility FACILITY ITF los define únicamente el desarrollador de la interfaz o función \_ que devuelve el código de estado. Para evitar conflictos en los códigos de error, quien defina la interfaz es responsable de coordinar y publicar los códigos de estado DE ITF FACILITY \_ asociados a esa interfaz.

Todos los códigos ITF FACILITY definidos por COM tienen un valor de código en el intervalo de \_ 0x0000-0x01FF. Aunque es legal usar cualquier código en FACILITY ITF, se recomienda usar solo los valores de código del intervalo de \_ 0x0200-0xFFFF. Esta recomendación se realiza como un medio para reducir la confusión con los errores definidos por COM.

También se recomienda que los desarrolladores definan nuevas funciones e interfaces para devolver códigos de error definidos por COM y en instalaciones que no son FACILITY \_ ITF. En concreto, las interfaces que tienen cualquier posibilidad de ser remotas mediante RPC en el futuro deben definir los códigos RPC FACILITY \_ como legales. E UNEXPECTED es un código de error específico que la mayoría de \_ los desarrolladores querrá que sea universalmente legal.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de errores en COM](error-handling-in-com.md)
</dt> </dl>

 

 




