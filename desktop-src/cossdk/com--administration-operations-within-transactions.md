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
# <a name="com-administration-operations-within-transactions"></a><span data-ttu-id="c36d3-103">Operaciones de administración de COM+ en transacciones</span><span class="sxs-lookup"><span data-stu-id="c36d3-103">COM+ Administration Operations Within Transactions</span></span>

<span data-ttu-id="c36d3-104">La base de datos de registro de COM+ (RegDB) es un administrador de recursos de transacción que puede participar en transacciones de COM+.</span><span class="sxs-lookup"><span data-stu-id="c36d3-104">The COM+ registration database (RegDB) is a transacted resource manager that can participate in COM+ transactions.</span></span> <span data-ttu-id="c36d3-105">Esto le permite realizar operaciones de administración dentro de una transacción y hacer que todos los cambios de configuración se confirmen o se anulen como una operación atómica, incluso en varios equipos.</span><span class="sxs-lookup"><span data-stu-id="c36d3-105">This enables you to perform administration operations within a transaction and have all configuration changes committed or aborted as an atomic operation, even across multiple computers.</span></span> <span data-ttu-id="c36d3-106">En algunas circunstancias, puede resultar muy beneficioso hacerlo, aunque hay un comportamiento de aislamiento y bloqueo que debe tener en cuenta y realizar tareas de administración dentro de las transacciones implica pequeños cambios en el modelo de programación de administración normal.</span><span class="sxs-lookup"><span data-stu-id="c36d3-106">In some circumstances, it can be very beneficial to do this, although there is isolation and blocking behavior that you should take into account, and performing administration tasks within transactions does involve slight changes to the normal administration programming model.</span></span>

## <a name="benefits-of-doing-administration-operations-within-transactions"></a><span data-ttu-id="c36d3-107">Ventajas de realizar operaciones de administración dentro de transacciones</span><span class="sxs-lookup"><span data-stu-id="c36d3-107">Benefits of Doing Administration Operations Within Transactions</span></span>

-   <span data-ttu-id="c36d3-108">**Coherencia de los datos:** Las operaciones de administración realizadas dentro de una transacción se confirman o anulan en conjunto, aunque hay algunos recursos de catálogo COM+ no transaccionales para los que puede que este no sea el caso.</span><span class="sxs-lookup"><span data-stu-id="c36d3-108">**Consistency of data—** Administration operations performed within a transaction are committed or aborted as a whole, although there are some non-transactional COM+ catalog resources for which this may not be the case.</span></span> <span data-ttu-id="c36d3-109">(Consulte a continuación los recursos de catálogo COM+ no transaccionales).</span><span class="sxs-lookup"><span data-stu-id="c36d3-109">(See Non-Transactional COM+ Catalog Resources below.)</span></span>
-   <span data-ttu-id="c36d3-110">**Implementación coherente en varias máquinas:** Si va a implementar aplicaciones COM+ en varios servidores, puede garantizar que todos los servidores se quedan con configuraciones idénticas.</span><span class="sxs-lookup"><span data-stu-id="c36d3-110">**Consistent deployment across multiple machines—** If you are deploying COM+ applications across multiple servers, you can guarantee that all servers are left with identical configurations.</span></span>
-   <span data-ttu-id="c36d3-111">**Escalado y rendimiento:** Cuando se realizan varias operaciones en una transacción, todas las escrituras en RegDB se realizan a la vez.</span><span class="sxs-lookup"><span data-stu-id="c36d3-111">**Scaling and performance—** When you do multiple operations within a transaction, all writes to RegDB are performed at once.</span></span> <span data-ttu-id="c36d3-112">Las escrituras persistentes en RegDB son una operación relativamente costosa; Si va a realizar muchas operaciones de escritura en RegDB, puede obtener una ventaja de gran rendimiento al hacerlos todos a la vez en lugar de hacerlo cada vez que llame a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges).</span><span class="sxs-lookup"><span data-stu-id="c36d3-112">Persisted writes to RegDB are a relatively expensive operation; if you are making many writes to RegDB, you can get a big performance benefit from doing them all at once instead of every time you call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges).</span></span>

