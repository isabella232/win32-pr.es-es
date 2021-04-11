---
description: Para obtener información general sobre la localización, vea servicios de globalización.
ms.assetid: 734961f6-de0a-4c54-9866-ade994c41c7e
title: Localizar un paquete de Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b325b211302fba632f454f30eefbcb688f30d819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154528"
---
# <a name="localizing-a-windows-installer-package"></a>Localizar un paquete de Windows Installer

Para obtener información general sobre la localización, vea [servicios de globalización](../intl/globalization-services.md). La localización de un paquete de Windows Installer requiere la modificación de las cadenas que muestra la interfaz de usuario y también puede requerir la adición o modificación de los recursos del producto. Por ejemplo, la localización puede incluir la adición de archivos dll internacionales y archivos localizados al producto.

**Para localizar un paquete de Windows Installer**

1.  Preparar la localización al crear el paquete de instalación original. Diseñar el diseño de archivos localizados de modo que las distintas versiones de idioma puedan coexistir de forma segura cuando se instalan en el equipo del usuario. Organice los archivos que requieren localización en componentes independientes e instálelos en directorios independientes. Cree una base de datos de instalación básica que tenga una página de control neutra. Consulte [preparación de un paquete de Windows Installer para la localización](preparing-a-windows-installer-package-for-localization.md).
2.  Establezca siempre la página de códigos de la base de datos que se va a localizar antes de agregar datos localizados. Si la página de códigos de la base de datos que se va a localizar es neutra, vea [establecer la página de códigos de una base de datos](setting-the-code-page-of-a-database.md). Para determinar la página de códigos, vea [determinar la página de códigos de una base de datos de instalación](determining-an-installation-database-s-code-page.md).
3.  Importe una tabla de [errores](error-table.md) localizada y una [tabla de ActionText](actiontext-table.md) en la base de datos. Para obtener más información, consulte [localizar las tablas de error y ActionText](localizing-the-error-and-actiontext-tables.md) para obtener una lista de los idiomas admitidos por el kit de desarrollo de software (SDK) de Microsoft Windows. Puede importar estas tablas mediante Msidb.exe o [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).
4.  Modifique cualquiera de las demás columnas localizables de la base de datos mediante un editor de tablas o consultas SQL. Para las funciones de acceso de SQL, consulte [trabajar con consultas](working-with-queries.md). En los temas de las tablas de base de datos se identifican las columnas de base de datos que se pueden localizar. Para obtener más información, vea la lista de tablas en [las tablas de base de datos](database-tables.md).
5.  Establezca la propiedad [**ProductLanguage**](productlanguage.md) de la [tabla de propiedades](property-table.md) en el LANGID de la base de datos. Al crear un paquete como idioma neutro, establezca la propiedad ProductLanguage en 0 y use la fuente MS Shell Dlg como estilo de texto para todos los cuadros de diálogo creados. Dado que algunas fuentes no admiten todos los juegos de caracteres, puede asegurarse de que el texto se muestre correctamente en todas las versiones localizadas del sistema operativo con esta fuente.
6.  Establezca el campo Language de la propiedad Summary de la [**plantilla**](template-summary.md) para que refleje el LANGID de la base de datos.
7.  Si las cadenas de texto del [flujo de información de Resumen](summary-information-stream.md) están localizadas, establezca la propiedad de Resumen de la página de [**códigos**](codepage-summary.md) en la página de códigos.
8.  Establezca la propiedad [**ProductCode**](productcode.md) en la [tabla de propiedades](property-table.md) y establezca el código del paquete en la propiedad Resumen del [**número de revisión**](revision-number-summary.md) en un nuevo código de paquete. Un producto localizado se considera un producto diferente. Por ejemplo, las versiones en alemán y en Inglés de una aplicación se consideran dos productos diferentes y deben tener distintos códigos de producto.
9.  La localización puede requerir la modificación de los recursos que ya existen o la adición de nuevos recursos como archivos o claves del registro. Asegúrese de que el código del componente se cambia para cada componente existente al que se ha agregado un nuevo recurso. Otras modificaciones también pueden requerir cambios en el código de un componente. Para obtener más información, vea [cambiar el código de componente](changing-the-component-code.md).
10. Asegúrese de guardar la localización y otros cambios en la base de datos guardando el paquete con la herramienta de edición o llamando a [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).

Para obtener más información, vea [un ejemplo de localización](a-localization-example.md).

 

 
