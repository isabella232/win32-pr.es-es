---
title: Grabación de una imagen de disco
description: La creación de patrones (grabación de un disco) mediante IMAPi consta de los pasos siguientes para crear una imagen de sistema de archivos que contiene los directorios y archivos que se van a escribir en el disco. Configure una grabadora de discos para comunicarse con el dispositivo óptico. Cree un escritor de datos y grabe la imagen en el disco.
ms.assetid: f2eee14e-695d-4678-b3c1-b521ab4d4a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e3086f728ca0b0826a001d26841edcfe07c6a1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358903"
---
# <a name="burning-a-disc-image"></a>Grabación de una imagen de disco

La maestra (grabación de un disco) mediante IMAPi consta de los siguientes pasos:

1.  Construya una imagen del sistema de archivos que contenga los directorios y archivos para escribir el disco.
2.  [Configure una grabadora de discos](#set-up-a-disc-recorder) para comunicarse con el dispositivo óptico.
3.  [Cree un escritor de datos](#create-a-data-writer-and-write-the-burn-image) y grabe la imagen en el disco.

Para obtener un ejemplo en el que se grabe una imagen de disco, vea el [ejemplo de VBScript](#vbscript-example).

## <a name="construct-a-burn-image"></a>Construir una imagen de grabación

Una imagen de grabación es un flujo de datos que está listo para escribirse en un medio óptico. La imagen de grabación para los formatos ISO9660, Joliet y UDF se compone de un sistema de archivos de archivos y directorios individuales. El objeto **CFileSystemImage** es el objeto del sistema de archivos que contiene los archivos y directorios que se colocarán en los medios ópticos. La interfaz [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) proporciona acceso al objeto y a la configuración del sistema de archivos.

Después de crear el objeto del sistema de archivos, llame a los métodos [**IFileSystemImage:: CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) y [**IFileSystemImage:: CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) para crear los objetos de archivo y directorio, respectivamente. Los objetos de archivo y directorio se pueden usar para proporcionar detalles específicos sobre el archivo y el directorio. Los métodos de control de eventos disponibles para [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) pueden identificar el archivo actual que se está agregando a la imagen del sistema de archivos, el número de sectores ya copiados y el número total de sectores que se van a copiar.

Opcionalmente, se puede adjuntar una imagen de arranque al sistema de archivos mediante la propiedad [**IFileSystemImage::p UT \_ BootImageOptions**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) . Para obtener un ejemplo, vea [Agregar una imagen de arranque](adding-a-boot-image.md).

Por último, llame a [**IFileSystemImage:: CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) para crear un flujo de datos y proporcionar acceso a través de [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult). El nuevo flujo de datos se puede proporcionar directamente al método [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) o guardarse en un archivo para su uso posterior.

## <a name="set-up-a-disc-recorder"></a>Configuración de una grabadora de discos

El objeto **MsftDiscMaster2** proporciona una enumeración de los dispositivos ópticos en el sistema. La interfaz [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) proporciona acceso a la enumeración del dispositivo resultante. Recorra las enumeraciones para buscar un dispositivo de grabación adecuado. El objeto **MsftDiscMaster2** también proporciona notificaciones de eventos cuando se agregan o eliminan dispositivos ópticos de un equipo.

Después de buscar una grabadora óptica y recuperar su identificador, cree un objeto **MsftDiscRecorder2** e inicialice la grabadora con el identificador de dispositivo. La interfaz [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) proporciona acceso al objeto de grabadora, así como a información básica del dispositivo, como el identificador del proveedor, el ID. del producto, la revisión del producto y los métodos para expulsar el medio y cerrar la bandeja.

## <a name="create-a-data-writer-and-write-the-burn-image"></a>Creación de un escritor de datos y escritura de la imagen de grabación

El objeto **MsftDiscFormat2Data** proporciona el método de escritura, las propiedades de la función de escritura y las propiedades específicas de los elementos multimedia. La interfaz [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) proporciona acceso al objeto **MsftDiscFormat2Data** .

La grabadora de CD vincula al escritor de formato mediante la propiedad [**IDiscFormat2Data::p UT \_ Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) . Después de enlazar la grabadora al escritor de formato, puede realizar consultas sobre el medio y actualizar las propiedades específicas de la escritura antes de escribir la imagen resultante en el disco mediante el método [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) .

Otras interfaces de escritura de formato proporcionadas por IMAPi funcionan de forma similar. entre las interfaces de escritura de formato adicionales se incluyen:

-   [**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) borra los medios ópticos regrabables.
-   [**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) escribe una imagen sin procesar en un medio óptico.
-   [**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) escribe pistas de audio en medios ópticos.

> [!Note]  
> Es posible que se produzca una transición de estado de energía durante una operación de grabación (es decir, el cierre de sesión del usuario o la suspensión del sistema), lo que provoca la interrupción del proceso de grabación y la posible pérdida de datos. Para conocer las consideraciones de programación, vea [evitar el cierre de sesión o la suspensión durante una grabación](preventing-logoff-or-suspend-during-a-burn.md).

 

## <a name="vbscript-example"></a>Ejemplo de VBScript

En este ejemplo de script se muestra cómo usar los objetos de IMAPi para grabar medios ópticos; más concretamente, escriba un directorio en un disco en blanco. El código no contiene ninguna comprobación de errores y asume lo siguiente:

-   Un dispositivo de disco compatible está instalado en el sistema.
-   El dispositivo de disco es la segunda unidad del sistema.
-   Se inserta un disco compatible en el dispositivo de disco.
-   El disco está en blanco.
-   Los archivos que se van a escribir en el disco se encuentran en "g: \\ burndir".

Puede agregarse a este script una funcionalidad adicional, como la comprobación de errores, la compatibilidad de dispositivos y medios, la notificación de eventos y el cálculo del espacio libre en el disco.


```VB
' This script burns data files to disc in a single session 
' using files from a single directory tree.
 
' Copyright (C) Microsoft Corp. 2006

Option Explicit

' *** CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to burn
    Dim Stream               ' Data stream for burning device
    
    Index = 1                ' Second drive on the system
    Path = "g:\BurnDir"      ' Files to transfer to disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim g_DiscMaster
    Set g_DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder object for the specified burning device.
    Dim uniqueId
    set recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    uniqueId = g_DiscMaster.Item(index)
    recorder.InitializeDiscRecorder( uniqueId )

    ' Create an image stream for a specified directory.
    Dim FSI                  ' Disc file system
    Dim Dir                  ' Root directory of the disc file system
    Dim dataWriter    
        
    ' Create a new file system image and retrieve root directory
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
    Set Dir = FSI.Root

    'Create the new disc format and set the recorder
    Set dataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    dataWriter.recorder = Recorder
    dataWriter.ClientName = "IMAPIv2 TEST"

    FSI.ChooseImageDefaults(recorder)
        
    ' Add the directory and its contents to the file system 
    Dir.AddTree Path, false
        
    ' Create an image from the file system
    Dim result
    Set result = FSI.CreateResultImage()
    Stream = result.ImageStream
    
    ' Write stream to disc using the specified recorder.
    WScript.Echo "Writing content to disc..."
    dataWriter.write(Stream)

    WScript.Echo "----- Finished writing content -----"
    Main = 0
End Function

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar IMAPi](using-imapi.md)
</dt> <dt>

[**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase)
</dt> <dt>

[**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd)
</dt> <dt>

[**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce)
</dt> <dt>

[**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2)
</dt> <dt>

[**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> <dt>

[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> </dl>

 

 