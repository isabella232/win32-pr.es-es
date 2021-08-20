---
description: Para validar una base de datos, use una herramienta de validación especial para combinar un archivo .cub que contiene los evaluadores de coherencia internos (ICE) en la base de datos, ejecutar los ICE e informar de los resultados.
ms.assetid: bdf38673-ee3d-47d8-ad6e-562cd5626918
title: Uso de evaluadores de coherencia internos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd0964b43bdf237c01b2645ca9556ed5560cefd2b047cc108a8919060d1fad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012753"
---
# <a name="using-internal-consistency-evaluators"></a>Uso de evaluadores de coherencia internos

Para validar una base de datos, use una herramienta de validación especial para combinar un archivo .cub que contiene los evaluadores de coherencia internos (ICE) en la base de datos, ejecutar los ICE e informar de los [resultados.](internal-consistency-evaluators-ices.md) Varias de estas herramientas se proporcionan en microsoft Windows Software Development Kit (SDK). Los entornos de creación de proveedores de terceros también pueden incorporar el sistema de validación ice en su entorno de creación. También es posible escribir su propia herramienta para realizar la validación de ICE. La mayoría de las herramientas de validación de ICE combinan el archivo .ice y la base de datos en una tercera base de datos temporal. Windows El instalador muestra advertencias, errores, información de depuración y errores de API a medida que ejecuta cada ICE en el archivo .ice. Cuando el instalador termina de ejecutar los ICE, cierra el archivo .msi, el archivo .cub y la base de datos temporal sin guardar ningún cambio. La .msi archivo y el archivo .cub permanecen sin cambios en la prueba de validación.

Las acciones personalizadas de ICE se comunican con el usuario mediante una [**llamada a MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) y la publicación de un mensaje INSTALLMESSAGE \_ USER. Un mensaje ICE normalmente devuelve información como la siguiente:

-   Nombre del ICE que ha encontrado un error
-   Fecha en que se creó el ICE
-   Autor del ICE
-   Fecha en que se modificó por última vez el ICE.
-   Descripción del error de API que provoca un error en el ICE
-   Descripción del error
-   Una advertencia para el usuario
-   Nombre de la tabla de base de datos que contiene el error o la advertencia
-   Nombre de la columna de tabla que contiene el error o la advertencia
-   Claves principales de la tabla que contiene el error o la advertencia
-   Una dirección URL a un archivo HTML que ofrece sugerencias de depuración
-   Cadena que puede contener otra información

Los autores de paquetes de instalación pueden escribir acciones personalizadas de ICE o usar el conjunto estándar de TIC incluidos en los archivos .packs proporcionados con el SDK. Para obtener más información sobre cómo escribir un ICE, consulte [Creación de un ICE.](building-an-ice.md)

Después de escribir los TIC adecuados para la validación, un desarrollador debe recopilar las acciones personalizadas juntas en una base de datos de .msi, denominada archivo .uu., que contiene solo los TIC y sus tablas necesarias. No se puede instalar un archivo .cub y solo se usa para almacenar y proporcionar acceso a acciones personalizadas de ICE. Para obtener más información sobre cómo crear archivos .uu., vea [Building an ICE Database](building-an-ice-database.md). Como alternativa, los desarrolladores pueden validar su paquete de instalación mediante los TIC existentes descritos en [Referencia de ICE.](ice-reference.md) Estos TIC se pueden obtener a partir de archivos .uu. estándar proporcionados con el SDK.

La instalación del editor de tablas de base de datos Orca o la herramienta de validación msival2 proporciona los archivos Logo.rev, Darice.rev y Mergemod.rev. El conjunto de ICEs del archivo Logo.rev es un subconjunto de los del archivo Darice.rev. Si el paquete pasa la validación mediante Darice.rev, pasará con Logo.rev. Mergemod.cub contiene un conjunto de TIC que se usan para validar los módulos de combinación. Para obtener más información, vea [Referencia de ICE del módulo de mezcla](merge-module-ice-reference.md).

**Para validar un paquete de instalación**

1.  Obtenga o cree las acciones personalizadas de ICE adecuadas. Es posible que pueda usar uno o varios de los TIC existentes que se describen en la referencia [de ICE.](ice-reference.md) Si la validación requiere un ICE que aún no está en esta lista, puede crear un nuevo ICE como se describe en [Creación de un ICE.](building-an-ice.md)
2.  Prepare una base de datos de ICE que contenga todas las acciones personalizadas de ICE. Consulte la sección Building An ICE Database (Creación de [una base de datos ice)](building-an-ice-database.md) para obtener información sobre cómo preparar un archivo .uu.
3.  Proporcione el archivo .cub y el .msi a una herramienta de validación de [ paquetes, comoOrca.exe](orca-exe.md) o [Msival2.exe](msival2-exe.md).

Tenga en cuenta que los módulos de combinación deben validarse como se describe [en Validación de módulos de mezcla](validating-merge-modules.md).

 

 



