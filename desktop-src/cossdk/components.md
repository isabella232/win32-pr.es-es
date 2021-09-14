---
description: Contiene un objeto para cada componente de la aplicación relacionada.
ms.assetid: f502ba60-b2b1-4556-8f91-22a474e60e0d
title: Colección de componentes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Components
api_type:
- COM
api_location: ''
ms.openlocfilehash: f68013985beff427b5681c5b78c2c00df9e69263
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358919"
---
# <a name="components-collection"></a>Colección de componentes

Contiene un objeto para cada componente de la aplicación relacionada. La **colección** Components siempre está relacionada con un objeto de la [**colección Applications.**](applications.md) Las propiedades expuestas por estos objetos mantienen la configuración realizada en el nivel de componente.

Esta colección admite el [**método Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection,**](comadmincatalogcollection.md) pero no [**el método Add.**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) Para instalar o importar componentes en una aplicación, use métodos en el [**objeto COMAdminCatalog.**](comadmincatalog.md)

## <a name="members"></a>Members

La **colección Components** hereda de la interfaz [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**InterfacesForComponent**](interfacesforcomponent.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForComponent**](rolesforcomponent.md)
-   [**SubscriptionsForComponent**](subscriptionsforcomponent.md)

Puede navegar a esta colección desde las siguientes colecciones:

-   [**Aplicaciones**](applications.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) de la colección admite las siguientes propiedades:

