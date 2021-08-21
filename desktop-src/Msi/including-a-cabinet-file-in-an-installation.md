---
description: En esta sección se describe cómo incluir archivos archivadores en instalaciones. Para obtener más información, vea Usar gabinetes y orígenes comprimidos.
ms.assetid: 17ea7f76-90b2-48fb-8187-64dc6d294443
title: Incluir un archivo archivador en una instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0970d87b8b219e1558c6b3f1daf78a6a01100a7bc41f9ae1dad51a25048b46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787345"
---
# <a name="including-a-cabinet-file-in-an-installation"></a>Incluir un archivo archivador en una instalación

En esta sección se describe cómo incluir archivos archivadores en instalaciones. Para obtener más información, [vea Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).

**Para incluir un archivo archivador en un paquete de instalación**

1.  Use una herramienta de creación de gabinetes para comprimir los archivos de origen en un archivo de archivador. Vea [Archivos archivadores](cabinet-files.md).
2.  El archivo de archivador debe encontrarse en un flujo de datos dentro del archivo .msi o en un archivo de archivado independiente ubicado en la raíz del árbol de origen especificado por la tabla [de directorios](directory-table.md).
3.  Determine si el origen debe ser un tipo comprimido o un tipo mixto que tenga archivos sin comprimir y comprimidos. Vea [Orígenes comprimidos y sin comprimir.](compressed-and-uncompressed-sources.md) Según el tipo de imagen de origen, establezca los bits de marca comprimidos o sin comprimir de la [**propiedad Resumen de recuento de**](word-count-summary.md) palabras.
4.  Agregue un registro a la [tabla Archivo](file-table.md) para cada uno de los archivos del archivador. Escriba una clave de archivo en la columna Archivo que coincida exactamente con la clave de archivo del archivo en el archivador. Las claves de archivo distinguen mayúsculas de minúsculas. La secuencia de instalación de archivos de la tabla Archivo y el archivador también deben ser iguales. El número de secuencia de la columna Secuencia especifica la secuencia de archivo. Para llegar al número de secuencia del primer archivo del archivador, haga lo siguiente. Busque el registro existente en la [tabla Media que](media-table.md) tenga el mayor valor en la columna DiskID. El campo LastSequence de este registro proporciona el último número de secuencia de archivo usado en el medio. En la tabla Archivo, asigne al primer archivo del nuevo gabinete un número de secuencia mayor que este. Asigne números de secuencia a todos los archivos restantes en el mismo orden que en el archivo de archivador. Para obtener una descripción de los campos de registro restantes, vea [Tabla de archivos](file-table.md).
5.  Agregue un registro a la [tabla Media](media-table.md) para el archivador. Especifique un valor en el campo DiskID de este nuevo registro que sea mayor que el valor de DiskID más grande que ya existe en la tabla. Coloque el nombre del gabinete en el campo Gabinete. Este nombre debe tener el formato de un tipo [de datos Cabinet.](cabinet.md) Antefiese el nombre con un signo de número " " si el gabinete es un flujo de \# datos almacenado en el .msi archivo. Tenga en cuenta que si el gabinete es un flujo de datos, el nombre del gabinete distingue mayúsculas de minúsculas. Si el archivador es un archivo independiente, el nombre del archivo no distingue mayúsculas de minúsculas.
6.  Determine el mayor número de secuencia de archivos en el nuevo gabinete comprobando la columna Secuencia de la tabla File actualizada. Escriba un valor mayor que este en el campo LastSequence del nuevo registro de la tabla Media. Para obtener una descripción de los campos de registro restantes, vea [Tabla multimedia](media-table.md).
7.  Puede almacenar el archivo de archivador en el paquete de instalación mediante una herramienta como Msidb.exe o mediante las funciones de base de datos [del instalador.](database-functions.md) En los cuatro pasos siguientes se explica cómo agregar el gabinete desde un programa mediante las funciones de base de datos.
8.  Para agregar el contenedor al paquete de instalación desde un programa, abra una vista en la [ \_ tabla](-streams-table.md) Secuencias de la base de datos [**mediante MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa).
9.  Use [**MsiRecordSetString para**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) establecer la columna Name de la tabla Secuencias en el nombre que aparece en la columna \_ Cabinet de la tabla [Media](media-table.md). Omita el signo de número: \# .
10. Use [**MsiRecordSetStream para**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) establecer la columna Datos de \_ la Secuencias tabla en los datos del contenedor.
11. Use [**MsiViewModify para**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) actualizar el registro en la \_ Secuencias tabla.
12. Para usar Msidb.exe para agregar el archivo de archivador Mycab.cab al paquete de instalación denominado Mydatabase.msi, use la siguiente línea de comandos: Msidb.exe -d mydatabase.msi -a mycab.cab. En este caso, la columna Gabinete de la tabla Media debe contener la cadena: \#mycab.cab.

 

 



