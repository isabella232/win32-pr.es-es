---
description: El Windows almacena todas las cadenas de base de datos en un único grupo de cadenas compartidas para reducir el tamaño de la base de datos y mejorar el rendimiento. Para obtener una lista de páginas de códigos numéricos, vea Localización de las tablas Error y ActionText.
ms.assetid: 5d413fb7-99da-49f3-ace3-ec285df2e634
title: Control de páginas de códigos (Windows instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db2788a1bfc6bdb49ec1402d5bba8a1a2594b30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158889"
---
# <a name="code-page-handling-windows-installer"></a>Control de páginas de códigos (Windows instalador)

El Windows almacena todas las cadenas de base de datos en un único grupo de cadenas compartidas para reducir el tamaño de la base de datos y mejorar el rendimiento. Para obtener una lista de páginas de códigos numéricos, vea [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md).

Para obtener más información, [consulte Determinar la página de códigos de una base de datos de instalación](determining-an-installation-database-s-code-page.md).

Windows El instalador [**usa IsValidCodePage para**](/windows/desktop/api/winnls/nf-winnls-isvalidcodepage) determinar si la página de códigos es válida.

### <a name="localizing-a-windows-installer-package"></a>Localización de un paquete Windows instalador

Si localiza un paquete de Windows Installer, puede implicar modificar la información de las tablas de base de datos, exportar las tablas a archivos de archivo de texto ANSI y, a continuación, importar los archivos de archivo en la base de datos que se está localizando. También puede agregar cambios de localización a una base de datos mediante un editor de tablas de base de datos o funciones [de base de datos](database-functions.md). Es importante establecer la página de códigos de la base de datos que se está localizando antes de realizar cambios de localización en la base de datos. No establezca la página de códigos de la base de datos después de la localización de la base de datos, ya que esto puede dañar los caracteres extendidos. Para obtener más información, vea [Establecer la página de códigos de una base de datos](setting-the-code-page-of-a-database.md).

El enfoque recomendado para controlar páginas de códigos es crear una base de datos neutra que solo contenga caracteres que se puedan traducir en cualquier página de códigos. Para obtener más información, vea [Crear una base de datos con una página de códigos neutra.](creating-a-database-with-a-neutral-code-page.md)

Si agrega información de localización con archivos de archivo de base de datos, puede usar [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) para exportar tablas de una base de datos que contiene cambios de localización en archivos de archivo de texto ANSI y, a continuación, importarlos en la base de datos que se localiza [**con MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). La página de códigos de un archivo de archivo exportado siempre es la misma que su base de datos principal. Las páginas de códigos de un archivo importado y la base de datos que recibe el archivo deben ser idénticas, o al menos una de las dos páginas de códigos debe ser neutra. Para obtener más información, vea [Control de páginas de códigos de tablas importadas y exportadas.](code-page-handling-of-imported-and-exported-tables.md)

Si agrega información de localización con [](database-functions.md) un editor de texto o funciones de base de datos, tenga cuidado de pasar solo parámetros de cadena a la API del instalador de Windows que usa la página de códigos de la base de datos que se está localizando. Si un parámetro de cadena contiene caracteres no representados por la página de códigos de la base de datos, se produce un error al llamar a [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit). Para obtener más información, vea [Control de páginas de códigos de cadenas de parámetros.](code-page-handling-of-parameter-strings.md)

Si se usa un paquete para instalar varias versiones de idioma de un producto, la transformación que se usa para localización de cadenas también puede cambiar la página de códigos de la base de datos.

 

 
