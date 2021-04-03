---
title: Interfaces para proveedores de servicios
description: Interfaces para proveedores de servicios
ms.assetid: bd61c5fa-047c-4d93-bae1-f3433696b95b
keywords:
- Windows Media Administrador de dispositivos, interfaces de proveedor de servicios
- Administrador de dispositivos, interfaces de proveedor de servicios
- proveedores de servicios, interfaces
- referencia de programación, interfaces de proveedor de servicios
- referencia de Windows Media Administrador de dispositivos, interfaces del proveedor de servicios
- interfaces de proveedor de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 019d31f05674f0d9e492f8a73748500bc1d9d514
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776944"
---
# <a name="interfaces-for-service-providers"></a>Interfaces para proveedores de servicios

En esta sección se describen las interfaces implementadas por los proveedores de servicios de Windows Media Administrador de dispositivos. Los proveedores de servicios realizan la mayor parte del trabajo real de comunicarse con un dispositivo, ya que implementan la mayoría de los métodos del SDK de Windows Media Administrador de dispositivos a los que llama la aplicación.

No es necesario que los proveedores de servicios implementen todas las interfaces enumeradas en esta sección. Por ejemplo, un dispositivo multimedia que no tiene almacenamiento incorporado no implementa las interfaces que se usan para controlar o exponer el contenido. El hecho de que se requiera un método o una interfaz se indica en la página de referencia correspondiente.



| Interfaz o clase                                     | Descripción                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CSecureChannelServer](csecurechannelserver-class.md) | Una clase auxiliar que permite a un proveedor de servicios o a un proveedor de contenido seguro autenticar una aplicación y crear firmas MAC para parámetros seguros.                                                                                                                                                         |
| [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider)       | Proporciona al cliente (normalmente Windows Media Administrador de dispositivos) un enumerador de dispositivos para los dispositivos que admite este proveedor de servicios.                                                                                                                                                                          |
| [**IMDServiceProvider2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2)     | Extiende **IMDServiceProvider** proporcionando un método para crear el dispositivo mediante la ruta de acceso del dispositivo.                                                                                                                                                                                                            |
| [**IMDServiceProvider3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider3)     | Extiende **IMDServiceProvider2** proporcionando un método para establecer las preferencias de enumeración de dispositivos.                                                                                                                                                                                                             |
| [**IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice)                     | Proporciona una asociación basada en instancia con un dispositivo multimedia. Mediante esta interfaz, el cliente puede enumerar los enumeradores de medios de almacenamiento para el dispositivo, obtener información sobre el dispositivo y enviar comandos opacos (de paso a través) al dispositivo.                                                                 |
| [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2)                   | Extiende **IMDSPDevice** proporcionando métodos para obtener formatos de vídeo extendidos, obteniendo nombres de dispositivos Plug and Play (PNP), lo que permite el uso de páginas de propiedades y permite obtener un puntero a un medio de almacenamiento a partir de su nombre. Esta interfaz es opcional para el proveedor de servicios, pero se recomienda. |
| [**IMDSPDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)                   | Extiende **IMDSPDevice2** proporcionando la capacidad de consultar las propiedades y capacidades del dispositivo con respecto a un formato de objeto.                                                                                                                                                                                 |
| [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)       | Proporciona métodos para controlar los dispositivos.                                                                                                                                                                                                                                                                         |
| [**IMDSPDirectTransfer**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdirecttransfer)     | Permite a Windows Media Administrador de dispositivos delegar la transferencia de contenido al proveedor de servicios. En este caso, Windows Media Administrador de dispositivos no realiza ningún procesamiento del contenido antes de enviarlo al proveedor de servicios. El proveedor de servicios obtiene el control total del origen.                                   |
| [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice)             | Enumera los dispositivos multimedia admitidos por este proveedor de servicios.                                                                                                                                                                                                                                                  |
| [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage)           | Enumera los medios de almacenamiento en un dispositivo y el contenido en un medio de almacenamiento.                                                                                                                                                                                                                                    |
| [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject)                     | Contiene métodos para las operaciones de transferencia de datos en un objeto de almacenamiento.                                                                                                                                                                                                                                                |
| [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)                   | Extiende **IMDSPObject** proporcionando una transmisión más eficaz de datos habilitados para DRM.                                                                                                                                                                                                                             |
| [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)             | Establece u obtiene la duración de la reproducción, la posición de la reproducción, el desplazamiento de reproducción o la longitud total de los objetos que se van a reproducir en un medio de almacenamiento.                                                                                                                                                                                                    |
| [**IMDSPRevoked**](/windows/desktop/api/mswmdm/nn-mswmdm-imdsprevoked)                   | Recupera la dirección URL desde la que se pueden descargar los componentes actualizados.                                                                                                                                                                                                                                                |
| [**IMDSPStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage)                   | Proporciona una asociación basada en instancias con un medio de almacenamiento en un dispositivo. Esta interfaz crea objetos de almacenamiento, recupera información sobre ellos y proporciona acceso a la interfaz **IMDSPEnumStorage** para enumerar las subcarpetas anidadas dentro del almacenamiento actual.                                      |
| [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2)                 | Extiende **IMDSPStorage** mediante la obtención y configuración de atributos extendidos y la posibilidad de obtener un puntero al almacenamiento desde su nombre.                                                                                                                                                                             |
| [**IMDSPStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage3)                 | Extiende **IMDSPStorage2** mediante la compatibilidad de metadatos.                                                                                                                                                                                                                                                                 |
| [**IMDSPStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)                 | Extiende **IMDSPStorage3** mediante la compatibilidad con objetos de lista de reproducción.                                                                                                                                                                                                                                                         |
| [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals)     | Recupera información global sobre un medio de almacenamiento, como la cantidad de espacio libre y el número total de archivos.                                                                                                                                                                                              |



 

En el diagrama siguiente se muestra cómo obtener las diversas interfaces implementadas por un proveedor de servicios. En este diagrama, las interfaces derivadas se muestran en la misma etiqueta para la compactación, por lo que IMDServiceProvider/2/3 representan tres interfaces: **IMDServiceProvider**, **IMDServiceProvider2** y **IMDServiceProvider3**. Los métodos que se muestran se extienden solo con una de estas interfaces. Las interfaces derivadas se obtienen llamando a **QueryInterface** en la interfaz base del objeto creado.

![diagrama que muestra el modo en que el administrador de dispositivos de Windows Media espera adquirir interfaces de un proveedor de servicios.](images/wmdm-sp-interfaces.gif)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> <dt>

[**Interfaces de DRM-Implemented de Windows Media**](windows-media-drm-implemented-interfaces.md)
</dt> </dl>

 

 




