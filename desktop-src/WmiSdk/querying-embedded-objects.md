---
description: Tiene varias opciones en cuanto al formulario que toma una consulta al consultar una clase de eventos que contiene objetos incrustados. Los resultados devueltos por la consulta varían en función del formato de la consulta que use.
ms.assetid: b959a695-be15-4aa7-9368-b840962ae0da
ms.tgt_platform: multiple
title: Consulta de objetos incrustados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7af6e0933ae12bb5867ff2ad446928d1b55f5ee7c2022ec60f53de61a3bd4bb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130917"
---
# <a name="querying-embedded-objects"></a>Consulta de objetos incrustados

Tiene varias opciones en cuanto al formulario que toma una consulta al consultar una clase de eventos que contiene objetos incrustados. Los resultados devueltos por la consulta varían en función del formato de la consulta que use.

## <a name="class-definitions"></a>Definiciones de clase

En el ejemplo siguiente se muestran las definiciones de clase que se usan para las consultas WQL de este tema.

``` syntax
class MyClass
{
   string Prop1;
   string Prop2;
};

class MyEvent : __ExtrinsicEvent
{
   MyClass E1;
   MyClass E2;
};
```

## <a name="examples"></a>Ejemplos

La consulta siguiente devuelve ambas clases incrustadas, **E1** y **E2,** cada una con **Prop1** y **Prop2** rellenadas con datos.

`SELECT * FROM MyEvent`

La consulta siguiente devuelve el **objeto incrustado E1,** pero no con **Prop1** ni **Prop2** rellenados con datos.

`SELECT E1 FROM MyEvent`

La consulta siguiente devuelve la clase **incrustada E1** con **solo Prop1** rellenado con datos.

`SELECT E1.Prop1 FROM MyEvent`

La consulta siguiente devuelve ambas clases incrustadas, **E1** y **E2,** cada una con **Prop1** y **Prop2** rellenadas con datos.

`ELECT E1.Prop1, E1.Prop2, E2.Prop1, E2.Prop2 FROM MyEvent`

Esto es equivalente a la primera consulta que usa el asterisco ( ) en \* lugar de especificar cada objeto y propiedad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consulta con WQL](querying-with-wql.md)
</dt> </dl>

 

 



