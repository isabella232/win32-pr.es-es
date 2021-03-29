---
description: Contiene un objeto para cada componente no configurado en la colección de aplicaciones. Los componentes no configurados no pueden hacer uso de servicios COM+. Las propiedades expuestas por estos objetos contienen la configuración realizada en el nivel de componente.
ms.assetid: 87f3b93f-71aa-4187-88d2-889c13d8bd06
title: Colección LegacyComponents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyComponents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5761950dcb0ceb5c857daf37ba2236733ec30c22
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807280"
---
# <a name="legacycomponents-collection"></a>Colección LegacyComponents

Contiene un objeto para cada componente no configurado en la colección de aplicaciones. Los componentes no configurados no pueden hacer uso de servicios COM+. Las propiedades expuestas por estos objetos contienen la configuración realizada en el nivel de componente.

Esta colección admite el método [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , pero no el método [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) . Para instalar o importar componentes en una aplicación, use métodos en el objeto [**COMAdminCatalog**](comadmincatalog.md) .

## <a name="members"></a>Miembros

La colección **LegacyComponents** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde las colecciones siguientes:

-   [**APLICACIONES**](applications.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:

-   [AccessPermissions](#accesspermissions)
-   [ActivateAtStorage](#activateatstorage)
-   [AppID](#appid)
-   [AppName](#appname)
-   [AuthenticationLevel](#authenticationlevel)
-   [Bits](#bitness)
-   [ClassName](#classname)
-   [CLSID](#clsid)
-   [DllSurrogate](#dllsurrogate)
-   [InprocHandler32](#inprochandler32)
-   [InprocServer32](#inprocserver32)
-   [IsEnabled](#isenabled)
-   [LaunchPermissions](#launchpermissions)
-   [LocalServer32](#localserver32)
-   [LocalService (Servicio local)](#localservice)
-   [Contraseña](#password)
-   [ProgID](#progid)
-   [RemoteServer](#remoteserver)
-   [RunAs](#runas)
-   [ServiceParameter](#serviceparameter)
-   [SRPTrustLevel](#srptrustlevel)
-   [ThreadingModel](#threadingmodel)

### <a name="accesspermissions"></a>AccessPermissions



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------|
| Descripción    | Especifica las cuentas de usuario a las que se permite o deniega el acceso al componente. |
| Access         | ReadWrite                                                                       |
| Tipo           | String                                                                          |
| Predeterminado        | N/D                                                                             |
| Sistema mínimo | Windows XP                                                                      |



 

### <a name="activateatstorage"></a>ActivateAtStorage



| Entrada | Value |
|----------------|------------------------------------------------------------------|
| Descripción    | Especifica si se debe ejecutar el servidor en la máquina de almacenamiento de datos. |
| Access         | ReadWrite                                                        |
| Tipo           | Valores de cadena posibles: "N" "Y"                                    |
| Valor predeterminado        | "N"                                                              |
| Sistema mínimo | Windows XP                                                       |



 

### <a name="appid"></a>AppID



| Entrada | Value |
|----------------|---------------------|
| Descripción    | El id. de aplicación. |
| Access         | ReadOnly            |
| Tipo           | String              |
| Predeterminado        | N/D                 |
| Sistema mínimo | Windows XP          |



 

### <a name="appname"></a>AppName



| Entrada | Value |
|----------------|------------------------------|
| Descripción    | Nombre de la aplicación. |
| Access         | ReadOnly                     |
| Tipo           | String                       |
| Predeterminado        | N/D                          |
| Sistema mínimo | Windows XP                   |



 

### <a name="authenticationlevel"></a>AuthenticationLevel



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Establece el nivel de autenticación de las llamadas, con los valores correspondientes a la configuración de autenticación de llamada a procedimiento remoto (RPC). Cuando se elige COMAdminAuthenticationDefault, se usa el valor de la propiedad DefaultAuthenticationLevel de la colección [**LocalComputer**](localcomputer.md) . |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                             |
| Tipo           | Valores posibles largos: COMAdminAuthenticationDefault (0) COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)                                              |
| Valor predeterminado        | COMAdminAuthenticationDefault (0)                                                                                                                                                                                                                                                                     |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> Se recomienda usar las constantes en la enumeración y no los valores numéricos.

 

### <a name="bitness"></a>Valor de bits



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Representa el tipo de bits binario del componente. En los sistemas que usan Windows de 64 bits, esta propiedad distingue entre los componentes de 64 bits y los componentes de 32 bits. |
| Access         | ReadOnly                                                                                                                                                              |
| Tipo           | Valores posibles largos: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0X2)                                                                                         |
| Valor predeterminado        | N/D                                                                                                                                                                   |
| Sistema mínimo | Windows XP                                                                                                                                                            |



 

### <a name="classname"></a>ClassName



| Entrada | Value |
|----------------|------------------------|
| Descripción    | Nombre de la clase. |
| Access         | ReadOnly               |
| Tipo           | String                 |
| Predeterminado        | N/D                    |
| Sistema mínimo | Windows XP             |



 

### <a name="clsid"></a>CLSID



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | GUID del componente. Esta propiedad se devuelve cuando se llama al método de propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección. |
| Access         | ReadOnly                                                                                                                                                  |
| Tipo           | String                                                                                                                                                    |
| Predeterminado        | N/D                                                                                                                                                       |
| Sistema mínimo | Windows XP                                                                                                                                                |



 

### <a name="dllsurrogate"></a>DllSurrogate



| Entrada | Value |
|----------------|------------------------------------------------------------|
| Descripción    | Especifica la ruta de acceso completa a una aplicación de servidor de surragate. |
| Access         | ReadWrite                                                  |
| Tipo           | String                                                     |
| Predeterminado        | N/D                                                        |
| Sistema mínimo | Windows XP                                                 |



 

### <a name="inprochandler32"></a>InprocHandler32



| Entrada | Value |
|----------------|--------------------------------------------------------------------|
| Descripción    | Especifica la ruta de acceso completa a un archivo DLL de controlador personalizado en proceso de 32 bits. |
| Access         | ReadWrite                                                          |
| Tipo           | String                                                             |
| Predeterminado        | N/D                                                                |
| Sistema mínimo | Windows XP                                                         |



 

### <a name="inprocserver32"></a>InprocServer32



| Entrada | Value |
|----------------|------------------------------------------------------------|
| Descripción    | Especifica la ruta de acceso completa a un archivo DLL de servidor en proceso de 32 bits. |
| Access         | ReadWrite                                                  |
| Tipo           | String                                                     |
| Predeterminado        | N/D                                                        |
| Sistema mínimo | Windows XP                                                 |



 

### <a name="isenabled"></a>IsEnabled



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Si el componente o la aplicación COM+ está deshabilitado, IsEnabled es false. Si el componente o la aplicación COM+ está habilitado, IsEnabled es true. |
| Access         | ReadWrite                                                                                                                                 |
| Tipo           | Bool                                                                                                                                      |
| Valor predeterminado        | True                                                                                                                                      |
| Sistema mínimo | Windows XP                                                                                                                                |



 

### <a name="launchpermissions"></a>LaunchPermissions



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------|
| Descripción    | Especifica las cuentas de usuario a las que se permite o se deniega el permiso para iniciar este componente. |
| Access         | ReadWrite                                                                              |
| Tipo           | String                                                                                 |
| Predeterminado        | N/D                                                                                    |
| Sistema mínimo | Windows XP                                                                             |



 

### <a name="localserver32"></a>LocalServer32



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Especifica la ruta de acceso completa a una aplicación de servidor local de 32 bits. Para ayudar a proteger la seguridad del sistema, utilice cadenas entre comillas en la ruta de acceso para indicar dónde finaliza el nombre del archivo ejecutable y los argumentos comienzan. Por ejemplo, " \\ C: archivos de la \\ compañía de archivos de programa \\ \\Application.exe\\ " parám1 parám2 ". |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                   |
| Tipo           | String                                                                                                                                                                                                                                                                                      |
| Predeterminado        | N/D                                                                                                                                                                                                                                                                                         |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                  |



 

### <a name="localservice"></a>LocalService (Servicio local)



| Entrada | Value |
|----------------|-----------------------------------------------------|
| Descripción    | Especifica la ruta de acceso completa a la aplicación de servicio. |
| Access         | ReadWrite                                           |
| Tipo           | String                                              |
| Predeterminado        | N/D                                                 |
| Sistema mínimo | Windows XP                                          |



 

### <a name="password"></a>Contraseña



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Establece la contraseña utilizada por el proceso de servidor para iniciar sesión con la identidad de ejecución especificada. La contraseña debe establecerse al mismo tiempo que la identidad runas, antes de usar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), ya que la contraseña y la identidad se validan antes de guardarse. Si la contraseña y la identidad no se sincronizan, el componente no se puede iniciar hasta que los restablezca un administrador. |
| Access         | WriteOnly                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Tipo           | String                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Predeterminado        | NULL                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="progid"></a>ProgID



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre que identifica el componente. Esta propiedad se devuelve cuando se llama al método de la propiedad Name en un objeto de esta colección. |
| Access         | ReadOnly                                                                                                                             |
| Tipo           | String                                                                                                                               |
| Predeterminado        | N/D                                                                                                                                  |
| Sistema mínimo | Windows XP                                                                                                                           |



 

### <a name="remoteserver"></a>RemoteServer



| Entrada | Value |
|----------------|---------------------------------------|
| Descripción    | Especifica el equipo del servidor remoto. |
| Access         | ReadWrite                             |
| Tipo           | String                                |
| Predeterminado        | N/D                                   |
| Sistema mínimo | Windows XP                            |



 

### <a name="runas"></a>RunAs



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Especifica el usuario bajo cuya identidad se ejecutará el componente. La contraseña debe establecerse al mismo tiempo que la identidad runas, antes de usar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), ya que la contraseña y la identidad se validan antes de guardarse. Si la contraseña y la identidad no se sincronizan, el componente no se puede iniciar hasta que los restablezca un administrador. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                         |
| Tipo           | String                                                                                                                                                                                                                                                                                                                                                                                            |
| Predeterminado        | N/D                                                                                                                                                                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="serviceparameter"></a>ServiceParameter



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------|
| Descripción    | Especifica los parámetros que se pasan a la aplicación cuando se invoca como una aplicación de servicio. |
| Access         | ReadWrite                                                                                 |
| Tipo           | String                                                                                    |
| Predeterminado        | N/D                                                                                       |
| Sistema mínimo | Windows XP                                                                                |



 

### <a name="srptrustlevel"></a>SRPTrustLevel



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica el nivel de confianza de la Directiva de restricción de software (SRP) del componente. El nivel de confianza de SRP hace referencia al nivel de confianza que desea dar a un componente. Un nivel de confianza SRP sin restricciones se corresponde con \_ el \_ valor de enumeración LEVELID FULLYTRUSTED más seguro, mientras que un nivel de confianza SRP no permitido corresponde al \_ valor de enumeración de LEVELID no \_ permitido. La enumeración para los niveles de confianza se define en Winsafer. h. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Tipo           | Valores posibles largos: LEVELID de seguridad no \_ \_ permitido (0X0) Safe \_ LEVELID \_ FULLYTRUSTED (0x40000)                                                                                                                                                                                                                                                                                                                                         |
| Valor predeterminado        | \_FULLYTRUSTED LEVELID \_ Safe                                                                                                                                                                                                                                                                                                                                                                                                        |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

Un componente que esté dispuesto a confiar en el acceso sin restricciones debe tener la seguridad más estricta asociada. Las aplicaciones que no están restringidas pueden cargar solo componentes no restringidos, mientras que las aplicaciones no permitidas no podrán ejecutarse y, por lo tanto, no podrán cargar ningún componente.

### <a name="threadingmodel"></a>ThreadingModel



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina cómo se asignan las instancias del componente a los subprocesos para la ejecución del método. Los valores corresponden a los modelos de subprocesos COM.                                                  |
| Access         | ReadOnly                                                                                                                                                                            |
| Tipo           | Valores posibles largos: COMAdminThreadingModelApartment (0) COMAdminThreadingModelFree (1) COMAdminThreadingModelMain (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4) |
| Valor predeterminado        | N/D                                                                                                                                                                                 |
| Sistema mínimo | Windows XP                                                                                                                                                                          |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
