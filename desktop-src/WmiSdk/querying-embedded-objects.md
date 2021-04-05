---
description: Tiene varias opciones para el formulario que realiza una consulta al consultar una clase de eventos que contiene objetos incrustados. Los resultados devueltos por la consulta varían en función del formulario de la consulta que use.
ms.assetid: b959a695-be15-4aa7-9368-b840962ae0da
ms.tgt_platform: multiple
title: Consultar objetos incrustados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed2e13bd9d9dc798891a723a6fed1b1734e1735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812440"
---
# <a name="querying-embedded-objects"></a>Consultar objetos incrustados

Tiene varias opciones para el formulario que realiza una consulta al consultar una clase de eventos que contiene objetos incrustados. Los resultados devueltos por la consulta varían en función del formulario de la consulta que use.

## <a name="class-definitions"></a>Definiciones de clase

En el siguiente ejemplo se muestran las definiciones de clase que se utilizan para las consultas WQL de este tema.

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

La consulta siguiente devuelve las clases incrustadas, **E1** y **E2**, cada una con **Prop1** y **Prop2** rellenados con datos.

`SELECT * FROM MyEvent`

La siguiente consulta devuelve el objeto de **E1** incrustado, pero no se ha rellenado con datos ni con **Prop1** ni **Prop2** .

`SELECT E1 FROM MyEvent`

La consulta siguiente devuelve la clase incrustada **E1** con solo **Prop1** rellenado con datos.

`SELECT E1.Prop1 FROM MyEvent`

La consulta siguiente devuelve las clases incrustadas, **E1** y **E2**, cada una con **Prop1** y **Prop2** rellenados con datos.

`ELECT E1.Prop1, E1.Prop2, E2.Prop1, E2.Prop2 FROM MyEvent`

Esto es equivalente a la primera consulta que usa el asterisco ( \* ) en lugar de especificar cada objeto y propiedad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Realizar consultas con WQL](querying-with-wql.md)
</dt> </dl>

 

 



