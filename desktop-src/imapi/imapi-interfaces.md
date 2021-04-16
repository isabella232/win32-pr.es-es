---
title: Interfaces de IMAPi
description: En las tablas siguientes se identifican y describen brevemente las interfaces utilizadas por los desarrolladores de C/C++ y el objeto de scripting asociado. Anteponga el nombre de objeto de la tabla con \ 0034; IMAPI2. \ 0034; para completar el nombre del objeto al crear el objeto en el script.
ms.assetid: dba81a45-34a8-4b49-9ccb-d61a7e7ee1f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac989a9871b761a1f1700ec599cc51affd30b2e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "105685672"
---
# <a name="imapi-interfaces"></a>Interfaces de IMAPi

En las tablas siguientes se identifican y describen brevemente las interfaces utilizadas por los desarrolladores de C/C++ y el objeto de scripting asociado. Anteponga el nombre del objeto en la tabla con "IMAPI2". para completar el nombre del objeto al crear el objeto en el script.

En la tabla siguiente se enumeran las interfaces asociadas a los dispositivos, el motor de grabación y el formato escritores y borrador.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaz</td>
<td>Object</td>
</tr>
<tr class="even">
<td>Motor de grabación de bajo nivel.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></li>
</ul></td>
<td>MsftWriteEngine2</td>
</tr>
<tr class="odd">
<td>Escritor de imagen principal.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></li>
</ul></td>
<td>MsftDiscFormat2Data</td>
</tr>
<tr class="even">
<td>Borrador de disco.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></li>
</ul></td>
<td>MsftDiscFormat2Erase</td>
</tr>
<tr class="odd">
<td>Escritor de imágenes sin formato.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></li>
</ul></td>
<td>MsftDiscFormat2RawCD</td>
</tr>
<tr class="even">
<td>Escritor de imágenes de un momento dado.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></li>
</ul></td>
<td>MsftDiscFormat2TrackAtOnce</td>
</tr>
<tr class="odd">
<td>Enumeración de los dispositivos de disco de la lista de hardware del sistema.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></li>
</ul></td>
<td>MsftDiscMaster2</td>
</tr>
<tr class="even">
<td>Delegado de notificación para el objeto MsftDiscMaster2.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></li>
</ul></td>
<td>DDiscMaster2Events</td>
</tr>
<tr class="odd">
<td>Dispositivo de grabación individual.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></li>
</ul></td>
<td>MsftDiscRecorder2</td>
</tr>
<tr class="even">
<td>Atributos de escritura de dispositivos, incluido el tipo de medio, la velocidad de escritura y el tipo de control de velocidad angular.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>IWriteSpeedDescriptor</strong></a></li>
</ul></td>
<td>MsftWriteSpeedDescriptor</td>
</tr>
</tbody>
</table>



 

En la tabla siguiente se enumeran las interfaces del sistema de archivos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaz</td>
<td>Object</td>
</tr>
<tr class="even">
<td>Secuencia de imagen de arranque y propiedades para integrar la imagen de arranque en la imagen de disco.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>IBootOptions</strong></a></li>
</ul></td>
<td>BootOptions</td>
</tr>
<tr class="odd">
<td>Imagen y propiedades del sistema de archivos. Este objeto incluye todas las pistas y referencias a la imagen de arranque y la imagen de resultado.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>DFileSystemImageEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>DFileSystemImageImportEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>IFileSystemImage</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></li>
</ul></td>
<td>CFileSystemImage</td>
</tr>
<tr class="even">
<td>Contenedor del flujo de datos proporcionado por el objeto del sistema de archivos.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>IFileSystemImageResult</strong></a></li>
</ul></td>
<td>FileSystemImageResult</td>
</tr>
<tr class="odd">
<td>Elemento de directorio de la imagen del sistema de archivos.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>IFsiDirectoryItem</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></li>
</ul></td>
<td>FsiDirectoryItem</td>
</tr>
<tr class="even">
<td>Elemento de archivo de la imagen del sistema de archivos.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>IFsiFileItem</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></li>
</ul></td>
<td>FsiFileItem</td>
</tr>
<tr class="odd">
<td>Interfaz que contiene propiedades comunes a los elementos de archivo y de directorio.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>IFsiItem</strong></a></li>
</ul></td>
<td>FsiItem</td>
</tr>
<tr class="even">
<td>Creación de imagen de CD sin formato.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>IRawCDImageCreator</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>IRawCDImageTrackInfo</strong></a></li>
</ul></td>
<td>MsftRawCDImageCreator</td>
</tr>
<tr class="odd">
<td>Objeto auxiliar de objeto de secuencia para concatenar varias secuencias.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>IStreamConcatenate</strong></a></li>
</ul></td>
<td>MsftStreamConcatenate</td>
</tr>
<tr class="even">
<td>Flujo intercalado que se va a agregar a la imagen de disco.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>IStreamInterleave</strong></a></li>
</ul></td>
<td>MsftStreamInterleave</td>
</tr>
<tr class="odd">
<td>Secuencia generada pseudoaleatorios.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>IStreamPseudoRandomBased</strong></a></li>
</ul></td>
<td>MsftStreamPrgn001</td>
</tr>
<tr class="even">
<td>El objeto de scripting <strong>MsftStreamZero</strong> no se implementa como una interfaz.</td>
<td><a href="msftstreamzero.md"><strong>MsftStreamZero</strong></a></td>
</tr>
</tbody>
</table>



 

En la tabla siguiente se enumeran las interfaces auxiliares.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaz</td>
<td>Object</td>
</tr>
<tr class="even">
<td>Colección de intervalos de sectores dentro de una imagen de sistema de archivos.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>IBlockRange</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>IBlockRangeList</strong></a></li>
</ul></td>
<td>Ningún objeto correspondiente</td>
</tr>
<tr class="odd">
<td>Compatibilidad con la comprobación de la grabación.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>IBurnVerification</strong></a></li>
</ul></td>
<td>Ningún objeto correspondiente</td>
</tr>
<tr class="even">
<td>Enumerador de FsiItems para las aplicaciones de C/C++.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>IEnumFsiItems</strong></a></li>
</ul></td>
<td>EnumFsiItems</td>
</tr>
<tr class="odd">
<td>Enumerador de ProgressItems para las aplicaciones de C/C++.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>IEnumProgressItems</strong></a></li>
</ul></td>
<td>EnumProgressItems</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>IFsiNamedStreams</strong></a></li>
</ul></td>
<td>FsiFileItem2</td>
</tr>
<tr class="odd">
<td>compatibilidad con la comprobación de imágenes. ISO.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>IIsoImageManager</strong></a></li>
</ul></td>
<td>Ningún objeto correspondiente</td>
</tr>
<tr class="even">
<td>Compatibilidad con varias sesiones.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>IMultisession</strong></a></li>
</ul></td>
<td>Ningún objeto correspondiente</td>
</tr>
<tr class="odd">
<td>Compatibilidad con varias sesiones secuenciales.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>IMultisessionSequential</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></li>
</ul></td>
<td>MsftMultisessionSequential</td>
</tr>
<tr class="even">
<td>Nombre de archivo y bloques asociados en la imagen de resultado.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>IProgressItem</strong></a></li>
</ul></td>
<td>ProgressItem</td>
</tr>
<tr class="odd">
<td>Lista de imágenes de resultados, desglosadas por nombre de archivo y por bloques asociados.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>IProgressItems</strong></a></li>
</ul></td>
<td>ProgressItems</td>
</tr>
</tbody>
</table>



 

 

 




