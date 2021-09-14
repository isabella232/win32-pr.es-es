---
description: Cuando un objeto se activa en un contexto determinado, las llamadas posteriores a o desde él, dentro del contexto, se controlan de forma diferente que las llamadas a través del límite de contexto.
ms.assetid: 9e234b41-f269-4674-adc4-12018277a14b
title: Interceptación de llamadas entre contextos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d70bc8bff83d02b13656f9854f0e6d16cd4e173
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168538"
---
# <a name="interception-of-cross-context-calls"></a>Interceptación de llamadas entre contextos

Cuando un objeto se activa en un contexto determinado, las llamadas posteriores a o desde él, dentro del contexto, se controlan de forma diferente que las llamadas a través del límite de contexto. Las llamadas a través del límite de contexto se controlan con servidores proxy ligeros. Estos servidores proxy controlan cualquier mediación necesaria para ajustar el entorno en tiempo de ejecución de uno que aloje al autor de la llamada a uno que aloje al destinatario. Este proceso se conoce como *interceptación.*

La interceptación de llamadas entre contextos es necesaria porque los objetos de contextos diferentes tienen requisitos en tiempo de ejecución diferentes; este es precisamente el motivo de los contextos. COM+ intercepta las referencias de objeto que se pasan como parámetros de método y las convierte automáticamente en servidores proxy para que se puedan usar en el nuevo contexto.

Si comparte referencias de objeto a través de los límites de contexto por otros medios (por ejemplo, en variables globales), siempre debe usar [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) y [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface). Estas funciones pueden traducir una referencia de objeto en un proxy que se puede usar en un contexto diferente. Nunca comparta una referencia de objeto sin formato entre los límites de contexto.

El comportamiento de las llamadas a través del contexto puede tener consecuencias no deseadas en el caso de objetos que exponen interfaces que no se pueden serializar. En esta circunstancia, es probable que quiera insotar que el objeto que no se puede serializar solo se active en el contexto de su autor de la llamada y nunca en su propio contexto. Para ello, seleccione la opción Must **be activated in caller's context** (Debe activarse en el contexto del autor de la llamada) en la pestaña Activación de la página Propiedades  **del** componente. (Consulte [Aplicación de la activación en el](enforcing-activation-in-the-caller-s-context.md) contexto del autor de la llamada para obtener instrucciones paso a paso).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Activación de contexto](context-activation.md)
</dt> </dl>

 

 
