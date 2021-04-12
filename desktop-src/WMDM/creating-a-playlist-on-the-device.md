---
title: Creación de una lista de reproducción en el dispositivo
description: Creación de una lista de reproducción en el dispositivo
ms.assetid: 9f803e1a-ff33-443a-9448-e8c875d77e51
keywords:
- Windows Media Administrador de dispositivos, listas de reproducción
- Administrador de dispositivos, listas de reproducción
- Guía de programación, listas de reproducción
- aplicaciones de escritorio, listas de reproducción
- crear aplicaciones de Windows Media Administrador de dispositivos, listas de reproducción
- listas de reproducción abstractas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c287cc406b795db07fde3f10103822dea32185a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356969"
---
# <a name="creating-a-playlist-on-the-device"></a>Creación de una lista de reproducción en el dispositivo

El SDK de Administrador de dispositivos de Windows Media proporciona los medios para que una aplicación MTP cree una lista de reproducción en un dispositivo. Este tipo de lista de reproducción se denomina lista de reproducción *abstracta* , ya que el archivo creado en el dispositivo no contiene datos multimedia, sino solo metadatos, que contienen los vínculos a archivos multimedia en la lista de reproducción.

Otros elementos abstractos que se pueden crear en el dispositivo son los álbumes (esencialmente listas de reproducción con propiedades adicionales como la cubierta), los contactos y los mensajes.

**Para crear una lista de reproducción**

1.  Adquiera una interfaz [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) en el dispositivo de destino.
2.  Llame a [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) para obtener la \_ propiedad g wszWMDMFormatsSupported.
3.  Si no se admiten formatos de lista de reproducción, no se permite el envío de listas de reproducción al dispositivo y se omiten los pasos siguientes. De lo contrario, elija el código de formato compatible con el dispositivo que coincida con el tipo de objeto previsto. Los códigos de formato genérico de WMDM \_ FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST y WMDM \_ FORMATCODE \_ ABSTRACTAUDIOLAYLIST son los que se admiten con más frecuencia.
4.  Obtenga una interfaz [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) para el almacenamiento (la raíz o una carpeta) en la que desea crear el objeto. Algunos dispositivos funcionan mejor si el objeto de lista de reproducción se coloca en una carpeta de nivel superior denominada "listas de reproducción".
5.  Cree un objeto de metadatos vacío mediante [**IWMDMStorage3:: CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).
6.  Con la interfaz **IWMDMMetaData** obtenida en el paso anterior, llame a [**IWMDMMetaData:: AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) para agregar el código de formato elegido (del paso 3) a las propiedades de los metadatos de almacenamiento.
7.  Obtenga la interfaz [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) de la interfaz **IWMDMStorage3** .
8.  Llame a [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) para insertar un nuevo archivo de lista de reproducción en el almacenamiento seleccionado. Este archivo contiene los metadatos representados por la interfaz **IWMDMMetaData** que creó en el paso 5 y que se pasaron a **Insert3**. El método devuelve una interfaz **IWMDMStorage** para el archivo de lista de reproducción; puede consultar la interfaz [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4) .
9.  Llame a [**IWMDMStorage4:: SetReferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) para crear referencias a las interfaces **IWMDMStorage** de los archivos multimedia en la lista de reproducción.

Para ver un ejemplo de código, vea la \_ función OnCreatePlaylist en la [aplicación de escritorio de ejemplo](sample-desktop-application.md).

> [!Note]  
> El proveedor de servicios MTP proporcionado por Microsoft permite a una aplicación establecer referencias en los metadatos. Para implementar listas de reproducción, la aplicación debe comunicarse con un dispositivo MTP o con un proveedor de servicios personalizado que pueda administrar objetos abstractos. El proveedor de servicios CE administra la lista de reproducción y los objetos de álbum.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escribir archivos en el dispositivo**](writing-files-to-the-device.md)
</dt> </dl>

 

 




