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
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539315"
---
# <a name="components-collection"></a>Colección de componentes

Contiene un objeto para cada componente de la aplicación relacionada. La colección de **componentes** siempre está relacionada con un objeto de la colección de [**aplicaciones**](applications.md) . Las propiedades expuestas por estos objetos contienen la configuración realizada en el nivel de componente.

Esta colección admite el método [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , pero no el método [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) . Para instalar o importar componentes en una aplicación, use métodos en el objeto [**COMAdminCatalog**](comadmincatalog.md) .

## <a name="members"></a>Miembros

La colección de **componentes** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**InterfacesForComponent**](interfacesforcomponent.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForComponent**](rolesforcomponent.md)
-   [**SubscriptionsForComponent**](subscriptionsforcomponent.md)

Puede navegar a esta colección desde las colecciones siguientes:

-   [**APLICACIONES**](applications.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:

-   [AllowInprocSubscribers](#allowinprocsubscribers)
-   [ApplicationID](#applicationid)
-   [Bits](#bitness)
-   [CLSID](#multiinterfacepublisherfilterclsid)
-   [ComponentAccessChecksEnabled](#componentaccesschecksenabled)
-   [ComponentTransactionTimeout](#componenttransactiontimeoutenabled)
-   [ComponentTransactionTimeoutEnabled](#componenttransactiontimeoutenabled)
-   [COMTIIntrinsics](#comtiintrinsics)
-   [ConstructionEnabled](#constructionenabled)
-   [ConstructorString](#constructorstring)
-   [CreationTimeout](#creationtimeout)
-   [Descripción](#description)
-   [DLL](#dll)
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
| Access         | ReadWrite                                                          |
| Tipo           | Bool                                                               |
| Valor predeterminado        | True                                                               |
| Sistema mínimo | Windows 2000                                                       |



 

### <a name="applicationid"></a>ApplicationID



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | GUID de la aplicación que contiene el componente. Debe ser un GUID de aplicación válido, que se comprueba antes de que se llame a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) . Si este valor se cambia para ser un GUID para una aplicación diferente, el componente se mueve a esa aplicación. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                        |
| Tipo           | String                                                                                                                                                                                                                                                                                           |
| Predeterminado        | N/D                                                                                                                                                                                                                                                                                              |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                     |



 

### <a name="bitness"></a>Valor de bits



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Representa el tipo de bits binario de un componente. En los sistemas que usan Windows de 64 bits, esta propiedad distingue entre los componentes de 64 bits y los componentes de 32 bits. |
| Access         | ReadOnly                                                                                                                                                            |
| Tipo           | Valores posibles largos: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0X2)                                                                                       |
| Valor predeterminado        | N/D                                                                                                                                                                 |
| Sistema mínimo | Windows XP                                                                                                                                                          |



 

### <a name="clsid"></a>CLSID



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | GUID del componente. Esta propiedad se devuelve cuando se llama al método de propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección. |
| Access         | ReadOnly                                                                                                                                                  |
| Tipo           | String                                                                                                                                                    |
| Predeterminado        | N/D                                                                                                                                                       |
| Sistema mínimo | Windows 2000                                                                                                                                              |



 

### <a name="componentaccesschecksenabled"></a>ComponentAccessChecksEnabled



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica si las comprobaciones de acceso basadas en roles se realizan en llamadas al componente y funcionan junto con las propiedades AccessChecksLevel y ApplicationAccessChecksEnabled en la aplicación. |
| Access         | ReadWrite                                                                                                                                                                                                  |
| Tipo           | Bool                                                                                                                                                                                                       |
| Valor predeterminado        | False                                                                                                                                                                                                      |
| Sistema mínimo | Windows 2000                                                                                                                                                                                               |



 

### <a name="componenttransactiontimeout"></a>ComponentTransactionTimeout



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Cuando se utiliza en una transacción, especifica el período de tiempo en el que este componente hace que se agote el tiempo de espera de la transacción. El valor predeterminado es 60 segundos y no puede ser superior a 3600 segundos (1 hora). El valor de tiempo de espera se puede establecer en 0, especificando un período de tiempo de espera de transacción infinito. Para usar esta propiedad, ComponentTransactionTimeoutEnabled debe ser true. El valor de esta propiedad invalida el tiempo de espera de la transacción global especificado por la propiedad TransactionTimeout de la colección [**LocalComputer**](localcomputer.md) . |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Tipo           | Long (0-3600)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Valor predeterminado        | 60                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

### <a name="componenttransactiontimeoutenabled"></a>ComponentTransactionTimeoutEnabled



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Especifica si el período de tiempo de espera de la transacción está habilitado para este componente. De forma predeterminada, la característica de tiempo de espera de la transacción está deshabilitada. Cuando esta propiedad es true, se usa el tiempo de espera especificado por ComponentTransactionTimeout. Cuando esta propiedad es false, se usa el tiempo de espera especificado por la propiedad TransactionTimeout de la colección [**LocalComputer**](localcomputer.md) . |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                      |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                                           |
| Valor predeterminado        | False                                                                                                                                                                                                                                                                                                                                                                                          |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="comtiintrinsics"></a>COMTIIntrinsics



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Permite pasar propiedades de contexto desde el integrador de transacciones COM (COMTI) al contexto de esta clase. El COMTI facilita la tarea de envolver transacciones de gran sistema y lógica de negocios como componentes COM. |
| Access         | ReadWrite                                                                                                                                                                                                            |
| Tipo           | Bool                                                                                                                                                                                                                 |
| Valor predeterminado        | False                                                                                                                                                                                                                |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                         |



 

### <a name="constructionenabled"></a>ConstructionEnabled



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------|
| Descripción    | Determina si el ConstructorString se pasa al objeto cuando se construye. |
| Access         | ReadWrite                                                                                |
| Tipo           | Bool                                                                                     |
| Valor predeterminado        | False                                                                                    |
| Sistema mínimo | Windows 2000                                                                             |



 

### <a name="constructorstring"></a>ConstructorString



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Cadena de inicialización para la construcción de componentes. Puede crear objetos diferentes del mismo componente genérico mediante cadenas de constructor de objeto. Si ConstructionEnabled es false, se omite esta propiedad. |
| Access         | ReadWrite                                                                                                                                                                                                          |
| Tipo           | String                                                                                                                                                                                                             |
| Predeterminado        | ""                                                                                                                                                                                                                 |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                       |



 

### <a name="creationtimeout"></a>CreationTimeout



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Al crear el objeto, se devuelve el número de milisegundos antes de que se devuelva un error de tiempo de espera. El tiempo de espera máximo es de 2147483647 milisegundos (unos 25 días). |
| Access         | ReadWrite                                                                                                                                              |
| Tipo           | Long (0-2147483647)                                                                                                                                    |
| Valor predeterminado        | 0                                                                                                                                                      |
| Sistema mínimo | Windows 2000                                                                                                                                           |



 

### <a name="description"></a>Descripción



| Entrada | Value |
|----------------|--------------------------|
| Descripción    | Describe el componente. |
| Access         | ReadWrite                |
| Tipo           | String                   |
| Predeterminado        | ""                       |
| Sistema mínimo | Windows 2000             |



 

### <a name="dll"></a>Archivo DLL



| Entrada | Value |
|----------------|---------------------------------------------------------|
| Descripción    | Nombre y ruta de acceso del archivo que contiene el componente. |
| Access         | ReadOnly                                                |
| Tipo           | String                                                  |
| Predeterminado        | N/D                                                     |
| Sistema mínimo | Windows 2000                                            |



 

### <a name="eventtrackingenabled"></a>EventTrackingEnabled



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina si se realiza el seguimiento de los eventos. Los eventos incluyen acciones como el cierre de la aplicación; creación y liberación de objetos; referencias a objetos, coherencia, activación y desactivación; llamadas al método, devuelve y excepciones; Inicio de la transacción, preparación para confirmar y anular; conexión, asignación y reciclaje del dispensador de recursos; asignación y reciclaje de subprocesos. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                     |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                          |
| Valor predeterminado        | True                                                                                                                                                                                                                                                                                                                                                                          |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="exceptionclass"></a>ExceptionClass



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | El CLSID, que puede ser un GUID o una cadena de moniker, para activar un programa alternativo durante el proceso de tratar con un programa de componentes en cola con errores repetidamente. |
| Access         | ReadWrite                                                                                                                                                                 |
| Tipo           | String                                                                                                                                                                    |
| Predeterminado        | ""                                                                                                                                                                        |
| Sistema mínimo | Windows 2000                                                                                                                                                              |



 

### <a name="fireinparallel"></a>FireInParallel



| Entrada | Value |
|----------------|----------------------------------------------------------------------------|
| Descripción    | Permite que los eventos se activen en paralelo si el componente es una clase de eventos. |
| Access         | ReadWrite                                                                  |
| Tipo           | Bool                                                                       |
| Valor predeterminado        | False                                                                      |
| Sistema mínimo | Windows 2000                                                               |



 

### <a name="iisintrinsics"></a>IISIntrinsics



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Habilita el paso de propiedades de contexto de IIS, como un objeto de sesión de aplicación o un objeto de sesión de usuario, en el contexto de esta clase. |
| Access         | ReadWrite                                                                                                                                   |
| Tipo           | Bool                                                                                                                                        |
| Valor predeterminado        | False                                                                                                                                       |
| Sistema mínimo | Windows 2000                                                                                                                                |



 

### <a name="initializeserverapplication"></a>InitializeServerApplication



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------|
| Descripción    | Indica si el componente se utiliza para inicializar una aplicación de servidor. |
| Access         | ReadWrite                                                                   |
| Tipo           | Bool                                                                        |
| Valor predeterminado        | False                                                                       |
| Sistema mínimo | Windows Server 2003                                                         |



 

### <a name="isenabled"></a>IsEnabled



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| Descripción    | False si el componente o la aplicación COM+ están deshabilitados. Si el componente o la aplicación COM+ está habilitado, IsEnabled es true. |
| Access         | ReadWrite                                                                                                                   |
| Tipo           | Bool                                                                                                                        |
| Valor predeterminado        | True                                                                                                                        |
| Sistema mínimo | Windows XP                                                                                                                  |



 

### <a name="iseventclass"></a>IsEventClass



| Entrada | Value |
|----------------|----------------------------------------------------|
| Descripción    | Indica si el componente es una clase de eventos. |
| Access         | ReadOnly                                           |
| Tipo           | Bool                                               |
| Valor predeterminado        | False                                              |
| Sistema mínimo | Windows 2000                                       |



 

### <a name="isinstalled"></a>IsInstalled



| Entrada | Value |
|----------------|-----------------------------------------------------------------|
| Descripción    | Indica si el componente está instalado en una aplicación. |
| Access         | ReadOnly                                                        |
| Tipo           | Bool                                                            |
| Valor predeterminado        | False                                                           |
| Sistema mínimo | Windows Server 2003                                             |



 

### <a name="isprivatecomponent"></a>IsPrivateComponent



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina si una aplicación de servidor es un componente privado. Un componente privado en una aplicación de servidor solo se puede activar desde dentro de la aplicación. Por ejemplo, si llama a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en un componente privado, se produce un error de fuera de proceso pero se realiza correctamente en proceso. Por el contrario, si llama a **CoCreateInstance** en un componente público, se realizará correctamente en proceso y fuera de proceso. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Valor predeterminado        | False                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="justintimeactivation"></a>JustInTimeActivation



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina si la [activación JIT](enabling-jit-activation-for-a-component.md) está habilitada para el componente. Esta propiedad se establece en true cuando la [compatibilidad con transacciones](setting-the-transaction-attribute.md) está establecida en Required, requiere New o Supported. Cuando JustInTimeActivation se establece en true, la [compatibilidad con la sincronización](setting-the-synchronization-attribute.md) debe establecerse en Required (el valor predeterminado) o requiere New. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Valor predeterminado        | False                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="loadbalancingsupported"></a>LoadBalancingSupported



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Si el servicio de equilibrio de carga de componentes está instalado y habilitado en el servidor, determina si el componente participa en el equilibrio de carga. |
| Access         | ReadWrite                                                                                                                                        |
| Tipo           | Bool                                                                                                                                             |
| Valor predeterminado        | False                                                                                                                                            |
| Sistema mínimo | Windows 2000                                                                                                                                     |



 

### <a name="maxpoolsize"></a>MaxPoolSize



| Entrada | Value |
|----------------|-----------------------------------|
| Descripción    | Número máximo de objetos agrupados. |
| Access         | ReadWrite                         |
| Tipo           | Long (1-1048576)                  |
| Valor predeterminado        | 1 048 576                           |
| Sistema mínimo | Windows 2000                      |



 

### <a name="minpoolsize"></a>MinPoolSize



| Entrada | Value |
|----------------|-----------------------------------|
| Descripción    | Número mínimo de objetos agrupados. |
| Access         | ReadWrite                         |
| Tipo           | Long (0-1048576)                  |
| Valor predeterminado        | 0                                 |
| Sistema mínimo | Windows 2000                      |



 

### <a name="multiinterfacepublisherfilterclsid"></a>MultiInterfacePublisherFilterCLSID



| Entrada | Value |
|----------------|-------------------------------------------------------------------------|
| Descripción    | CLSID del filtro de publicador utilizado si el componente es una clase de eventos. |
| Access         | ReadWrite                                                               |
| Tipo           | String                                                                  |
| Predeterminado        | N/D                                                                     |
| Sistema mínimo | Windows 2000                                                            |



 

### <a name="mustruninclientcontext"></a>MustRunInClientContext



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------|
| Descripción    | Indica que el componente debe activarse en el contexto del autor de la llamada original. De lo contrario, se produce un error en la activación. |
| Access         | ReadWrite                                                                                                 |
| Tipo           | Bool                                                                                                      |
| Valor predeterminado        | False                                                                                                     |
| Sistema mínimo | Windows XP                                                                                                |



 

### <a name="mustrunindefaultcontext"></a>MustRunInDefaultContext



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica que el componente se debe activar en el contexto del llamador predeterminado. De lo contrario, se produce un error en la activación. |
| Access         | ReadWrite                                                                                                    |
| Tipo           | Bool                                                                                                         |
| Valor predeterminado        | False                                                                                                        |
| Sistema mínimo | Windows 2000                                                                                                 |



 

### <a name="objectpoolingenabled"></a>ObjectPoolingEnabled



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------|
| Descripción    | Determina si la [agrupación de objetos com+](com--object-pooling.md) está habilitada para el componente. |
| Access         | ReadWrite                                                                                       |
| Tipo           | Bool                                                                                            |
| Valor predeterminado        | False                                                                                           |
| Sistema mínimo | Windows 2000                                                                                    |



 

### <a name="progid"></a>ProgID



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre descriptivo que se usa para identificar el componente. Esta propiedad se devuelve cuando se llama al método de la propiedad [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Access         | ReadOnly                                                                                                                                                                              |
| Tipo           | String                                                                                                                                                                                |
| Predeterminado        | N/D                                                                                                                                                                                   |
| Sistema mínimo | Windows 2000                                                                                                                                                                          |



 

### <a name="publisherid"></a>PublisherID



| Entrada | Value |
|----------------|------------------------------------------------------------------------|
| Descripción    | Identificador del publicador de eventos si el componente es una clase de eventos. |
| Access         | ReadWrite                                                              |
| Tipo           | String                                                                 |
| Predeterminado        | ""                                                                     |
| Sistema mínimo | Windows 2000                                                           |



 

### <a name="soapassemblyname"></a>SoapAssemblyName



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------|
| Descripción    | GUID que identifica el ensamblado de GAC que se ejecuta cuando se invoca el componente como un servicio SOAP. |
| Access         | ReadWrite                                                                                        |
| Tipo           | String                                                                                           |
| Predeterminado        | NULL                                                                                             |
| Sistema mínimo | Windows Server 2003                                                                              |



 

### <a name="soaptypename"></a>SoapTypeName



| Entrada | Value |
|----------------|------------------------------------------------------------------------------|
| Descripción    | El nombre de tipo administrado para un componente que se puede invocar como un servicio SOAP. |
| Access         | ReadWrite                                                                    |
| Tipo           | String                                                                       |
| Predeterminado        | NULL                                                                         |
| Sistema mínimo | Windows Server 2003                                                          |



 

### <a name="synchronization"></a>Synchronization



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina la [sincronización](setting-the-synchronization-attribute.md) de llamadas para el componente.                                                                                                     |
| Access         | ReadWrite                                                                                                                                                                                           |
| Tipo           | Valores posibles largos: COMAdminSynchronizationIgnored (0) COMAdminSynchronizationNone (1) COMAdminSynchronizationSupported (2) COMAdminSynchronizationRequired (3) COMAdminSynchronizationRequiresNew (4) |
| Valor predeterminado        | COMAdminSynchronizationIgnored (0)                                                                                                                                                                  |
| Sistema mínimo | Windows 2000                                                                                                                                                                                        |



 

### <a name="threadingmodel"></a>ThreadingModel



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina cómo se asignan las instancias del componente a los subprocesos para la ejecución del método. Los valores corresponden a los modelos de subprocesos COM.                                                                                        |
| Access         | ReadOnly                                                                                                                                                                                                                  |
| Tipo           | Valores posibles largos: COMAdminThreadingModelApartment (0) COMAdminThreadingModelFree (1) COMAdminThreadingModelMain (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4) COMAdminThreadingModelNotSpecified (5) |
| Valor predeterminado        | N/D                                                                                                                                                                                                                       |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                              |



 

### <a name="transaction"></a>Transacción



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina cómo un componente admite [transacciones](setting-the-transaction-attribute.md). Se recomienda usar las constantes en la enumeración y no los valores numéricos. |
| Access         | ReadWrite                                                                                                                                                                              |
| Tipo           | Valores posibles largos: COMAdminTransactionIgnored (0) COMAdminTransactionNone (1) COMAdminTransactionSupported (2) COMAdminTransactionRequired (3) COMAdminTransactionRequiresNew (4)        |
| Valor predeterminado        | COMAdminTransactionNone (1)                                                                                                                                                            |
| Sistema mínimo | Windows 2000                                                                                                                                                                           |



 

### <a name="txisolationlevel"></a>TxIsolationLevel



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica los niveles de aislamiento de transacción. Hay cinco niveles de aislamiento: ninguno, lectura no confirmada, lectura confirmada, lectura repetible y serializada. El nivel de aislamiento predeterminado es serializado.                           |
| Access         | ReadWrite                                                                                                                                                                                                                  |
| Tipo           | Valores posibles largos: COMAdminTxIsolationLevelAny (0) COMAdminTxIsolationLevelReadUnCommitted (1) COMAdminTxIsolationLevelReadCommitted (2) COMAdminTxIsolationLevelRepeatableRead (3) COMAdminTxIsolationLevelSerializable (4) |
| Valor predeterminado        | COMAdminTxIsolationLevelSerializable (4)                                                                                                                                                                                   |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                 |



 

### <a name="versionbuild"></a>VersionBuild



| Entrada | Value |
|----------------|---------------------------|
| Descripción    | Identificador de compilación de versión. |
| Access         | ReadOnly                  |
| Tipo           | String                    |
| Predeterminado        | ""                        |
| Sistema mínimo | Windows 2000              |



 

### <a name="versionmajor"></a>VersionMajor



| Entrada | Value |
|----------------|---------------------|
| Descripción    | Identificador de la versión. |
| Access         | ReadOnly            |
| Tipo           | String              |
| Predeterminado        | ""                  |
| Sistema mínimo | Windows 2000        |



 

### <a name="versionminor"></a>VersionMinor



| Entrada | Value |
|----------------|-------------------------|
| Descripción    | Subidentificador de versión. |
| Access         | ReadOnly                |
| Tipo           | String                  |
| Predeterminado        | ""                      |
| Sistema mínimo | Windows 2000            |



 

### <a name="versionsubbuild"></a>VersionSubBuild



| Entrada | Value |
|----------------|-------------------------------|
| Descripción    | Identificador de subcompilación de versión. |
| Access         | ReadOnly                      |
| Tipo           | String                        |
| Predeterminado        | ""                            |
| Sistema mínimo | Windows 2000                  |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
