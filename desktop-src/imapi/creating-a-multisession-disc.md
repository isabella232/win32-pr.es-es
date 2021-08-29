---
title: Creación de un disco multisesión
ms.assetid: 327304c4-fdb9-47c6-9b19-49100b933590
description: 'Más información sobre: Creación de un disco multisesión'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95147cbadedc76487ae64797c342eb256df0967bf99efecb9e9cda443b5d3010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758581"
---
# <a name="creating-a-multisession-disc"></a>Creación de un disco multisesión

[Image Mastering API](about-imapi.md) (IMAPI) admite la adición y eliminación de archivos hacia o desde los siguientes tipos de disco multisesión:

-   CD-R/CD-RW
-   Single-Layer DVD+R/DVD-R
-   Capa dual de DVD+R
-   BD-R
-   DVD-RW/DVD+RW (**Windows 7 Only**)
-   DVD-RAM (**solo Windows 7**)
-   BD-RE (**solo Windows 7**)

La creación de un disco multisesión mediante IMAPI consta de los pasos siguientes. Cada uno de estos pasos documentados contiene la parte pertinente del ejemplo completo Visual Basic script proporcionado en la sección final.

## <a name="initializing-the-disc-recorder"></a>Inicialización de la grabadora de discos

Antes de la inicialización del dispositivo, **el objeto MsftDiscMaster2** proporciona una enumeración de los dispositivos ópticos en el sistema. La [**interfaz IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) proporciona acceso a esta enumeración de dispositivos para facilitar la ubicación del dispositivo de grabación adecuado. El **objeto MsftDiscMaster2** también proporciona notificaciones de eventos cuando los dispositivos ópticos se agregan o quitan de una máquina.

Después de localizar una grabadora óptica y recuperar el identificador asignado a ella, cree un nuevo objeto **MsftDiscMaster2** e inicialice la grabadora con el identificador de dispositivo específico.

La [**interfaz IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) proporciona acceso a información básica del dispositivo, como el identificador del proveedor, el identificador del producto, la revisión del producto, así como los métodos para expulsar medios o cerrar la bandeja.

> [!Note]  
> Las constantes y dimensiones adicionales declaradas en el ejemplo siguiente se usan más adelante en el script de ejemplo completo ubicado en la sección final de este documento. Estos elementos no son necesarios para el acto de inicializar una grabadora de disco.

 


```VB
' *** CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to add
    Dim Stream               ' Data stream for burning device
    
    Index = 0                ' First drive on the system
    Path = "G:\BurnDir"      ' Files to add to the disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim DiscMaster
    Set DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder2 object for the specified burning device.
    Dim UniqueId
    set Recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    UniqueId = DiscMaster.Item(Index)
    Recorder.InitializeDiscRecorder(UniqueId)
```



## <a name="creating-a-data-writer"></a>Creación de un escritor de datos

El **objeto MsftDiscFormat2Data proporciona** el método de escritura, sus propiedades, así como las propiedades específicas del medio. La [**interfaz IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) proporciona acceso a este objeto .

La grabadora de discos se enlaza al sistema de escritura de formato mediante la [**propiedad IDiscFormat2Data::p ut \_ Recorder.**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) Después de enlazar la grabadora al sistema de escritura de formato, se pueden realizar consultas de medios y de propiedades específicas de escritura antes de escribir la imagen de resultado en el disco mediante el método [**IDiscFormat2Data::Write.**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write)

> [!Note]  
> La cadena de nombre de cliente especificada en el código de ejemplo siguiente debe ajustarse según corresponda para la aplicación específica.

 


```VB
    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"
```



## <a name="creating-the-file-system-object"></a>Crear el objeto del sistema de archivos

Para registrar una nueva sesión, primero se debe generar una imagen de grabación para ella. Una imagen de grabación **para los formatos ISO9660**, **Joliet** y **UDF** consta de sistemas de archivos de archivos y directorios individuales. El **objeto MsftFileSystemImage** es el objeto del sistema de archivos que contiene los archivos y directorios que se colocarán en el medio óptico. La [**interfaz IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) proporciona acceso al objeto y la configuración del sistema de archivos.


```VB
    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
```



## <a name="importing-a-file-system"></a>Importar un sistema de archivos

Antes de continuar, asegúrese de que el disco no está en blanco comprobando la propiedad [**IDiscFormat2::get \_ MediaHeuristicallyBlank.**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank)

Después de crear el objeto **MsftFileSystemImage,** se debe inicializar la propiedad [**\_ MultisessionInterfaces de IFileSystemImage::p ut**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) antes de llamar al método [**IFileSystemImage::ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) o [**IFileSystemImage::ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) para importar el sistema de archivos desde la última sesión registrada. Estos métodos rellenarán automáticamente el **objeto MsftFileSystemImage** con información que describa los archivos y directorios registrados anteriormente.

> [!Note]  
> La propiedad [**IFileSystemImage::p ut \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) normalmente se inicializa con las interfaces multisesión proporcionadas por el escritor de datos a través de la propiedad [**IDiscFormat2Data::get \_ MultisessionInterfaces.**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces)

 

Los intentos de establecer la propiedad **IFileSystemImage::p ut \_ MultisessionInterfaces** producirán un error si IMAPI no admite multisesión para el medio insertado actualmente o no se puede anexar el medio por algún otro motivo (por ejemplo, porque está cerrado).

