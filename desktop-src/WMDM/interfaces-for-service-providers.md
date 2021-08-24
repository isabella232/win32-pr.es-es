---
title: Interfaces para proveedores de servicios
description: Interfaces para proveedores de servicios
ms.assetid: bd61c5fa-047c-4d93-bae1-f3433696b95b
keywords:
- Windows Media Administrador de dispositivos,service provider interfaces
- Administrador de dispositivos,interfaces del proveedor de servicios
- proveedores de servicios, interfaces
- referencia de programación, interfaces de proveedor de servicios
- referencia de Windows de Administrador de dispositivos, interfaces de proveedor de servicios
- interfaces del proveedor de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73a7b178ec0f3ab70f0a133a2286a97e294d449264061681fec540ae9b434c94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766715"
---
# <a name="interfaces-for-service-providers"></a>Interfaces para proveedores de servicios

En esta sección se describen las interfaces implementadas por Windows proveedores de Administrador de dispositivos multimedia. Los proveedores de servicios realizan la mayor parte del trabajo real de comunicación con un dispositivo, ya que implementan la mayoría de los métodos del SDK de Windows Media Administrador de dispositivos a los que llama la aplicación.

Los proveedores de servicios no necesitan implementar todas las interfaces enumeradas en esta sección. Por ejemplo, un dispositivo multimedia que no tiene almacenamiento interno no implementa las interfaces que se usan para controlar o exponer contenido. Si se requiere un método o una interfaz, se indica en la página de referencia adecuada.



| Interfaz o clase                                     | Descripción                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CSecureChannelServer](csecurechannelserver-class.md) | Clase auxiliar que permite a un proveedor de servicios o a un proveedor de contenido seguro autenticar una aplicación y crear firmas MAC para parámetros seguros.                                                                                                                                                         |
| [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider)       | Proporciona al cliente (normalmente Windows Media Administrador de dispositivos) un enumerador de dispositivos para los dispositivos que admite este proveedor de servicios.                                                                                                                                                                          |
| [**IMDServiceProvider2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2)     | Extiende **IMDServiceProvider proporcionando** un método para crear el dispositivo mediante la ruta de acceso del dispositivo.                                                                                                                                                                                                            |
| [**IMDServiceProvider3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider3)     | Extiende **IMDServiceProvider2** proporcionando un método para establecer las preferencias de enumeración de dispositivos.                                                                                                                                                                                                             |
| [**IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice)                     | Proporciona una asociación basada en instancias con un dispositivo multimedia. Con esta interfaz, el cliente puede enumerar los enumeradores de medios de almacenamiento para el dispositivo, obtener información sobre el dispositivo y enviar comandos opacos (paso a través) al dispositivo.                                                                 |
| [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2)                   | Extiende **IMDSPDevice** proporcionando métodos para obtener formatos de vídeo extendidos, obtener nombres de dispositivo de Plug and Play (PnP), habilitar el uso de páginas de propiedades y hacer posible obtener un puntero a un medio de almacenamiento a partir de su nombre. Esta interfaz es opcional para el proveedor de servicios, pero se recomienda. |
| [**IMDSPDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)                   | Extiende **IMDSPDevice2** al proporcionar la capacidad de consultar las propiedades y funcionalidades del dispositivo con respecto a un formato de objeto.                                                                                                                                                                                 |
| [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)       | Proporciona métodos para controlar los dispositivos.                                                                                                                                                                                                                                                                         |
| [**IMDSPDirectTransfer**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdirecttransfer)     | Permite Windows De Administrador de dispositivos para delegar la transferencia de contenido al proveedor de servicios. En este caso, Windows media Administrador de dispositivos no realiza ningún procesamiento del contenido antes de enviarlo al proveedor de servicios. El proveedor de servicios obtiene el control total del origen.                                   |
| [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice)             | Enumera los dispositivos multimedia admitidos por este proveedor de servicios.                                                                                                                                                                                                                                                  |
| [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage)           | Enumera los medios de almacenamiento de un dispositivo y el contenido de un medio de almacenamiento.                                                                                                                                                                                                                                    |
| [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject)                     | Contiene métodos para las operaciones de transferencia de datos en un objeto de almacenamiento.                                                                                                                                                                                                                                                |
| [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)                   | Extiende **IMDSPObject al** proporcionar una transmisión más eficaz de los datos habilitados para DRM.                                                                                                                                                                                                                             |
| [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)             | Establece u obtiene la longitud de reproducción, la posición de reproducción, el desplazamiento de reproducción o la longitud total de los objetos que se pueden reproducir en un medio de almacenamiento.                                                                                                                                                                                                    |
| [**IMDSPRevoked**](/windows/desktop/api/mswmdm/nn-mswmdm-imdsprevoked)                   | Recupera la dirección URL desde la que se pueden descargar los componentes actualizados.                                                                                                                                                                                                                                                |
| [**IMDSPStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage)                   | Proporciona una asociación basada en instancias con un medio de almacenamiento en un dispositivo. Esta interfaz crea objetos de almacenamiento, recupera información sobre ellos y proporciona acceso a la interfaz **IMDSPEnumStorage** para enumerar las subcarpetas anidadas en el almacenamiento actual.                                      |
| [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2)                 | Extiende **IMDSPStorage** obteniendo y estableciendo atributos extendidos y haciendo posible obtener un puntero al almacenamiento desde su nombre.                                                                                                                                                                             |
| [**IMDSPStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage3)                 | Extiende **IMDSPStorage2 al** admitir metadatos.                                                                                                                                                                                                                                                                 |
| [**IMDSPStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)                 | Extiende **IMDSPStorage3 al** admitir objetos de lista de reproducción.                                                                                                                                                                                                                                                         |
| [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals)     | Recupera información global sobre un medio de almacenamiento, como la cantidad de espacio libre y el número total de archivos.                                                                                                                                                                                              |



 

En el diagrama siguiente se muestra cómo obtener las distintas interfaces implementadas por un proveedor de servicios. En este diagrama, las interfaces derivadas se muestran en la misma etiqueta para la compactación, por lo que IMDServiceProvider/2/3 representaría tres interfaces: **IMDServiceProvider,** **IMDServiceProvider2** e **IMDServiceProvider3**. Los métodos mostrados se extienden solo por una de estas interfaces. Las interfaces derivadas se obtienen llamando a **QueryInterface** en la interfaz base del objeto creado.

![diagrama que muestra cómo el administrador de dispositivos multimedia de Windows espera adquirir interfaces de un proveedor de servicios.](images/wmdm-sp-interfaces.gif)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> <dt>

[**Windows Interfaces DRM-Implemented multimedia**](windows-media-drm-implemented-interfaces.md)
</dt> </dl>

 

 




