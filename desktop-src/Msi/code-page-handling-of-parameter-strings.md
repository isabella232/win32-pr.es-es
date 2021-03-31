---
description: Puede agregar información de localización a una base de datos de instalación mediante un editor de tablas de base de datos como orca que se proporciona con el SDK de Windows Installer o mediante una llamada a las funciones de base de datos desde una aplicación.
ms.assetid: cc1eb336-5dec-40cc-8aa5-564cd167855d
title: Control de páginas de códigos de cadenas de parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a52872472d5509e1abdf35aa12be5afb6a8d13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275669"
---
# <a name="code-page-handling-of-parameter-strings"></a>Control de páginas de códigos de cadenas de parámetros

Puede agregar información de localización a una base de datos de instalación mediante un editor de tablas de base de datos como orca que se proporciona con el SDK de Windows Installer o mediante una llamada a las [funciones de base de datos](database-functions.md) desde una aplicación. Tenga cuidado de pasar solo los parámetros de cadena que usan la página de códigos de la base de datos que se va a localizar. Si un parámetro de cadena contiene caracteres que no se pueden representar mediante la página de códigos de la base de datos, el instalador devuelve un error al llamar a [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Para obtener una lista de páginas de códigos numéricas, consulte [localizar las tablas de error y ActionText](localizing-the-error-and-actiontext-tables.md).

Para obtener más información, vea [determinar la página de códigos de una base de datos de instalación](determining-an-installation-database-s-code-page.md).

## <a name="adding-localization-information-to-a-database"></a>Agregar información de localización a una base de datos

Al agregar información de localización a una base de datos, la página de códigos de la base de datos debe ser compatible con el sistema operativo. No tiene que ser la página de códigos actual del sistema. [**IsValidCodePage**](/windows/desktop/api/winnls/nf-winnls-isvalidcodepage) debe devolver **true** para la página de códigos de la base de datos. Dado que el sistema convierte las cadenas ANSI en Unicode, se produce un error si la página de códigos del usuario actual no es igual que la página de códigos de la base de datos.

La llamada a la versión ANSI de la API de Windows Installer convierte la cadena traducida en Unicode mediante la página de códigos del sistema actual. Cuando se confirma la base de datos, la cadena Unicode se convierte en ANSI mediante la página de códigos de la base de datos. Si la página de códigos del sistema actual difiere de la página de códigos de la cadena localizada, el resultado puede ser una pérdida de datos y una conversión de cadena incorrecta.

En el procedimiento siguiente se muestra cómo almacenar los datos de localización.

**Para almacenar datos de localización**

1.  Establezca la página de códigos de la base de datos en la página de códigos de la cadena localizada.
2.  Convierta la cadena ANSI en Unicode mediante la función [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) y especifique la página de códigos de los datos localizados.
3.  Llame a la versión Unicode de la API de Windows Installer mediante la cadena Unicode para agregar los datos localizados.
4.  Confirme los cambios de localización en la base de datos mediante [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).

También puede agregar información de localización a una base de datos de instalación importando y exportando archivos de archivo de texto ASCII. Para obtener más información, vea [control de páginas de códigos de tablas importadas y exportadas](code-page-handling-of-imported-and-exported-tables.md).

 

 
