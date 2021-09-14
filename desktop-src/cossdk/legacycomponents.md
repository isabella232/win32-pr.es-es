---
description: Contiene un objeto para cada componente no configurado de la colección Applications. Los componentes no configurados no pueden hacer uso de servicios COM+. Las propiedades expuestas por estos objetos mantienen la configuración realizada en el nivel de componente.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361687"
---
# <a name="legacycomponents-collection"></a>Colección LegacyComponents

Contiene un objeto para cada componente no configurado de la colección Applications. Los componentes no configurados no pueden hacer uso de servicios COM+. Las propiedades expuestas por estos objetos mantienen la configuración realizada en el nivel de componente.

Esta colección admite el [**método Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection,**](comadmincatalogcollection.md) pero no [**el método Add.**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) Para instalar o importar componentes en una aplicación, use métodos en el [**objeto COMAdminCatalog.**](comadmincatalog.md)

## <a name="members"></a>Members

La **colección LegacyComponents** hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde las siguientes colecciones:

-   [**Aplicaciones**](applications.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades dentro de la colección:

-   [AccessPermissions](#accesspermissions)
-   [ActivateAtStorage](#activateatstorage)
-   [AppID](#appid)
-   [AppName](#appname)
-   [AuthenticationLevel](#authenticationlevel)
-   [Bitness](#bitness)
-   [Classname](#classname)
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
| Acceso         | ReadWrite                                                                       |
| Tipo           | String                                                                          |
| Predeterminado        | N/D                                                                             |
| Sistema mínimo | Windows XP                                                                      |



 

### <a name="activateatstorage"></a>ActivateAtStorage



| Entrada | Value |
|----------------|------------------------------------------------------------------|
| Descripción    | Especifica si se debe ejecutar el servidor en la máquina de almacenamiento de datos. |
| Acceso         | ReadWrite                                                        |
| Tipo           | Valores posibles de cadena:"N""Y"                                    |
| Valor predeterminado        | "N"                                                              |
| Sistema mínimo | Windows XP                                                       |



 

### <a name="appid"></a>AppID



| Entrada | Value |
|----------------|---------------------|
| Descripción    | El id. de aplicación. |
| Acceso         | ReadOnly            |
| Tipo           | String              |
| Predeterminado        | N/D                 |
| Sistema mínimo | Windows XP          |



 

### <a name="appname"></a>AppName



| Entrada | Value |
|----------------|------------------------------|
| Descripción    | Nombre de la aplicación. |
| Acceso         | ReadOnly                     |
| Tipo           | String                       |
| Predeterminado        | N/D                          |
| Sistema mínimo | Windows XP                   |



 

### <a name="authenticationlevel"></a>AuthenticationLevel



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Establece el nivel de autenticación para las llamadas, con valores correspondientes a la configuración de autenticación de llamada a procedimiento remoto (RPC). Cuando se elige COMAdminAuthenticationDefault, se usa la configuración de la propiedad DefaultAuthenticationLevel dentro de [**la colección LocalComputer.**](localcomputer.md) |
| Acceso         | ReadWrite                                                                                                                                                                                                                                                                                             |
| Tipo           | Valores largos posibles:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)                                              |
| Valor predeterminado        | COMAdminAuthenticationDefault (0)                                                                                                                                                                                                                                                                     |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> Se recomienda usar las constantes de la enumeración y no los valores numéricos.

 

### <a name="bitness"></a>Valor de bits



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Representa el tipo de bits binario del componente. En sistemas que usan componentes de 64 Windows bits, esta propiedad distingue entre componentes de 64 bits y componentes de 32 bits. |
| Acceso         | ReadOnly                                                                                                                                                              |
| Tipo           | Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)                                                                                         |
| Valor predeterminado        | N/D                                                                                                                                                                   |
| Sistema mínimo | Windows XP                                                                                                                                                            |



 

### <a name="classname"></a>ClassName



| Entrada | Value |
|----------------|------------------------|
| Descripción    | Nombre de la clase. |
| Acceso         | ReadOnly               |
| Tipo           | String                 |
| Predeterminado        | N/D                    |
| Sistema mínimo | Windows XP             |



 

### <a name="clsid"></a>CLSID



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | GUID para el componente. Esta propiedad se devuelve cuando se llama [**al método**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) de propiedad Key en un objeto de esta colección. |
| Acceso         | ReadOnly                                                                                                                                                  |
| Tipo           | String                                                                                                                                                    |
| Predeterminado        | N/D                                                                                                                                                       |
| Sistema mínimo | Windows XP                                                                                                                                                |



 

### <a name="dllsurrogate"></a>DllSurrogate



| Entrada | Value |
|----------------|------------------------------------------------------------|
| Descripción    | Especifica la ruta de acceso completa a una aplicación de servidor suplente. |
| Acceso         | ReadWrite                                                  |
| Tipo           | String                                                     |
| Predeterminado        | N/D                                                        |
| Sistema mínimo | Windows XP                                                 |



 

### <a name="inprochandler32"></a>InprocHandler32



| Entrada | Value |
|----------------|--------------------------------------------------------------------|
| Descripción    | Especifica la ruta de acceso completa a un archivo DLL de controlador personalizado en proceso de 32 bits. |
| Acceso         | ReadWrite                                                          |
| Tipo           | String                                                             |
| Predeterminado        | N/D                                                                |
| Sistema mínimo | Windows XP                                                         |



 

### <a name="inprocserver32"></a>InprocServer32



| Entrada | Value |
|----------------|------------------------------------------------------------|
| Descripción    | Especifica la ruta de acceso completa a un archivo DLL de servidor en proceso de 32 bits. |
| Acceso         | ReadWrite                                                  |
| Tipo           | String                                                     |
| Predeterminado        | N/D                                                        |
| Sistema mínimo | Windows XP                                                 |



 

### <a name="isenabled"></a>IsEnabled



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Si la aplicación o componente COM+ está deshabilitado, IsEnabled es False. Si la aplicación o componente COM+ está habilitado, IsEnabled es True. |
| Acceso         | ReadWrite                                                                                                                                 |
| Tipo           | Bool                                                                                                                                      |
| Valor predeterminado        | True                                                                                                                                      |
| Sistema mínimo | Windows XP                                                                                                                                |



 

### <a name="launchpermissions"></a>LaunchPermissions



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------|
| Descripción    | Especifica las cuentas de usuario a las que se permite o se deniega el permiso para iniciar este componente. |
| Acceso         | ReadWrite                                                                              |
| Tipo           | String                                                                                 |
| Predeterminado        | N/D                                                                                    |
| Sistema mínimo | Windows XP                                                                             |



 

### <a name="localserver32"></a>LocalServer32



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Especifica la ruta de acceso completa a una aplicación de servidor local de 32 bits. Para ayudar a proteger la seguridad del sistema, use cadenas entre comillas en la ruta de acceso para indicar dónde finaliza el nombre de archivo ejecutable y comienzan los argumentos. Por ejemplo, "C: Archivos de programa Archivos de \\ \\ empresaApplication.exe" \\ \\ \\ param1 param2". |
| Acceso         | ReadWrite                                                                                                                                                                                                                                                                                   |
| Tipo           | String                                                                                                                                                                                                                                                                                      |
| Predeterminado        | N/D                                                                                                                                                                                                                                                                                         |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                  |



 

### <a name="localservice"></a>LocalService (Servicio local)



| Entrada | Value |
|----------------|-----------------------------------------------------|
| Descripción    | Especifica la ruta de acceso completa a la aplicación de servicio. |
| Acceso         | ReadWrite                                           |
| Tipo           | String                                              |
| Predeterminado        | N/D                                                 |
| Sistema mínimo | Windows XP                                          |



 

### <a name="password"></a>Contraseña



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Establece la contraseña usada por el proceso del servidor para iniciar sesión en la identidad RunAs especificada. La contraseña debe establecerse al mismo tiempo que la identidad RunAs, antes de usar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), porque la contraseña y la identidad se validan antes de guardarse. Si la contraseña y la identidad no se sincronizan, el componente no se puede iniciar hasta que un administrador los restablezca. |
| Acceso         | WriteOnly                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Tipo           | String                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Predeterminado        | NULL                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="progid"></a>ProgID



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre que identifica el componente. Esta propiedad se devuelve cuando se llama al método de propiedad Name en un objeto de esta colección. |
| Acceso         | ReadOnly                                                                                                                             |
| Tipo           | String                                                                                                                               |
| Predeterminado        | N/D                                                                                                                                  |
| Sistema mínimo | Windows XP                                                                                                                           |



 

### <a name="remoteserver"></a>RemoteServer



| Entrada | Value |
|----------------|---------------------------------------|
| Descripción    | Especifica el equipo del servidor remoto. |
| Acceso         | ReadWrite                             |
| Tipo           | String                                |
| Predeterminado        | N/D                                   |
| Sistema mínimo | Windows XP                            |



 

### <a name="runas"></a>RunAs



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Especifica el usuario con cuya identidad se ejecutará el componente. La contraseña debe establecerse al mismo tiempo que la identidad RunAs, antes de usar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), porque la contraseña y la identidad se validan antes de guardarse. Si la contraseña y la identidad no se sincronizan, el componente no se puede iniciar hasta que un administrador los restablezca. |
| Acceso         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                         |
| Tipo           | String                                                                                                                                                                                                                                                                                                                                                                                            |
| Predeterminado        | N/D                                                                                                                                                                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="serviceparameter"></a>ServiceParameter



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------|
| Descripción    | Especifica los parámetros pasados a la aplicación cuando se invocan como una aplicación de servicio. |
| Acceso         | ReadWrite                                                                                 |
| Tipo           | String                                                                                    |
| Predeterminado        | N/D                                                                                       |
| Sistema mínimo | Windows XP                                                                                |



 

### <a name="srptrustlevel"></a>SRPTrustLevel



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Indica el nivel de confianza de la directiva de restricción de software (SRP) del componente. El nivel de confianza de SRP hace referencia al nivel de confianza que está dispuesto a dar a un componente. Un nivel de confianza de SRP sin restricciones corresponde al valor de enumeración SAFER LEVELID FULLYTRUSTED, mientras que un nivel de confianza de SRP no permitido corresponde al valor de enumeración \_ \_ SAFER \_ LEVELID \_ DISALLOWED. La enumeración de los niveles de confianza se define en Winsafer.h. |
| Acceso         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Tipo           | Long Possible values:SAFER \_ LEVELID \_ DISALLOWED (0x0)SAFER \_ LEVELID \_ FULLYTRUSTED (0x40000)                                                                                                                                                                                                                                                                                                                                         |
| Valor predeterminado        | LEVELID \_ MÁS SEGURO ES TOTALMENTE DE \_ CONFIANZA                                                                                                                                                                                                                                                                                                                                                                                                        |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

Un componente en el que esté dispuesto a confiar con acceso sin restricciones debe tener asociada la seguridad más estricta. Las aplicaciones que no están restringidas solo pueden cargar componentes sin restricciones, mientras que las aplicaciones no permitidas no podrán ejecutarse y, por tanto, no podrán cargar ningún componente.

### <a name="threadingmodel"></a>ThreadingModel



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina cómo se asignan las instancias del componente a los subprocesos para la ejecución de métodos. Los valores corresponden a los modelos de subprocesamiento COM.                                                  |
| Acceso         | ReadOnly                                                                                                                                                                            |
| Tipo           | Valores posibles largos:COMAdminThreadingModelThread (0)COMAdminThreadingModelFree (1)COMAdminThreadingModelMain (2)COMAdminThreadingModelBoth (3)COMAdminThreadingModelNeutral (4) |
| Valor predeterminado        | N/D                                                                                                                                                                                 |
| Sistema mínimo | Windows XP                                                                                                                                                                          |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
