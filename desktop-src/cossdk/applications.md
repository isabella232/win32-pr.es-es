---
description: Contiene un objeto para cada aplicación COM+ instalada en el equipo local. Las propiedades expuestas por estos objetos mantienen todas las configuraciones realizadas en el nivel de aplicación.
ms.assetid: c0c46592-5282-412d-8f54-67637be8218a
title: Colección de aplicaciones
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Applications
api_type:
- COM
api_location: ''
ms.openlocfilehash: 085983bf390998910f36a87ac41aaa15e783b55d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884826"
---
# <a name="applications-collection"></a>Colección de aplicaciones

Contiene un objeto para cada aplicación COM+ instalada en el equipo local. Las propiedades expuestas por estos objetos mantienen todas las configuraciones realizadas en el nivel de aplicación.

Las propiedades de los componentes de una aplicación se establecen mediante la colección [**Components**](components.md) relacionada. Los roles se asignan a una aplicación mediante la colección [**roles**](roles.md) relacionada.

Para instalar componentes en una aplicación, use métodos en el [**objeto COMAdminCatalog.**](comadmincatalog.md) Para instalar una aplicación desde un archivo o para apagar o exportar una aplicación, use también métodos en el **objeto COMAdminCatalog.** De lo contrario, para crear una nueva aplicación, puede agregar un objeto a la **colección** Aplicaciones.

Esta colección admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**y Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Miembros

La **colección** Applications hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   [**ApplicationInstances**](applicationinstances.md)
-   [**Componentes**](components.md)
-   [**ErrorInfo**](errorinfo.md)
-   [**LegacyComponents**](legacycomponents.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**Roles**](roles.md)

Puede navegar a esta colección desde las siguientes colecciones:

-   [**Particiones**](partitions.md)
-   [**Raíz**](root.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) de la colección admite las siguientes propiedades:

