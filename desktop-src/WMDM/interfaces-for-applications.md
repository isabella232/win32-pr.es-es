---
title: Interfaces para aplicaciones
description: Interfaces para aplicaciones
ms.assetid: bea867d6-a875-4150-9958-7f683cd215b9
keywords:
- Windows Media Administrador de dispositivos,interfaces de aplicación
- Administrador de dispositivos,interfaces de aplicación
- aplicaciones de escritorio, interfaces
- referencia de programación, interfaces de aplicación
- referencia de Windows de Administrador de dispositivos,interfaces de aplicación
- complementos, interfaces
- interfaces de aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49d66272c42679fd38d01b0114a834ee6f33e92
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068513"
---
# <a name="interfaces-for-applications"></a>Interfaces para aplicaciones

En esta sección se describen las interfaces usadas o implementadas por las aplicaciones que usan Windows Media Administrador de dispositivos SDK para comunicarse con dispositivos. El término "aplicación" que se usa aquí significa cualquier ejecutable, complemento u objeto COM que exista en un equipo de escritorio y necesite comunicación de alto nivel con un dispositivo portátil conectado. Esto puede incluir una aplicación de reproductor multimedia, un complemento Reproductor de Windows Media (si necesita acceso directo a un dispositivo portátil) o un objeto COM de medición de recuento de reproducción.

La aplicación implementa algunas de estas interfaces, mientras que la aplicación llama a otras. La documentación de cada interfaz indica si se implementa o se llama (y, si se implementa, si es opcional o obligatorio).

Las aplicaciones usan las siguientes interfaces o clases.



| Interfaz o clase                                           | Descripción                                                                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CSecureChannelClient (clase)](csecurechannelclient-class.md) | Una clase auxiliar que permite que las aplicaciones se autentiquen, cifre y descifren los datos, y cree macs.                                                                                                     |
| [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager)                 | El nivel superior Windows interfaz Administrador de dispositivos multimedia para aplicaciones.                                                                                                                                              |
| [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2)               | Extiende **IWMDeviceManager proporcionando** métodos de enumeración avanzados y otros métodos.                                                                                                                           |
| [**IWMDeviceManager3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager3)               | Extiende la interfaz **IWMDeviceManager2** proporcionando un método que establece la preferencia de enumeración de dispositivos.                                                                                                      |
| [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)                           | Proporciona métodos para examinar y explorar un único dispositivo portátil.                                                                                                                                                   |
| [**IWMDMDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2)                         | Extiende **IWMDMDevice** al hacer posible obtener los formatos de vídeo admitidos por un dispositivo, buscar un almacenamiento por nombre y usar páginas de propiedades.                                                                       |
| [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3)                         | Extiende **IWMDMDevice2** proporcionando métodos para consultar las propiedades de un dispositivo, enviar códigos de control de E/S de dispositivo y proporcionar también métodos actualizados para buscar almacenamientos y recuperar funcionalidades de formato de dispositivo. |
| [**IWMDMDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicecontrol)             | Proporciona métodos para controlar los dispositivos.                                                                                                                                                                           |
| [**IWMDMDeviceSession**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevicesession)             | Mejora la eficacia de las operaciones de dispositivo al agrupar varias operaciones en una sesión.                                                                                                                       |
| [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice)                   | Enumera los dispositivos portátiles conectados a un equipo.                                                                                                                                                                 |
| [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage)                 | Enumera los almacenamientos de un dispositivo.                                                                                                                                                                                    |
| [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata)                       | Establece y recupera las propiedades de metadatos (como el intérprete, el álbum, el género, entre otros) de un almacenamiento.                                                                                                                      |
| [**IWMDMObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmobjectinfo)                   | Obtiene y establece información que controla cómo la interfaz **IWMDMDeviceControl** controla los archivos que se pueden reproducir en el dispositivo.                                                                                            |
| [**IWMDMRevoked**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmrevoked)                         | Recupera la dirección URL desde la que se pueden descargar los componentes actualizados, si se produce un error de revocación en una transferencia.                                                                                                     |
| [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage)                         | Proporciona métodos para examinar y explorar un almacenamiento (archivo, carpeta, lista de reproducción) en un dispositivo.                                                                                                                             |
| [**IWMDMStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage2)                       | Extiende **IWMDMStorage** al hacer posible obtener un almacenamiento secundario por nombre y para obtener y establecer atributos extendidos.                                                                                              |
| [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3)                       | Extiende **IWMDMStorage2 mediante** la exposición de metadatos.                                                                                                                                                                     |
| [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4)                       | Extiende **IWMDMStorage3** proporcionando métodos para recuperar un subconjunto de metadatos disponibles para un almacenamiento y para establecer y recuperar una lista de referencias a otros almacenamientos.                                  |
| [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)           | Se usa para insertar, eliminar o mover archivos dentro de un dispositivo o entre un dispositivo y el equipo.                                                                                                                        |
| [**IWMDMStorageControl2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol2)         | Extiende **IWMDMStorageControl** al hacer posible establecer el nombre del archivo de destino al insertar contenido en un almacenamiento.                                                                                |
| [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3)         | Extiende **IWMDMStorageControl2** al hacer posible pasar un puntero de interfaz **IWMDMMetaData.**                                                                                                           |
| [**IWMDMStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorageglobals)           | Proporciona métodos para recuperar información global sobre un medio de almacenamiento (por ejemplo, una tarjeta DE ROM flash) en un dispositivo.                                                                                                   |
| [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md)                   | Permite que una aplicación realice medición, sincronización de licencias y actualización de los componentes DRM de un dispositivo.                                                                                                       |
| [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md)                 | Extiende **IWMDRMDeviceApp** proporcionando una nueva versión del **método QueryDeviceStatus.**                                                                                                                         |



 