## <a name="isolation-behavior-of-regdb"></a><span data-ttu-id="c36d3-113">Comportamiento de aislamiento de RegDB</span><span class="sxs-lookup"><span data-stu-id="c36d3-113">Isolation Behavior of RegDB</span></span>

<span data-ttu-id="c36d3-114">Para garantizar la coherencia de datos y las transacciones serializables adecuadas, RegDB aplica un comportamiento de bloqueo y aislamiento determinado cuando se realizan operaciones de administración dentro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="c36d3-114">To ensure proper data consistency and serializable transactions, RegDB enforces particular blocking and isolation behavior when administration operations are being performed within transactions.</span></span>

<span data-ttu-id="c36d3-115">Cada vez que un componente que trabaja en una transacción llama a cualquier método que cause una escritura en el catálogo COM+, como [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication)o [**InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent), se realiza un bloqueo de escritor en el código del servidor de catálogo com+ que bloqueará la llegada de cualquier otro escritor hasta que la transacción actual se confirme o se anule.</span><span class="sxs-lookup"><span data-stu-id="c36d3-115">Whenever a component that is doing work within a transaction calls any method that will cause a write to the COM+ catalog—such as [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication), or [**InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)—a writer lock is taken on COM+ catalog server code that will block any other writers from coming in until the current transaction commits or aborts.</span></span> <span data-ttu-id="c36d3-116">Es decir, los escritores solo pueden aparecer si tienen la afinidad de transacción correcta y están participando en la transacción actual.</span><span class="sxs-lookup"><span data-stu-id="c36d3-116">That is, writers can come in only if they have the correct transaction affinity and are participating in the current transaction.</span></span>

<span data-ttu-id="c36d3-117">Los lectores no se bloquean.</span><span class="sxs-lookup"><span data-stu-id="c36d3-117">Readers are not blocked.</span></span> <span data-ttu-id="c36d3-118">Sin embargo, los datos que los lectores ven no reflejan ningún cambio provisional realizado dentro de la transacción hasta que la transacción se confirma realmente.</span><span class="sxs-lookup"><span data-stu-id="c36d3-118">However, the data that readers see does not reflect any interim changes made within the transaction until that transaction actually commits.</span></span> <span data-ttu-id="c36d3-119">Los componentes que participan en esa transacción ven los Estados de datos provisionales cuando leen los datos, pero todos los componentes ajenos a la transacción ven esos cambios solo después de que la transacción se haya completado.</span><span class="sxs-lookup"><span data-stu-id="c36d3-119">Any components participating in that transaction sees interim data states when they read data, but all components outside the transaction see those changes only after the transaction has completed.</span></span>

## <a name="savechanges-behavior"></a><span data-ttu-id="c36d3-120">Comportamiento de SaveChanges</span><span class="sxs-lookup"><span data-stu-id="c36d3-120">SaveChanges Behavior</span></span>

<span data-ttu-id="c36d3-121">Para lograr el comportamiento de aislamiento descrito anteriormente, RegDB proporciona de forma eficaz una memoria caché a la que actúan los componentes de la transacción.</span><span class="sxs-lookup"><span data-stu-id="c36d3-121">To achieve the isolation behavior described above, RegDB effectively provides a cache that is acted on by components within the transaction.</span></span> <span data-ttu-id="c36d3-122">Esto cambia el comportamiento del método [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) .</span><span class="sxs-lookup"><span data-stu-id="c36d3-122">This changes the behavior of the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method.</span></span>

