---
description: Un archivador es un único archivo, normalmente con una .cab, que almacena archivos comprimidos en una biblioteca de archivos.
ms.assetid: df240302-b875-49bf-8e62-7a35204c35fb
title: Archivos archivadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b54ae737785abc33edd46c9e53edc93fcd288
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158951"
---
# <a name="cabinet-files"></a>Archivos archivadores

Un archivador es un único archivo, normalmente con una .cab, que almacena archivos comprimidos en una biblioteca de archivos. El formato de gabinete es una manera eficaz de empaquetar varios archivos porque la compresión se realiza a través de los límites de archivo, lo que mejora significativamente la relación de compresión.

Los desarrolladores pueden usar una herramienta de creación de archivos como Makecab.exe para crear archivos archivadores para su uso con paquetes del instalador. La utilidad Makecab.exe se incluye en los componentes [del SDK de Windows para Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

Los desarrolladores también pueden usar una herramienta de creación de archivos como Cabarc.exe para crear archivos de archivador para su uso con paquetes del instalador. Esta herramienta escribe en la estructura del gabinete Diamond.

Las claves de archivo de los archivos almacenados dentro de un [](file-table.md) archivo archivado deben coincidir con las entradas de la columna Archivo de la tabla Archivo y la secuencia de archivos del archivador debe coincidir con la secuencia de archivos especificada en la columna Secuencia . Para obtener más información, [vea Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).

Los archivos grandes se pueden dividir entre dos o más archivos archivadores. No puede haber más de 15 archivos en un archivo de archivador que se extiende al siguiente archivo de archivador. Por ejemplo, si tiene tres archivos de gabinete, el primer gabinete puede tener 15 archivos que abarcan el segundo archivo de archivador y el segundo archivo de gabinete puede tener 15 archivos que abarcan el tercer archivo de archivador.

El instalador extrae los archivos de un gabinete cuando los necesita la instalación y los instala en el mismo orden en que se almacenan en el archivo del gabinete. Los requisitos de espacio para instalar un archivo almacenado en un archivador no son diferentes de para instalar un archivo sin comprimir.

Un archivo de archivador se puede encontrar dentro o fuera del .msi archivo. A partir de Windows Installer 5.0 que se ejecuta en Windows 7 o Windows Server 2008 R2, el instalador guarda los gabinetes insertados en el archivo .msi antes de almacenar en caché el paquete de instalación.

**[Windows instalador 4.5 o anterior:](not-supported-in-windows-installer-4-5.md)** Para ahorrar espacio en disco, el instalador siempre quita los gabinetes insertados en el archivo .msi antes de almacenar en caché el paquete de instalación en el equipo del usuario.

 

 



