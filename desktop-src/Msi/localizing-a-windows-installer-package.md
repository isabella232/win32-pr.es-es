---
description: Para obtener información general sobre la localización, vea Globalization Services.
ms.assetid: 734961f6-de0a-4c54-9866-ade994c41c7e
title: Localización de un paquete Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b325b211302fba632f454f30eefbcb688f30d819
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071945"
---
# <a name="localizing-a-windows-installer-package"></a>Localización de un paquete Windows Installer

Para obtener información general sobre la localización, vea [Globalization Services](../intl/globalization-services.md). La localización de un Windows Installer requiere modificar las cadenas mostradas por la interfaz de usuario y también puede requerir agregar o modificar recursos del producto. Por ejemplo, la localización puede incluir la adición de archivos DLL internacionales y archivos localizados al producto.

**Para encontrar un paquete Windows Installer**

1.  Prepárese para la localización al crear el paquete de instalación original. Diseñe el diseño de los archivos localizados de forma que las distintas versiones de idioma puedan coexistir de forma segura cuando se instalan en el equipo del usuario. Organice los archivos que requieren localización en componentes independientes e instale estos archivos en directorios independientes. Cree una base de datos de instalación base que tenga una página de control neutra. Vea [Preparar un paquete Windows Installer para la localización.](preparing-a-windows-installer-package-for-localization.md)
2.  Establezca siempre la página de códigos de la base de datos que se va a localizar antes de agregar los datos localizados. Si la página de códigos de la base de datos que se localiza es neutra, vea [Establecer la página de códigos de una base de datos](setting-the-code-page-of-a-database.md). Para determinar la página de códigos, vea [Determinar la página de códigos de una base de datos de instalación](determining-an-installation-database-s-code-page.md).
3.  Importe una tabla [error localizada y](error-table.md) una tabla [ActionText](actiontext-table.md) en la base de datos. Para obtener más información, vea Localización de las tablas Error y [ActionText](localizing-the-error-and-actiontext-tables.md) para obtener una lista de los idiomas admitidos por el Kit de desarrollo de software (SDK) de Microsoft Windows. Puede importar estas tablas mediante Msidb.exe [**o MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).
4.  Modifique cualquiera de las demás columnas localizables de la base de datos mediante un editor de tablas o SQL consultas. Para obtener SQL de acceso, vea [Trabajar con consultas](working-with-queries.md). Los temas de las tablas de base de datos identifican qué columnas de base de datos se pueden localizar. Para obtener más información, vea la lista de tablas de tablas [de base de datos](database-tables.md).
5.  Establezca la [**propiedad ProductLanguage de**](productlanguage.md) la [tabla Property](property-table.md) en el LANGID de la base de datos. Al crear un paquete como idioma neutro, establezca la propiedad ProductLanguage en 0 y use la fuente Dlg de MS Shell como estilo de texto para todos los cuadros de diálogo de creación. Dado que algunas fuentes no admiten todos los juegos de caracteres, puede asegurarse de que el texto se muestra correctamente en todas las versiones localizadas del sistema operativo mediante esta fuente.
6.  Establezca el campo de idioma de la [**propiedad Resumen de**](template-summary.md) plantilla para reflejar el LANGID de la base de datos.
7.  Si las cadenas de texto de la secuencia de información de [resumen](summary-information-stream.md) están localizadas, establezca la [**propiedad Resumen**](codepage-summary.md) de página de códigos en la página de códigos.
8.  Establezca la [**propiedad ProductCode**](productcode.md) en la [tabla Property](property-table.md) y establezca el código del paquete de la propiedad [**Resumen**](revision-number-summary.md) del número de revisión en un nuevo código de paquete. Un producto localizado se considera un producto diferente. Por ejemplo, las versiones en alemán e inglés de una aplicación se consideran dos productos diferentes y deben tener códigos de producto diferentes.
9.  La localización puede requerir la modificación de los recursos que ya existen o la adición de nuevos recursos, como archivos o claves del Registro. Asegúrese de que se cambia el código del componente para todos los componentes existentes a los que se ha agregado un nuevo recurso. Otras modificaciones también pueden requerir cambios en el código de un componente. Para obtener más información, [vea Cambiar el código del componente](changing-the-component-code.md).
10. Asegúrese de guardar la localización y otros cambios en la base de datos guardando el paquete con la herramienta de edición o llamando a [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).

Para obtener más información, vea [Un ejemplo de localización](a-localization-example.md).

 

 
