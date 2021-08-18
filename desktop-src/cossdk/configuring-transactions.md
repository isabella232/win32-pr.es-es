---
description: El atributo de transacción es una propiedad declarativa que administra automáticamente las transacciones para el desarrollador de componentes. Al establecer este atributo, se elimina la necesidad de usar controles de transacción explícitos en el componente.
ms.assetid: ea0e4d7e-2598-4a42-993c-58815f2fa138
title: Configuración de transacciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d613eb49a5f053b869e3efc90e04b9455644ea52acbaf651f33b00909e6e35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128897"
---
# <a name="configuring-transactions"></a>Configuración de transacciones

El *atributo de transacción* es una propiedad declarativa que administra automáticamente las transacciones para el desarrollador de componentes. Al establecer este atributo, se elimina la necesidad de usar controles de transacción explícitos en el componente.

COM+ usa el atributo de transacción del componente para determinar el tipo de protección de transacciones necesaria para cada objeto que activa. En función de sus requisitos, un objeto puede compartir la transacción de su autor de la llamada, requerir una nueva transacción o funcionar sin protección de transacciones.

COM+ proporciona los siguientes valores de atributo de transacción:

<dl> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>Deshabilitado
</dt> <dd>

En general, debe establecer este valor de atributo solo cuando esté seguro de que el componente nunca tiene acceso a un administrador de recursos. Al deshabilitar el atributo de transacción, COM+ omite los requisitos transaccionales del componente para determinar la ubicación de contexto del objeto. Como resultado, el objeto puede compartir el contexto (y la transacción) del autor de la llamada. Al migrar un componente COM a COM+, debe deshabilitar el atributo de transacción para mantener el mismo comportamiento transaccional que el componente COM no configurado.

> [!Note]  
> Un *componente no configurado es* un componente COM que no se ha instalado en una aplicación COM+.

 

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>No compatible
</dt> <dd>

Al establecer este valor de atributo, COM+ garantiza que ningún objeto creado a partir del componente nunca participa en una transacción, independientemente del estado transaccional de su autor de la llamada. Al declarar este valor, se asegura de que un objeto no vota en la transacción de su autor de la llamada ni puede iniciar una transacción propia. No compatible es el valor predeterminado para todos los componentes.

</dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>Apoyado
</dt> <dd>

Al establecer este valor de atributo, COM+ garantiza que cualquier objeto creado a partir del componente participa en una transacción si existe alguna. Este valor se declara cuando se desea que un objeto comparta la transacción de su autor de la llamada sin necesidad de una transacción propia.

</dd> <dt>

<span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>Obligatorio
</dt> <dd>

Al establecer este valor de atributo, COM+ garantiza que cualquier objeto creado a partir del componente sea transaccional. Cuando COM+ activa un objeto con la configuración Requerido, examina el estado transaccional de su autor de la llamada. Si el autor de la llamada tiene una transacción, el nuevo objeto se incluye en la transacción actual. De lo contrario, COM+ inicia una transacción, lo que hace que el nuevo objeto sea la raíz de la transacción. Esta es la configuración preferida para un componente que realiza actividades de recursos porque ayuda a proporcionar protección de transacciones para esas actividades.

</dd> <dt>

<span id="Requires_New"></span><span id="requires_new"></span><span id="REQUIRES_NEW"></span>Requiere nuevo
</dt> <dd>

Al establecer este valor de atributo, COM+ garantiza que los objetos creados a partir del componente deben participar en una nueva transacción como raíz de la transacción, independientemente del estado transaccional del autor de la llamada. COM+ inicia automáticamente una nueva transacción distinta de la transacción del autor de la llamada.

> [!Note]  
> COM+ no admite transacciones anidadas. Cuando un objeto transaccional llama a otro componente marcado como Requiere nuevo, COM+ crea un límite transaccional independiente para el objeto recién activado. La segunda transacción no puede afectar a la primera transacción a menos que la primera apunte explícitamente los resultados de la segunda transacción y modifique su voto en función de esos resultados.

 

</dd> </dl>

## <a name="transaction-attribute-dependencies"></a>Dependencias de atributo de transacción

En la tabla siguiente se muestran las características de cada valor de atributo de transacción COM+, incluido el efecto del valor en las características de transacción. COM+ aplica la activación [y sincronización JIT](com--just-in-time-activation.md) [para](com--synchronization.md) todos los componentes de transacción.



