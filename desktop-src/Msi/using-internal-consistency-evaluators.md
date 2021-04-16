---
description: Para validar una base de datos, use una herramienta de validación especial para combinar un archivo. Cub que contenga los evaluadores de coherencia internos (CIEM) en la base de datos, ejecute el ICEs y informe de los resultados.
ms.assetid: bdf38673-ee3d-47d8-ad6e-562cd5626918
title: Usar evaluadores de coherencia interna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423e6dab453ae495dc6029b54eb039c8acc60f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677397"
---
# <a name="using-internal-consistency-evaluators"></a>Usar evaluadores de coherencia interna

Para validar una base de datos, use una herramienta de validación especial para combinar un archivo. Cub que contenga los [evaluadores de coherencia internos](internal-consistency-evaluators-ices.md) (CIEM) en la base de datos, ejecute el ICEs y informe de los resultados. En el kit de desarrollo de software (SDK) de Microsoft Windows se proporcionan varias herramientas de este tipo. Los entornos de creación de otros fabricantes también pueden incorporar el sistema de validación de ICE a su entorno de creación. También es posible escribir su propia herramienta para realizar la validación de ICE. La mayoría de las herramientas de validación de ICE combinan el archivo. Cub y la base de datos en una tercera base de datos temporal. En Windows Installer se muestran las advertencias, los errores, la información de depuración y los errores de API cuando se ejecuta cada ICE en el archivo. Cub. Cuando el instalador termina de ejecutar el ICEs, cierra el archivo. msi, el archivo. Cub y la base de datos temporal sin guardar los cambios. El archivo. msi y el archivo. Cub permanecen inalterados por la prueba de validación.

Las acciones personalizadas de ICE se comunican con el usuario mediante una llamada a [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) y el envío de un mensaje de usuario de INSTALLMESSAGE \_ . Un mensaje de ICE suele devolver información como la siguiente:

-   Nombre del ICE que ha encontrado un error
-   Fecha en que se creó el ICE
-   Autor del ICE
-   Fecha en que se modificó por última vez el ICE.
-   Descripción del error de API que produce un error en ICE
-   Descripción del error
-   ADVERTENCIA al usuario
-   Nombre de la tabla de la base de datos que contiene el error o la advertencia
-   Nombre de la columna de la tabla que contiene el error o la advertencia
-   Claves principales de la tabla que contiene el error o la advertencia
-   Una dirección URL a un archivo HTML que ofrece sugerencias de depuración
-   Una cadena que puede contener otra información.

Los autores de paquetes de instalación pueden escribir acciones personalizadas de ICE o utilizar el conjunto estándar de CIEM incluido en los archivos. Cub que se proporcionan con el SDK. Para obtener más información sobre cómo escribir un ICE, consulte [creación de un ICE](building-an-ice.md).

Después de escribir el ICEs apropiado para la validación, el desarrollador debe recopilar las acciones personalizadas en una base de datos. msi, denominada archivo. Cub, que solo contiene el ICEs y las tablas necesarias. No se puede instalar un archivo. Cub y solo se usa para almacenar y proporcionar acceso a las acciones personalizadas de ICE. Para obtener más información sobre cómo crear archivos. Cub, vea [crear una base de datos de ICE](building-an-ice-database.md). Como alternativa, los desarrolladores pueden validar su paquete de instalación mediante el ICEs existente descrito en [referencia de ICE](ice-reference.md). Estos se pueden obtener a partir de archivos. Cub estándar que se proporcionan con el SDK.

La instalación del editor de tablas de base de datos Orca o la herramienta de validación msival2 proporciona los archivos logo. Cub, Darice. Cub y Mergemod. Cub. El conjunto de ICEs en el archivo logo. Cub es un subconjunto de los del archivo Darice. Cub. Si el paquete pasa la validación mediante Darice. Cub, se pasará con logo. Cub. Mergemod. Cub contiene un conjunto de ICEs que se usa para validar los módulos de combinación. Para obtener más información, consulte [Merge Module Ice Reference](merge-module-ice-reference.md).

**Para validar un paquete de instalación**

1.  Obtenga o cree las acciones personalizadas de ICE adecuadas. Es posible que pueda usar uno o más de los CIEM existentes descritos en la [referencia de ICE](ice-reference.md). Si la validación requiere un ICE que todavía no se encuentra en esta lista, puede crear un nuevo ICE como se describe en [creación de un ICE](building-an-ice.md).
2.  Preparar una base de datos de ICE que contenga todas las acciones personalizadas de ICE. Vea la sección [Building a Ice Database](building-an-ice-database.md) para obtener información sobre cómo preparar un archivo. Cub.
3.  Proporcione el archivo. Cub y el archivo. msi a una herramienta de validación de paquetes como [Orca.exe](orca-exe.md) o [Msival2.exe](msival2-exe.md).

Tenga en cuenta que los módulos de combinación deben validarse tal y como se describe en [validación de módulos de combinación](validating-merge-modules.md).

 

 



