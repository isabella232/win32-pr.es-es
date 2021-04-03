---
description: El archivo de características de concierto del producto original, MNP2000, contiene un error en el archivo de Concert.txt.
ms.assetid: 4289bd0c-bdf3-4747-9287-94f737ce4f5c
title: Planeación de una revisión de actualización pequeña
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f15f3667c6a18ab7a71e86997091bd76d4b15577
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "103914250"
---
# <a name="planning-a-small-update-patch"></a>Planeación de una revisión de actualización pequeña

El archivo de características de concierto del producto original, MNP2000, contiene un error en el archivo de Concert.txt. Dado que Windows Installer se usó para la instalación y la configuración de la aplicación, las correcciones secundarias en la aplicación se pueden controlar mediante la instalación de un paquete de revisión de actualización pequeño. Una [actualización pequeña](small-updates.md) realiza cambios en uno o varios archivos de aplicación que son demasiado pequeños para cambiar el código de producto. En el ejemplo siguiente se muestra cómo crear un paquete de revisión de Windows Installer que puede aplicar la actualización pequeña y proporcionar una corrección rápida del producto MNP2000.

Para crear la actualización pequeña, primero obtenga una imagen totalmente descomprimida del producto MNP2000 que incluye el error en Concert.txt. La imagen debe incluir MNP2000.msi y todos los archivos de código fuente descritos en [planear la instalación](planning-the-installation.md). En la siguiente explicación, esto se denomina imagen de destino. La imagen de destino debe descomprimirse completamente porque el proceso de creación de revisiones no puede generar revisiones binarias para archivos comprimidos en los archivadores. Coloque el archivo. msi y todos los archivos de origen de la imagen de destino en una carpeta denominada Target.

A continuación, obtenga una imagen totalmente descomprimida del producto MNP2000 con un archivo Concert.txt que sea fijo. Esto se denomina imagen actualizada en la siguiente explicación. Use una herramienta de edición de base de datos de instalación, como orca, para actualizar el archivo. msi. Por ejemplo, si el tamaño de la Concert.txt corregida es menor que el original, asegúrese de especificar el nuevo tamaño en el campo de archivo de la tabla de archivos de la imagen actualizada. Tenga en cuenta que, dado que el paquete ha cambiado, debe asignar un nuevo código de paquete en la propiedad [**Resumen del número de revisión**](revision-number-summary.md) . Coloque el archivo. msi y todos los archivos de origen de la imagen actualizada en una carpeta denominada actualizado.

Para los fines de este ejemplo, supongamos que cambia el tamaño del archivo Concert.txt. Esto significa que los campos de archivo de las tablas de archivos del destino y de la base de datos actualizada contienen datos diferentes.

La siguiente [tabla de archivos](file-table.md) identifica el registro de la imagen de destino.



| Archivo        | Componente\_ | FileName    | FileSize | Versión | Idioma | Atributos | Secuencia |
|-------------|-------------|-------------|----------|---------|----------|------------|----------|
| Concert.txt | Concierto     | Concert.txt | 1000     |         |          | 0          | 1        |



 

La siguiente tabla de archivos identifica el registro de la imagen actualizada.



| Archivo        | Componente\_ | FileName    | FileSize | Versión | Idioma | Atributos | Secuencia |
|-------------|-------------|-------------|----------|---------|----------|------------|----------|
| Concert.txt | Concierto     | Concert.txt | 900      |         |          | 0          | 1        |



 

> [!Note]
> El archivo debe tener la misma clave en las [tablas de archivo](file-table.md) de la imagen de destino y la imagen actualizada. Los valores de cadena de la columna de archivo de ambas tablas deben ser idénticos. Los caracteres en mayúsculas y minúsculas también deben ser idénticos.
> 
> Siga las directrices descritas en [creación de un paquete de revisión](creating-a-patch-package.md). No cree un paquete con claves de [tabla de archivos](file-table.md) que solo se diferencien por mayúsculas y minúsculas, porque [Msimsp.exe](msimsp-exe.md) y [Patchwiz.dll](patchwiz-dll.md) llaman a Makecab.exe, que no distingue entre mayúsculas y minúsculas y se produce un error en la generación de revisiones.

[Continuar](creating-a-patch-creation-properties-file.md)

 

 