<span data-ttu-id="c36d3-123">Normalmente, sin la presencia de una transacción, los cambios pendientes se escriben en el catálogo cuando se llama a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)y **SaveChanges** no devuelve hasta que se completen todas las operaciones de escritura.</span><span class="sxs-lookup"><span data-stu-id="c36d3-123">Normally, without the presence of a transaction, any pending changes are written to the catalog when you call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), and **SaveChanges** doesn't return until all writes are completed.</span></span> <span data-ttu-id="c36d3-124">Esto garantiza que si una llamada a **SaveChanges** se devuelve correctamente, puede llamar a [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) y activará la aplicación con datos nuevos.</span><span class="sxs-lookup"><span data-stu-id="c36d3-124">This guarantees that if a call to **SaveChanges** returns successfully, you can call [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) and it will activate the application with fresh data.</span></span>

<span data-ttu-id="c36d3-125">Sin embargo, en una transacción, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) solo afecta a la memoria caché, no al propio RegDB, y **SaveChanges** devuelve inmediatamente si todos los cambios se han confirmado de manera transaccional a RegDB.</span><span class="sxs-lookup"><span data-stu-id="c36d3-125">However, within a transaction, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) affects only the cache, not the RegDB itself, and **SaveChanges** returns immediately whether all changes have been transactionally committed to RegDB.</span></span> <span data-ttu-id="c36d3-126">No hay ninguna garantía de que [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) esté usando datos nuevos posteriores a la devolución de **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="c36d3-126">There is no guarantee that [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) is using fresh data subsequent to **SaveChanges** returning.</span></span> <span data-ttu-id="c36d3-127">Si necesita llamar a **StartApplication** en este contexto, es aconsejable esperar durante un período de tiempo antes de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="c36d3-127">If you need to call **StartApplication** in this context, it is advisable to wait for some period of time before doing so.</span></span>

## <a name="transaction-time-out-period"></a><span data-ttu-id="c36d3-128">Período de Time-Out de transacción</span><span class="sxs-lookup"><span data-stu-id="c36d3-128">Transaction Time-Out Period</span></span>

<span data-ttu-id="c36d3-129">Si está realizando numerosas operaciones de administración dentro de una transacción, puede ser una transacción de larga ejecución.</span><span class="sxs-lookup"><span data-stu-id="c36d3-129">If you are doing numerous administration operations within a transaction, it may be a long running transaction.</span></span> <span data-ttu-id="c36d3-130">En este caso, el valor de tiempo de espera de la transacción puede ser un problema.</span><span class="sxs-lookup"><span data-stu-id="c36d3-130">In this case, the transaction time-out value can be an issue.</span></span> <span data-ttu-id="c36d3-131">Esto viene determinado por el valor de tiempo de espera de la transacción establecido para el componente que inicia la transacción o por la configuración de tiempo de espera de todo el equipo para el equipo en el que se ejecuta el componente.</span><span class="sxs-lookup"><span data-stu-id="c36d3-131">This is determined either by the transaction time-out value set for the component initiating the transaction or by the machine-wide time-out setting for the machine where that component is running.</span></span> <span data-ttu-id="c36d3-132">Si está realizando numerosas operaciones dentro de una transacción, es aconsejable establecer el período de tiempo de espera de la transacción adecuado en un valor suficientemente largo y, si es necesario, restaurar el valor original cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="c36d3-132">If you are doing numerous operations within a transaction, it is advisable to set the appropriate transaction time-out period to a sufficiently long value and, if necessary, to restore the original setting when you are finished.</span></span>

## <a name="non-transactional-com-catalog-resources"></a><span data-ttu-id="c36d3-133">Recursos del catálogo COM+ no transaccional</span><span class="sxs-lookup"><span data-stu-id="c36d3-133">Non-Transactional COM+ Catalog Resources</span></span>

<span data-ttu-id="c36d3-134">El registro, el sistema de archivos y Windows Installer (MSI) son recursos del catálogo COM+ que no son transaccionales.</span><span class="sxs-lookup"><span data-stu-id="c36d3-134">The registry, the file system, and Windows Installer (MSI) are COM+ catalog resources that are not transactional.</span></span>

