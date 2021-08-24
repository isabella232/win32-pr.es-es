---
description: Cuando instala un proveedor de red, la aplicación debe crear las claves y los valores del Registro que se describen en este tema.
ms.assetid: cc5a4a7b-02b5-4ecd-967c-de0656f00846
title: Claves del Registro de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c245cdb27a0d661e7e6df82ed0d1d0ed35a59ea05bf74bf98ebd39ba3dc791
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883685"
---
# <a name="authentication-registry-keys"></a>Claves del Registro de autenticación

Cuando instala un proveedor de red, la aplicación debe crear las claves y los valores del Registro que se describen en este tema. Estas claves y valores proporcionan información a MPR sobre los proveedores de red instalados en el sistema. MpR comprueba estas claves cuando se inicia y carga los archivos DLL del proveedor de red que encuentra.

Antes de crear un conjunto de claves para contener información sobre el proveedor de red, debe agregar el nombre del proveedor de red a la **clave de** pedido. Esta clave es una subclave de la clave siguiente:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
```

La **clave** de pedido contiene un valor único, **ProviderOrder**, que enumera los proveedores instalados y especifica el orden en el que se deben probar durante las operaciones que atraviesan los proveedores hasta que se encuentra un proveedor de aceptación.

El **valor ProviderOrder** contiene una lista separada por comas de nombres de clave. Cada nombre de clave **de ProviderOrder** identifica un proveedor de red. Cuando MPR pasa por los proveedores, los llama en el orden en que aparecen en esta lista.

El nombre del proveedor establecido en **ProviderOrder** también debe usarse como nombre de la clave del Registro que contiene información sobre ese proveedor. Las claves del Registro específicas del proveedor se crean como subclaves de la clave siguiente:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

En otras palabras, los nombres de proveedor especificados en **ProviderOrder** son la ruta de acceso al registro de las claves específicas del proveedor de red, en relación con la ruta de acceso siguiente:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

Cuando se instala el servicio de proveedor de red, la aplicación de instalación debe agregar una clave como se muestra a continuación:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            ProviderName
```

Donde *ProviderName* es el nombre del proveedor de red tal y como se especifica en el **valor ProviderOrder** de la **clave de** pedido. El **valor** group bajo la *clave ProviderName* debe establecerse en "NetworkProvider". Esto identifica el servicio como en el grupo de proveedores de red.

También debe crear una subclave *de ProviderName*, **networkprovider**. Esta clave contiene los siguientes valores que describen el proveedor de red.



| Value                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nombre**<br/>         | Contiene el nombre del proveedor. Este nombre se muestra al usuario como el nombre de la red en los cuadros de diálogo examinar y debe coincidir con el campo **lpProvider** devuelto en las [**estructuras NETRESOURCE.**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) Este nombre debe ser una variación del nombre del producto, preferiblemente con alguna indicación de la empresa, para que sea claro y único. Por ejemplo, "MS-LanMan" es un buen nombre, mientras que "La red" sería una opción deficiente.<br/> |
| **ProviderPath**<br/> | Contiene la ruta de acceso completa del archivo DLL que implementa el proveedor de red. MPR llama [**a LoadLibrary en**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) esta ruta de acceso.<br/>                                                                                                                                                                                                                                                                                                                                |



 

Los siguientes valores solo los usan los proveedores de red que admiten las funciones de administración de credenciales, [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) y [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify).



| Value                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Clase**<br/>               | DWORD **que** identifica la clase o el tipo de funcionalidad de proveedor que admite este proveedor. Los valores pueden estar unidos por el **operador OR** cuando sea necesario. Los valores válidos para esto son WN \_ NETWORK \_ CLASS, WN \_ CREDENTIAL \_ CLASS, WN \_ PRIMARY \_ AUTHENT \_ CLASS y WN SERVICE \_ \_ CLASS.<br/> Aunque un proveedor puede admitir la funcionalidad del autenticador principal, se usará otro medio para determinar qué autenticador es principal.<br/> **Windows XP/2000:** No se admite el cambio de autenticadores principales, por lo que este valor se omite. <br/> |
| **AuthentProviderPath**<br/> | Este es el nombre de archivo completo del archivo DLL que exporta las funciones de administración de credenciales. Este valor es útil (pero no obligatorio) solo cuando el proveedor se identifica como un proveedor CREDENTIAL CLASS o \_ PRIMARY \_ AUTHENT \_ CLASS. Si este valor no está presente para un proveedor de esta clase, se espera que las funciones de administración de credenciales se exporten desde el archivo DLL identificado por el valor ProviderPath. Este valor solo se usa si es conveniente empaquetar las funciones de red y las funciones del administrador de credenciales en archivos DLL independientes.<br/>  |



 

Además de los valores usados para registrar proveedores de red y administradores de credenciales, puede agregar un valor al registro para registrar un archivo DLL para recibir notificaciones de conexión. Para ello, cree un valor REG \_ EXPAND SZ bajo la siguiente \_ clave:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
               Notifyees
```

Este valor debe especificar la ruta de acceso a un archivo DLL que implementa la [conexión API de notificación](connection-notification-api.md). El nombre de este valor puede ser cualquier cosa que desee, siempre y cuando no entre en conflicto con nombres de valor preexistente.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestran las claves del Registro de un sistema que tiene dos proveedores de red instalados: LanmanWorkStation y AnotherNetSvc. AnotherNetSvc también es un administrador de credenciales. En el ejemplo, los nombres de clave están en negrita y los nombres de valor están en cursiva.

**HKEY \_ ORDEN DE \_ LOCAL MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Control** \\  \\ **NetworkProvider**

*ProviderOrder* = "LanmanWorkStation,AnotherNetSvc"

**HKEY \_ NOTIFICACIÓN \_ DE LOCAL MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Control** \\ **NetworkProvider** \\ **Notifyees**

*MyNotifyApp* = "c: \\ connect \\connect.dll"

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation**\\

*Group* = "NetworkProvider"

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation** \\ **NetworkProvider**

*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"

*Clase* = 0x00000001 (WN \_ NETWORK \_ CLASS)

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **AnotherNetSvc**\\

*Group* = "NetworkProvider"

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **AnotherNetSvc** \\ **NetworkProvider**

*Name* = "Another Network"*ProviderPath* = "c: \\ another \\anet.dll"

*Clase* = 0x00000003 (CLASE \_ WN NETWORK \_ \| WN \_ CREDENTIAL \_ CLASS)

*AuthentProviderPath* = "c: \\ otro \\anetCM.dll"

 

