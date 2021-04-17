---
description: El Windows Installer almacena todas las cadenas de base de datos en un único grupo de cadenas compartidas para reducir el tamaño de la base de datos y mejorar el rendimiento. Para obtener una lista de páginas de códigos numéricas, consulte localizar las tablas de error y ActionText.
ms.assetid: 5d413fb7-99da-49f3-ace3-ec285df2e634
title: Control de páginas de códigos (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db2788a1bfc6bdb49ec1402d5bba8a1a2594b30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666685"
---
# <a name="code-page-handling-windows-installer"></a>Control de páginas de códigos (Windows Installer)

El Windows Installer almacena todas las cadenas de base de datos en un único grupo de cadenas compartidas para reducir el tamaño de la base de datos y mejorar el rendimiento. Para obtener una lista de páginas de códigos numéricas, consulte [localizar las tablas de error y ActionText](localizing-the-error-and-actiontext-tables.md).

Para obtener más información, [determine la página de códigos de la base de datos de instalación](determining-an-installation-database-s-code-page.md).

Windows Installer usa [**IsValidCodePage**](/windows/desktop/api/winnls/nf-winnls-isvalidcodepage) para determinar si la página de códigos es válida.

### <a name="localizing-a-windows-installer-package"></a>Localizar un paquete de Windows Installer

Si localiza un paquete de Windows Installer, puede implicar la modificación de la información de las tablas de base de datos, la exportación de las tablas a archivos de almacenamiento de texto ANSI y la importación de los archivos de almacenamiento en la base de datos que se va a localizar. También puede Agregar cambios de localización a una base de datos mediante el editor de tablas de base de datos o las [funciones de base de datos](database-functions.md). Es importante establecer la página de códigos de la base de datos que se va a localizar antes de realizar cualquier cambio de localización en la base de datos. No establezca la página de códigos de la base de datos después de localizar la base de datos, ya que puede dañar los caracteres extendidos. Para obtener más información, vea [establecer la página de códigos de una base de datos](setting-the-code-page-of-a-database.md).

El enfoque recomendado para controlar las páginas de códigos es crear una base de datos neutra que solo contenga caracteres que se puedan traducir en cualquier página de códigos. Para obtener más información, vea [crear una base de datos con una página de códigos neutra](creating-a-database-with-a-neutral-code-page.md).

Si agrega información de localización con archivos de almacenamiento de base de datos, puede usar [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) para exportar las tablas de una base de datos que contenga cambios de localización a archivos de archivo de texto ANSI y, a continuación, importarlos en la base de datos que se localiza con [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). La página de códigos de un archivo de almacenamiento exportado es siempre la misma que su base de datos principal. Las páginas de códigos de un archivo importado y la base de datos que lo está recibiendo deben ser idénticas, o al menos una de las dos páginas de códigos debe ser neutra. Para obtener más información, vea [control de páginas de códigos de tablas importadas y exportadas](code-page-handling-of-imported-and-exported-tables.md).

Si agrega información de localización con un editor de texto o las [funciones de base de datos](database-functions.md) , tenga cuidado de pasar solo los parámetros de cadena a la API de Windows Installer que utiliza la página de códigos de la base de datos que se va a localizar. Si un parámetro de cadena contiene caracteres no representados por la página de códigos de la base de datos, se produce un error al llamar a [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit). Para obtener más información, vea [control de páginas de códigos de cadenas de parámetros](code-page-handling-of-parameter-strings.md).

Si se usa un paquete para instalar varias versiones de idioma de un producto, la transformación que se usa para localizar cadenas también puede cambiar la página de códigos de la base de datos.

 

 
