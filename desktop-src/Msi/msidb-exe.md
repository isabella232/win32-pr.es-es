---
description: Msidb.exe usa MsiDatabaseImport y MsiDatabaseExport para importar y exportar tablas y secuencias de base de datos.
ms.assetid: 2eee535f-e7f6-4e1a-9667-df4b8067b132
title: Msidb.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86f2e1fa6a1cf1a9dc8a01b9f9d6542607dd9275
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071880"
---
# <a name="msidbexe"></a>Msidb.exe

Msidb.exe usa [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) y [**MsiDatabaseExport para**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) importar y exportar tablas [y](database-tables.md) secuencias de base de datos.

Si el modo, la carpeta, la base de datos y la lista de tablas se especifican en la línea de comandos, Msidb.exe no muestra ninguna interfaz de usuario y funciona como una utilidad de línea de comandos silenciosa adecuada para el script de compilación.

## <a name="syntax"></a>Sintaxis

**MsiDb** *{option}***...** _{option}_* _..._ * *{table}***...** _{table}_

## <a name="command-line-options"></a>Opciones de la línea de comandos

Msidb.exe usa las siguientes opciones de línea de comandos que no tienen en cuenta las mayúsculas y minúsculas. También se puede usar un delimitador de barra diagonal en lugar de un guión.



| Opción | Descripción                                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -i     | Importe los archivos de archivo de texto de la carpeta a la base de datos. Los nombres de tabla para la importación son nombres de archivo de 8 caracteres con una extensión ".idt". Los nombres más largos se truncan a 8 caracteres si se proporcionan mediante el comando para la importación. Se pueden usar especificaciones de comodín estándar.                                                                 |
| -E     | Exporte las tablas seleccionadas de la base de datos a archivos de archivo de texto de la carpeta . Los nombres de tabla para la exportación son nombres de tabla. Solo se puede usar la especificación \* de caracteres comodín, "". Las tablas se pueden exportar desde una base de datos de solo lectura.                                                                                                               |
| -c     | Crea un nuevo archivo de base de datos e importa tablas. Sobrescribe un archivo de base de datos existente.                                                                                                                                                                                                                                               |
| -f     | Especifica la carpeta que contiene los archivos de archivo de texto para tablas y secuencias. Si no se especifica la carpeta que contiene los archivos de archivo de texto, la utilidad solicita al usuario la carpeta.                                                                                                                                       |
| -d     | Ruta de acceso completa al archivo de base de datos.                                                                                                                                                                                                                                                                                          |
| -M     | Ruta de acceso completa a la base de datos en la que se va a combinar. Esta opción solo está disponible en modo de línea de comandos silenciosa. Pueden producirse varias instancias de esta opción hasta un máximo de 10. Si la base de datos no se especifica en la línea de comandos, la utilidad solicita al usuario la base de datos.                                       |
| -T     | Ruta de acceso completa a la transformación que se va a aplicar. Esta opción solo está disponible en modo de línea de comandos silenciosa. Pueden producirse varias instancias de esta opción hasta un máximo de 10.                                                                                                                                                     |
| -j     | Nombre del almacenamiento que se quitará de la base de datos. Esta opción solo está disponible en modo de línea de comandos silenciosa. Pueden producirse varias instancias de esta opción hasta un máximo de 10.                                                                                                                                                             |
| -k     | Nombre del flujo que se quitará de la base de datos. Esta opción solo está disponible en modo de línea de comandos silenciosa. Pueden producirse varias instancias de esta opción hasta un máximo de 10.                                                                                                                                                                 |
| -X     | Nombre de la secuencia que se guardará en un archivo de disco en el directorio actual. Esta opción solo está disponible en modo de línea de comandos silenciosa. Los flujos de datos binarios se almacenan como archivos independientes con la extensión ".ibd". El nombre de archivo binario utilizado son los datos de clave principal de la fila que contiene la secuencia.                                                  |
| -w     | Nombre del almacenamiento que se guardará en un archivo de disco en el directorio actual. Esta opción solo está disponible en modo de línea de comandos silenciosa.                                                                                                                                                                                                         |
| -a     | Nombre del archivo que se agregará a la base de datos como una secuencia. Esta opción solo está disponible en modo de línea de comandos silenciosa. Pueden producirse varias instancias de esta opción hasta un máximo de 10. Los flujos de datos binarios se almacenan como archivos independientes con la extensión ".ibd". El nombre de archivo binario utilizado son los datos de clave principal de la fila que contiene la secuencia. |
| -r     | Nombre del almacenamiento que se agregará a la base de datos como un subalmacenamiento. Esta opción solo está disponible en modo de línea de comandos silenciosa. Pueden producirse varias instancias de esta opción hasta un máximo de 10.                                                                                                                                                     |
| -S     | Truncar los nombres de tabla a 8 caracteres al exportar a un archivo .idt. El nombre de la tabla se trunca a 8 caracteres y se agrega la extensión ".idt".                                                                                                                                                                                           |
| -?     | Muestra el cuadro de diálogo de ayuda de la línea de comandos                                                                                                                                                                                                                                                                                               |



 

> [!Note]  
> Cuando use nombres de archivo largos con espacios, use comillas alrededor de ellos. Por ejemplo, para una base de datos que se encuentra en la carpeta "Mis documentos", es posible especificarla como "c: \\ mis documentos".

 

Esta herramienta solo está disponible en los componentes del [SDK de Windows para Windows programadores del instalador](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Herramientas de desarrollo del instalador](windows-installer-development-tools.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