-   [3GigSupportEnabled](#3gigsupportenabled)
-   [AccessChecksLevel](#accesscheckslevel)
-   [Activación](#recycleactivationlimit)
-   [ApplicationAccessChecksEnabled](#applicationaccesschecksenabled)
-   [ApplicationDirectory](#applicationdirectory)
-   [ApplicationProxy](#applicationproxyservername)
-   [ApplicationProxyServerName](#applicationproxyservername)
-   [AppPartitionID](#apppartitionid)
-   [Autenticación](#authenticationcapability)
-   [AuthenticationCapability](#authenticationcapability)
-   [Cambiable](#changeable)
-   [CommandLine](#commandline)
-   [ConcurrentApps](#concurrentapps)
-   [CreatedBy](#createdby)
-   [CRMEnabled](#crmenabled)
-   [CRMLogFile](#crmlogfile)
-   [Eliminable](#deleteable)
-   [Descripción](#description)
-   [DumpEnabled](#dumpenabled)
-   [DumpOnException](#dumponexception)
-   [DumpOnFailfast](#dumponfailfast)
-   [DumpPath](#dumppath)
-   [EventsEnabled](#eventsenabled)
-   [ID](#applications-collection)
-   [Identidad](#identity)
-   [ImpersonationLevel](#impersonationlevel)
-   [IsEnabled](#isenabled)
-   [IsSystem](#issystem)
-   [MaxDumpCount](#maxdumpcount)
-   [Nombre](#applicationproxyservername)
-   [Contraseña](#password)
-   [QCAuthenticateMsgs](#qcauthenticatemsgs)
-   [QCListenerMaxThreads](#qclistenermaxthreads)
-   [QueueListenerEnabled](#queuelistenerenabled)
-   [QueuingEnabled](#queuingenabled)
-   [RecycleActivationLimit](#recycleactivationlimit)
-   [RecycleCallLimit](#recyclecalllimit)
-   [RecycleExpirationTimeout](#recycleexpirationtimeout)
-   [RecycleLifetimeLimit](#recyclelifetimelimit)
-   [RecycleMemoryLimit](#recyclememorylimit)
-   [Replicable](#replicable)
-   [RunForever](#runforever)
-   [ServiceName](#servicename)
-   [ShutdownAfter](#shutdownafter)
-   [SoapActivated](#soapactivated)
-   [SoapBaseUrl](#soapbaseurl)
-   [SoapMailTo](#soapmailto)
-   [SoapVRoot](#soapvroot)
-   [SRPEnabled](#srpenabled)
-   [SRPTrustLevel](#srptrustlevel)

### <a name="3gigsupportenabled"></a>3GigSupportEnabled



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica si la aplicación puede usar 3 GB de memoria en su proceso. Si esto no está habilitado, la aplicación solo puede usar 2 GB de memoria. |
| Access         | ReadWrite                                                                                                                                     |
| Tipo           | Bool                                                                                                                                          |
| Valor predeterminado        | False                                                                                                                                         |
| Sistema mínimo | Windows 2000                                                                                                                                  |



 

### <a name="accesscheckslevel"></a>AccessChecksLevel



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica si las comprobaciones de acceso se realizan solo en el nivel de proceso o en el nivel de proceso y componente. Se recomienda usar las constantes de la enumeración y no los valores numéricos. |
| Access         | ReadWrite                                                                                                                                                                                                       |
| Tipo           | Valores largos posibles: COMAdminAccessChecksApplicationLevel (0) COMAdminAccessChecksApplicationComponentLevel (1)                                                                                                |
| Valor predeterminado        | COMAdminAccessChecksApplicationComponentLevel (1)                                                                                                                                                               |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                    |



 

### <a name="activation"></a>Activación



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | La activación local indica que los objetos dentro de la aplicación se ejecutan dentro de un proceso de servidor local dedicado (aplicación de servidor). La activación en proceso indica que los objetos se ejecutan en el proceso de su creador (aplicación de biblioteca). |
| Access         | ReadWrite                                                                                                                                                                                                                           |
| Tipo           | Long Possible values:COMAdminActivationInproc (0)COMAdminActivationLocal (1)                                                                                                                                                        |
| Valor predeterminado        | COMAdminActivationLocal (1)                                                                                                                                                                                                         |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                        |



 

### <a name="applicationaccesschecksenabled"></a>ApplicationAccessChecksEnabled



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------|
| Descripción    | Indica si se realizan comprobaciones de acceso para la aplicación cuando los clientes realizan llamadas a ella. |
| Access         | ReadWrite                                                                                          |
| Tipo           | Bool                                                                                               |
| Valor predeterminado        | True                                                                                               |
| Sistema mínimo | Windows 2000                                                                                       |



 

### <a name="applicationdirectory"></a>ApplicationDirectory



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Ruta de acceso completa a la aplicación. Esta información es necesaria al configurar ensamblados en paralelo (SxS). Los ensamblados en paralelo (SxS) permiten a las aplicaciones ASP especificar qué versión de un archivo DLL del sistema compatible con SxS se va a usar, como MSVCRT, MSXML, COMCTL, GDIPLUS, y así sucesivamente. Por ejemplo, si la aplicación ASP se basa en la versión 2.0 de MSVCRT, puede asegurarse de que la aplicación todavía usa la versión 2.0 de MSVCRT, incluso después de aplicar Service Pack al servidor. Cualquier nueva versión de MSVCRT todavía está instalada en el equipo, pero la versión 2.0 permanece y la usa la aplicación. Los archivos DLL compatibles con SxS se almacenan en %WINDIR% \\ WinSxS. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Tipo           | String                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Predeterminado        | ""                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

> [!Note]  
> Solo se puede usar una versión de un archivo DLL del sistema en cualquier grupo de aplicaciones, aunque esta característica se pueda configurar en el nivel de aplicación. Por ejemplo, si la aplicación App1 usa MSVCRT, la versión 2.5 y la aplicación App2 usa MSVCRT, versión 2.4, App1 y App2 no deben estar en el mismo grupo de aplicaciones. Si es así, la aplicación que se carga primero tiene su versión de MSVCRT cargada y la otra aplicación se ve forzada a usarla hasta que se descarguen las aplicaciones.

 

Para obtener más información, vea "Ensamblados en paralelo" en Cambios en servicios [COM+ en IIS 6.0.](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90))

### <a name="applicationproxy"></a>ApplicationProxy



| Entrada | Valor |
|----------------|------------------------------------------------------------|
| Descripción    | Indica si la aplicación es un proxy de aplicación. |
| Access         | ReadOnly                                                   |
| Tipo           | Bool                                                       |
| Valor predeterminado        | False                                                      |
| Sistema mínimo | Windows 2000                                               |



 

### <a name="applicationproxyservername"></a>ApplicationProxyServerName



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre de servidor remoto que se usa al exportar el proxy de aplicación. Es este nombre de servidor al que apunta el proxy de aplicación cuando se instala en un equipo cliente. |
| Access         | ReadWrite                                                                                                                                                              |
| Tipo           | String                                                                                                                                                                 |
| Predeterminado        | ""                                                                                                                                                                     |
| Sistema mínimo | Windows 2000                                                                                                                                                           |



 

### <a name="apppartitionid"></a>AppPartitionID



| Entrada | Valor |
|----------------|---------------------------------------------------|
| Descripción    | GUID que representa el identificador de partición de la aplicación. |
| Access         | ReadOnly                                          |
| Tipo           | String                                            |
| Predeterminado        | &lt;Generado&gt;                                 |
| Sistema mínimo | Windows Server 2003                               |



 

### <a name="authentication"></a>Autenticación



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Establece el nivel de autenticación para las llamadas, con valores correspondientes a la configuración de autenticación de llamada a procedimiento remoto (RPC). Cuando se elige COMAdminAuthenticationDefault, se usa la configuración de la propiedad DefaultAuthenticationLevel dentro de [**la colección LocalComputer.**](localcomputer.md) |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                             |
| Tipo           | Valores largos posibles:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)                                              |
| Valor predeterminado        | COMAdminAuthenticationPacket (4)                                                                                                                                                                                                                                                                      |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                          |



 

> [!Note]  
> Para las aplicaciones de biblioteca (en proceso), la única configuración válida aquí es COMAdminAuthenticationDefault y COMAdminAuthenticationNone. Se recomienda usar las constantes de la enumeración y no los valores numéricos.

 

### <a name="authenticationcapability"></a>AuthenticationCapability



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina qué identidad se presenta cuando se suplantan las llamadas.                                                                                                                                                                      |
| Access         | ReadWrite                                                                                                                                                                                                                               |
| Tipo           | Valores largos posibles:COMAdminAuthenticationCapabilitiesNone (0x0)COMAdminAuthenticationCapabilitiesSecureReference (0x2)COMAdminAuthenticationCapabilitiesStaticCloaking (0x20)COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40) |
| Valor predeterminado        | COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)                                                                                                                                                                                |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                            |



 

### <a name="changeable"></a>Cambiable



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina si se permiten cambios en la configuración de la aplicación o en los de sus componentes, ya sea mediante programación o a través de la herramienta de administración servicios de componentes. |
| Access         | ReadWrite                                                                                                                                                                     |
| Tipo           | Bool                                                                                                                                                                          |
| Valor predeterminado        | True                                                                                                                                                                          |
| Sistema mínimo | Windows 2000                                                                                                                                                                  |



 

### <a name="commandline"></a>CommandLine



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Cadena de línea de comandos para su uso en la depuración. La aplicación se puede iniciar en un depurador con la línea de comandos especificada. |
| Access         | ReadWrite                                                                                                                  |
| Tipo           | String                                                                                                                     |
| Predeterminado        | ""                                                                                                                         |
| Sistema mínimo | Windows 2000                                                                                                               |



 

### <a name="concurrentapps"></a>ConcurrentApps



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------|
| Descripción    | Especifica el número máximo de aplicaciones agrupables que se pueden ejecutar simultáneamente. |
| Access         | ReadWrite                                                                        |
| Tipo           | Long (1-1048576)                                                                 |
| Valor predeterminado        | 1                                                                                |
| Sistema mínimo | Windows XP                                                                       |



 

### <a name="createdby"></a>CreatedBy



| Entrada | Valor |
|----------------|---------------------------------------------------------------|
| Descripción    | Cadena de información para describir quién creó la aplicación. |
| Access         | ReadWrite                                                     |
| Tipo           | String                                                        |
| Predeterminado        | ""                                                            |
| Sistema mínimo | Windows 2000                                                  |



 

### <a name="crmenabled"></a>CRMEnabled



| Entrada | Valor |
|----------------|------------------------------------------------------------------|
| Descripción    | Determina si la opción Compensating Resource Manager está habilitada. |
| Access         | ReadWrite                                                        |
| Tipo           | Bool                                                             |
| Valor predeterminado        | False                                                            |
| Sistema mínimo | Windows 2000                                                     |



 

### <a name="crmlogfile"></a>CRMLogFile



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------|
| Descripción    | Nombre y ruta de acceso del archivo para mantener el registro del administrador de recursos de compensación (CRM). |
| Access         | ReadWrite                                                                              |
| Tipo           | String                                                                                 |
| Predeterminado        | ""                                                                                     |
| Sistema mínimo | Windows 2000                                                                           |



 

### <a name="deleteable"></a>Eliminable



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Establece si la aplicación se puede eliminar, ya sea mediante programación o a través de la herramienta de administración servicios de componentes. |
| Access         | ReadWrite                                                                                                                   |
| Tipo           | Bool                                                                                                                        |
| Valor predeterminado        | True                                                                                                                        |
| Sistema mínimo | Windows 2000                                                                                                                |



 

### <a name="description"></a>Descripción



| Entrada | Valor |
|----------------|----------------------------|
| Descripción    | Describe la aplicación. |
| Access         | ReadWrite                  |
| Tipo           | String                     |
| Predeterminado        | ""                         |
| Sistema mínimo | Windows 2000               |



 

### <a name="dumpenabled"></a>DumpEnabled



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------|
| Descripción    | Habilita el volcado del estado de una aplicación COM+ en el momento del error en un directorio designado. |
| Access         | ReadWrite                                                                                             |
| Tipo           | Bool                                                                                                  |
| Valor predeterminado        | False                                                                                                 |
| Sistema mínimo | Windows XP                                                                                            |



 

> [!Note]  
> A partir Windows Server 2003, solo los administradores tienen privilegios de acceso de lectura a los archivos de volcado com+.

 

### <a name="dumponexception"></a>DumpOnException



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Habilita el volcado del estado de una aplicación COM+ cuando la aplicación provoca una excepción no controlada y el tiempo de ejecución de COM+ finaliza. |
| Access         | ReadWrite                                                                                                                                     |
| Tipo           | Bool                                                                                                                                          |
| Valor predeterminado        | False                                                                                                                                         |
| Sistema mínimo | Windows XP                                                                                                                                    |



 

### <a name="dumponfailfast"></a>DumpOnFailfast



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------|
| Descripción    | Habilita el volcado del estado de una aplicación COM+ cuando se produce un error en la aplicación. |
| Access         | ReadWrite                                                                       |
| Tipo           | Bool                                                                            |
| Valor predeterminado        | False                                                                           |
| Sistema mínimo | Windows XP                                                                      |



 

### <a name="dumppath"></a>DumpPath



| Entrada | Valor |
|----------------|--------------------------------------------------------------|
| Descripción    | Ruta de acceso del directorio en el que se guardan los archivos de volcado. |
| Access         | ReadWrite                                                    |
| Tipo           | String                                                       |
| Predeterminado        | "%systemroot% \\ system32 \\ com \\ dmp"                           |
| Sistema mínimo | Windows XP                                                   |



 

> [!Note]  
> A partir Windows Server 2003, solo los administradores tienen privilegios de acceso de lectura a los archivos de volcado com+.

 

### <a name="eventsenabled"></a>EventsEnabled



| Entrada | Valor |
|----------------|-----------------------------------------------------------|
| Descripción    | Indica si los eventos están habilitados para la aplicación. |
| Access         | ReadWrite                                                 |
| Tipo           | Bool                                                      |
| Valor predeterminado        | True                                                      |
| Sistema mínimo | Windows 2000                                              |



 

### <a name="id"></a>ID



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | GUID que representa la aplicación. Esta propiedad se devuelve cuando se llama al método de propiedad [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección. |
| Access         | WriteOnce                                                                                                                                                            |
| Tipo           | String                                                                                                                                                               |
| Predeterminado        | &lt;Generado&gt;                                                                                                                                                    |
| Sistema mínimo | Windows 2000                                                                                                                                                         |



 

### <a name="identity"></a>Identidad



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Establece la identidad del proceso de servidor para la aplicación. Especifique una cuenta de usuario válida o "Usuario interactivo" para que la aplicación asuma la identidad del usuario actual que ha iniciado sesión. También puede especificar las cadenas "nt authority \\ localservice", "nt authority \\ networkservice" y "nt authority \\ system". La contraseña predeterminada para estas tres cuentas es "" (cadena vacía). |
| Access         |                                                                                                                                                                                                                                                                                                                                                                                    |
| Tipo           |                                                                                                                                                                                                                                                                                                                                                                                    |
| Valor predeterminado        |                                                                                                                                                                                                                                                                                                                                                                                    |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                       |



 

La propiedad Identity no está habilitada para las aplicaciones de biblioteca, que se ejecutan en el proceso de cliente.

La propiedad Password debe establecerse al mismo tiempo que Identity, antes de usar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), porque la contraseña y la identidad se validan antes de guardarse. Si la contraseña y la identidad no se sincronizan, la aplicación no se puede iniciar hasta que un administrador las restablezca.

### <a name="impersonationlevel"></a>ImpersonationLevel



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Establece el nivel de suplantación utilizado para las llamadas realizadas a otras aplicaciones.                                                                                           |
| Access         | ReadWrite                                                                                                                                                     |
| Tipo           | Long Possible values:COMAdminImpersonationAnonymous (1)COMAdminImpersonationIdentify (2)COMAdminImpersonationImpersonate (3)COMAdminImpersonationDelegate (4) |
| Valor predeterminado        | COMAdminImpersonationImpersonate (3)                                                                                                                          |
| Sistema mínimo | Windows 2000                                                                                                                                                  |



 

### <a name="isenabled"></a>IsEnabled



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Si la aplicación o componente COM+ está deshabilitado, IsEnabled es False. Si la aplicación o componente COM+ está habilitado, IsEnabled es True. |
| Access         | ReadWrite                                                                                                                                 |
| Tipo           | Bool                                                                                                                                      |
| Valor predeterminado        | True                                                                                                                                      |
| Sistema mínimo | Windows XP                                                                                                                                |



 

### <a name="issystem"></a>IsSystem



| Entrada | Valor |
|----------------|--------------------------------------|
| Descripción    | Identifica las aplicaciones del sistema COM+. |
| Access         | ReadOnly                             |
| Tipo           | Bool                                 |
| Valor predeterminado        | False                                |
| Sistema mínimo | Windows 2000                         |



 

### <a name="maxdumpcount"></a>MaxDumpCount



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------|
| Descripción    | Indica el número máximo de archivos que se generarán antes de que se sobrescriba. |
| Access         | ReadWrite                                                                        |
| Tipo           | Long (1-200)                                                                     |
| Predeterminado        | 5                                                                                |
| Sistema mínimo | Windows XP                                                                       |



 

### <a name="name"></a>Nombre



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre de la aplicación. Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se [**llama al método**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) de propiedad Name en un objeto de esta colección. |
| Access         | ReadWrite                                                                                                                                                                                                                            |
| Tipo           | String                                                                                                                                                                                                                               |
| Predeterminado        | "Nueva aplicación"                                                                                                                                                                                                                    |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                         |



 

> [!Note]  
> Se deben elegir nombres únicos para las aplicaciones. Si se crean varias aplicaciones con el mismo nombre, puede interferir con la referencia a las aplicaciones por nombre, lo que da lugar a un comportamiento imprevisible.

 

### <a name="password"></a>Contraseña



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------|
| Descripción    | Establece la contraseña usada por el proceso de servidor para iniciar sesión en la identidad. |
| Access         | WriteOnly                                                                  |
| Tipo           | String                                                                     |
| Predeterminado        | ""                                                                         |
| Sistema mínimo | Windows 2000                                                               |



 

La contraseña debe establecerse al mismo tiempo que Identity, antes de usar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), porque la contraseña y la identidad se validan antes de guardarse. Si la contraseña y la identidad no se sincronizan, la aplicación no se puede iniciar hasta que un administrador las restablezca.

### <a name="qcauthenticatemsgs"></a>QCAuthenticateMsgs



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica en qué circunstancias se autentican las solicitudes en cola a una aplicación.                                                 |
| Access         | ReadWrite                                                                                                                               |
| Tipo           | Long Possible values:COMAdminQCMessageAuthenticateSecureApps (0)COMAdminQCMessageAuthenticateOff (1)COMAdminQCMessageAuthenticateOn (2) |
| Valor predeterminado        | COMAdminQCMessageAuthenticateSecureApps (0)                                                                                             |
| Sistema mínimo | Windows XP                                                                                                                              |



 

### <a name="qclistenermaxthreads"></a>QCListenerMaxThreads



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica el número máximo de subprocesos de escucha simultáneos. El intervalo válido para esta propiedad es de 0 a 1000. Para una aplicación recién creada, la configuración se deriva del algoritmo utilizado actualmente para determinar el número predeterminado de subprocesos de escucha: 16 veces el número de CPU en el servidor. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                 |
| Tipo           | Long (0-1000)                                                                                                                                                                                                                                                                                             |
| Valor predeterminado        | 0                                                                                                                                                                                                                                                                                                         |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                |



 

> [!Note]  
> Esta propiedad también está disponible con la funcionalidad de lectura y escritura en la pestaña **Cola** de la herramienta administrativa Servicios de componentes.

 

### <a name="queuelistenerenabled"></a>QueueListenerEnabled



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica si el agente de escucha de componentes en cola está habilitado para la aplicación. Si está habilitada, el agente de escucha se inicia cuando se inicia la aplicación. Esta propiedad solo tiene efecto si QueuingEnabled está establecido en True. |
| Access         | ReadWrite                                                                                                                                                                                                            |
| Tipo           | Bool                                                                                                                                                                                                                 |
| Valor predeterminado        | False                                                                                                                                                                                                                |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                         |



 

### <a name="queuingenabled"></a>QueuingEnabled



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------|
| Descripción    | Indica si el servicio componentes en cola de COM+ está habilitado para la aplicación. |
| Access         | ReadWrite                                                                            |
| Tipo           | Bool                                                                                 |
| Valor predeterminado        | False                                                                                |
| Sistema mínimo | Windows 2000                                                                         |



 

### <a name="recycleactivationlimit"></a>RecycleActivationLimit



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica el número máximo de activaciones de objetos configurados en la aplicación que se aceptan antes de reciclar el proceso. El número predeterminado de activaciones es 0. |
| Access         | ReadWrite                                                                                                                                                            |
| Tipo           | Long (0-1048576)                                                                                                                                                     |
| Valor predeterminado        | 0                                                                                                                                                                    |
| Sistema mínimo | Windows XP                                                                                                                                                           |



 

### <a name="recyclecalllimit"></a>RecycleCallLimit



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica el número máximo de llamadas para permitir que los objetos configurados en la aplicación acepten antes de reciclar el proceso. El número predeterminado de llamadas es 0. |
| Access         | ReadWrite                                                                                                                                                      |
| Tipo           | Long (0-1048576)                                                                                                                                               |
| Valor predeterminado        | 0                                                                                                                                                              |
| Sistema mínimo | Windows XP                                                                                                                                                     |



 

### <a name="recycleexpirationtimeout"></a>RecycleExpirationTimeout



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica la cantidad de tiempo (en minutos) para permitir que un proceso reciclado se ejecute antes de apagarlo. La cuenta atrás comienza inmediatamente después de reciclar el proceso. El tiempo de espera máximo de expiración es de 1440 minutos (24 horas) y el valor predeterminado es 15 minutos. |
| Access         | ReadWrite                                                                                                                                                                                                                                                        |
| Tipo           | Long (1-1440)                                                                                                                                                                                                                                                    |
| Valor predeterminado        | 15                                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                       |



 

### <a name="recyclelifetimelimit"></a>RecycleLifetimeLimit



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica el número máximo de minutos para permitir que un proceso se ejecute antes de reciclarlo. El límite máximo de duración es de 30240 minutos (21 días) y el valor predeterminado es 0 minutos. |
| Access         | ReadWrite                                                                                                                                                                   |
| Tipo           | Long (0-30240)                                                                                                                                                              |
| Valor predeterminado        | 0                                                                                                                                                                           |
| Sistema mínimo | Windows XP                                                                                                                                                                  |



 

### <a name="recyclememorylimit"></a>RecycleMemoryLimit



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica la cantidad máxima de uso de memoria (en kilobytes) permitida para un proceso antes de reciclarse. Si el uso de memoria del proceso supera el número especificado durante un período superior a un minuto, el proceso se recicla. La cantidad predeterminada de uso de memoria es de 0 KB. |
| Access         | ReadWrite                                                                                                                                                                                                                                                              |
| Tipo           | Long (0-1048576)                                                                                                                                                                                                                                                       |
| Valor predeterminado        | 0                                                                                                                                                                                                                                                                      |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                             |



 

### <a name="replicable"></a>Replicable



| Entrada | Valor |
|----------------|------------------------------------------------------|
| Descripción    | Indica si la aplicación se puede replicar. |
| Access         | ReadWrite                                            |
| Tipo           | Bool                                                 |
| Valor predeterminado        | True                                                 |
| Sistema mínimo | Windows XP                                           |



 

### <a name="runforever"></a>RunForever



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Permite que un proceso de servidor continúe si una aplicación está inactiva. Si se establece en True, el proceso del servidor no se cierra cuando se deja inactivo. Si se establece en False, el proceso se cierra según el valor establecido por la propiedad ShutdownAfter. RunForever no está habilitado para las aplicaciones de biblioteca (en proceso). |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                     |
| Valor predeterminado        | False                                                                                                                                                                                                                                                                                                    |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                             |



 

### <a name="servicename"></a>ServiceName



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre del servicio correspondiente a la aplicación configurada para ejecutarse como una aplicación de servicio. Si este valor es **NULL,** la aplicación no está configurada para ejecutarse como servicio. De lo contrario, la información de configuración del servicio se puede encontrar mediante el nombre del servicio. |
| Access         | ReadOnly                                                                                                                                                                                                                                                                         |
| Tipo           | String                                                                                                                                                                                                                                                                           |
| Predeterminado        | ""                                                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                       |



 

### <a name="shutdownafter"></a>ShutdownAfter



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Establece el retraso antes de apagar un proceso de servidor después de que esté inactivo. La latencia de apagado oscila entre 0 y 1440 minutos (24 horas). Si RunForever está establecido en True, esta propiedad se omite. ShutdownAfter no está habilitado para las aplicaciones de biblioteca (en proceso). |
| Access         | ReadWrite                                                                                                                                                                                                                                                          |
| Tipo           | Long (0-1440)                                                                                                                                                                                                                                                      |
| Valor predeterminado        | 3                                                                                                                                                                                                                                                                  |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                       |



 

### <a name="soapactivated"></a>SoapActivated



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------|
| Descripción    | Indica si esta aplicación se expone para su consumo a través del protocolo SOAP. |
| Access         | ReadWrite                                                                            |
| Tipo           | Bool                                                                                 |
| Valor predeterminado        | False                                                                                |
| Sistema mínimo | Windows Server 2003                                                                  |



 

### <a name="soapbaseurl"></a>SoapBaseUrl



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------|
| Descripción    | Punto de conexión de dirección URL en el que esta aplicación se expone a través del protocolo SOAP. |
| Access         | ReadWrite                                                                    |
| Tipo           | String                                                                       |
| Predeterminado        | ""                                                                           |
| Sistema mínimo | Windows Server 2003                                                          |



 

### <a name="soapmailto"></a>SoapMailTo



| Entrada | Valor |
|----------------|-------------------------------------------------------------------------------|
| Descripción    | Dirección de correo electrónico en la que se expone esta aplicación a través del protocolo SOAP. |
| Access         | ReadWrite                                                                     |
| Tipo           | String                                                                        |
| Predeterminado        | ""                                                                            |
| Sistema mínimo | Windows Server 2003                                                           |



 

### <a name="soapvroot"></a>SoapVRoot



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| Descripción    | Directorio raíz virtual de IIS en el que residen los scripts de acceso que exponen la aplicación a través del protocolo SOAP. |
| Access         | ReadWrite                                                                                                            |
| Tipo           | String                                                                                                               |
| Predeterminado        | ""                                                                                                                   |
| Sistema mínimo | Windows Server 2003                                                                                                  |



 

### <a name="srpenabled"></a>SRPEnabled



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina la directiva de restricción de software (SRP) para la aplicación. Si se establece en True, se usa la propiedad SRPTrustLevel para la aplicación. Si se establece en False, se usan las directivas de restricción de software de la configuración de seguridad local. La configuración de seguridad local se controla mediante el complemento Directiva de seguridad local del Microsoft Management Console. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                             |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                                                  |
| Valor predeterminado        | False                                                                                                                                                                                                                                                                                                                                                                 |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                            |



 

### <a name="srptrustlevel"></a>SRPTrustLevel



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica el nivel de confianza de la directiva de restricción de software (SRP) de la aplicación. Esta propiedad solo se usa si la propiedad SRPEnabled está establecida en True. El nivel de confianza de SRP hace referencia al nivel de confianza que está dispuesto a dar a una aplicación. Un nivel de confianza de SRP sin restricciones corresponde al valor de enumeración SAFER LEVELID FULLYTRUSTED, mientras que un nivel de confianza de SRP no permitido corresponde al valor de enumeración \_ \_ SAFER \_ LEVELID \_ DISALLOWED. La enumeración de los niveles de confianza se define en Winsafer.h. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Tipo           | Long Possible values:SAFER \_ LEVELID \_ DISALLOWED (0x0)SAFER \_ LEVELID \_ FULLYTRUSTED (0x40000)                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Valor predeterminado        | LEVELID \_ MÁS SEGURO DE PLENA CONFIANZA \_ (0x40000)                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

Una aplicación en la que esté dispuesto a confiar con acceso sin restricciones debe tener asociada la seguridad más estricta. Las aplicaciones que no están restringidas solo pueden cargar componentes sin restricciones, mientras que las aplicaciones no permitidas no podrán ejecutarse y, por tanto, no podrán cargar ningún componente.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
