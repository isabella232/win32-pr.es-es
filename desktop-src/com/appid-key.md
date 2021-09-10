---
title: Clave appID
description: Agrupa las opciones de configuración de uno o varios objetos DCOM en una ubicación centralizada del Registro. Los objetos DCOM hospedados por el mismo ejecutable se agrupan en un AppID para simplificar la administración de valores comunes de seguridad y configuración.
ms.assetid: 4e3d8c87-e6d7-4b4d-8f72-7180be1e51cf
keywords:
- Com de clave del Registro AppID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b283a9cc47907cf418c2d7d6d613d151c7e5c5e6
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369536"
---
# <a name="appid-key"></a>Clave appID

Agrupa las opciones de configuración de uno o varios objetos DCOM en una ubicación centralizada del Registro. Los objetos DCOM hospedados por el mismo ejecutable se agrupan en un AppID para simplificar la administración de valores comunes de seguridad y configuración.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Clases de SOFTWARE DE MÁQUINA LOCAL \_ \\ \\ \\ AppID** \\ *{* AppID \_ GUID *}*



| Valor del Registro                                           | Descripción                                                                                                                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessPermission**](accesspermission.md)             | Describe la lista Access Control (ACL) de las entidades de seguridad que pueden tener acceso a las instancias de esta clase. Esta ACL solo la usan las aplicaciones que no llaman a [**CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) |
| [**ActivateAtStorage**](activateatstorage.md)           | Configura el cliente para crear instancias de objetos en el mismo equipo que el estado persistente que usan o desde el que se inicializan.                                                                    |
| [**Appid**](appid.md)                                   | Identifica el GUID de AppID que corresponde al ejecutable con nombre.                                                                                                                                             |
| [**AppIDFlags**](appidflags.md)                         | Configura cómo un cliente inicia o enlaza un servidor COM configurado para ejecutarse como "usuario interactivo" en un escritorio no predeterminado.                                                              |
| [**AuthenticationLevel**](authenticationlevel.md)       | Establece el nivel de autenticación para las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o para las aplicaciones que llaman a **CoInitializeSecurity** y especifican un AppID.               |
| [**DllSurrogate**](dllsurrogate.md)                     | Permite que los servidores DLL se ejecuten en un proceso suplente. Si se especifica una cadena vacía, se usa el suplente proporcionado por el sistema; De lo contrario, el valor especifica la ruta de acceso del suplente que se va a usar.                 |
| [**DllSurrogateExecutable**](dllsurrogateexecutable.md) | Permite que los servidores DLL se ejecuten en un proceso suplente personalizado, junto con el valor del Registro [**DllSurrogate.**](dllsurrogate.md)                                                                          |
| [**Puntos de conexión**](endpoints.md)                           | Configura una aplicación COM para usar un número de puerto TCP especificado para las comunicaciones DCOM.                                                                                                                        |
| [**LaunchPermission**](launchpermission.md)             | Describe la lista Access Control (ACL) de las entidades de seguridad que pueden iniciar nuevos servidores para esta clase.                                                                                                            |
| [**LoadUserSettings**](loadusersettings.md)             | Determina si COM cargará el perfil de usuario para los servidores COM que se ejecutan como identidad de aplicación de usuario de inicio.                                                                                           |
| [**LocalService (Servicio local)**](localservice.md)                     | Instala un objeto como una aplicación de servicio.                                                                                                                                                                    |
| [**PreferredServerBitness**](preferredserverbitness.md) | Establece la arquitectura preferida, de 32 o 64 bits, para este servidor COM.                                                                                                                                         |
| [**RemoteServerName**](remoteservername.md)             | Configura el cliente para solicitar que el objeto se ejecute en un equipo determinado cada vez que se llama a una función de activación para la que no se especifica una estructura [**COSERVERINFO.**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)              |
| [**ROTFlags**](rotflags.md)                             | Controla el registro de un servidor COM en la tabla de objetos en ejecución (ROT).                                                                                                                                    |
| [**RunAs**](runas.md)                                   | Configura una clase para que se ejecute con una cuenta de usuario específica cuando lo active un cliente remoto sin que se escriba como una aplicación de servicio.                                                                       |
| [**ServiceParameters**](serviceparameters.md)           | Especifica los parámetros de línea de comandos que se pasarán a un objeto instalado para su uso por COM a través del valor del Registro [**LocalService.**](localservice.md)                                                       |
| [**SRPTrustLevel**](srptrustlevel.md)                   | Establece el nivel de confianza de la directiva de restricción de software (SRP) para las aplicaciones.                                                                                                                                        |



 

## <a name="remarks"></a>Observaciones

Los appID se asignan a ejecutables y clases mediante dos mecanismos diferentes:

-   Uso de un identificador único global (GUID) de 128 bits que identifica la **clave AppID.** Una clase indica su AppID correspondiente bajo la [**clave CLSID**](clsid-key-hklm.md) en un valor con nombre "AppID". Esta asignación se usa durante la activación.
-   Usar un valor con nombre que indique un nombre ejecutable (como "MYOLDAPP.EXE"). Este valor con nombre es de tipo **REG \_ SZ** y contiene la representación de cadena del AppID asociado al ejecutable. Esta asignación se usa para obtener los permisos de acceso predeterminados y el nivel de autenticación.

La **clave HKEY \_ LOCAL MACHINE \_ SOFTWARE \\ \\ Classes** corresponde a la clave RAÍZ **HKEY \_ CLASSES, \_** que se conservaba por compatibilidad con versiones anteriores de COM.

En el caso de los servidores COM, la asignación normalmente se genera y escribe en el Registro durante el proceso de registro o al ejecutar dcomcnfg.exe. Sin embargo, los clientes COM que desean establecer la seguridad mediante la clave [](/windows/desktop/SysInfo/registry-functions) **AppID** deben crear las claves del Registro adecuadas y especificar la asignación necesaria llamando a las funciones del Registro o Regedit.exe. A continuación, se pueden establecer valores como [**AccessPermission**](accesspermission.md) [**o AuthenticationLevel**](authenticationlevel.md) para el cliente. Por ejemplo, suponga que el nombre del ejecutable para el proceso de cliente es "YourClient.exe" y desea establecer el nivel de autenticación en "None". Usaría Guidgen.exe o Uuidgen.exe para crear el GUID que es el AppID del ejecutable. A continuación, establecería valores en el Registro como se muestra en el ejemplo siguiente, donde 00000001 representa un nivel de autenticación de "None":

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {MyGuid}
      AuthenticationLevel = 00000001
   MyClient.exe
      AppID = {MyGUID}
```

 

 