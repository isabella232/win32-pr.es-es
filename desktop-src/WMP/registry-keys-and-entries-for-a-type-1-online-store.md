---
title: Claves del registro y entradas para una tienda en línea de tipo 1
description: Claves del registro y entradas para una tienda en línea de tipo 1
ms.assetid: cf25a004-e0c3-407c-8704-54be3601528b
keywords:
- Windows Media Player tiendas en línea, registro
- tiendas en línea, registro
- tipo 1 tiendas en línea, registro
- registro, tipo 1 tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1329ad69e91ebce41b258d1e148403f62caceb96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105685680"
---
# <a name="registry-keys-and-entries-for-a-type-1-online-store"></a>Claves del registro y entradas para una tienda en línea de tipo 1

Para que una tienda en línea de tipo 1 esté disponible en Windows Media Player, el proveedor de la tienda en línea debe crear las siguientes subclaves del registro y entradas en el equipo del usuario.


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\AppID\appid]
@=pluginName
"DllSurrogate"=""

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className
"AppID"="appid"

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="threading"
```



> [!Note]  
> Al establecer el valor de DllSurrogate en la cadena vacía, se indica que el tiempo de ejecución de COM cargará el complemento de la tienda en línea en el suplente de DLL predeterminado, dllhost.exe.

 

En la sintaxis del registro anterior, los símbolos en cursiva son marcadores de posición para los nombres y los identificadores únicos globales (GUID) que son específicos de la tienda en línea. En la tabla siguiente se describen esos marcadores de posición.



| Marcador de posición    | Descripción                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *keyName*      | Cadena acordada entre Microsoft y la tienda en línea. Esta cadena identifica de forma única la tienda en línea. Ejemplo: "Proseware"<br/>                                                                                                                                                                                   |
| *flags*        | Un or **bit a** bit de uno o más marcadores de capacidad de complemento estas marcas especifican si Windows Media Player debe llamar a métodos concretos de [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner). Para obtener información sobre las marcas admitidas, vea la tabla de marcas de capacidad de complementos que se indican a continuación de esta tabla. Ejemplo: 00000058<br/> |
| *CLSID*        | GUID que es el identificador de clase (CLSID) de la clase que implementa **IWMPContentPartner** en el complemento de la tienda en línea. Este GUID debe estar en formato de registro, completar con las llaves. Formato: {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX}<br/>                                                                  |
| *FriendlyName* | Un nombre descriptivo para la tienda en línea. Ejemplo: "servicio de música de Proseware"<br/>                                                                                                                                                                                                                                              |
| *appid*        | GUID que es el identificador de la aplicación (AppID) para el complemento de la tienda en línea. Este GUID debe estar en formato de registro, completar con las llaves. Formato: {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX}<br/>                                                                                                                |
| *pluginName*   | Un nombre para el complemento de la tienda en línea. Ejemplo: "complemento de asociado de contenido de Proseware"<br/>                                                                                                                                                                                                                                   |
| *className*    | Nombre de la clase que implementa **IWMPContentpartner** en el complemento de la tienda en línea. Ejemplo: "CProsewarePartner"<br/>                                                                                                                                                                                              |
| *moduleName*   | Ruta de acceso completa al archivo DLL que implementa el complemento de la tienda en línea. Ejemplo: "C: \\ archivos de programa \\ Proseware \\ProsewarePartner.dll"<br/>                                                                                                                                                                         |
| *Threading*    | Tipo de apartamento en el que se ejecuta el complemento. "ThreadingModel" = "Apartment" indica que el complemento se ejecuta en un contenedor uniproceso (STA). "ThreadingModel" = "Free" indica que el complemento se ejecuta en el contenedor multiproceso (MTA).                                                                                     |



 

En la tabla siguiente se describen las marcas de capacidad del complemento.



| Marca                                    | Value | Descripción                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| límite de suscripción \_ \_ BACKGROUNDPROCESSING | 0x8   | Windows Media Player debe llamar a [IWMPContentPartner:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) para informar al complemento cuando debe iniciar y detener el procesamiento en segundo plano.                                                                                                     |
| límite de suscripción \_ \_ DEVICEAVAILABLE      | 0x10  | Windows Media Player debe llamar a [IWMPContentPartner:: UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice).                                                                                                                                                                   |
| el \_ límite de suscripción \_ es \_ CONTENTPARTNER   | 0x40  | Informa a Windows Media Player de que el complemento implementa la interfaz **IWMPContentPartner** . Todos los complementos de la tienda en línea de tipo 1 deben establecer esta marca.                                                                                                                         |
| límite de suscripción \_ \_ ALTLOGIN             | 0x80  | Informa a Windows Media Player de que el complemento admite un inicio de sesión alternativo. Si el complemento admite un inicio de sesión alternativo, Windows Media Player recupera la dirección URL de inicio de sesión y el título alternativos llamando a [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo). |



 

**Entradas del registro para desarrollo y pruebas**

Cuando empiece a desarrollar la tienda en línea, Microsoft le proporcionará dos claves: una clave de prueba y una clave de producción. Durante la fase de desarrollo y pruebas, la tienda en línea aparecerá en Windows Media Player solo si la clave de prueba o la clave de producción se encuentra en el registro del equipo del usuario. Para obtener más información acerca de las claves de prueba y de producción, consulte [claves de prueba y de producción para una tienda en línea de tipo 1](test-and-production-keys-for-a-type-1-online-store.md).

Coloque la clave de prueba o de producción en la siguiente ubicación del registro.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



Tenga en cuenta que el valor de la entrada del registro TestParameter puede especificar varias claves de prueba o de producción. Por ejemplo, supongamos que Proseware tiene una clave de prueba de "1234" y Contoso tiene una clave de prueba de "2345". La siguiente entrada del registro especifica que los almacenes de pruebas para Proseware y contoso aparecerán en Windows Media Player.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



**Entrada del registro ActiveService**

Cuando el usuario activa una tienda en línea, Windows Media Player escribe información en el registro que identifica la tienda en línea activa. Windows Media Player coloca la información en la siguiente ubicación del registro en el equipo del usuario.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



En la sintaxis del registro anterior, *serviceInfo* es un marcador de posición para una cadena que contiene información descriptiva acerca de la tienda en línea activa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de las tiendas en línea de tipo 1**](reference-for-type-1-online-stores.md)
</dt> </dl>

 

 