| Valor del atributo          | Nueva transacción   | Transacción del cliente                 | Raíz de transacción                        | Activación JIT      | Sincronización     |
|--------------------------|-------------------|--------------------------------------|-----------------------------------------|---------------------|---------------------|
| Disabled<br/>      | Nunca.<br/>  | Es posible<br/>                     | Nunca.<br/>                        | Opcional<br/> | Opcional<br/> |
| No compatible<br/> | Nunca<br/>  | Nunca<br/>                     | Nunca<br/>                        | Opcional<br/> | Opcional<br/> |
| Compatible<br/>     | Nunca.<br/>  | Si el cliente tiene transacción<br/> | Nunca.<br/>                        | Obligatorio<br/> | Obligatorio<br/> |
| Obligatorio<br/>      | Es posible<br/>  | Si el cliente tiene transacción<br/> | Si el cliente no tiene ninguna transacción<br/> | Obligatorio<br/> | Obligatorio<br/> |
| Se requiere nueva<br/>  | Siempre<br/> | Nunca.<br/>                     | Siempre<br/>                       | Obligatorio<br/> | Obligatorio<br/> |



 

## <a name="transaction-boundaries"></a>Límites de transacción

Una transacción tiene un principio, un final y se produce exactamente una vez. Durante su ejecución, una transacción puede llamar a en un recurso, como una base de datos o una cola, para realizar una o varias tareas. Cada recurso se encuentra dentro del límite *de transacción*. Todos los recursos dentro de un límite de transacción, que pueden abarcar varios límites de proceso y equipo, comparten una única transacción. Es importante administrar la coherencia a través de estos límites de proceso y equipo.

COM+ garantiza la coherencia mediante la administración automática de los límites de transacción, en función del valor del atributo de transacción que establezca para cada componente. Una transacción COM+ fluye automáticamente a los objetos a los que se indica que participen en una transacción y omite los objetos que se le indica que se ejecuten fuera de una transacción. COM+ no admite transacciones anidadas. En su lugar, las transacciones COM+ son distintas y de corta duración.

El primer objeto de un límite de transacción es especial para la transacción y se denomina el *objeto raíz* de la transacción. Solo puede haber un objeto raíz en una transacción. Todos los demás objetos de la jerarquía transaccional bajo el objeto raíz se denominan *objetos interiores.*

## <a name="mapping-transactions"></a>Transacciones de asignación

Una manera de asegurarse de que un objeto se incluye en el límite de transacción correcto es asignar las transacciones antes de empezar a escribir los componentes. Mediante la asignación de transacciones, puede determinar la mejor configuración para cada componente que escriba. Cuanto más seguro esté de cómo se usarán los componentes, más fácil será seleccionar el valor de atributo de transacción correcto.

En tiempo de ejecución, COM+ examina el atributo de transacción para determinar si un objeto debe ser la raíz de una nueva transacción, crearse en una transacción existente o crearse como un objeto no transaccional.

En la ilustración siguiente se muestra una posible asignación de transacciones. En la ilustración, el cliente crea el objeto 1, que requiere una transacción. Dado que no existe ninguna transacción, COM+ crea la transacción 1 y coloca el objeto 1 en ella como el objeto raíz. El objeto 1 crea el objeto 2, que admite transacciones y, por tanto, se coloca en la transacción 1. El objeto 2 crea el objeto 3, que no admite transacciones y, por tanto, se coloca fuera de todas las transacciones. El objeto 2 también crea el objeto 4, que requiere una transacción y, por tanto, se coloca en la transacción 1. El objeto 3 crea el objeto 5, que admite transacciones. Sin embargo, dado que el objeto 5 se crea mediante un objeto que no existe dentro de una transacción, también se coloca fuera de todas las transacciones. El objeto 4 crea el objeto 6, que requiere una nueva transacción, por lo que COM+ crea la transacción 2 y coloca el objeto 6 en él como el objeto raíz. El objeto 6 crea el objeto 7, que admite transacciones y, por tanto, se coloca en la transacción 2.

![Diagrama que muestra una interacción del cliente con la transacción 1 y la transacción 2.](images/fc7e2d03-94c2-40d9-a79b-1e05ca31dd80.png)

En la ilustración anterior se muestran dos posibles áreas problemáticas. En primer lugar, la mayoría del trabajo se divide entre dos transacciones distintas. Si se produce un error en la transacción 1 después de que el objeto 4 cree el objeto 6, la transacción 2 se ejecuta sin que el resultado de la transacción 1 se vería afectado. Si este resultado no es intencionado, es posible que prefiera plegar las operaciones de ambas transacciones en una sola transacción, lo que puede lograr cambiando el atributo de transacción del objeto 6 a Requerido.

En la ilustración de asignación también se muestra que el objeto 3 y el objeto 5 no son transaccionales y se ejecutan completamente fuera del ámbito de las transacciones 1 y 2. Si el objeto 5 actualiza los datos persistentes, puede que desee volver a considerar su estado no transaccional. El objeto 5 se puede colocar dentro de una transacción cambiando su atributo de transacción a Requerido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer el atributo de transacción](setting-the-transaction-attribute.md)
</dt> </dl>

 

 




