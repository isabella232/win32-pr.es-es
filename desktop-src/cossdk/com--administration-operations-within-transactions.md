---
description: Operaciones de administración de COM+ en transacciones
ms.assetid: 832f2e6d-26ff-416e-a92e-ebaa33d4e7e5
title: Operaciones de administración de COM+ en transacciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21612ffec1b9f082dc6a91861882a71f18fb07be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807970"
---
# <a name="com-administration-operations-within-transactions"></a>Operaciones de administración de COM+ en transacciones

La base de datos de registro de COM+ (RegDB) es un administrador de recursos de transacción que puede participar en transacciones de COM+. Esto le permite realizar operaciones de administración dentro de una transacción y hacer que todos los cambios de configuración se confirmen o se anulen como una operación atómica, incluso en varios equipos. En algunas circunstancias, puede resultar muy beneficioso hacerlo, aunque hay un comportamiento de aislamiento y bloqueo que debe tener en cuenta y realizar tareas de administración dentro de las transacciones implica pequeños cambios en el modelo de programación de administración normal.

## <a name="benefits-of-doing-administration-operations-within-transactions"></a>Ventajas de realizar operaciones de administración dentro de transacciones

-   **Coherencia de los datos:** Las operaciones de administración realizadas dentro de una transacción se confirman o anulan en conjunto, aunque hay algunos recursos de catálogo COM+ no transaccionales para los que puede que este no sea el caso. (Consulte a continuación los recursos de catálogo COM+ no transaccionales).
-   **Implementación coherente en varias máquinas:** Si va a implementar aplicaciones COM+ en varios servidores, puede garantizar que todos los servidores se quedan con configuraciones idénticas.
-   **Escalado y rendimiento:** Cuando se realizan varias operaciones en una transacción, todas las escrituras en RegDB se realizan a la vez. Las escrituras persistentes en RegDB son una operación relativamente costosa; Si va a realizar muchas operaciones de escritura en RegDB, puede obtener una ventaja de gran rendimiento al hacerlos todos a la vez en lugar de hacerlo cada vez que llame a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges).

## <a name="isolation-behavior-of-regdb"></a>Comportamiento de aislamiento de RegDB

Para garantizar la coherencia de datos y las transacciones serializables adecuadas, RegDB aplica un comportamiento de bloqueo y aislamiento determinado cuando se realizan operaciones de administración dentro de transacciones.

Cada vez que un componente que trabaja en una transacción llama a cualquier método que cause una escritura en el catálogo COM+, como [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication)o [**InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent), se realiza un bloqueo de escritor en el código del servidor de catálogo com+ que bloqueará la llegada de cualquier otro escritor hasta que la transacción actual se confirme o se anule. Es decir, los escritores solo pueden aparecer si tienen la afinidad de transacción correcta y están participando en la transacción actual.

Los lectores no se bloquean. Sin embargo, los datos que los lectores ven no reflejan ningún cambio provisional realizado dentro de la transacción hasta que la transacción se confirma realmente. Los componentes que participan en esa transacción ven los Estados de datos provisionales cuando leen los datos, pero todos los componentes ajenos a la transacción ven esos cambios solo después de que la transacción se haya completado.

## <a name="savechanges-behavior"></a>Comportamiento de SaveChanges

Para lograr el comportamiento de aislamiento descrito anteriormente, RegDB proporciona de forma eficaz una memoria caché a la que actúan los componentes de la transacción. Esto cambia el comportamiento del método [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) .

Normalmente, sin la presencia de una transacción, los cambios pendientes se escriben en el catálogo cuando se llama a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)y **SaveChanges** no devuelve hasta que se completen todas las operaciones de escritura. Esto garantiza que si una llamada a **SaveChanges** se devuelve correctamente, puede llamar a [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) y activará la aplicación con datos nuevos.

Sin embargo, en una transacción, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) solo afecta a la memoria caché, no al propio RegDB, y **SaveChanges** devuelve inmediatamente si todos los cambios se han confirmado de manera transaccional a RegDB. No hay ninguna garantía de que [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) esté usando datos nuevos posteriores a la devolución de **SaveChanges** . Si necesita llamar a **StartApplication** en este contexto, es aconsejable esperar durante un período de tiempo antes de hacerlo.

## <a name="transaction-time-out-period"></a>Período de Time-Out de transacción

Si está realizando numerosas operaciones de administración dentro de una transacción, puede ser una transacción de larga ejecución. En este caso, el valor de tiempo de espera de la transacción puede ser un problema. Esto viene determinado por el valor de tiempo de espera de la transacción establecido para el componente que inicia la transacción o por la configuración de tiempo de espera de todo el equipo para el equipo en el que se ejecuta el componente. Si está realizando numerosas operaciones dentro de una transacción, es aconsejable establecer el período de tiempo de espera de la transacción adecuado en un valor suficientemente largo y, si es necesario, restaurar el valor original cuando haya terminado.

## <a name="non-transactional-com-catalog-resources"></a>Recursos del catálogo COM+ no transaccional

El registro, el sistema de archivos y Windows Installer (MSI) son recursos del catálogo COM+ que no son transaccionales.

> [!Note]  
> Si se produce un error que anula una transacción, es posible que no se reviertan los cambios realizados en estos recursos.

 

Si se produce un error al instalar una aplicación COM+ existente desde un archivo. msi, la aplicación no aparecerá en el complemento Servicios de componentes, pero podría aparecer en Agregar o quitar programas, en cuyo caso tendrá que quitarla manualmente.

## <a name="recovering-in-the-event-of-system-hangs"></a>Recuperación en caso de que el sistema se bloquee

Si un componente que realiza operaciones de administración dentro de una transacción tuviera que responder mientras contiene un bloqueo de escritor en el código del servidor de catálogo, bloquearía a todos los demás usuarios de realizar cambios en el catálogo. Si esto ocurre, puede desactivar el bloqueo en el catálogo cerrando y reiniciando la aplicación del sistema.

## <a name="scripting-with-a-transactioncontext-object"></a>Scripting con un objeto TransactionContext

Una manera sencilla de realizar operaciones de administración dentro de las transacciones es usar un objeto [**TransactionContext**](transactioncontext.md) para controlar la transacción. Por ejemplo, el siguiente script de Visual Basic muestra cómo agregar de forma transaccional dos nuevas aplicaciones para que se creen ambas aplicaciones o ninguna de ellas:


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

[Ejemplo introductorio con el catálogo de administración de COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Información general de los objetos COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Recuperar recopilaciones en el catálogo de COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Establecer propiedades y guardar cambios en el catálogo de COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



