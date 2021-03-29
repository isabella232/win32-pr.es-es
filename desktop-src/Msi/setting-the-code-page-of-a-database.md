---
description: Establezca siempre la página de códigos de una base de datos antes de agregar información de localización.
ms.assetid: 0d8aee30-989a-4093-8718-1bb90029c0fb
title: Establecer la página de códigos de una base de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ef04c2969d0933c4601bbca2f3897d86de43a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810904"
---
# <a name="setting-the-code-page-of-a-database"></a>Establecer la página de códigos de una base de datos

Establezca siempre la página de códigos de una base de datos antes de agregar información de localización. No se recomienda intentar establecer la página de códigos después de escribir los datos en la base de datos, ya que esto podría dañar los caracteres extendidos. La localización puede facilitarse en gran medida al empezar con una base de datos que es de la página de códigos neutral. Para obtener más información, vea [crear una base de datos con una página de códigos neutra](creating-a-database-with-a-neutral-code-page.md). Puede determinar la página de códigos actual de una base de datos como se describe en determinación de la [Página de códigos de una base de datos de instalación](determining-an-installation-database-s-code-page.md). Consulte [localizar las tablas de error y ActionText](localizing-the-error-and-actiontext-tables.md) para obtener una lista de páginas de códigos numéricas.

Puede establecer la página de códigos de una base de datos vacía, o una base de datos con una página de códigos neutra, importando un archivo de almacenamiento de texto con una página de códigos no neutra con [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Esto establece la página de códigos de la base de datos en la página de códigos del archivo importado. Todos los archivos de almacenamiento importados posteriormente en la base de datos deben tener la misma página de códigos que el primer archivo. Si se exporta un archivo de almacenamiento de texto desde una base de datos, la página de códigos del archivo de almacenamiento es la misma que la base de datos primaria. Vea [control de páginas de códigos de tablas importadas y exportadas](code-page-handling-of-imported-and-exported-tables.md).

La página de códigos de cualquier base de datos se puede establecer en una página de códigos numérica especificada mediante [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) para importar un archivo de almacenamiento de texto con el siguiente formato: dos líneas en blanco; seguido de una línea que contiene la página de códigos numérica, un delimitador de tabulador y la cadena exacta: \_ ForceCodepage. Tenga en cuenta que con Windows 2000, se traducen todas las cadenas de la base de datos a la página de códigos de \_ ForceCodepage. Esto puede deberse a la localización de una base de datos existente y a la traducción de todas las cadenas no neutras a la nueva página de códigos. Sin embargo, esto provoca un error si la base de datos contiene cadenas no neutras que no se van a traducir.

La utilidad WiLangId.vbs proporciona un ejemplo de cómo establecer la página de códigos de un paquete mediante el [**método de importación**](database-import.md). En el SDK de Windows Installer se proporciona una copia de WiLangId.vbs. Puede usar esta utilidad para determinar las versiones de idioma admitidas por la base de datos (paquete), el idioma que usa el instalador para cualquier cadena de la interfaz de usuario que no se haya creado en la base de datos (producto) o la página de códigos ANSI única para el grupo de cadenas (CodePage). Para obtener información sobre el uso de WiLangId.vbs vea la página de ayuda: [administrar idioma y página de códigos](manage-language-and-codepage.md).

Para determinar los valores de Product, package y CodePage, ejecute WiLangId.vbs como se indica a continuación.

**cscript wilangid.vbs** *\[ ruta de acceso \] a la base de datos*

Para establecer la página de códigos del paquete, ejecute la siguiente línea de comandos.

**cscript wilangid.vbs** *\[ ruta de acceso \] al* *\[ valor \]* **CodePage** de la base de datos

Por ejemplo, para establecer la página de códigos de test.msi en el valor numérico de la página de códigos ANSI 1252, ejecute la siguiente línea de comandos.

**cscript wilangid.vbs c: \\ temp \\test.msi CodePage 1252**

 

 