-   [AllowInprocSubscribers](#allowinprocsubscribers)
-   [ApplicationID](#applicationid)
-   [Bitness](#bitness)
-   [CLSID](#multiinterfacepublisherfilterclsid)
-   [ComponentAccessChecksEnabled](#componentaccesschecksenabled)
-   [ComponentTransactionTimeout](#componenttransactiontimeoutenabled)
-   [ComponentTransactionTimeoutEnabled](#componenttransactiontimeoutenabled)
-   [COMTIIntrinsics](#comtiintrinsics)
-   [ConstructionEnabled](#constructionenabled)
-   [ConstructorString](#constructorstring)
-   [CreationTimeout](#creationtimeout)
-   [Descripción](#description)
-   [Archivo DLL](#dll)
-   [EventTrackingEnabled](#eventtrackingenabled)
-   [ExceptionClass](#exceptionclass)
-   [FireInParallel](#fireinparallel)
-   [IISIntrinsics](#iisintrinsics)
-   [InitializeServerApplication](#initializeserverapplication)
-   [IsEnabled](#isenabled)
-   [IsEventClass](#iseventclass)
-   [IsInstalled](#isinstalled)
-   [IsPrivateComponent](#isprivatecomponent)
-   [JustInTimeActivation](#justintimeactivation)
-   [LoadBalancingSupported](#loadbalancingsupported)
-   [MaxPoolSize](#maxpoolsize)
-   [MinPoolSize](#minpoolsize)
-   [MultiInterfacePublisherFilterCLSID](#multiinterfacepublisherfilterclsid)
-   [MustRunInClientContext](#mustruninclientcontext)
-   [MustRunInDefaultContext](#mustrunindefaultcontext)
-   [ObjectPoolingEnabled](#objectpoolingenabled)
-   [ProgID](#progid)
-   [PublisherID](#publisherid)
-   [SoapAssemblyName](#soapassemblyname)
-   [SoapTypeName](#soaptypename)
-   [Sincronización](#synchronization)
-   [ThreadingModel](#threadingmodel)
-   [Transacción](#componenttransactiontimeout)
-   [TxIsolationLevel](#txisolationlevel)
-   [VersionBuild](#versionbuild)
-   [VersionMajor](#versionmajor)
-   [VersionMinor](#versionminor)
-   [VersionSubBuild](#versionsubbuild)

### <a name="allowinprocsubscribers"></a>AllowInprocSubscribers



| Entrada | Value |
|----------------|--------------------------------------------------------------------|
| Descripción    | Habilita en los suscriptores de proceso si el componente es una clase de eventos. |
| Acceso         | ReadWrite                                                          |
| Tipo           | Bool                                                               |
| Default        | True                                                               |
| Sistema mínimo | Windows 2000                                                       |



 

### <a name="applicationid"></a>ApplicationID



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | GUID de la aplicación que contiene el componente. Debe ser un GUID de aplicación válido, que se comprueba antes [**de llamar a SaveChanges.**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) Si este valor se cambia para que sea un GUID para una aplicación diferente, el componente se mueve a esa aplicación. |
| Acceso         | ReadWrite                                                                                                                                                                                                                                                                                        |
| Tipo           | String                                                                                                                                                                                                                                                                                           |
| Predeterminado        | N/D                                                                                                                                                                                                                                                                                              |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                     |



 

### <a name="bitness"></a>Valor de bits



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Representa el tipo de bits binario de un componente. En sistemas que usan componentes de 64 Windows, esta propiedad distingue entre componentes de 64 bits y componentes de 32 bits. |
| Acceso         | ReadOnly                                                                                                                                                            |
| Tipo           | Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)                                                                                       |
| Default        | N/D                                                                                                                                                                 |
| Sistema mínimo | Windows XP                                                                                                                                                          |



 

### <a name="clsid"></a>CLSID



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | GUID para el componente. Esta propiedad se devuelve cuando se llama [**al método**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) de propiedad Key en un objeto de esta colección. |
| Acceso         | ReadOnly                                                                                                                                                  |
| Tipo           | String                                                                                                                                                    |
| Predeterminado        | N/D                                                                                                                                                       |
| Sistema mínimo | Windows 2000                                                                                                                                              |



 

### <a name="componentaccesschecksenabled"></a>ComponentAccessChecksEnabled



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica si las comprobaciones de acceso basado en rol se realizan en llamadas al componente y funciona junto con las propiedades AccessChecksLevel y ApplicationAccessChecksEnabled en la aplicación. |
| Acceso         | ReadWrite                                                                                                                                                                                                  |
| Tipo           | Bool                                                                                                                                                                                                       |
| Valor predeterminado        | False                                                                                                                                                                                                      |
| Sistema mínimo | Windows 2000                                                                                                                                                                                               |



 

### <a name="componenttransactiontimeout"></a>ComponentTransactionTimeout



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Cuando se usa en una transacción, especifica el período de tiempo en el que este componente hace que la transacción se resalte. El valor predeterminado es 60 segundos y no puede ser superior a 3600 segundos (1 hora). El valor de tiempo de espera se puede establecer en 0, especificando un período de tiempo de espera de transacción infinito. Para que se utilice esta propiedad, ComponentTransactionTimeoutEnabled debe ser True. El valor de esta propiedad invalida el tiempo de espera de transacción global especificado por la propiedad TransactionTimeout de la [**colección LocalComputer.**](localcomputer.md) |
| Acceso         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Tipo           | Long (0-3600)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Default        | 60                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

### <a name="componenttransactiontimeoutenabled"></a>ComponentTransactionTimeoutEnabled



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Especifica si el período de tiempo de espera de la transacción está habilitado para este componente. De forma predeterminada, la característica de tiempo de espera de transacción está deshabilitada. Cuando esta propiedad es True, se usa el tiempo de espera especificado por ComponentTransactionTimeout. Cuando esta propiedad es False, se usa el tiempo de espera especificado por la propiedad TransactionTimeout de la [**colección LocalComputer.**](localcomputer.md) |
| Acceso         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                      |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                                           |
| Valor predeterminado        | False                                                                                                                                                                                                                                                                                                                                                                                          |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="comtiintrinsics"></a>COMTIIntrinsics



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Permite pasar propiedades de contexto del Integrador de transacciones COM (COMTI) al contexto de esta clase. COMTI facilita la tarea de encapsular las transacciones del sistema central y la lógica de negocios como componentes COM. |
| Acceso         | ReadWrite                                                                                                                                                                                                            |
| Tipo           | Bool                                                                                                                                                                                                                 |
| Valor predeterminado        | False                                                                                                                                                                                                                |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                         |



 

### <a name="constructionenabled"></a>ConstructionEnabled



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------|
| Descripción    | Determina si constructorString se pasa al objeto cuando se construye. |
| Acceso         | ReadWrite                                                                                |
| Tipo           | Bool                                                                                     |
| Valor predeterminado        | False                                                                                    |
| Sistema mínimo | Windows 2000                                                                             |



 

### <a name="constructorstring"></a>ConstructorString



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Cadena de inicialización para la construcción de componentes. Puede crear objetos diferentes a partir del mismo componente genérico mediante cadenas de constructor de objetos. Si ConstructionEnabled es False, se omite esta propiedad. |
| Acceso         | ReadWrite                                                                                                                                                                                                          |
| Tipo           | String                                                                                                                                                                                                             |
| Predeterminado        | ""                                                                                                                                                                                                                 |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                       |



 

### <a name="creationtimeout"></a>CreationTimeout



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Al crear el objeto, se devuelve el número de milisegundos antes de que se devuelva un error de tiempo de espera. El tiempo de espera máximo es 2147483647 milisegundos (aproximadamente 25 días). |
| Acceso         | ReadWrite                                                                                                                                              |
| Tipo           | Long (0-2147483647)                                                                                                                                    |
| Default        | 0                                                                                                                                                      |
| Sistema mínimo | Windows 2000                                                                                                                                           |



 

### <a name="description"></a>Descripción



| Entrada | Value |
|----------------|--------------------------|
| Descripción    | Describe el componente. |
| Acceso         | ReadWrite                |
| Tipo           | String                   |
| Predeterminado        | ""                       |
| Sistema mínimo | Windows 2000             |



 

### <a name="dll"></a>Archivo DLL



| Entrada | Value |
|----------------|---------------------------------------------------------|
| Descripción    | Nombre y ruta de acceso del archivo que contiene el componente. |
| Acceso         | ReadOnly                                                |
| Tipo           | String                                                  |
| Predeterminado        | N/D                                                     |
| Sistema mínimo | Windows 2000                                            |



 

### <a name="eventtrackingenabled"></a>EventTrackingEnabled



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina si se realiza un seguimiento de los eventos. Los eventos incluyen acciones como el cierre de la aplicación; creación y liberación de objetos; referencias a objetos, coherencia, activación y desactivación; llamadas a métodos, devoluciones y excepciones; inicio de transacción, preparación para confirmar y anular; conexión, asignación y reciclaje del dispensador de recursos; asignación y reciclaje de subprocesos. |
| Acceso         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                     |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                          |
| Default        | True                                                                                                                                                                                                                                                                                                                                                                          |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="exceptionclass"></a>ExceptionClass



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | CLSID, que puede ser un GUID o una cadena de moniker, para activar un programa alternativo durante el proceso de tratar con un programa de componentes en cola con errores repetidos. |
| Acceso         | ReadWrite                                                                                                                                                                 |
| Tipo           | String                                                                                                                                                                    |
| Predeterminado        | ""                                                                                                                                                                        |
| Sistema mínimo | Windows 2000                                                                                                                                                              |



 

### <a name="fireinparallel"></a>FireInParallel



| Entrada | Value |
|----------------|----------------------------------------------------------------------------|
| Descripción    | Permite activar eventos en paralelo si el componente es una clase de eventos. |
| Acceso         | ReadWrite                                                                  |
| Tipo           | Bool                                                                       |
| Valor predeterminado        | False                                                                      |
| Sistema mínimo | Windows 2000                                                               |



 

### <a name="iisintrinsics"></a>IISIntrinsics



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Permite pasar propiedades de contexto de IIS, como un objeto de sesión de aplicación o un objeto de sesión de usuario, al contexto de esta clase. |
| Acceso         | ReadWrite                                                                                                                                   |
| Tipo           | Bool                                                                                                                                        |
| Valor predeterminado        | False                                                                                                                                       |
| Sistema mínimo | Windows 2000                                                                                                                                |



 

### <a name="initializeserverapplication"></a>InitializeServerApplication



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------|
| Descripción    | Indica si el componente se usa para inicializar una aplicación de servidor. |
| Acceso         | ReadWrite                                                                   |
| Tipo           | Bool                                                                        |
| Valor predeterminado        | False                                                                       |
| Sistema mínimo | Windows Server 2003                                                         |



 

### <a name="isenabled"></a>IsEnabled



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| Descripción    | False si la aplicación o componente com+ está deshabilitado. Si la aplicación o componente COM+ está habilitado, IsEnabled es True. |
| Acceso         | ReadWrite                                                                                                                   |
| Tipo           | Bool                                                                                                                        |
| Default        | True                                                                                                                        |
| Sistema mínimo | Windows XP                                                                                                                  |



 

### <a name="iseventclass"></a>IsEventClass



| Entrada | Value |
|----------------|----------------------------------------------------|
| Descripción    | Indica si el componente es una clase de eventos. |
| Acceso         | ReadOnly                                           |
| Tipo           | Bool                                               |
| Valor predeterminado        | False                                              |
| Sistema mínimo | Windows 2000                                       |



 

### <a name="isinstalled"></a>IsInstalled



| Entrada | Value |
|----------------|-----------------------------------------------------------------|
| Descripción    | Indica si el componente está instalado en una aplicación. |
| Acceso         | ReadOnly                                                        |
| Tipo           | Bool                                                            |
| Valor predeterminado        | False                                                           |
| Sistema mínimo | Windows Server 2003                                             |



 

### <a name="isprivatecomponent"></a>IsPrivateComponent



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina si una aplicación de servidor es un componente privado. Un componente privado de una aplicación de servidor solo se puede activar desde dentro de la aplicación. Por ejemplo, si llama a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en un componente privado, se produce un error fuera de proceso, pero se realiza correctamente en el proceso. Por el contrario, si llama a **CoCreateInstance** en un componente público, se realiza correctamente tanto en proceso como fuera de proceso. |
| Acceso         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Valor predeterminado        | False                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="justintimeactivation"></a>JustInTimeActivation



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina si la [activación JIT](enabling-jit-activation-for-a-component.md) está habilitada para el componente. Esta propiedad se establece en True cuando [la compatibilidad con](setting-the-transaction-attribute.md) transacciones se establece en Requerido, Requiere nuevo o Compatible. Cuando JustInTimeActivation se establece en [True,](setting-the-synchronization-attribute.md) la compatibilidad con la sincronización debe establecerse en Requerido (valor predeterminado) o Requiere nuevo. |
| Acceso         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Valor predeterminado        | False                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="loadbalancingsupported"></a>LoadBalancingSupported



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Si el servicio de equilibrio de carga de componentes está instalado y habilitado en el servidor, determina si el componente participa en el equilibrio de carga. |
| Acceso         | ReadWrite                                                                                                                                        |
| Tipo           | Bool                                                                                                                                             |
| Valor predeterminado        | False                                                                                                                                            |
| Sistema mínimo | Windows 2000                                                                                                                                     |



 

### <a name="maxpoolsize"></a>MaxPoolSize



| Entrada | Value |
|----------------|-----------------------------------|
| Descripción    | Número máximo de objetos agrupados. |
| Acceso         | ReadWrite                         |
| Tipo           | Long (1-1048576)                  |
| Default        | 1 048 576                           |
| Sistema mínimo | Windows 2000                      |



 

### <a name="minpoolsize"></a>MinPoolSize



| Entrada | Value |
|----------------|-----------------------------------|
| Descripción    | Número mínimo de objetos agrupados. |
| Acceso         | ReadWrite                         |
| Tipo           | Long (0-1048576)                  |
| Default        | 0                                 |
| Sistema mínimo | Windows 2000                      |



 

### <a name="multiinterfacepublisherfilterclsid"></a>MultiInterfacePublisherFilterCLSID



| Entrada | Value |
|----------------|-------------------------------------------------------------------------|
| Descripción    | CLSID para el filtro del publicador utilizado si el componente es una clase de eventos. |
| Acceso         | ReadWrite                                                               |
| Tipo           | String                                                                  |
| Predeterminado        | N/D                                                                     |
| Sistema mínimo | Windows 2000                                                            |



 

### <a name="mustruninclientcontext"></a>MustRunInClientContext



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------|
| Descripción    | Indica que el componente debe activarse en el contexto del autor de la llamada original. De lo contrario, se produce un error en la activación. |
| Acceso         | ReadWrite                                                                                                 |
| Tipo           | Bool                                                                                                      |
| Valor predeterminado        | False                                                                                                     |
| Sistema mínimo | Windows XP                                                                                                |



 

### <a name="mustrunindefaultcontext"></a>MustRunInDefaultContext



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica que el componente debe activarse en el contexto del llamador predeterminado. De lo contrario, se produce un error en la activación. |
| Acceso         | ReadWrite                                                                                                    |
| Tipo           | Bool                                                                                                         |
| Valor predeterminado        | False                                                                                                        |
| Sistema mínimo | Windows 2000                                                                                                 |



 

### <a name="objectpoolingenabled"></a>ObjectPoolingEnabled



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------|
| Descripción    | Determina si la [agrupación de objetos COM+](com--object-pooling.md) está habilitada para el componente. |
| Acceso         | ReadWrite                                                                                       |
| Tipo           | Bool                                                                                            |
| Valor predeterminado        | False                                                                                           |
| Sistema mínimo | Windows 2000                                                                                    |



 

### <a name="progid"></a>ProgID



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre descriptivo que se usa para identificar el componente. Esta propiedad se devuelve cuando se [**llama al método**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) de propiedad Name en un objeto de esta colección. |
| Acceso         | ReadOnly                                                                                                                                                                              |
| Tipo           | String                                                                                                                                                                                |
| Predeterminado        | N/D                                                                                                                                                                                   |
| Sistema mínimo | Windows 2000                                                                                                                                                                          |



 

### <a name="publisherid"></a>PublisherID



| Entrada | Value |
|----------------|------------------------------------------------------------------------|
| Descripción    | Identificador del publicador de eventos si el componente es una clase de eventos. |
| Acceso         | ReadWrite                                                              |
| Tipo           | String                                                                 |
| Predeterminado        | ""                                                                     |
| Sistema mínimo | Windows 2000                                                           |



 

### <a name="soapassemblyname"></a>SoapAssemblyName



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------|
| Descripción    | GUID que identifica el ensamblado gac que se ejecuta cuando se invoca el componente como un servicio SOAP. |
| Acceso         | ReadWrite                                                                                        |
| Tipo           | String                                                                                           |
| Predeterminado        | NULL                                                                                             |
| Sistema mínimo | Windows Server 2003                                                                              |



 

### <a name="soaptypename"></a>SoapTypeName



| Entrada | Value |
|----------------|------------------------------------------------------------------------------|
| Descripción    | Nombre de tipo administrado para un componente que se puede invocar como un servicio SOAP. |
| Acceso         | ReadWrite                                                                    |
| Tipo           | String                                                                       |
| Predeterminado        | NULL                                                                         |
| Sistema mínimo | Windows Server 2003                                                          |



 

### <a name="synchronization"></a>Sincronización



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina la sincronización [de llamadas](setting-the-synchronization-attribute.md) para el componente.                                                                                                     |
| Acceso         | ReadWrite                                                                                                                                                                                           |
| Tipo           | Long Possible values:COMAdminSynchronizationIgnored (0)COMAdminSynchronizationNone (1)COMAdminSynchronizationSupported (2)COMAdminSynchronizationRequired (3)COMAdminSynchronizationRequiresNew (4) |
| Default        | COMAdminSynchronizationIgnored (0)                                                                                                                                                                  |
| Sistema mínimo | Windows 2000                                                                                                                                                                                        |



 

### <a name="threadingmodel"></a>ThreadingModel



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina cómo se asignan las instancias del componente a los subprocesos para la ejecución de métodos. Los valores corresponden a los modelos de subprocesamiento COM.                                                                                        |
| Acceso         | ReadOnly                                                                                                                                                                                                                  |
| Tipo           | Valores largos posibles:COMAdminThreadingModelThread (0)COMAdminThreadingModelFree (1)COMAdminThreadingModelMain (2)COMAdminThreadingModelBoth (3)COMAdminThreadingModelNeutral (4)COMAdminThreadingModelNotSpecified (5) |
| Default        | N/D                                                                                                                                                                                                                       |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                              |



 

### <a name="transaction"></a>Transacción



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina cómo un componente admite [transacciones](setting-the-transaction-attribute.md). Se recomienda usar las constantes de la enumeración y no los valores numéricos. |
| Acceso         | ReadWrite                                                                                                                                                                              |
| Tipo           | Long Possible values:COMAdminTransactionIgnored (0)COMAdminTransactionNone (1)COMAdminTransactionSupported (2)COMAdminTransactionRequired (3)COMAdminTransactionRequiresNew (4)        |
| Default        | COMAdminTransactionNone (1)                                                                                                                                                            |
| Sistema mínimo | Windows 2000                                                                                                                                                                           |



 

### <a name="txisolationlevel"></a>TxIsolationLevel



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica los niveles de aislamiento de transacción. Hay cinco niveles de aislamiento: ninguno, lectura no confirmada, lectura confirmada, lectura repetible y serializada. El nivel de aislamiento predeterminado se serializa.                           |
| Acceso         | ReadWrite                                                                                                                                                                                                                  |
| Tipo           | Long Possible values:COMAdminTxIsolationLevelAny (0)COMAdminTxIsolationLevelReadUnCommitted (1)COMAdminTxIsolationLevelReadCommitted (2)COMAdminTxIsolationLevelRepeatableRead (3)COMAdminTxIsolationLevelSerializable (4) |
| Default        | COMAdminTxIsolationLevelSerializable (4)                                                                                                                                                                                   |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                 |



 

### <a name="versionbuild"></a>VersionBuild



| Entrada | Value |
|----------------|---------------------------|
| Descripción    | Identificador de compilación de versión. |
| Acceso         | ReadOnly                  |
| Tipo           | String                    |
| Predeterminado        | ""                        |
| Sistema mínimo | Windows 2000              |



 

### <a name="versionmajor"></a>VersionMajor



| Entrada | Value |
|----------------|---------------------|
| Descripción    | Identificador de versión. |
| Acceso         | ReadOnly            |
| Tipo           | String              |
| Predeterminado        | ""                  |
| Sistema mínimo | Windows 2000        |



 

### <a name="versionminor"></a>VersionMinor



| Entrada | Value |
|----------------|-------------------------|
| Descripción    | Sub identifier de versión. |
| Acceso         | ReadOnly                |
| Tipo           | String                  |
| Predeterminado        | ""                      |
| Sistema mínimo | Windows 2000            |



 

### <a name="versionsubbuild"></a>VersionSubBuild



| Entrada | Value |
|----------------|-------------------------------|
| Descripción    | Identificador de la sub compilación de la versión. |
| Acceso         | ReadOnly                      |
| Tipo           | String                        |
| Predeterminado        | ""                            |
| Sistema mínimo | Windows 2000                  |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
