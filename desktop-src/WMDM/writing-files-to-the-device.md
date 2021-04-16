---
title: Escribir archivos en el dispositivo
description: Escribir archivos en el dispositivo
ms.assetid: 66eaed16-032b-4ac0-a768-aded80f10255
keywords:
- Windows Media Administrador de dispositivos, escribir archivos en dispositivos
- Administrador de dispositivos, escribir archivos en dispositivos
- Guía de programación, escribir archivos en dispositivos
- aplicaciones de escritorio, escribir archivos en dispositivos
- crear aplicaciones de Windows Media Administrador de dispositivos, escribir archivos en dispositivos
- escribir archivos en dispositivos, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d8b5234cc275eed1b4aa344c16a2b927b8122d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531887"
---
# <a name="writing-files-to-the-device"></a>Escribir archivos en el dispositivo

Antes de enviar un archivo a un dispositivo, la aplicación debe averiguar qué tipos de archivos y formatos puede controlar el dispositivo, de modo que la aplicación pueda determinar si el archivo se debe transcodificar antes de enviarlo o enviarlo sin modificarlo o no enviarlo.

En los pasos siguientes se muestra cómo enviar un archivo existente al dispositivo. Para crear un archivo nuevo en el dispositivo, como una lista de reproducción, consulte [creación de una lista de reproducción en el dispositivo](creating-a-playlist-on-the-device.md).

1.  Obtiene el formato del archivo que desea enviar al dispositivo. Para obtener más información, vea [detectar el formato de un archivo](discovering-a-files-format.md).
2.  Si el dispositivo está diseñado para reproducir el archivo,
    -   Consulte el archivo para obtener sus capacidades de formato. Para obtener más información, consulte [detectar capacidades de formato de dispositivo](discovering-device-format-capabilities.md).
    -   Busque un formato aceptable que la aplicación pueda crear a partir del archivo original.
    -   Si es necesario transcodificar el archivo, transcodificarlo.
3.  Busque un almacenamiento primario para el nuevo objeto. Windows Media Administrador de dispositivos no proporciona una manera de detectar la ubicación de almacenamiento estándar para los tipos de archivo en particular (archivos de vídeo o audio, WMV o BMP, una carpeta "favoritos", etc.), por lo que tendrá que examinar cada dispositivo para intentar averiguar dónde es mejor almacenar el nuevo objeto. (Otras aplicaciones imponen una determinada estructura de carpetas, por ejemplo, Windows Media Player crea álbumes, listas de reproducción y carpetas de música donde la carpeta música contiene un artista y una jerarquía nombre del álbum. Por esta razón, y dado que es posible que algunos dispositivos no se hayan probado con software que no sea Windows Media Player, tenga en cuenta que la ubicación de los objetos de la lista de reproducción o del álbum en cualquier carpeta que no sea la lista de reproducción o las carpetas de álbumes a veces puede conducir a la no función de objetos en algunos dispositivos).
4.  Si el almacenamiento de destino admite [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3), cree una nueva interfaz de metadatos mediante una llamada a [**IWMDMStorage3:: CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject). Establezca los metadatos en una interfaz [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata) . Para obtener más información, consulte [configuración de metadatos en un archivo](setting-metadata-on-a-file.md). Los únicos metadatos necesarios son g \_ wszWMDMFormatCode (un valor [**\_ FORMATCODE de WMDM**](wmdm-formatcode.md) que describe el contenido), pero los más metadatos que se pueden proporcionar es más eficaz para el proveedor de servicios.
5.  Envíe el archivo al dispositivo mediante el método [**Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)o [**Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) . **Insert3** permite incluir los metadatos en el dispositivo como parte del método. Para obtener más información, consulte [Enviar el archivo al dispositivo](sending-the-file-to-the-device.md).

El código que muestra cada uno de estos pasos se proporciona en las páginas del tema vinculado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear una aplicación de Windows Media Administrador de dispositivos**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




