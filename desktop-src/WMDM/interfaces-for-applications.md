---
title: Interfaces para aplicaciones
description: Interfaces para aplicaciones
ms.assetid: bea867d6-a875-4150-9958-7f683cd215b9
keywords:
- Windows Media Administrador de dispositivos, interfaces de aplicación
- Administrador de dispositivos, interfaces de aplicación
- aplicaciones de escritorio, interfaces
- referencia de programación, interfaces de aplicación
- referencia de Windows Media Administrador de dispositivos, interfaces de aplicación
- complementos, interfaces
- interfaces de aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49d66272c42679fd38d01b0114a834ee6f33e92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357198"
---
# <a name="interfaces-for-applications"></a>Interfaces para aplicaciones

En esta sección se describen las interfaces usadas o implementadas por aplicaciones que usan el SDK de Windows Media Administrador de dispositivos para comunicarse con dispositivos. El término "aplicación" que se usa aquí significa cualquier archivo ejecutable, complemento u objeto COM que exista en un equipo de escritorio y necesite comunicación de alto nivel con un dispositivo portátil conectado. Esto puede incluir una aplicación de reproductor de media, un complemento de Media Player de Windows (si necesita acceso directo a un dispositivo portátil) o un objeto COM de medición de recuento de reproducción.

La aplicación implementa algunas de estas interfaces, mientras que otras son llamadas por la aplicación. La documentación de cada interfaz indica si se ha implementado o se ha llamado (y si se ha implementado, si es opcional o es obligatorio).

Las aplicaciones usan las siguientes interfaces o clases.



| Interfaz o clase                                           | Descripción                                                                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Clase CSecureChannelClient](csecurechannelclient-class.md) | Una clase auxiliar que permite a las aplicaciones autenticarse, cifrar y descifrar los datos, y crear equipos Mac.                                                                                                     |
| [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager)                 | La interfaz de Windows Media de nivel superior Administrador de dispositivos para las aplicaciones.                                                                                                                                              |
| [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2)               | Extiende **IWMDeviceManager** proporcionando métodos de enumeración avanzados y otros métodos.                                                                                                                           |
| [**IWMDeviceManager3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager3)               | Extiende la interfaz **IWMDeviceManager2** proporcionando un método que establece la preferencia de enumeración de dispositivos.                                                                                                      |
| [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)                           | Proporciona métodos para examinar y explorar un solo dispositivo portátil.                                                                                                                                                   |
| [**IWMDMDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2)                         | Extiende **IWMDMDevice** , ya que permite obtener los formatos de vídeo admitidos por un dispositivo, buscar un almacenamiento por nombre y usar páginas de propiedades.                                                                       |
| [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3)                         | Extiende **IWMDMDevice2** proporcionando métodos para consultar las propiedades de un dispositivo, enviar códigos de control de e/s de dispositivo y proporcionar también métodos actualizados para buscar almacenamientos y recuperar funcionalidades de formato de dispositivo. |
| [**IWMDMDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicecontrol)             | Proporciona métodos para controlar los dispositivos.                                                                                                                                                                           |
| [**IWMDMDeviceSession**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicesession)             | Mejora la eficacia de las operaciones de dispositivo mediante la agrupación de varias operaciones en una sesión.                                                                                                                       |
| [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice)                   | Enumera los dispositivos portátiles conectados a un equipo.                                                                                                                                                                 |
| [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage)                 | Enumera los almacenamientos de un dispositivo.                                                                                                                                                                                    |
| [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata)                       | Establece y recupera propiedades de metadatos (como intérprete, álbum, género, etc.) de un almacenamiento.                                                                                                                      |
| [**IWMDMObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmobjectinfo)                   | Obtiene y establece la información que controla cómo se controlan los archivos que se pueden reproducir en el dispositivo mediante la interfaz **IWMDMDeviceControl**                                                                                            |
| [**IWMDMRevoked**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmrevoked)                         | Recupera la dirección URL desde la que se pueden descargar los componentes actualizados si se produce un error de revocación en una transferencia.                                                                                                     |
| [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage)                         | Proporciona métodos para examinar y explorar un almacenamiento (archivo, carpeta, lista de reproducción) en un dispositivo.                                                                                                                             |
| [**IWMDMStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage2)                       | Extiende **IWMDMStorage** , ya que permite obtener un almacenamiento secundario por nombre y obtener y establecer atributos extendidos.                                                                                              |
| [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3)                       | Extiende **IWMDMStorage2** mediante la exposición de metadatos.                                                                                                                                                                     |
| [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4)                       | Extiende **IWMDMStorage3** proporcionando métodos para recuperar un subconjunto de metadatos disponibles para un almacenamiento y para establecer y recuperar una lista de referencias a otros almacenamientos.                                  |
| [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)           | Se usa para insertar, eliminar o migrar archivos dentro de un dispositivo, o entre un dispositivo y el equipo.                                                                                                                        |
| [**IWMDMStorageControl2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol2)         | Extiende **IWMDMStorageControl** haciendo posible establecer el nombre del archivo de destino al insertar contenido en un almacenamiento.                                                                                |
| [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3)         | Extiende **IWMDMStorageControl2** haciendo posible pasar un puntero de la interfaz **IWMDMMetaData** .                                                                                                           |
| [**IWMDMStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals)           | Proporciona métodos para recuperar información global sobre un medio de almacenamiento (por ejemplo, una tarjeta ROM) en un dispositivo.                                                                                                   |
| [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md)                   | Permite a una aplicación realizar la medición, la sincronización de licencias y la actualización de los componentes de DRM de un dispositivo.                                                                                                       |
| [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md)                 | Extiende **IWMDRMDeviceApp** proporcionando una nueva versión del método **QueryDeviceStatus** .                                                                                                                         |



 

