---
description: Establezca siempre la página de códigos de una base de datos antes de agregar cualquier información de localización.
ms.assetid: 0d8aee30-989a-4093-8718-1bb90029c0fb
title: Establecer la página de códigos de una base de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ef04c2969d0933c4601bbca2f3897d86de43a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272351"
---
# <a name="setting-the-code-page-of-a-database"></a>Establecer la página de códigos de una base de datos

Establezca siempre la página de códigos de una base de datos antes de agregar cualquier información de localización. No se recomienda intentar establecer la página de códigos después de escribir datos en la base de datos porque podría dañar caracteres extendidos. La localización se puede facilitar enormemente a partir de una base de datos que sea neutra en la página de códigos. Para obtener más información, consulte [Creación de una base de datos con una página de códigos neutra.](creating-a-database-with-a-neutral-code-page.md) Puede determinar la página de códigos actual de una base de datos como se describe en Determinar la página de códigos de una base [de datos de instalación](determining-an-installation-database-s-code-page.md). Vea [Localización de las tablas Error y ActionText](localizing-the-error-and-actiontext-tables.md) para obtener una lista de páginas de códigos numéricas.

Puede establecer la página de códigos de una base de datos en blanco o una base de datos con una página de códigos neutra importando un archivo de archivo de texto que tenga una página de códigos no neutra con [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Esto establece la página de códigos de la base de datos en la página de códigos del archivo importado. Todos los archivos de archivo importados posteriormente en la base de datos deben tener la misma página de códigos que el primer archivo. Si se exporta un archivo de archivo de texto desde una base de datos, la página de códigos del archivo de archivo es la misma que la base de datos primaria. Vea [Control de páginas de códigos de tablas importadas y exportadas.](code-page-handling-of-imported-and-exported-tables.md)

La página de códigos de cualquier base de datos se puede establecer en una página de códigos numérica especificada mediante [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) para importar un archivo de archivo de texto con el formato siguiente: Dos líneas en blanco; seguido de una línea que contiene la página de códigos numéricos, un delimitador de tabulación y la cadena exacta: \_ ForceCodepage. Tenga en cuenta que Windows 2000, esto traduce todas las cadenas de la base de datos a la página de códigos \_ de ForceCodepage. Esto puede estar pensado para la localización de una base de datos existente y la traducción de todas las cadenas no neutras a la nueva página de códigos. Sin embargo, esto produce un error si la base de datos contiene cadenas no neutras que no se van a traducir.

La utilidad WiLangId.vbs proporciona un ejemplo de cómo establecer la página de códigos de un paquete mediante el [**método Import**](database-import.md). Se proporciona una copia WiLangId.vbs en el SDK Windows Installer. Puede usar esta utilidad para determinar las versiones de idioma admitidas por la base de datos (Paquete), el idioma que usa el instalador para las cadenas de la interfaz de usuario que no se han creado en la base de datos (Product) o la página de códigos ANSI única para el grupo de cadenas (Página de códigos). Para obtener información sobre el uso WiLangId.vbs la página de ayuda: Administrar lenguaje [y página de códigos](manage-language-and-codepage.md).

Para determinar los valores de Product, Package y Codepage, ejecute WiLangId.vbs como se muestra a continuación.

**Ruta de acceso wilangid.vbscscript** *\[ a la base de datos \]*

Para establecer la página de códigos del paquete, ejecute la siguiente línea de comandos.

**Ruta de acceso wilangid.vbscscript** *\[ al valor \] de* página de códigos de la base **de** *\[ datos \]*

Por ejemplo, para establecer la página de códigos test.msi en el valor numérico de la página de códigos ANSI 1252, ejecute la siguiente línea de comandos.

**cscript wilangid.vbs c: \\ temp \\test.msi Codepage 1252**

 

 



