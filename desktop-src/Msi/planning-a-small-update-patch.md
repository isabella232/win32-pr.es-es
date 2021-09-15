---
description: El archivo de características concert del producto original, MNP2000, contiene un error en el Concert.txt archivo.
ms.assetid: 4289bd0c-bdf3-4747-9287-94f737ce4f5c
title: Planear una revisión de actualización pequeña
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f15f3667c6a18ab7a71e86997091bd76d4b15577
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473972"
---
# <a name="planning-a-small-update-patch"></a>Planear una revisión de actualización pequeña

El archivo de características concert del producto original, MNP2000, contiene un error en el Concert.txt archivo. Dado Windows instalador de actualizaciones se usó para la instalación y configuración de la aplicación, las correcciones secundarias de la aplicación se pueden controlar mediante la instalación de un pequeño paquete de revisión de actualización. Una [pequeña actualización realiza](small-updates.md) cambios en uno o varios archivos de aplicación que son demasiado menores para cambiar el código del producto. En el ejemplo siguiente se muestra cómo crear un paquete de revisión de Windows Installer que puede aplicar la pequeña actualización y proporcionar una corrección rápida al producto MNP2000.

Para crear la actualización pequeña, obtenga primero una imagen completamente sin comprimir del producto MNP2000 que incluya el error en Concert.txt. La imagen debe incluir MNP2000.msi y todos los archivos de origen descritos en [Planeamiento de la instalación de](planning-the-installation.md). En la siguiente explicación, esto se denomina imagen de destino. La imagen de destino debe estar completamente descomprimida porque el proceso de creación de revisiones no puede generar revisiones binarias para archivos comprimidos en archivadores. Coloque el .msi y todos los archivos de origen de la imagen de destino en una carpeta denominada Destino.

A continuación, obtenga una imagen completamente descomprimida del producto MNP2000 con un Concert.txt fijo. Esto se denomina imagen actualizada en la explicación siguiente. Use una herramienta de edición de base de datos de instalación, como Orca, para actualizar el archivo .msi instalación. Por ejemplo, si el tamaño del archivo Concert.txt es menor que el original, asegúrese de escribir el nuevo tamaño en el campo FileSize de la tabla File de la imagen actualizada. Tenga en cuenta que, dado que el paquete ha cambiado, debe asignar un nuevo código de paquete en la [**propiedad Resumen de número de**](revision-number-summary.md) revisión. Coloque el .msi y todos los archivos de origen de la imagen actualizada en una carpeta denominada Actualizado.

Para los fines de este ejemplo, suponga que cambia el tamaño del Concert.txt archivo. Esto significa que los campos FileSize de las tablas File de la base de datos Target y Upgraded contienen datos diferentes.

En la [tabla de archivos siguiente](file-table.md) se identifica el registro de la imagen de destino.



| Archivo        | Componente\_ | FileName    | FileSize | Versión | Idioma | Atributos | Secuencia |
|-------------|-------------|-------------|----------|---------|----------|------------|----------|
| Concert.txt | Concierto     | Concert.txt | 1000     |         |          | 0          | 1        |



 

En la tabla de archivos siguiente se identifica el registro de la imagen actualizada.



| Archivo        | Componente\_ | FileName    | FileSize | Versión | Idioma | Atributos | Secuencia |
|-------------|-------------|-------------|----------|---------|----------|------------|----------|
| Concert.txt | Concierto     | Concert.txt | 900      |         |          | 0          | 1        |



 

> [!Note]
> El archivo debe tener la misma clave en las tablas [de archivos](file-table.md) de la imagen de destino y de la imagen actualizada. Los valores de cadena de la columna Archivo de ambas tablas deben ser idénticos. Las mayúsculas y minúsculas también deben ser idénticas.
> 
> Siga las instrucciones descritas en [Creación de un paquete de revisión.](creating-a-patch-package.md) No cree un [](file-table.md) paquete con claves de tabla de archivos que solo difieren por mayúsculas y minúsculas, porque [Msimsp.exe](msimsp-exe.md) yPatchwiz.dllllaman [Makecab.exe,](patchwiz-dll.md) que no distingue mayúsculas de minúsculas y se produce un error en la generación de revisiones.

[Continuar](creating-a-patch-creation-properties-file.md)

 

 



