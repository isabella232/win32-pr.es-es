---
description: Puede agregar información de localización a una base de datos de instalación mediante un editor de tablas de base de datos como Orca que se proporciona con el SDK del instalador de Windows o llamando a las funciones de base de datos desde una aplicación.
ms.assetid: cc1eb336-5dec-40cc-8aa5-564cd167855d
title: Control de páginas de códigos de cadenas de parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a52872472d5509e1abdf35aa12be5afb6a8d13
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158893"
---
# <a name="code-page-handling-of-parameter-strings"></a>Control de páginas de códigos de cadenas de parámetros

Puede agregar información de localización a una base de datos de instalación mediante un editor de tablas [](database-functions.md) de base de datos como Orca que se proporciona con el SDK del instalador de Windows o llamando a las funciones de base de datos desde una aplicación. Tenga cuidado de pasar solo los parámetros de cadena que usan la página de códigos de la base de datos que se está localizando. Si un parámetro de cadena contiene caracteres que no se pueden representar mediante la página de códigos de la base de datos, el instalador devuelve un error al llamar a [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Para obtener una lista de páginas de códigos numéricos, vea [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md).

Para obtener más información, vea [Determinar la página de códigos de](determining-an-installation-database-s-code-page.md)una base de datos de instalación .

## <a name="adding-localization-information-to-a-database"></a>Agregar información de localización a una base de datos

Al agregar información de localización a una base de datos, el sistema operativo debe ser compatible con la página de códigos de la base de datos. No tiene que ser la página de códigos actual del sistema. [**IsValidCodePage debe**](/windows/desktop/api/winnls/nf-winnls-isvalidcodepage) devolver **TRUE para** la página de códigos de la base de datos. Dado que el sistema convierte cadenas ANSI en Unicode, se produce un error si la página de códigos de usuario actual no es la misma que la página de códigos de la base de datos.

Al llamar a la versión ANSI de Windows Installer API se convierte la cadena localizada en Unicode mediante la página de códigos del sistema actual. Cuando se confirma la base de datos, la cadena Unicode se convierte a ANSI mediante la página de códigos de la base de datos. Si la página de códigos del sistema actual difiere de la página de códigos de la cadena localizada, el resultado puede ser una pérdida de datos y una conversión de cadena incorrecta.

En el procedimiento siguiente se muestra cómo almacenar los datos de localización.

**Para almacenar datos de localización**

1.  Establezca la página de códigos de la base de datos en la página de códigos de la cadena localizada.
2.  Convierta la cadena ANSI a Unicode mediante la [**función MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) y especifique la página de códigos de los datos localizados.
3.  Llame a la versión Unicode de la API Windows Installer mediante la cadena Unicode para agregar los datos localizados.
4.  Confirme los cambios de localización en la base de datos [**mediante MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).

También puede agregar información de localización a una base de datos de instalación importando y exportando archivos de archivo de texto ASCII. Para obtener más información, vea [Control de páginas de códigos de tablas importadas y exportadas.](code-page-handling-of-imported-and-exported-tables.md)

 

 
