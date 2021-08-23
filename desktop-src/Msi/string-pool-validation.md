---
description: El Windows almacena todas las cadenas de base de datos en un único grupo de cadenas compartidas para reducir el tamaño de la base de datos y mejorar el rendimiento.
ms.assetid: b627f3da-3545-4c1a-85b0-d8845fdac621
title: String-Pool validación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1e895a9e9032cb0cf5d94b5a8c3c9070c46fe79041dee41e4ea10366043b4af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627365"
---
# <a name="string-pool-validation"></a>String-Pool validación

El Windows almacena todas las cadenas de base de datos en un único grupo de cadenas compartidas para reducir el tamaño de la base de datos y mejorar el rendimiento. El único medio de validar el grupo de cadenas es usar la herramienta MsiInfo que se encuentra en el SDK Windows Installer.

La comprobación del grupo de cadenas consta de dos comprobaciones principales:

-   [Pruebas de cadena de DBCS](#dbcs-string-tests)
-   [Comprobación del recuento de referencias](#reference-count-verification)

## <a name="dbcs-string-tests"></a>Pruebas de cadena de DBCS

Las pruebas de cadena dbcs analizan cada cadena de la base de datos en busca de dos criterios: para los paquetes con una página de códigos neutra marcada, si algún carácter es un carácter extendido (mayor que 127), la cadena se marca y se muestra un mensaje que indica que la página de códigos de la base de datos no es válida porque estos caracteres requieren que una página de códigos específica se represente de forma coherente en todos los sistemas.

Si la base de datos tiene una página de códigos, se examina cada cadena en busca de un indicador DBCS no válido. Si una cadena no neutra se ha marcado incorrectamente, los caracteres no se representarán correctamente. (Esto se produce normalmente al forzar la página de códigos a un valor determinado mediante el \_ Tabla ForceCodepage con cadenas no neutras que ya están en la base de datos). Tenga en cuenta que esta comprobación requiere que la página de códigos de la base de datos esté instalada en el sistema.

Si hay un problema en la página de códigos, el usuario puede corregir el error mediante la tabla ForceCodepage para forzar la página de códigos de la base de datos \_ al valor adecuado. Para obtener más información, vea [Control de páginas de códigos.](code-page-handling-windows-installer-.md)

## <a name="reference-count-verification"></a>Comprobación del recuento de referencias

Para comprobar los recuentos de referencias de todas las cadenas, se examina cada tabla en busca de valores de cadena, se mantiene un recuento de cada cadena distinta y el resultado se compara con el recuento de referencias almacenado en el grupo de cadenas de base de datos.

Si hay un problema de recuento de referencias de cadena, el usuario debe exportar inmediatamente cada tabla de la base de datos mediante [**MsiDatabaseExport,**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)crear una nueva base de datos e importar las tablas en la nueva base de datos [**mediante MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). A continuación, la nueva base de datos tiene el mismo contenido que la base de datos anterior, pero los recuentos de referencias de cadena son correctos. Agregar o eliminar datos de una base de datos con un grupo de cadenas dañado puede aumentar los daños en la base de datos y la pérdida de datos, por lo que es importante realizar estos pasos rápidamente para evitar una mayor pérdida de datos.

Al volver a generar bases de datos, no olvide insertar los almacenamientos y secuencias necesarios en la nueva base de datos (consulte [ \_ Secuencias Table](-streams-table.md) and [ \_ Storages Table](-storages-table.md)) y tenga en cuenta los problemas de la página de códigos. Recuerde también establecer cada una de las propiedades [de Flujo de información de resumen](summary-information-stream.md) necesarias.

 

 



