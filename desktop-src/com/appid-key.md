---
title: Clave AppID
description: Agrupa las opciones de configuración de uno o más objetos DCOM en una ubicación centralizada en el registro. Los objetos DCOM hospedados por el mismo archivo ejecutable se agrupan en un AppID para simplificar la administración de opciones de configuración y seguridad comunes.
ms.assetid: 4e3d8c87-e6d7-4b4d-8f72-7180be1e51cf
keywords:
- Clave del registro de AppID COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b283a9cc47907cf418c2d7d6d613d151c7e5c5e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421483"
---
# <a name="appid-key"></a>Clave AppID

Agrupa las opciones de configuración de uno o más objetos DCOM en una ubicación centralizada en el registro. Los objetos DCOM hospedados por el mismo archivo ejecutable se agrupan en un AppID para simplificar la administración de opciones de configuración y seguridad comunes.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ \_Clases de software de máquina local \\ \\ \\ AppID** \\ *{* AppID \_ GUID *}*



| Valor del Registro                                           | Descripción                                                                                                                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessPermission**](accesspermission.md)             | Describe la lista de Access Control (ACL) de las entidades de seguridad que pueden tener acceso a las instancias de esta clase. Esta ACL solo la usan las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). |
| [**ActivateAtStorage**](activateatstorage.md)           | Configura el cliente para crear instancias de objetos en el mismo equipo que el estado persistente que están usando o desde el que se inicializan.                                                                    |
| [**AppID**](appid.md)                                   | Identifica el GUID de AppID que corresponde al ejecutable con nombre.                                                                                                                                             |
| [**AppIDFlags**](appidflags.md)                         | Configura cómo un cliente de un escritorio no predeterminado iniciará o enlazará un servidor COM que está configurado para ejecutarse como "usuario interactivo".                                                              |
| [**AuthenticationLevel**](authenticationlevel.md)       | Establece el nivel de autenticación para las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o para las aplicaciones que llaman a **CoInitializeSecurity** y especifican un AppID.               |
| [**DllSurrogate**](dllsurrogate.md)                     | Permite que los servidores DLL se ejecuten en un proceso suplente. Si se especifica una cadena vacía, se usa el suplente proporcionado por el sistema; de lo contrario, el valor especifica la ruta de acceso del suplente que se va a usar.                 |
| [**DllSurrogateExecutable**](dllsurrogateexecutable.md) | Permite que los servidores DLL se ejecuten en un proceso suplente personalizado, junto con el valor del registro [**DllSurrogate**](dllsurrogate.md) .                                                                          |
| [**Puntos de conexión**](endpoints.md)                           | Configura una aplicación COM para que use un número de puerto TCP especificado para las comunicaciones DCOM.                                                                                                                        |
| [**LaunchPermission**](launchpermission.md)             | Describe la lista de Access Control (ACL) de las entidades de seguridad que pueden iniciar nuevos servidores para esta clase.                                                                                                            |
| [**LoadUserSettings**](loadusersettings.md)             | Determina si COM cargará el perfil de usuario para los servidores COM que se ejecutan como la identidad de la aplicación de inicio.                                                                                           |
| [**LocalService (Servicio local)**](localservice.md)                     | Instala un objeto como una aplicación de servicio.                                                                                                                                                                    |
| [**PreferredServerBitness**](preferredserverbitness.md) | Establece la arquitectura preferida, 32 bits o 64 bits, para este servidor COM.                                                                                                                                         |
| [**RemoteServerName**](remoteservername.md)             | Configura el cliente para solicitar que el objeto se ejecute en un equipo determinado cada vez que se llame a una función de activación para la que no se especifica una estructura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) .              |
| [**ROTFlags**](rotflags.md)                             | Controla el registro de un servidor COM en la tabla de objetos en ejecución (ROT).                                                                                                                                    |
| [**RunAs**](runas.md)                                   | Configura una clase para que se ejecute en una cuenta de usuario específica cuando está activada por un cliente remoto sin escribirse como una aplicación de servicio.                                                                       |
| [**ServiceParameters**](serviceparameters.md)           | Especifica los parámetros de línea de comandos que se van a pasar a un objeto instalado para que lo use COM mediante el valor del registro [**LocalService**](localservice.md) .                                                       |
| [**SRPTrustLevel**](srptrustlevel.md)                   | Establece el nivel de confianza de la Directiva de restricción de software (SRP) para las aplicaciones.                                                                                                                                        |



 

## <a name="remarks"></a>Observaciones

Los AppIDs se asignan a los ejecutables y las clases mediante dos mecanismos diferentes:

-   Usar un identificador único global (GUID) de 128 bits que identifica la clave **AppID** . Una clase indica su AppID correspondiente en la clave [**CLSID**](clsid-key-hklm.md) en un valor con nombre "AppID". Esta asignación se usa durante la activación.
-   Usar un valor con nombre que indica un nombre de archivo ejecutable (por ejemplo, "MYOLDAPP.EXE"). Este valor con nombre es de tipo **reg \_ SZ** y contiene la representación de cadena del AppID asociado al archivo ejecutable. Esta asignación se utiliza para obtener los permisos de acceso y el nivel de autenticación predeterminados.

La clave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde a la clave **\_ \_ raíz de las clases HKEY** , que se conserva por compatibilidad con versiones anteriores de com.

En el caso de los servidores COM, normalmente la asignación se genera y se escribe en el registro durante el proceso de registro o cuando se ejecuta dcomcnfg.exe. Sin embargo, los clientes COM que deseen establecer la seguridad mediante la clave **AppID** deben crear las claves del registro adecuadas y especificar la asignación necesaria llamando a las [funciones del registro](/windows/desktop/SysInfo/registry-functions) o usando Regedit.exe. A continuación, se pueden establecer valores como [**AccessPermission**](accesspermission.md) o [**AuthenticationLevel**](authenticationlevel.md) para el cliente. Por ejemplo, supongamos que el nombre del archivo ejecutable del proceso de cliente es "YourClient.exe" y desea establecer el nivel de autenticación en "none". Usaría Guidgen.exe o Uuidgen.exe para crear el GUID que es el AppID del archivo ejecutable. A continuación, establecería valores en el registro tal como se muestra en el ejemplo siguiente, donde 00000001 representa un nivel de autenticación de "none":

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {MyGuid}
      AuthenticationLevel = 00000001
   MyClient.exe
      AppID = {MyGUID}
```

 

 