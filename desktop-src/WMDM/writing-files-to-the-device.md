---
title: Escribir archivos en el dispositivo
description: Escribir archivos en el dispositivo
ms.assetid: 66eaed16-032b-4ac0-a768-aded80f10255
keywords:
- Windows Archivos Administrador de dispositivos, escribir archivos en dispositivos
- Administrador de dispositivos,escribir archivos en dispositivos
- guía de programación, escritura de archivos en dispositivos
- aplicaciones de escritorio, escribir archivos en dispositivos
- crear Windows aplicaciones Administrador de dispositivos multimedia, escribir archivos en dispositivos
- escribir archivos en dispositivos, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d797d792390e4da0f0ae86a2819e47769bffc810db239f947ea06c409552469b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957155"
---
# <a name="writing-files-to-the-device"></a>Escribir archivos en el dispositivo

Antes de enviar un archivo a un dispositivo, la aplicación debe averiguar qué tipos de archivos y formatos puede controlar el dispositivo, para que la aplicación pueda determinar si el archivo debe transcodificarse antes de enviarlo, enviarse sin modificar o no enviarse en absoluto.

En los pasos siguientes se muestra cómo enviar un archivo existente al dispositivo. Para crear un nuevo archivo en el dispositivo, como una lista de reproducción, consulte Creación de una lista [de reproducción en el dispositivo.](creating-a-playlist-on-the-device.md)

1.  Obtenga el formato del archivo que va a enviar al dispositivo. Para obtener más información, vea [Detectar el formato de un archivo.](discovering-a-files-format.md)
2.  Si el dispositivo está pensado para reproducir el archivo,
    -   Consulte el archivo para ver sus funcionalidades de formato. Para más información, consulte [Detección de funcionalidades de formato de dispositivo.](discovering-device-format-capabilities.md)
    -   Busque un formato aceptable que la aplicación pueda crear a partir del archivo original.
    -   Si es necesario transcodificar el archivo, transcodifique el archivo.
3.  Busque un almacenamiento primario para el nuevo objeto. Windows Media Administrador de dispositivos no proporciona una manera de detectar la ubicación de almacenamiento estándar para ningún tipo de archivo determinado (archivos de audio o vídeo, WMV o BMP, una carpeta "Favoritos", entre otros), por lo que tendrá que examinar cada dispositivo para intentar averiguar dónde almacenar mejor el nuevo objeto. (Otras aplicaciones aplican una estructura de carpetas determinada, por ejemplo, Reproductor de Windows Media crea carpetas de álbumes, listas de reproducción y Música donde la carpeta Música contiene un elemento Artist y AlbumName. Por este motivo, y dado que es posible que algunos dispositivos no se hayan probado con software que no sea Reproductor de Windows Media, tenga en cuenta que la colocación de objetos de lista de reproducción o de álbum en cualquier carpeta que no sea las carpetas Listas de reproducción o Álbumes a veces puede dar lugar a objetos no funcionales en algunos dispositivos).
4.  Si el almacenamiento de destino admite [**IWMDMStorageControl3,**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3)cree una nueva interfaz de metadatos llamando a [**IWMDMStorage3::CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject). Establezca metadatos en una [**interfaz IWMDMMetaData.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata) Para obtener más información, vea [Establecer metadatos en un archivo](setting-metadata-on-a-file.md). Los únicos metadatos necesarios son g \_ wszWMDMFormatCode (un valor [**\_ FORMATCODE de WMDM**](wmdm-formatcode.md) que describe el contenido), pero cuanto más metadatos pueda proporcionar, más eficaz será la transferencia para el proveedor de servicios.
5.  Envíe el archivo al dispositivo mediante el [**método Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)o [**Insert3.**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) **Insert3** permite incluir los metadatos en el dispositivo como parte del método . Para obtener más información, [vea Envío del archivo al dispositivo.](sending-the-file-to-the-device.md)

El código que muestra cada uno de estos pasos se proporciona en las páginas de temas vinculados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de una Windows de Administrador de dispositivos multimedia**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




