---
description: Cuando se instala un proveedor de red, la aplicación debe crear las claves y los valores del registro que se describen en este tema.
ms.assetid: cc5a4a7b-02b5-4ecd-967c-de0656f00846
title: Claves del registro de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2e42febe7516060dd61a7b751a33dcf62cb9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002182"
---
# <a name="authentication-registry-keys"></a>Claves del registro de autenticación

Cuando se instala un proveedor de red, la aplicación debe crear las claves y los valores del registro que se describen en este tema. Estas claves y valores proporcionan información al MPR sobre los proveedores de red instalados en el sistema. El MPR comprueba estas claves cuando se inicia y carga los archivos DLL del proveedor de red que encuentra.

Antes de crear un conjunto de claves que contengan información sobre el proveedor de red, debe agregar el nombre de su proveedor de red a la clave de **orden** . Esta clave es una subclave de la siguiente clave:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
```

La clave **Order** contiene un valor único, **ProviderOrder**, que enumera los proveedores instalados y especifica el orden en que se deben probar durante las operaciones que atraviesan los proveedores hasta que se encuentra un proveedor de aceptación.

El valor **ProviderOrder** contiene una lista separada por comas de nombres de clave. Cada nombre de clave de **ProviderOrder** identifica un proveedor de red. Cuando MPR recorre los proveedores, los llama en el orden en que aparecen en esta lista.

El nombre del proveedor establecido en **ProviderOrder** también debe usarse como el nombre de la clave del registro que contiene información sobre ese proveedor. Las claves del registro específicas del proveedor se crean como subclaves de la clave siguiente:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

En otras palabras, los nombres de proveedor especificados en **ProviderOrder** son la ruta de acceso al registro de las claves específicas del proveedor de red, con respecto a la ruta de acceso siguiente:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

Cuando se instala el servicio de proveedor de red, la aplicación de instalación debe agregar una clave de la siguiente manera:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            ProviderName
```

Donde *providerName* es el nombre del proveedor de red tal y como se especifica en el valor **ProviderOrder** de la clave **Order** . El valor de **Grupo** de la clave *providerName* debe establecerse en "NetworkProvider". Esto identifica el servicio como en el grupo de proveedores de red.

También debe crear una subclave de *providerName*, **networkprovider**. Esta clave contiene los siguientes valores que describen el proveedor de red.



| Value                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nombre**<br/>         | Contiene el nombre del proveedor. Este nombre se muestra al usuario como el nombre de la red en los cuadros de diálogo examinar y debe coincidir con el campo **lpProvider** devuelto en las estructuras [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) . Este nombre debe ser una variación del nombre del producto, preferiblemente también con alguna indicación de la empresa, de modo que sea claro y único. Por ejemplo, "MS-LanMan" es un buen nombre, mientras que "The net" sería una opción deficiente.<br/> |
| **ProviderPath**<br/> | Contiene la ruta de acceso completa del archivo DLL que implementa el proveedor de red. MPR llama a [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) en esta ruta de acceso.<br/>                                                                                                                                                                                                                                                                                                                                |



 

Los siguientes valores solo los usan los proveedores de red que admiten las funciones de administración de credenciales, [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) y [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify).



| Value                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Clase**<br/>               | **DWORD** que identifica la clase, o tipo, de la funcionalidad del proveedor que admite este proveedor. Los valores pueden estar Unidos por el operador **o** cuando sea necesario. Los valores válidos son la \_ clase de red WN \_ , la clase de credencial WN, la clase \_ \_ \_ AUTHENT primaria WN y la \_ \_ \_ clase de servicio WN \_ .<br/> Aunque un proveedor puede admitir la funcionalidad principal del autenticador, se usará otro medio para determinar qué autenticador es principal.<br/> **Windows XP/2000:** No se admite el cambio de autenticadores principales, por lo que este valor se omite. <br/> |
| **AuthentProviderPath**<br/> | Este es el nombre de archivo completo para el archivo DLL que exporta las funciones de administración de credenciales. Este valor es útil (pero no obligatorio) solo cuando el proveedor se identifica como una clase de credencial o como un \_ \_ proveedor de clase AUTHENT principal \_ . Si este valor no está presente para un proveedor de esta clase, se espera que las funciones de administración de credenciales se exporten desde el archivo DLL identificado por el valor de ProviderPath. Este valor solo se utiliza si es deseable empaquetar las funciones de red y las funciones del administrador de credenciales en archivos dll independientes.<br/>  |



 

Además de los valores que se usan para registrar proveedores de redes y administradores de credenciales, puede Agregar un valor al registro para registrar un archivo DLL para recibir notificaciones de conexión. Para ello, cree un valor REG \_ Expand \_ en la clave siguiente:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
               Notifyees
```

Este valor debe especificar la ruta de acceso a un archivo DLL que implementa la [API de notificación de conexión](connection-notification-api.md). El nombre de este valor puede ser el que desee, siempre y cuando no se produzca ningún conflicto con los nombres de valor preexistentes.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestran las claves del registro para un sistema que tiene instalados dos proveedores de red: LanmanWorkStation y AnotherNetSvc. AnotherNetSvc también es un administrador de credenciales. En el ejemplo, los nombres de clave están en negrita y los nombres de valor están en cursiva.

**HKEY \_ \_** \\ **Sistema del** equipo local \\ **CurrentControlSet** \\ **control** \\ **NetworkProvider** \\ **orden**

*ProviderOrder* = "LanmanWorkStation, AnotherNetSvc"

**HKEY \_ Sistema \_ del equipo local** NetworkProvider de los \\  \\  \\  \\  \\ **notificantes**

*MyNotifyApp* = "c: \\ Connect \\connect.dll"

**HKEY \_ Sistema de \_ equipo local** \\  \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation**\\

*Group* = "NetworkProvider"

**HKEY \_ Sistema de \_ equipo local** \\  \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation** \\ **NetworkProvider**

*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"

*Class* = 0x00000001 ( \_ clase de red WN \_ )

**HKEY \_ Sistema de \_ equipo local** \\  \\ **CurrentControlSet** \\ **Services** \\ **AnotherNetSvc**\\

*Group* = "NetworkProvider"

**HKEY \_ Sistema de \_ equipo local** \\  \\ **CurrentControlSet** \\ **Services** \\ **AnotherNetSvc** \\ **NetworkProvider**

*Name* = "otra red"*ProviderPath* = "c: \\ otra \\anet.dll"

*Class* = 0x00000003 ( \_ clase de credencial de clase de red WN \_ \| \_ \_ )

*AuthentProviderPath* = "c: \\ otro \\anetCM.dll"

 

