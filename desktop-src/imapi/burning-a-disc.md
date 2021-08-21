---
title: Grabación de una imagen de disco
description: La mastering (grabación de un disco) mediante IMAPI consta de los pasos siguientes Construcción de una imagen del sistema de archivos que contiene los directorios y archivos para escribir el disco. Configure una grabadora de disco para comunicarse con el dispositivo óptico. Cree un escritor de datos y grabe la imagen en un disco.
ms.assetid: f2eee14e-695d-4678-b3c1-b521ab4d4a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 237a4aa73b6820b75b4a9a1ed03baeeb87ac093bfc549cb9cc0ed947077515dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758915"
---
# <a name="burning-a-disc-image"></a>Grabación de una imagen de disco

La mastering (grabación de un disco) mediante IMAPI consta de los pasos siguientes:

1.  Construya una imagen del sistema de archivos que contenga los directorios y archivos que se escribirán en el disco.
2.  [Configure una grabadora de disco](#set-up-a-disc-recorder) para comunicarse con el dispositivo óptico.
3.  [Cree un escritor de datos](#create-a-data-writer-and-write-the-burn-image) y grabe la imagen en un disco.

Para obtener un ejemplo en el que se graba una imagen de disco, vea [el ejemplo de VBScript](#vbscript-example).

## <a name="construct-a-burn-image"></a>Construcción de una imagen de grabación

Una imagen de grabación es un flujo de datos que está listo para escribirse en medios ópticos. La imagen de grabación para los formatos ISO9660, Joliet y UDF consta de un sistema de archivos de archivos y directorios individuales. El **objeto CFileSystemImage** es el objeto del sistema de archivos que contiene los archivos y directorios que se colocarán en los medios ópticos. La [**interfaz IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) proporciona acceso al objeto y la configuración del sistema de archivos.

Después de crear el objeto del sistema de archivos, llame a los métodos [**IFileSystemImage::CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) e [**IFileSystemImage::CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) para crear los objetos de archivo y directorio, respectivamente. Los objetos de archivo y directorio se pueden usar para proporcionar detalles específicos sobre el archivo y el directorio. Los métodos de controlador de eventos disponibles para [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) pueden identificar el archivo actual que se agrega a la imagen del sistema de archivos, el número de sectores ya copiados y el número total de sectores que se van a copiar.

Opcionalmente, se puede adjuntar una imagen de arranque al sistema de archivos mediante la propiedad [**IFileSystemImage::p ut \_ BootImageOptions.**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) Para obtener un ejemplo, vea [Agregar una imagen de arranque.](adding-a-boot-image.md)

Por último, llame a [**IFileSystemImage::CreateResultImage para**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) crear un flujo de datos y proporciona acceso a través [**de IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult). A continuación, el nuevo flujo de datos se puede proporcionar directamente al método [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) o guardarse en un archivo para su uso posterior.

## <a name="set-up-a-disc-recorder"></a>Configuración de una grabadora de discos

El **objeto MsftDiscMaster2** proporciona una enumeración de los dispositivos ópticos del sistema. La [**interfaz IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) proporciona acceso a la enumeración de dispositivo resultante. Recor las enumeraciones para buscar un dispositivo de grabación adecuado. El **objeto MsftDiscMaster2** también proporciona notificaciones de eventos cuando se agregan o eliminan dispositivos ópticos de un equipo.

Después de encontrar una grabadora óptica y recuperar su identificador, cree un objeto **MsftDiscRecorder2** e inicialice la grabadora con el identificador de dispositivo. La [**interfaz IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) proporciona acceso al objeto de grabadora, así como información básica del dispositivo, como el identificador del proveedor, el identificador de producto, la revisión del producto y los métodos para expulsar el medio y cerrar la bandeja.

## <a name="create-a-data-writer-and-write-the-burn-image"></a>Creación de un escritor de datos y escritura de la imagen de grabación

El **objeto MsftDiscFormat2Data proporciona** el método de escritura, las propiedades sobre la función de escritura y las propiedades específicas del medio. La [**interfaz IDiscFormat2Data proporciona**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) acceso al objeto **MsftDiscFormat2Data.**

La grabadora de discos se vincula al sistema de escritura de formato mediante [**la propiedad IDiscFormat2Data::p ut \_ Recorder.**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) Después de enlazar la grabadora al sistema de escritura de formato, puede realizar consultas con respecto al medio y actualizar las propiedades específicas de escritura antes de escribir la imagen de resultado en el disco mediante el método [**IDiscFormat2Data::Write.**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write)

Otras interfaces de escritura de formato proporcionadas por IMAPI funcionan de forma similar; Las interfaces de escritura de formato adicionales incluyen:

-   [**IDiscFormat2Erase borra**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) los medios ópticos reescritos.
-   [**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) escribe una imagen sin procesar en medios ópticos.
-   [**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) escribe pistas de audio en medios ópticos.

> [!Note]  
> Es posible que se lleve a cabo una transición de estado de energía durante una operación de grabación (es decir, cierre de sesión del usuario o suspensión del sistema) que conduce a la interrupción del proceso de grabación y a una posible pérdida de datos. Para ver las consideraciones de programación, vea [Preventing Logoff or Suspend During a Burn](preventing-logoff-or-suspend-during-a-burn.md).

 

## <a name="vbscript-example"></a>Ejemplo de VBScript

En este ejemplo de script se muestra cómo usar los objetos IMAPI para grabar medios ópticos. más específicamente, escriba un directorio en un disco en blanco. El código no contiene ninguna comprobación de errores y asume lo siguiente:

-   Un dispositivo de disco compatible está instalado en el sistema.
-   El dispositivo de disco es la segunda unidad del sistema.
-   Se inserta un disco compatible en el dispositivo del disco.
-   El disco está en blanco.
-   Los archivos para escribir en el disco se encuentran en "g: \\ burndir".

A este script se pueden agregar funcionalidades adicionales, como la comprobación de errores, la compatibilidad de dispositivos y medios, la notificación de eventos y el cálculo del espacio libre en el disco.


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

[Uso de IMAPI](using-imapi.md)
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

[**Istream**](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> </dl>

 

 