---
description: Un contenedor es un archivo único, normalmente con una extensión. cab, que almacena los archivos comprimidos en una biblioteca de archivos.
ms.assetid: df240302-b875-49bf-8e62-7a35204c35fb
title: Archivos. cab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b54ae737785abc33edd46c9e53edc93fcd288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667009"
---
# <a name="cabinet-files"></a>Archivos. cab

Un contenedor es un archivo único, normalmente con una extensión. cab, que almacena los archivos comprimidos en una biblioteca de archivos. El formato de archivo. cab es una manera eficaz de empaquetar varios archivos, ya que la compresión se realiza a través de los límites de los archivos, lo que mejora significativamente la razón de compresión.

Los desarrolladores pueden usar una herramienta de creación de archivos. cab como Makecab.exe para crear archivos. cab para su uso con paquetes de instalador. La utilidad de Makecab.exe se incluye en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).

Los desarrolladores también pueden utilizar una herramienta de creación de archivos. cab como Cabarc.exe para crear archivos. cab para su uso con paquetes de instalador. Esta herramienta escribe en la estructura del archivo. cab de Diamond.

Las claves de archivo de los archivos almacenados dentro de un archivo. cab deben coincidir con las entradas de la columna File de la [tabla File](file-table.md) y la secuencia de archivos del archivo. cab debe coincidir con la secuencia de archivos especificada en la columna Sequence. Para obtener más información, consulte [uso de archivadores y orígenes comprimidos](using-cabinets-and-compressed-sources.md).

Los archivos grandes pueden dividirse entre dos o más archivos. cab. No puede haber más de 15 archivos en un archivo contenedor que abarque al siguiente archivo. cab. Por ejemplo, si tiene tres archivos. cab, el primero puede tener 15 archivos que abarcan el segundo archivo. cab y el segundo archivo. cab puede tener 15 archivos que abarcan el tercer archivo. cab.

El instalador extrae los archivos de un archivo. cab, ya que los necesita la instalación y los instala en el mismo orden en el que se almacenan en el archivo. cab. Los requisitos de espacio para instalar un archivo almacenado en un archivo. cab no son diferentes a los de la instalación de un archivo sin comprimir.

Un archivo. cab se puede ubicar dentro o fuera del archivo. msi. A partir de Windows Installer 5,0 que se ejecuta en Windows 7 o Windows Server 2008 R2, el instalador guarda los archivadores que están incrustados en el archivo. msi antes de almacenar en caché el paquete de instalación.

**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** Para conservar espacio en disco, el instalador siempre quita todos los gabinetes que están incrustados en el archivo. msi antes de almacenar en caché el paquete de instalación en el equipo del usuario.

 

 