Interfaces de devolución de llamada

Una aplicación implementa las siguientes interfaces opcionales para realizar el seguimiento del progreso de una solicitud asincrónica, como una solicitud de lectura o escritura.



| Interfaz                                      | Descripción                                                                                                                                                             |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) | Permite a las aplicaciones y proveedores de servicios recibir notificaciones cuando los dispositivos o los almacenamientos de memoria (como tarjetas RAM) están conectados o desconectados del equipo. |
| [**IWMDMOperation2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation2)     | Extiende **IWMDMOperation** proporcionando métodos para obtener y establecer atributos extendidos.                                                                                     |
| [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3)     | Extiende **IWMDMOperation** proporcionando un nuevo método para transferir los datos sin cifrar para mayor eficacia.                                                            |
| [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation)       | Permite que una aplicación controle el modo en que los datos se leen o se escriben en el equipo durante una transferencia de archivos.                                                               |
| [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)       | Extiende el método **IWMDMProgress:: end** proporcionando un indicador de estado.                                                                                              |
| [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)       | Extiende **IWMDMProgress2** proporcionando parámetros de entrada adicionales para especificar el identificador de evento y la información específica del contexto.                                           |
| [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)         | Permite que una aplicación realice el seguimiento del progreso de las operaciones, como el formato de transferencias de archivos o medios.                                                                  |



 

En el diagrama siguiente se muestra cómo se adquieren la mayoría de las interfaces de aplicación importantes de la interfaz raíz **IWMDeviceManager** . Una aplicación obtiene esta interfaz raíz cocreando el objeto MediaDevMgr, solicitando la interfaz **IComponentAuthenticate** , autenticando el componente y, a continuación, solicitando **IWMDeviceManager** (estos pasos se describen en [autenticar la aplicación](authenticating-the-application.md)). Una vez que se ha adquirido esta interfaz raíz, se llama a [**IWMDeviceManager:: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) para crear un objeto que implementa [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice). Otras interfaces se obtienen mediante la llamada a métodos en interfaces en el orden mostrado. Las interfaces derivadas como [**IWMDMDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2) se obtienen llamando a **QueryInterface** en la interfaz base.

En el diagrama siguiente, las interfaces derivadas se etiquetan con marcas de barras diagonales, por lo que "IWMDMStorage/2/3" indicaría **IWMDMStorage**, **IWMDMStorage2** y **IWMDMStorage3**.

![diagrama que muestra cómo obtener las principales interfaces de aplicación en el administrador de dispositivos de Windows Media.](images/wmdm-app-interfaces.gif)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 




