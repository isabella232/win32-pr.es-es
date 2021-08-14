---
description: Operaciones de administración de COM+ dentro de transacciones
ms.assetid: 832f2e6d-26ff-416e-a92e-ebaa33d4e7e5
title: Operaciones de administración de COM+ dentro de transacciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4182b143de38d838aea7c5aabd2d91bdb84f94480b2bed4c4441e204412ac834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308254"
---
# <a name="com-administration-operations-within-transactions"></a>Operaciones de administración de COM+ dentro de transacciones

La base de datos de registro com+ (RegDB) es un administrador de recursos con transacciones que puede participar en transacciones COM+. Esto le permite realizar operaciones de administración dentro de una transacción y hacer que todos los cambios de configuración se confirman o anulan como una operación atómica, incluso en varios equipos. En algunas circunstancias, puede ser muy beneficioso hacerlo, aunque hay un comportamiento de aislamiento y bloqueo que debe tener en cuenta, y realizar tareas de administración dentro de las transacciones implica pequeños cambios en el modelo de programación de administración normal.

## <a name="benefits-of-doing-administration-operations-within-transactions"></a>Ventajas de realizar operaciones de administración dentro de transacciones

-   **Coherencia de los datos:** Las operaciones de administración realizadas dentro de una transacción se confirman o anulan en su totalidad, aunque hay algunos recursos de catálogo com+ no transaccionales para los que puede que no sea el caso. (Vea Recursos del catálogo com+ no transaccional a continuación).
-   **Implementación coherente en varias máquinas:** Si va a implementar aplicaciones COM+ en varios servidores, puede garantizar que todos los servidores se quedan con configuraciones idénticas.
-   **Escalado y rendimiento:** Cuando se realizan varias operaciones dentro de una transacción, todas las escrituras en RegDB se realizan a la vez. Las escrituras persistentes en RegDB son una operación relativamente costosa; Si está realizando muchas escrituras en RegDB, puede obtener una gran ventaja de rendimiento al realizarlas todas a la vez en lugar de cada vez que llame a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges).

## <a name="isolation-behavior-of-regdb"></a>Comportamiento de aislamiento de RegDB

Para garantizar la coherencia adecuada de los datos y las transacciones serializables, RegDB aplica un comportamiento concreto de bloqueo y aislamiento cuando se realizan operaciones de administración dentro de las transacciones.

Cada vez que un componente que está realizando el trabajo dentro de una transacción llama a cualquier método que provocará una escritura en el catálogo de COM+, como [**SaveChanges,**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication)o [**InstallComponent,**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)se toma un bloqueo de escritor en el código del servidor de catálogo com+ que impedirá que otros escritores entren hasta que la transacción actual se confirme o anule. Es decir, los escritores solo pueden entrar si tienen la afinidad de transacción correcta y participan en la transacción actual.

Los lectores no están bloqueados. Sin embargo, los datos que ven los lectores no reflejan los cambios provisionales realizados dentro de la transacción hasta que esa transacción se confirma realmente. Todos los componentes que participan en esa transacción ven estados de datos provisionales cuando leen datos, pero todos los componentes fuera de la transacción solo ven esos cambios una vez completada la transacción.

## <a name="savechanges-behavior"></a>Comportamiento de SaveChanges

Para lograr el comportamiento de aislamiento descrito anteriormente, RegDB proporciona eficazmente una memoria caché sobre la que actúan los componentes de la transacción. Esto cambia el comportamiento del [**método SaveChanges.**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)

Normalmente, sin la presencia de una transacción, los cambios pendientes se escriben en el catálogo cuando se llama a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)y **SaveChanges** no se devuelve hasta que se completan todas las escrituras. Esto garantiza que si una llamada a **SaveChanges** se devuelve correctamente, puede llamar a [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) y activará la aplicación con datos nuevos.

Sin embargo, dentro de una transacción, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) solo afecta a la memoria caché, no a la propia RegDB, y **SaveChanges** devuelve inmediatamente si todos los cambios se han confirmado transaccionalmente en RegDB. No hay ninguna garantía de que [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) use datos nuevos posteriores a **la devolución de SaveChanges.** Si necesita llamar a **StartApplication** en este contexto, es aconsejable esperar un período de tiempo antes de hacerlo.

## <a name="transaction-time-out-period"></a>Período de Time-Out transacción

Si está realizando numerosas operaciones de administración dentro de una transacción, puede ser una transacción de larga duración. En este caso, el valor de tiempo de espera de la transacción puede ser un problema. Esto viene determinado por el valor de tiempo de espera de transacción establecido para el componente que inicia la transacción o por la configuración de tiempo de espera de todo el equipo para la máquina donde se ejecuta ese componente. Si está realizando numerosas operaciones dentro de una transacción, es aconsejable establecer el período de tiempo de espera de la transacción adecuado en un valor lo suficientemente largo y, si es necesario, restaurar la configuración original cuando haya terminado.

## <a name="non-transactional-com-catalog-resources"></a>Recursos de catálogo com+ no transaccionales

El Registro, el sistema de archivos y Windows instalador (MSI) son recursos de catálogo com+ que no son transaccionales.

> [!Note]  
> Si se produce un error que anula una transacción, es posible que los cambios en estos recursos no se revierte.

 

Si se produce un error al instalar una aplicación COM+ existente desde un archivo .msi, la aplicación no aparece en el complemento Servicios de componentes, pero puede aparecer en Agregar o quitar programas, en cuyo caso debe quitarla manualmente.

## <a name="recovering-in-the-event-of-system-hangs"></a>Recuperación en caso de que el sistema se desasocupe

Si un componente que realiza operaciones de administración dentro de una transacción se bloqueara mientras mantiene un bloqueo de escritura en el código del servidor de catálogo, impediría que todos los demás realizara cambios en el catálogo. En caso de que esto suceda, puede borrar el bloqueo en el catálogo apagando y reiniciando la aplicación Del sistema.

## <a name="scripting-with-a-transactioncontext-object"></a>Scripting con un objeto TransactionContext

Una manera sencilla de realizar operaciones de administración dentro de las transacciones es usar un [**objeto TransactionContext**](transactioncontext.md) para controlar la transacción. Por ejemplo, el siguiente script Visual Basic muestra cómo agregar transaccionalmente dos aplicaciones nuevas para que se cree tanto aplicaciones como ninguna aplicación:


```VB
Dim txctx
Dim cat
Dim apps
Dim app1
Dim app2
  
WScript.Echo "Starting"
Set txctx = CreateObject("TxCtx.TransactionContext")
Set cat = txctx.CreateInstance("COMAdmin.COMAdminCatalog")
Set apps = cat.GetCollection("Applications")
Set app1 = apps.Add
app1.Value("Name") = "Test App #1"
apps.SaveChanges
Set app2 = apps.Add
app2.Value("Name") = "Test App #2"
apps.SaveChanges
  
WScript.Echo "Ending"
txctx.Commit

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de errores de administración de COM+](handling-com--administration-errors.md)
</dt> <dt>

[Ejemplo introductorio de uso del catálogo de administración de COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Información general de los objetos COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Recuperación de colecciones en el catálogo de COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Establecimiento de propiedades y guardado de cambios en el catálogo de COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



