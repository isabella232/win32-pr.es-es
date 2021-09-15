---
title: Claves y entradas del Registro para un almacén en línea de tipo 2
description: Claves y entradas del Registro para un almacén en línea de tipo 2
ms.assetid: 17dff940-3884-488a-9016-29bb47c51caf
keywords:
- Reproductor de Windows Media en línea, registro
- tiendas en línea, registro
- tipo 2 tiendas en línea, registro
- registry,type 2 online stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685a26514730e7c370c698cbc9c64c29366c35ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476209"
---
# <a name="registry-keys-and-entries-for-a-type-2-online-store"></a>Claves y entradas del Registro para un almacén en línea de tipo 2

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso por las tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

Para que una tienda en línea de tipo 2 esté disponible en Reproductor de Windows Media, el proveedor de la tienda en línea debe crear las siguientes subclaves y entradas del Registro en el equipo del usuario.


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="Apartment"
```



En la sintaxis del Registro anterior, los símbolos en cursiva son marcadores de posición para nombres e identificadores únicos globales (GUID) que son específicos del almacén en línea. En la tabla siguiente se describen esos marcadores de posición.



| Marcador de posición    | Descripción                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *keyName*      | Cadena acordado entre Microsoft y la tienda en línea. Esta cadena identifica de forma única la tienda en línea. Ejemplo: "Proseware"<br/>                                                                                                                                                                                                                                                          |
| *flags*        | OR bit  a bit de una o varias marcas de funcionalidad del complemento Estas marcas especifican si Reproductor de Windows Media debe llamar a métodos concretos de [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) e [IWMPSubscriptionService2.](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2) Para obtener información sobre las marcas admitidas, consulte la tabla de marcas de funcionalidad del complemento que sigue a esta tabla. Ejemplo: 00000037<br/> |
| *Clsid*        | GUID que es el identificador de clase (CLSID) de la clase que implementa **IWMPSubscriptionService** en el complemento del almacén en línea. Este GUID debe estar en formato del Registro, junto con las llaves. Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                                                                                                                                    |
| *friendlyname* | Un nombre descriptivo para la tienda en línea. Ejemplo: "Proseware Música Service"<br/>                                                                                                                                                                                                                                                                                                                     |
| *pluginName*   | Nombre del complemento de la tienda en línea. Ejemplo: "Complemento de servicio de Proseware"<br/>                                                                                                                                                                                                                                                                                                                  |
| *className*    | Nombre de la clase que implementa **IWMPSubscriptionService** en el complemento de la tienda en línea. Ejemplo: "CProsewareService"<br/>                                                                                                                                                                                                                                                                |
| *moduleName*   | Ruta de acceso completa al archivo DLL que implementa el complemento de la tienda en línea. Ejemplo: "C: \\ Archivos \\ de programa Proseware \\ProsewareService.dll"<br/>                                                                                                                                                                                                                                                |



 

En la tabla siguiente se describen las marcas de funcionalidad del complemento.



| Marca                                    | Value | Descripción                                                                                                                                                                                                                        |
|-----------------------------------------|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LÍMITE \_ DE SUSCRIPCIÓN \_ ALLOWPLAY            | 0X1   | Reproductor de Windows Media llamar a [IWMPSubscriptionService::allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay).                                                                                                                      |
| LÍMITE \_ DE SUSCRIPCIÓN \_ ALLOWCDCOMBINACIÓN          | 0X2   | Reproductor de Windows Media llamar a [IWMPSubscriptionService::allowCDConexión](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn).                                                                                                                  |
| LÍMITE \_ DE \_ SUSCRIPCIÓN ALLOWPDATRANSFER     | 0X4   | Reproductor de Windows Media llamar a [IWMPSubscriptionService::allowPDATransfer](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer).                                                                                                        |
| \_BACKGROUNDPROCESSING DEL LÍMITE DE \_ SUSCRIPCIÓN | 0X8   | Reproductor de Windows Media llamar a [IWMPSubscriptionService::startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing).                                                                                      |
| DISPOSITIVO \_ DE LÍMITE DE SUSCRIPCIÓN \_ DISPONIBLE      | 0X10  | Reproductor de Windows Media llamar a [IWMPSubscriptionService2::d eviceAvailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).                                                                                                        |
| LÍMITE \_ DE SUSCRIPCIÓN \_ PREPAREFORSYNC       | 0X20  | Reproductor de Windows Media llamar a [IWMPSubscriptionService2::p repareForSync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync).                                                                                                          |
| LÍMITES \_ DE SUSCRIPCIÓN \_ V1                  | 0XF   | Predeterminada. Este valor se usa si no se registra ninguno. Esto equivale a combinar SUBSCRIPTION \_ CAP \_ ALLOWPLAY, SUBSCRIPTION \_ CAP \_ ALLOWCDTRANSFER, \_ SUBSCRIPTION CAP \_ ALLOWPDATRANSFER y SUBSCRIPTION CAP \_ \_ BACKGROUNDPROCESSING. |



 

**Entradas del Registro para desarrollo y pruebas**

Cuando empiece a desarrollar su tienda en línea, Microsoft le proporciona dos claves: una clave de prueba y una clave de producción. Durante la fase de desarrollo y pruebas, la tienda en línea aparecerá en Reproductor de Windows Media solo si la clave de prueba o la clave de producción se encuentra en el registro del equipo del usuario. Para obtener más información sobre las claves de prueba y producción, vea Claves de prueba y [producción para un almacén en línea de tipo 2.](test-and-production-keys-for-a-type-2-online-store.md)

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

Cuando el usuario activa una tienda en línea, Reproductor de Windows Media escribe información en el registro que identifica la tienda en línea activa. Reproductor de Windows Media la información en la siguiente ubicación del Registro en el equipo del usuario.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



En la sintaxis del Registro anterior, *serviceInfo* es un marcador de posición para una cadena que contiene información descriptiva sobre el almacén en línea activo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de las tiendas en línea de tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





