---
description: Msidb.exe usa MsiDatabaseImport y MsiDatabaseExport para importar y exportar tablas y secuencias de base de datos.
ms.assetid: 2eee535f-e7f6-4e1a-9667-df4b8067b132
title: Msidb.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86f2e1fa6a1cf1a9dc8a01b9f9d6542607dd9275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667673"
---
# <a name="msidbexe"></a>Msidb.exe

Msidb.exe usa [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) y [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) para importar y exportar [tablas](database-tables.md) y secuencias de base de datos.

Si el modo, la carpeta, la base de datos y la lista de tablas se especifican en la línea de comandos, Msidb.exe no muestra ninguna interfaz de usuario y funciona como una utilidad de línea de comandos silenciosa adecuada para el script de compilación.

## <a name="syntax"></a>Sintaxis

**MsiDb** *{opción} ***...** _{opción}_* _..._ * * {Table} ***...** _{TABLE}_

## <a name="command-line-options"></a>Opciones de la línea de comandos

Msidb.exe usa las siguientes opciones de la línea de comandos que no distinguen mayúsculas de minúsculas. También se puede usar un delimitador de barra diagonal en lugar de un guión.



| Opción | Descripción                                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -i     | Importar archivos de archivo de texto de la carpeta a la base de datos. Los nombres de tabla para la importación son nombres de archivo de 8 caracteres de longitud con una extensión ". IDT". Los nombres más largos se truncan a 8 caracteres si los proporciona el comando para la importación. Se pueden utilizar las especificaciones de caracteres comodín estándar.                                                                 |
| -E     | Exportar las tablas seleccionadas de la base de datos a archivos de almacenamiento de texto en la carpeta. Los nombres de tabla para la exportación son nombres de tabla. Solo se puede utilizar la especificación de caracteres comodín, " \* ". Las tablas se pueden exportar desde una base de datos de solo lectura.                                                                                                               |
| -c     | Crea un nuevo archivo de base de datos e importa tablas. Sobrescribe un archivo de base de datos existente.                                                                                                                                                                                                                                               |
| -f     | Especifica la carpeta que contiene los archivos de archivo de texto para las tablas y las secuencias. Si no se especifica la carpeta que contiene los archivos de archivo de texto, la utilidad solicitará al usuario la carpeta.                                                                                                                                       |
| -d     | Ruta de acceso completa al archivo de base de datos.                                                                                                                                                                                                                                                                                          |
| -M     | Ruta de acceso completa a la base de datos en la que se va a combinar. Esta opción solo está disponible en modo de línea de comandos silencioso. Se pueden producir varias instancias de esta opción en un máximo de 10. Si la base de datos no se especifica en la línea de comandos, la utilidad solicita al usuario la base de datos.                                       |
| -T     | Ruta de acceso completa a la transformación que se va a aplicar. Esta opción solo está disponible en modo de línea de comandos silencioso. Se pueden producir varias instancias de esta opción en un máximo de 10.                                                                                                                                                     |
| -j     | Nombre del almacenamiento que se va a quitar de la base de datos. Esta opción solo está disponible en modo de línea de comandos silencioso. Se pueden producir varias instancias de esta opción en un máximo de 10.                                                                                                                                                             |
| -k     | Nombre del flujo que se va a quitar de la base de datos. Esta opción solo está disponible en modo de línea de comandos silencioso. Se pueden producir varias instancias de esta opción en un máximo de 10.                                                                                                                                                                 |
| -X     | Nombre de la secuencia que se va a guardar en un archivo de disco en el directorio actual. Esta opción solo está disponible en modo de línea de comandos silencioso. Los flujos de datos binarios se almacenan como archivos independientes con la extensión ". ibd". El nombre de archivo binario usado es datos de clave principal para la fila que contiene la secuencia.                                                  |
| -w     | Nombre del almacenamiento que se va a guardar en un archivo de disco en el directorio actual. Esta opción solo está disponible en modo de línea de comandos silencioso.                                                                                                                                                                                                         |
| -a     | Nombre del archivo que se va a agregar a la base de datos como una secuencia. Esta opción solo está disponible en modo de línea de comandos silencioso. Se pueden producir varias instancias de esta opción en un máximo de 10. Los flujos de datos binarios se almacenan como archivos independientes con la extensión ". ibd". El nombre de archivo binario usado es datos de clave principal para la fila que contiene la secuencia. |
| -r     | Nombre del almacenamiento que se va a agregar a la base de datos como un subalmacenamiento. Esta opción solo está disponible en modo de línea de comandos silencioso. Se pueden producir varias instancias de esta opción en un máximo de 10.                                                                                                                                                     |
| -S     | Truncar los nombres de tabla a 8 caracteres en la exportación a un. IDT. El nombre de la tabla se trunca a 8 caracteres y se agrega la extensión ". IDT".                                                                                                                                                                                           |
| -?     | Muestra el cuadro de diálogo ayuda de la línea de comandos                                                                                                                                                                                                                                                                                               |



 

> [!Note]  
> Al usar nombres de archivo largos con espacios, use comillas alrededor de ellos. Por ejemplo, para una base de datos que se encuentra en la carpeta "Mis documentos", especifíquelo como "c: \\ Mis documentos".

 

Esta herramienta solo está disponible en los [componentes de Windows SDK para los desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Herramientas de desarrollo de Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



