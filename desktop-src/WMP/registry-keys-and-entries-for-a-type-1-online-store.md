---
title: Claves y entradas del Registro para un almacén en línea de tipo 1
description: Claves y entradas del Registro para un almacén en línea de tipo 1
ms.assetid: cf25a004-e0c3-407c-8704-54be3601528b
keywords:
- Reproductor de Windows Media en línea, registro
- tiendas en línea, registro
- tipo 1 tiendas en línea, registro
- registry,type 1 online stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1329ad69e91ebce41b258d1e148403f62caceb96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070918"
---
# <a name="registry-keys-and-entries-for-a-type-1-online-store"></a>Claves y entradas del Registro para un almacén en línea de tipo 1

Para que una tienda en línea de tipo 1 esté disponible en Reproductor de Windows Media, el proveedor de la tienda en línea debe crear las siguientes subclaves y entradas del Registro en el equipo del usuario.


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
> Establecer el valor de DllSurrogate en la cadena vacía indica que el tiempo de ejecución COM cargará el complemento de la tienda en línea en el suplente de DLL predeterminado, dllhost.exe.

 

En la sintaxis del Registro anterior, los símbolos en cursiva son marcadores de posición para los nombres y los identificadores únicos globales (GUID) que son específicos del almacén en línea. En la tabla siguiente se describen esos marcadores de posición.



| Marcador de posición    | Descripción                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *keyName*      | Cadena acordado entre Microsoft y la tienda en línea. Esta cadena identifica de forma única la tienda en línea. Ejemplo: "Proseware"<br/>                                                                                                                                                                                   |
| *flags*        | OR bit **a** bit de una o varias marcas de funcionalidad del complemento Estas marcas especifican si Reproductor de Windows Media llamar a métodos concretos de [IWMPContentPartner.](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) Para obtener información sobre las marcas admitidas, consulte la tabla de marcas de funcionalidad del complemento que sigue a esta tabla. Ejemplo: 00000058<br/> |
| *Clsid*        | GUID que es el identificador de clase (CLSID) de la clase que implementa **IWMPContentPartner** en el complemento del almacén en línea. Este GUID debe estar en formato del Registro, con las llaves. Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                                                                  |
| *friendlyname* | Nombre descriptivo de la tienda en línea. Ejemplo: "Proseware Música Service"<br/>                                                                                                                                                                                                                                              |
| *appid*        | GUID que es el identificador de aplicación (AppID) para el complemento de la tienda en línea. Este GUID debe estar en formato del Registro, con las llaves. Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                                                                                                                |
| *pluginName*   | Nombre del complemento de la tienda en línea. Ejemplo: "Complemento de asociado de contenido de Proseware"<br/>                                                                                                                                                                                                                                   |
| *className*    | Nombre de la clase que implementa **IWMPContentpartner en** el complemento de la tienda en línea. Ejemplo: "CProsewarePartner"<br/>                                                                                                                                                                                              |
| *moduleName*   | Ruta de acceso completa al archivo DLL que implementa el complemento de la tienda en línea. Ejemplo: "C: \\ Archivos \\ de programa Proseware \\ProsewarePartner.dll"<br/>                                                                                                                                                                         |
| *Threading*    | Tipo de apartamento en el que se ejecuta el complemento. "ThreadingModel"="Apartment" indica que el complemento se ejecuta en un apartamento de un solo subproceso (STA). "ThreadingModel"="Free" indica que el complemento se ejecuta en el apartamento multiproceso (MTA).                                                                                     |



 

En la tabla siguiente se describen las marcas de funcionalidad del complemento.



| Marca                                    | Value | Descripción                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LÍMITE DE \_ SUSCRIPCIÓN \_ BACKGROUNDPROCESSING | 0x8   | Reproductor de Windows Media llamar a [IWMPContentPartner::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) para informar al complemento cuándo debe iniciar y detener el procesamiento en segundo plano.                                                                                                     |
| LÍMITE \_ DE SUSCRIPCIÓN \_ DEVICEAVAILABLE      | 0x10  | Reproductor de Windows Media llamar a [IWMPContentPartner::UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice).                                                                                                                                                                   |
| EL \_ LÍMITE DE SUSCRIPCIÓN ES \_ \_ CONTENTPARTNER   | 0x40  | Informa Reproductor de Windows Media que el complemento implementa la **interfaz IWMPContentPartner.** Todos los complementos de la tienda en línea de tipo 1 deben establecer esta marca.                                                                                                                         |
| \_ALTLOGIN DE LÍMITE DE \_ SUSCRIPCIÓN             | 0x80  | Informa Reproductor de Windows Media que el complemento admite un inicio de sesión alternativo. Si el complemento admite un inicio de sesión alternativo, Reproductor de Windows Media recupera la dirección URL y el título de inicio de sesión alternativos llamando a [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo). |



 

**Entradas del Registro para desarrollo y pruebas**

Cuando empiece a desarrollar su tienda en línea, Microsoft le proporciona dos claves: una clave de prueba y una clave de producción. Durante la fase de desarrollo y pruebas, la tienda en línea aparecerá en Reproductor de Windows Media solo si la clave de prueba o la clave de producción están en el registro del equipo del usuario. Para obtener más información sobre las claves de prueba y producción, vea [Test and Production Keys for a Type 1 Online Store](test-and-production-keys-for-a-type-1-online-store.md).

Coloque la clave de prueba o producción en la siguiente ubicación del Registro.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



Tenga en cuenta que el valor de la entrada del Registro TestParameter puede especificar varias claves de prueba o producción. Por ejemplo, suponga que Proseware tiene una clave de prueba de "1234" y Contoso tiene una clave de prueba de "2345". La siguiente entrada del Registro especifica que los almacenes de prueba para Proseware y Contoso aparecerán en Reproductor de Windows Media.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



**Entrada del Registro ActiveService**

Cuando el usuario activa una tienda en línea, Reproductor de Windows Media escribe información en el registro que identifica la tienda en línea activa. Reproductor de Windows Media coloca la información en la siguiente ubicación del Registro en el equipo del usuario.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



En la sintaxis del Registro anterior, *serviceInfo* es un marcador de posición para una cadena que contiene información descriptiva sobre el almacén en línea activo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de las tiendas en línea de tipo 1**](reference-for-type-1-online-stores.md)
</dt> </dl>

 

 