Si la sesión de grabación anterior contenía más de un tipo de sistema de archivos, el método [**IFileSystemImage::ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) importará información del tipo de sistema de archivos más avanzado presente. Por ejemplo, en el ejemplo proporcionado en este tema, UDF es el sistema de archivos importado. Sin embargo, el uso del [**método IFileSystemImage::ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) permite importar la selección específica del sistema de archivos.

> [!Note]  
> El [**método IFileSystemImage::IdentifyFileSystemsOnDisc**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc) se puede usar para determinar qué sistemas de archivos están disponibles en el disco.

 


```VB
    ' Import the last session, if the disc is not empty, or initialize
    ' the file system, if the disc is empty
    If Not DataWriter.MediaHeuristicallyBlank _
    Then
        On Error Resume Next
        FSI.MultisessionInterfaces = DataWriter.MultisessionInterfaces
        If Err.Number <> 0 _
        Then
            WScript.Echo "Multisession is not supported for this disc"
            Main = 1
            Exit Function
        End If
        On Error Goto 0

        WScript.Echo "Importing data from the previous session..."
        FSI.ImportFileSystem()
    Else 
        FSI.ChooseImageDefaults(Recorder)
    End If
```



## <a name="adding-or-removing-files-to-the-file-system"></a>Agregar o quitar archivos al sistema de archivos

Después de crear el objeto del sistema de archivos e importar el sistema de archivos de la sesión anterior, llame a los métodos [**IFileSystemImage::CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) e [**IFileSystemImage::CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) para crear nuevos objetos de archivo y directorio, respectivamente. Los objetos de archivo y directorio proporcionan detalles específicos sobre los archivos y directorios. Como alternativa, el método [**IFsiDirectoryItem::AddTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree) de un objeto de directorio, representado a través de la interfaz [**IFsiDirectoryItem,**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) se puede usar para agregar archivos y directorios existentes desde otro dispositivo de almacenamiento (es decir, una unidad de disco duro).

El método de actualización del controlador de eventos disponible para [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) identifica el archivo actual que se agrega a la imagen del sistema de archivos, el número de sectores ya copiados y el número total de sectores que se van a copiar.

Para quitar archivos y directorios existentes del sistema de archivos, use los métodos [**IFsiDirectoryItem::Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) e [**IFsiDirectoryItem::RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) de los objetos de directorio representados a través de la [**interfaz IFsiDirectoryItem.**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) La [**propiedad IFileSystemImage::get \_ Root**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_root) se usa para obtener un puntero al directorio raíz del sistema de archivos y la interfaz **IFsiDirectoryItem** para recorrer el árbol de directorios.

> [!Note]  
> Los archivos y directorios quitados a través de los métodos [**IFsiDirectoryItem::Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) e [**IFsiDirectoryItem::RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) no se quitan físicamente del disco y el software avanzado puede recuperar fácilmente la información eliminada.

 


```VB
    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false
```



## <a name="constructing-a-file-system-image"></a>Construir una imagen del sistema de archivos

El paso final consiste en llamar a [**IFileSystemImage::CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) para crear un flujo de datos para la imagen de grabación y proporcionar acceso a ella a través de la [**interfaz IFileSystemImageResult.**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) Este flujo de datos se puede proporcionar directamente al método [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) o guardarse en un archivo para su uso posterior.


```VB
    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
```



## <a name="example-summary"></a>Resumen de ejemplo

En el ejemplo Visual Basic script siguiente se muestra cómo usar objetos IMAPI para crear discos de varias sesiones. En el ejemplo se crea una nueva sesión y se agrega un directorio al disco. Por motivos de simplicidad, el código no realiza una comprobación de errores exhaustiva y asume lo siguiente:

-   Un dispositivo de disco compatible está instalado en el sistema.
-   El dispositivo de disco es la primera unidad del sistema.
-   Se inserta un disco compatible en el dispositivo del disco.
-   Los archivos que se van a agregar al disco se encuentran en "g: \\ burndir".

Se pueden agregar al script funcionalidades adicionales, como la comprobación de errores extensa, la compatibilidad de dispositivos y medios, la notificación de eventos y el cálculo del espacio libre en el disco.


```VB
' This script adds data files from a single directory tree to a
' disc (a new session is added, if the disc already contains data)

' Copyright (C) Microsoft. All rights reserved.

Option Explicit

' *** CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to add
    Dim Stream               ' Data stream for burning device
    
    Index = 0                ' First drive on the system
    Path = "G:\BurnDir"      ' Files to add to the disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim DiscMaster
    Set DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder2 object for the specified burning device.
    Dim UniqueId
    set Recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    UniqueId = DiscMaster.Item(Index)
    Recorder.InitializeDiscRecorder(UniqueId)

    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"

    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")

    ' Import the last session, if the disc is not empty, or initialize
    ' the file system, if the disc is empty
    If Not DataWriter.MediaHeuristicallyBlank _
    Then
        On Error Resume Next
        FSI.MultisessionInterfaces = DataWriter.MultisessionInterfaces
        If Err.Number <> 0 _
        Then
            WScript.Echo "Multisession is not supported for this disc"
            Main = 1
            Exit Function
        End If
        On Error Goto 0

        WScript.Echo "Importing data from the previous session..."
        FSI.ImportFileSystem()
    Else 
        FSI.ChooseImageDefaults(Recorder)
    End If

    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false

    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
    
    ' Write stream to disc using the specified recorder
    WScript.Echo "Writing content to the disc..."
    DataWriter.Write(Stream)

    WScript.Echo "Finished writing content."
    Main = 0
End Function

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de IMAPI](using-imapi.md)
</dt> <dt>

[**Istream**](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> <dt>

[**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> </dl>

 

 
