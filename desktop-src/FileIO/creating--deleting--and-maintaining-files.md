---
description: Funciones que se van a usar para crear, eliminar y mantener archivos.
ms.assetid: b9cf0ddf-efda-4997-bcc3-3056026c1264
title: Crear, eliminar y mantener archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 921388e84ac44a42e0c24880b1b56971ba84c12b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669698"
---
# <a name="creating-deleting-and-maintaining-files"></a>Crear, eliminar y mantener archivos

En los temas siguientes se describe cómo crear, eliminar y mantener archivos.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                   | Descripción                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Nomenclatura de archivos, rutas de acceso y espacios de nombres](naming-a-file.md)<br/>     | Reglas, convenciones y limitaciones de los nombres de archivos y directorios, incluidas las convenciones de nomenclatura, los nombres de archivo cortos y los nombres de archivo largos, rutas de acceso completas frente a rutas de acceso relativas, límite de longitud de ruta de acceso máxima, nombres de archivo de 8,3 y espacios de nombres.<br/>            |
| [Crear y abrir archivos](creating-and-opening-files.md)<br/> | Consideraciones para crear o abrir un archivo mediante la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .<br/>                                                                                                                                                            |
| [Mover y reemplazar archivos](moving-and-replacing-files.md)<br/> | Consideraciones para mover y reemplazar archivos mediante las funciones CopyFileEx, CreateFile, Replacefile y MoveFileEx.<br/>                                                                                                                                        |
| [Cerrar y eliminar archivos](closing-and-deleting-files.md)<br/> | Para utilizar los recursos del sistema operativo de forma eficaz, una aplicación debe cerrar los archivos cuando ya no se necesiten mediante la función [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) . Si un archivo está abierto cuando una aplicación finaliza, el sistema lo cierra automáticamente.<br/> |
| [Desfragmentar archivos](defragmenting-files.md)<br/>               | La *desfragmentación* es el proceso por el que se mueven partes de los archivos en un disco para desfragmentar archivos, es decir, el proceso de mover los clústeres de archivos de un disco para que sean contiguos.<br/>                                                                               |



 

 

