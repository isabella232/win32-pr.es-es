---
title: Claves del registro y entradas para una tienda en línea de tipo 2
description: Claves del registro y entradas para una tienda en línea de tipo 2
ms.assetid: 17dff940-3884-488a-9016-29bb47c51caf
keywords:
- Windows Media Player tiendas en línea, registro
- tiendas en línea, registro
- tipo 2 tiendas en línea, registro
- registro, tipo 2 tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685a26514730e7c370c698cbc9c64c29366c35ee
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104149120"
---
# <a name="registry-keys-and-entries-for-a-type-2-online-store"></a>Claves del registro y entradas para una tienda en línea de tipo 2

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

Para que una tienda en línea de tipo 2 esté disponible en Windows Media Player, el proveedor de la tienda en línea debe crear las siguientes subclaves del registro y entradas en el equipo del usuario.


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



En la sintaxis del registro anterior, los símbolos en cursiva son marcadores de posición para los nombres y los identificadores únicos globales (GUID) que son específicos de la tienda en línea. En la tabla siguiente se describen esos marcadores de posición.



| Marcador de posición    | Descripción                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *keyName*      | Cadena acordada entre Microsoft y la tienda en línea. Esta cadena identifica de forma única la tienda en línea. Ejemplo: "Proseware"<br/>                                                                                                                                                                                                                                                          |
| *flags*        | Un or **bit a** bit de uno o más marcadores de capacidad de complemento estas marcas especifican si Windows Media Player debe llamar a métodos concretos de [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) y [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2). Para obtener información sobre las marcas admitidas, vea la tabla de marcas de capacidad de complementos que se indican a continuación de esta tabla. Ejemplo: 00000037<br/> |
| *CLSID*        | GUID que es el identificador de clase (CLSID) de la clase que implementa **IWMPSubscriptionService** en el complemento de la tienda en línea. Este GUID debe estar en formato de registro, completar con las llaves. Formato: {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX}<br/>                                                                                                                                    |
| *FriendlyName* | Un nombre descriptivo para la tienda en línea. Ejemplo: "servicio de música de Proseware"<br/>                                                                                                                                                                                                                                                                                                                     |
| *pluginName*   | Un nombre para el complemento de la tienda en línea. Ejemplo: "complemento de servicio de Proseware"<br/>                                                                                                                                                                                                                                                                                                                  |
| *className*    | Nombre de la clase que implementa **IWMPSubscriptionService** en el complemento de la tienda en línea. Ejemplo: "CProsewareService"<br/>                                                                                                                                                                                                                                                                |
| *moduleName*   | Ruta de acceso completa al archivo DLL que implementa el complemento de la tienda en línea. Ejemplo: "C: \\ archivos de programa \\ Proseware \\ProsewareService.dll"<br/>                                                                                                                                                                                                                                                |



 

En la tabla siguiente se describen las marcas de capacidad del complemento.



| Marca                                    | Value | Descripción                                                                                                                                                                                                                        |
|-----------------------------------------|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| límite de suscripción \_ \_ ALLOWPLAY            | 0X1   | Windows Media Player debe llamar a [IWMPSubscriptionService:: allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay).                                                                                                                      |
| límite de suscripción \_ \_ ALLOWCDBURN          | 0X2   | Windows Media Player debe llamar a [IWMPSubscriptionService:: allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn).                                                                                                                  |
| límite de suscripción \_ \_ ALLOWPDATRANSFER     | 0X4   | Windows Media Player debe llamar a [IWMPSubscriptionService:: allowPDATransfer](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer).                                                                                                        |
| límite de suscripción \_ \_ BACKGROUNDPROCESSING | 0X8   | Windows Media Player debe llamar a [IWMPSubscriptionService:: startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing).                                                                                      |
| límite de suscripción \_ \_ DEVICEAVAILABLE      | 0X10  | Windows Media Player debe llamar a [IWMPSubscriptionService2::D eviceavailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).                                                                                                        |
| límite de suscripción \_ \_ PREPAREFORSYNC       | 0X20  | Windows Media Player debe llamar a [IWMPSubscriptionService2::P repareforsync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync).                                                                                                          |
| Cap de suscripción \_ v1 \_                  | 0XF   | Predeterminada. Este valor se usa si no se registra ninguno. Esto es equivalente a la combinación de Cap de suscripción \_ \_ ALLOWPLAY, el límite de la suscripción \_ ALLOWCDBURN, el límite de la \_ suscripción \_ \_ ALLOWPDATRANSFER y el límite de la suscripción \_ \_ BACKGROUNDPROCESSING. |



 

**Entradas del registro para desarrollo y pruebas**

Cuando empiece a desarrollar la tienda en línea, Microsoft le proporcionará dos claves: una clave de prueba y una clave de producción. Durante la fase de desarrollo y pruebas, la tienda en línea aparecerá en Windows Media Player solo si la clave de prueba o la clave de producción se encuentra en el registro del equipo del usuario. Para obtener más información acerca de las claves de prueba y de producción, consulte [claves de prueba y producción para una tienda en línea de tipo 2](test-and-production-keys-for-a-type-2-online-store.md).

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

[**Referencia de las tiendas en línea de tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





