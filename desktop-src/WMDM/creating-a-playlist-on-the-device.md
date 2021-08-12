---
title: Creación de una lista de reproducción en el dispositivo
description: Creación de una lista de reproducción en el dispositivo
ms.assetid: 9f803e1a-ff33-443a-9448-e8c875d77e51
keywords:
- Windows Media Administrador de dispositivos,playlists
- Administrador de dispositivos,listas de reproducción
- guía de programación, listas de reproducción
- aplicaciones de escritorio, listas de reproducción
- crear Windows aplicaciones de Administrador de dispositivos multimedia, listas de reproducción
- listas de reproducción abstractas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a61d45c234f1cdbe03a713e4d10568fa45c83bdd90227b815c85b0f544d2a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585868"
---
# <a name="creating-a-playlist-on-the-device"></a>Creación de una lista de reproducción en el dispositivo

El SDK Windows Media Administrador de dispositivos proporciona los medios para que una aplicación MTP cree una lista de reproducción en un dispositivo. Este tipo de lista de reproducción se denomina lista de reproducción *abstracta,* porque el archivo creado en el dispositivo no contiene datos multimedia, sino solo metadatos, que contiene los vínculos a los archivos multimedia de la lista de reproducción.

Otros elementos abstractos que se pueden crear en el dispositivo incluyen álbumes (básicamente listas de reproducción con propiedades adicionales, como material de portada), contactos y mensajes.

**Para crear una lista de reproducción**

1.  Adquiera una [**interfaz IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) en el dispositivo de destino.
2.  Llame [**a IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) para obtener la propiedad \_ g wszWMDMFormatsSupported.
3.  Si no se admite ningún formato de lista de reproducción, no permite enviar listas de reproducción al dispositivo y omita los pasos siguientes. De lo contrario, elija el código de formato compatible con el dispositivo que coincida más estrechamente con el tipo de objeto deseado. Los códigos de formato GENÉRICOS WMDM \_ FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST y WMDM \_ FORMATCODE ABSTRACTAUDIOLAYLIST son los más \_ admitidos.
4.  Obtenga una [**interfaz IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) para el almacenamiento (la raíz o una carpeta) donde desea crear el objeto. Algunos dispositivos funcionan mejor si el objeto de lista de reproducción se coloca en una carpeta de nivel superior denominada "Listas de reproducción".
5.  Cree un objeto de metadatos vacío [**mediante IWMDMStorage3::CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).
6.  Mediante la **interfaz IWMDMMetaData** obtenida en el paso anterior, llame a [**IWMDMMetaData::AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) para agregar el código de formato elegido (del paso 3) a las propiedades de metadatos de almacenamiento.
7.  Obtenga la [**interfaz IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) de la **interfaz IWMDMStorage3.**
8.  Llame [**a IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) para insertar un nuevo archivo de lista de reproducción en el almacenamiento seleccionado. Este archivo contiene los metadatos representados por la **interfaz IWMDMMetaData** que creó en el paso 5 y pasó a **Insert3.** El método devuelve una **interfaz IWMDMStorage** para el archivo de lista de reproducción; puede consultar la interfaz [**IWMDMStorage4.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4)
9.  Llame [**a IWMDMStorage4::SetReferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) para crear referencias a las interfaces **IWMDMStorage** de los archivos multimedia de la lista de reproducción.

Para obtener código de ejemplo, vea \_ la función OnCreatePlaylist en [la aplicación de escritorio de ejemplo](sample-desktop-application.md).

> [!Note]  
> El proveedor de servicios MTP proporcionado por Microsoft permite a una aplicación establecer referencias en los metadatos. Para implementar listas de reproducción, la aplicación debe comunicarse con un dispositivo MTP o usar un proveedor de servicios personalizado que pueda controlar objetos abstractos. El proveedor de servicios ce controla los objetos de lista de reproducción y álbum.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escritura de archivos en el dispositivo**](writing-files-to-the-device.md)
</dt> </dl>

 

 