> [!Note]  
> <span data-ttu-id="c36d3-135">Si se produce un error que anula una transacción, es posible que no se reviertan los cambios realizados en estos recursos.</span><span class="sxs-lookup"><span data-stu-id="c36d3-135">If there is an error that aborts a transaction, changes to these resources may not be rolled back.</span></span>

 

<span data-ttu-id="c36d3-136">Si se produce un error al instalar una aplicación COM+ existente desde un archivo. msi, la aplicación no aparecerá en el complemento Servicios de componentes, pero podría aparecer en Agregar o quitar programas, en cuyo caso tendrá que quitarla manualmente.</span><span class="sxs-lookup"><span data-stu-id="c36d3-136">If there is an error while installing an existing COM+ application from an .msi file, the application doesn't appear in the Component Services snap-in but it might appear in Add/Remove programs, in which case you need to manually remove it.</span></span>

## <a name="recovering-in-the-event-of-system-hangs"></a><span data-ttu-id="c36d3-137">Recuperación en caso de que el sistema se bloquee</span><span class="sxs-lookup"><span data-stu-id="c36d3-137">Recovering in the Event of System Hangs</span></span>

<span data-ttu-id="c36d3-138">Si un componente que realiza operaciones de administración dentro de una transacción tuviera que responder mientras contiene un bloqueo de escritor en el código del servidor de catálogo, bloquearía a todos los demás usuarios de realizar cambios en el catálogo.</span><span class="sxs-lookup"><span data-stu-id="c36d3-138">If a component doing administration operations within a transaction were to hang while it holds a writer lock on the catalog server code, it would block everyone else from making any changes to the catalog.</span></span> <span data-ttu-id="c36d3-139">Si esto ocurre, puede desactivar el bloqueo en el catálogo cerrando y reiniciando la aplicación del sistema.</span><span class="sxs-lookup"><span data-stu-id="c36d3-139">Should this happen, you can clear the lock on the catalog by shutting down and restarting the System application.</span></span>

## <a name="scripting-with-a-transactioncontext-object"></a><span data-ttu-id="c36d3-140">Scripting con un objeto TransactionContext</span><span class="sxs-lookup"><span data-stu-id="c36d3-140">Scripting with a TransactionContext Object</span></span>

<span data-ttu-id="c36d3-141">Una manera sencilla de realizar operaciones de administración dentro de las transacciones es usar un objeto [**TransactionContext**](transactioncontext.md) para controlar la transacción.</span><span class="sxs-lookup"><span data-stu-id="c36d3-141">A simple way to do administration operations within transactions is to use a [**TransactionContext**](transactioncontext.md) object to control the transaction.</span></span> <span data-ttu-id="c36d3-142">Por ejemplo, el siguiente script de Visual Basic muestra cómo agregar de forma transaccional dos nuevas aplicaciones para que se creen ambas aplicaciones o ninguna de ellas:</span><span class="sxs-lookup"><span data-stu-id="c36d3-142">For example, the following Visual Basic script demonstrates how to transactionally add two new applications so that either both applications or neither application is created:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c36d3-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c36d3-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c36d3-144">Control de errores de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="c36d3-144">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="c36d3-145">Ejemplo introductorio con el catálogo de administración de COM+</span><span class="sxs-lookup"><span data-stu-id="c36d3-145">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="c36d3-146">Información general de los objetos COMAdmin</span><span class="sxs-lookup"><span data-stu-id="c36d3-146">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="c36d3-147">Recuperar recopilaciones en el catálogo de COM+</span><span class="sxs-lookup"><span data-stu-id="c36d3-147">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="c36d3-148">Establecer propiedades y guardar cambios en el catálogo de COM+</span><span class="sxs-lookup"><span data-stu-id="c36d3-148">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



