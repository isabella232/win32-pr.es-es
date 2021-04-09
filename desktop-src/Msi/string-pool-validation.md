---
description: El Windows Installer almacena todas las cadenas de base de datos en un único grupo de cadenas compartidas para reducir el tamaño de la base de datos y mejorar el rendimiento.
ms.assetid: b627f3da-3545-4c1a-85b0-d8845fdac621
title: Validación de String-Pool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb544b5c76026846f7e8b8f6f331195426ab55c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155124"
---
# <a name="string-pool-validation"></a>Validación de String-Pool

El Windows Installer almacena todas las cadenas de base de datos en un único grupo de cadenas compartidas para reducir el tamaño de la base de datos y mejorar el rendimiento. El único medio para validar el grupo de cadenas es usar la herramienta MsiInfo que se encuentra en el SDK de Windows Installer.

La comprobación del grupo de cadenas consta de dos comprobaciones principales:

-   [Pruebas de cadenas DBCS](#dbcs-string-tests)
-   [Comprobación del recuento de referencias](#reference-count-verification)

## <a name="dbcs-string-tests"></a>Pruebas de cadenas DBCS

Las pruebas de cadenas DBCS examinan cada cadena de la base de datos para ver si hay dos criterios: en el caso de los paquetes con una página de códigos neutra marcada, si alguno de los caracteres es un carácter extendido (mayor que 127), la cadena se marca y se muestra un mensaje que indica que la página de códigos de la base de datos no es válida, ya que estos caracteres requieren

Si la base de datos tiene una página de códigos, se examina cada cadena para detectar un indicador DBCS no válido. Si una cadena no neutra se ha marcado incorrectamente, los caracteres no se representarán correctamente. (Esto se debe normalmente al forzar la página de códigos a un valor determinado mediante el \_ Tabla ForceCodepage con cadenas no neutras que ya están en la base de datos.) Tenga en cuenta que esta comprobación requiere que la página de códigos de la base de datos esté instalada en el sistema.

Si hay un problema de página de códigos, el usuario puede corregir el error mediante la \_ tabla ForceCodepage para forzar a la página de códigos de la base de datos al valor adecuado. Para obtener más información, vea [control de páginas de códigos](code-page-handling-windows-installer-.md).

## <a name="reference-count-verification"></a>Comprobación del recuento de referencias

Para comprobar los recuentos de referencias de todas las cadenas, se examinan los valores de cadena de cada tabla, se mantiene un recuento de cada cadena distinta y el resultado se compara con el recuento de referencias almacenado en el grupo de cadenas de base de datos.

Si hay un problema de recuento de referencias de cadena, el usuario debe exportar inmediatamente cada tabla de la base de datos mediante [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), crear una nueva base de datos e importar las tablas en la nueva base de datos mediante [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). La nueva base de datos tiene el mismo contenido que la antigua, pero los recuentos de referencias de cadena son correctos. Agregar o eliminar datos de una base de datos con un grupo de cadenas dañado puede aumentar el daño de la base de datos y la pérdida de datos, por lo que realizar estos pasos rápidamente es importante para evitar la pérdida de datos.

Al volver a generar las bases de datos, recuerde insertar los flujos y almacenamientos necesarios en la nueva base de datos (consulte [ \_ tabla](-storages-table.md)de [ \_ transmisiones](-streams-table.md) y tablas de almacenamiento) y tener en cuenta los problemas de las páginas de códigos. Recuerde también establecer cada una de las propiedades de [flujo de información de Resumen](summary-information-stream.md) necesarias.

 

 