Interfaces de devolución de llamada

Una aplicación implementa las siguientes interfaces opcionales con el fin de realizar un seguimiento del progreso de una solicitud asincrónica, como una solicitud de lectura o escritura.



| Interfaz                                      | Descripción                                                                                                                                                             |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) | Permite que las aplicaciones y los proveedores de servicios reciban notificaciones cuando los dispositivos o los almacenamientos de memoria (como las tarjetas RAM) están conectados o desconectados del equipo. |
| [**IWMDMOperation2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation2)     | Extiende **IWMDMOperation proporcionando métodos** para obtener y establecer atributos extendidos.                                                                                     |
| [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3)     | Extiende **IWMDMOperation proporcionando** un nuevo método para transferir datos sin cifrar para aumentar la eficacia.                                                            |
| [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation)       | Permite a una aplicación controlar cómo se leen o escriben datos en el equipo durante una transferencia de archivos.                                                               |
| [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)       | Extiende el **método IWMDMProgress::End** proporcionando un indicador de estado.                                                                                              |
| [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)       | Extiende **IWMDMProgress2** proporcionando parámetros de entrada adicionales para especificar el identificador de evento y la información específica del contexto.                                           |
| [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)         | Permite que una aplicación realice un seguimiento del progreso de las operaciones, como dar formato a medios o transferencias de archivos.                                                                  |



 

En el diagrama siguiente se muestra cómo se adquieren la mayoría de las interfaces de aplicación importantes de la interfaz **IWMDeviceManager** raíz. Una aplicación obtiene esta interfaz raíz mediante la creación del objeto MediaDevMgr, la solicitud de la interfaz **IComponentAuthenticate,** la autenticación del componente y la solicitud de **IWMDeviceManager** (estos pasos se describen en [Autenticación](authenticating-the-application.md)de la aplicación). Una vez adquirida esta interfaz raíz, se llama a [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) para crear un objeto que implementa [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice). Otras interfaces se obtienen llamando a métodos en interfaces en el orden mostrado. Las interfaces derivadas, [**como IWMDMDevice2,**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2) se obtienen mediante una llamada a **QueryInterface** en la interfaz base.

En el diagrama siguiente, las interfaces derivadas se etiquetan con barras diagonales, por lo que "IWMDMStorage/2/3" indicaría **IWMDMStorage**, **IWMDMStorage2** e **IWMDMStorage3**.

![diagrama que muestra cómo obtener las interfaces de aplicación principales en el administrador de dispositivos multimedia de Windows.](images/wmdm-app-interfaces.gif)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> </dl>

 

 




