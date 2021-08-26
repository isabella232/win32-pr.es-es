---
description: Funciones que se usan para crear, eliminar y mantener archivos.
ms.assetid: b9cf0ddf-efda-4997-bcc3-3056026c1264
title: Crear, eliminar y mantener archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff20362e2ff5f1d8b01b515c7cbbb9fae250d930b2610c49c5e8aaeeabe7b401
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982125"
---
# <a name="creating-deleting-and-maintaining-files"></a>Crear, eliminar y mantener archivos

En los temas siguientes se describe cómo crear, eliminar y mantener archivos.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                   | Descripción                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Asignar nombres a archivos, rutas de acceso y espacios de nombres](naming-a-file.md)<br/>     | Reglas, convenciones y limitaciones de nombres para archivos y directorios, incluidas convenciones de nomenclatura, nombres de archivo cortos frente a nombres de archivo largos, rutas de acceso completas frente a rutas de acceso relativas, limitación de longitud máxima de ruta de acceso, nombres de archivo 8.3 y espacios de nombres.<br/>            |
| [Crear y abrir archivos](creating-and-opening-files.md)<br/> | Consideraciones para crear o abrir un archivo mediante la [**función CreateFile.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)<br/>                                                                                                                                                            |
| [Mover y reemplazar archivos](moving-and-replacing-files.md)<br/> | Consideraciones para mover y reemplazar archivos mediante las funciones CopyFileEx, CreateFile, Replacefile y MoveFileEx.<br/>                                                                                                                                        |
| [Cerrar y eliminar archivos](closing-and-deleting-files.md)<br/> | Para usar los recursos del sistema operativo de forma eficaz, una aplicación debe cerrar los archivos cuando ya no sean necesarios mediante la [**función CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) Si un archivo está abierto cuando finaliza una aplicación, el sistema lo cierra automáticamente.<br/> |
| [Desfragmentación de archivos](defragmenting-files.md)<br/>               | *La* desfragmentación es el proceso de mover partes de archivos en un disco para desfragmentar archivos, es decir, el proceso de mover clústeres de archivos en un disco para que estén contiguos.<br/>                                                                               |



 

 

