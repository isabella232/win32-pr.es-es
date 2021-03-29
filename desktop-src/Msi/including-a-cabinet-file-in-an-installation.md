---
description: En esta sección se describen los archivos. cab en las instalaciones de. Para obtener más información, consulte uso de archivadores y orígenes comprimidos.
ms.assetid: 17ea7f76-90b2-48fb-8187-64dc6d294443
title: Incluir un archivo. cab en una instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098e660de3f7ec7097ab02613d75219ac0a0d624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652585"
---
# <a name="including-a-cabinet-file-in-an-installation"></a>Incluir un archivo. cab en una instalación

En esta sección se describen los archivos. cab en las instalaciones de. Para obtener más información, consulte [uso de archivadores y orígenes comprimidos](using-cabinets-and-compressed-sources.md).

**Para incluir un archivo. cab en un paquete de instalación**

1.  Use una herramienta de creación de contenedores para comprimir los archivos de origen en un archivo. cab. Consulte [archivos. cab](cabinet-files.md).
2.  El archivo. cab debe estar ubicado en un flujo de datos dentro del archivo. msi o en un archivo. cab independiente ubicado en la raíz del árbol de origen especificado por la [tabla de directorio](directory-table.md).
3.  Determine si el origen va a ser un tipo comprimido o un tipo mixto que tiene archivos sin comprimir y comprimidos. Vea [orígenes comprimidos y sin comprimir](compressed-and-uncompressed-sources.md). Dependiendo del tipo de imagen de origen, establezca los bits de marca comprimido o sin comprimir de la propiedad de [**Resumen de recuento de palabras**](word-count-summary.md) .
4.  Agregue un registro a la [tabla de archivos](file-table.md) para cada uno de los archivos del archivo. cab. Escriba una clave de archivo en la columna de archivo que coincida exactamente con la clave de archivo del archivo en el archivo. cab. Las claves de archivo distinguen mayúsculas de minúsculas. La secuencia de instalación de archivos en la tabla de archivos y el archivo. cab también debe ser la misma. La secuencia de archivos se especifica mediante el número de secuencia de la columna de secuencia. Para llegar al número de secuencia del primer archivo del archivo. cab, haga lo siguiente. Busque el registro existente en la [tabla de medios](media-table.md) que tenga el valor más alto en la columna de despatín. El campo LastSequence de este registro proporciona el último número de secuencia de archivo usado en el medio. En la tabla archivo, asigne al primer archivo del nuevo contenedor un número de secuencia que sea mayor que este. Asigne números de secuencia a todos los archivos restantes en el mismo orden que en el archivo. cab. Para obtener una descripción de los campos de registro restantes, vea [File Table](file-table.md).
5.  Agregue un registro a la [tabla de medios](media-table.md) del archivo. cab. Especifique un valor en el campo de patina de este nuevo registro que sea mayor que el valor de dipatine más grande ya existente en la tabla. Coloque el nombre del archivo. cab en el campo del archivo. cab. Este nombre debe tener la forma de un tipo de datos de [archivo. cab](cabinet.md) . Anteponga al nombre un signo de número " \# " si el contenedor es un flujo de datos almacenado en el archivo. msi. Tenga en cuenta que si el archivo. cab es un flujo de datos, el nombre del contenedor distingue mayúsculas de minúsculas. Si el contenedor es un archivo independiente, el nombre del archivo no distingue entre mayúsculas y minúsculas.
6.  Determine el número de secuencia de archivo más grande en el nuevo archivo. para ello, Compruebe la columna Sequence de la tabla de archivos actualizada. Escriba un valor que sea mayor que este en el campo LastSequence del nuevo registro de la tabla de medios. Para obtener una descripción de los campos de registro restantes, consulte [tabla de medios](media-table.md).
7.  Puede almacenar el archivo. cab en el paquete de instalación mediante una herramienta como Msidb.exe o mediante las [funciones de base de datos](database-functions.md)del instalador. En los cuatro pasos siguientes se explica cómo agregar el archivo. cab desde un programa mediante las funciones de base de datos.
8.  Para agregar el archivo. cab al paquete de instalación desde un programa, abra una vista en la [ \_ tabla streams](-streams-table.md) de la base de datos mediante [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa).
9.  Use [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) para establecer la columna de nombre de la \_ tabla streams en el nombre que aparece en la columna Cabinet de la [tabla de medios](media-table.md). Omita el signo de número: \# .
10. Use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) para establecer la columna de datos de la \_ tabla streams en los datos del archivo. cab.
11. Use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para actualizar el registro en la \_ tabla streams.
12. Para usar Msidb.exe para agregar el archivo. cab Mycab.cab al paquete de instalación denominado Mydatabase.msi, use la siguiente línea de comandos: Msidb.exe-d mydatabase.msi-a mycab.cab. En este caso, la columna Cabinet de la tabla de medios debe contener la cadena: \#mycab.cab.

 

 



