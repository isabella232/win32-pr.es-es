---
description: Para validar una base de datos, use una herramienta de validación especial para combinar un archivo .uu. que contiene los evaluadores de coherencia interna (CIE) en la base de datos, ejecutar los TIC e informar de los resultados.
ms.assetid: bdf38673-ee3d-47d8-ad6e-562cd5626918
title: Uso de evaluadores de coherencia internos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423e6dab453ae495dc6029b54eb039c8acc60f33
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254037"
---
# <a name="using-internal-consistency-evaluators"></a>Uso de evaluadores de coherencia internos

Para validar una base de datos, use una herramienta de validación especial para combinar un archivo .uu. que contiene los evaluadores de coherencia interna (CIE) en la base de datos, ejecutar los TIC e informar de los [resultados.](internal-consistency-evaluators-ices.md) Varias de estas herramientas se proporcionan en Microsoft Windows Software Development Kit (SDK). Los entornos de creación de proveedores de terceros también pueden incorporar el sistema de validación de ICE en su entorno de creación. También es posible escribir su propia herramienta para realizar la validación de ICE. La mayoría de las herramientas de validación de ICE combinan el archivo .uu. y la base de datos en una tercera base de datos temporal. Windows El instalador muestra advertencias, errores, información de depuración y errores de API a medida que ejecuta cada ICE en el archivo .uu. Cuando el instalador termina de ejecutar los ICE, cierra el archivo .msi, el archivo .uu. y la base de datos temporal sin guardar ningún cambio. La .msi archivo y el archivo .uu. permanecen sin cambios en la prueba de validación.

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
-   Claves principales de la tabla que contiene el error o advertencia
-   Una dirección URL a un archivo HTML que ofrece sugerencias de depuración
-   Cadena que puede contener otra información

Los autores de paquetes de instalación pueden escribir acciones personalizadas de ICE o usar el conjunto estándar de TIC incluidos en los archivos .packs proporcionados con el SDK. Para obtener más información sobre cómo escribir un ICE, vea Building an ICE ( [Creación de un ICE).](building-an-ice.md)

Después de escribir los TIC adecuados para la validación, un desarrollador debe recopilar las acciones personalizadas juntas en una base de datos de .msi, denominada archivo .csv, que contiene solo los TIC y sus tablas necesarias. No se puede instalar un archivo .uu. y solo se usa para almacenar y proporcionar acceso a acciones personalizadas de ICE. Para obtener más información sobre cómo crear archivos .uu., vea [Building an ICE Database](building-an-ice-database.md). Como alternativa, los desarrolladores pueden validar su paquete de instalación mediante los TIC existentes descritos en [La referencia de ICE](ice-reference.md). Estos TIC se pueden obtener a partir de archivos .uu. estándar proporcionados con el SDK.

La instalación del editor de tablas de base de datos Orca o la herramienta de validación msival2 proporciona los archivos Logo.rev, Darice.rev y Mergemod.uu. El conjunto de ICE del archivo Logo.uu. es un subconjunto de los del archivo Darice.rev. Si el paquete pasa la validación mediante Darice.rev, se pasará con Logo.uu. Mergemod.uu contiene un conjunto de TIC que se usan para validar los módulos de combinación. Para obtener más información, vea [Merge Module ICE Reference](merge-module-ice-reference.md).

**Para validar un paquete de instalación**

1.  Obtenga o cree las acciones personalizadas de ICE adecuadas. Es posible que pueda usar uno o varios de los TIC existentes descritos en la referencia [de ICE.](ice-reference.md) Si la validación requiere un ICE que aún no está en esta lista, puede crear un NUEVO ICE como se describe en [Creación de un ICE.](building-an-ice.md)
2.  Prepare una base de datos ice que contenga todas las acciones personalizadas de ICE. Consulte la sección Building An ICE Database (Creación de [una base de datos ICE)](building-an-ice-database.md) para obtener información sobre cómo preparar un archivo .uu.
3.  Proporcione el archivo .uu. y el .msi a una herramienta de validación de [ paquetes, comoOrca.exe](orca-exe.md) o [Msival2.exe](msival2-exe.md).

Tenga en cuenta que los módulos de combinación deben validarse como se describe [en Validación de módulos de mezcla.](validating-merge-modules.md)

 

 



