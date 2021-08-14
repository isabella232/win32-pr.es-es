---
title: E (RPC)
description: Palabras que comienzan por E en el glosario de llamada a procedimiento remoto (RPC).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 76e35c3c-91dd-42e3-9699-6767e37b2699
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df69c06e72a84207cffd7c708cea3673a3cb33e2d6eea477024a7c66963b3878
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930532"
---
# <a name="e-rpc"></a>E (RPC)

[A](a-glos.md) [B](b-glos.md) [C](c-glos.md) [D](d-glos.md) E [F](f-glos.md) G H [I](i-glos.md) J K L [M](l-glos.md) [N](m-glos.md) [](n-glos.md) [O](o-glos.md) [P P](p-glos.md) [Q](q.md) [R](r-glos.md) [S](s-glos.md) [T](t-glos.md) [U](u-glos.md) [V](v-glos.md) [W](w-glos.md) X Y Z

<dl> <dt>

<span id="_rpc_embedded_pointer_glos"></span><span id="_RPC_EMBEDDED_POINTER_GLOS"></span>**puntero incrustado**
</dt> <dd>

Puntero incrustado en un parámetro que es una estructura de datos, como una matriz, una estructura o una unión. Vea también [*puntero de nivel superior*](t-glos.md).

</dd> <dt>

<span id="_rpc_encoding_services_glos"></span><span id="_RPC_ENCODING_SERVICES_GLOS"></span>**servicios de codificación**
</dt> <dd>

Rutinas de código auxiliar generadas por MIDL que proporcionan compatibilidad con la codificación y la codificación de datos (también conocidas como selección *o* *serialización).* Permitir a los programadores controlar los búferes que contienen datos que se deben serializar y desmarshalar. Vea también [*serialización de tipos*](t-glos.md), [*serialización de procedimientos.*](p-glos.md)

</dd> <dt>

<span id="_rpc_endpoint_glos"></span><span id="_RPC_ENDPOINT_GLOS"></span>**Extremo**
</dt> <dd>

Dirección específica de red de un proceso de servidor para llamadas a procedimiento remoto. El nombre real del punto de conexión depende de la secuencia de protocolo que se esté utilizando. Consulte también punto [*de conexión dinámico*](d-glos.md) y punto de conexión [*conocido.*](w-glos.md)

</dd> <dt>

<span id="_rpc_endpoint_mapper_glos"></span><span id="_RPC_ENDPOINT_MAPPER_GLOS"></span>**asignador de puntos de conexión**
</dt> <dd>

Parte del subsistema RPC (RPCSS) que permite a la biblioteca en tiempo de ejecución asignar y resolver puntos de conexión dinámicamente. Consulte también el [punto de conexión](/windows).

</dd> <dt>

<span id="_rpc_encapsulated_union_glos"></span><span id="_RPC_ENCAPSULATED_UNION_GLOS"></span>**unión encapsulada**
</dt> <dd>

Construcción MIDL que permite pasar uniones como parte de una llamada a procedimiento remoto insertando la unión en una estructura en la que el discriminador es el primer campo de la estructura y la unión es el segundo (y último) campo de la estructura. El modificador de palabra **clave** [*IDL*](i-glos.md) especifica que se encapsula una unión. Vea también [*nonencapsulated union*](n-glos.md).

</dd> <dt>

<span id="_rpc_epv_glos"></span><span id="_RPC_EPV_GLOS"></span>**vector de punto de entrada (EPV)**
</dt> <dd>

Matriz de punteros a funciones que implementan las operaciones especificadas en la interfaz . Cada elemento de la matriz corresponde a una función definida en el archivo IDL. Los vectores de punto de entrada permiten que las aplicaciones distribuidas admitan más de una implementación de las funciones definidas en el archivo IDL.

</dd> </dl>

 

 
