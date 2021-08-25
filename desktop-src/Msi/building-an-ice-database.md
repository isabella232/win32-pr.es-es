---
description: Después de seleccionar los TIC adecuados para la validación, un desarrollador debe recopilar las acciones personalizadas juntas en una base de datos ICE.
ms.assetid: 69151d5a-be6e-4947-862d-cea65306c536
title: Creación de una base de datos ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e078517f8942454320e3f743d7379bbfeb22a7c44afe635a8276568a56c27f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926995"
---
# <a name="building-an-ice-database"></a>Creación de una base de datos ICE

Después de seleccionar los [TIC adecuados](internal-consistency-evaluators-ices.md) para la validación, un desarrollador debe recopilar las acciones personalizadas juntas en una base de datos ICE. Un archivo .cub es una base de .msi base de datos que contiene solo los TIC y sus tablas necesarias. No se puede instalar un archivo .cub y solo se usa para almacenar y proporcionar acceso a acciones personalizadas de ICE.

Un archivo .cub contiene las siguientes tablas de base de datos.



| Tabla                                  | Descripción                                                                                                                                                                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Binario](binary-table.md)             | Los archivos de script, archivos DLL y EXE de las acciones de limpieza de ICE a las que se hace referencia en la tabla CustomAction.                                                                                                                                                                 |
| [CustomAction](customaction-table.md) | Cada registro de esta tabla corresponde a una acción personalizada de ICE incluida en el archivo .uu.                                                                                                                                                                                   |
| \_ICESequence                          | En esta tabla se enumeran las acciones legales de ICE incluidas en el archivo .uu. en su secuencia de ejecución. Las acciones personalizadas de ICE enumeradas en esta tabla se ejecutan mediante una llamada a [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)o se ejecutan individualmente mediante [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona). |
| [\_Validación](-validation-table.md)  | Esta tabla contiene las entradas de archivo .uu. que se van a combinar en la \_ tabla Validación.                                                                                                                                                                               |
| \_Especial                              | Todas las tablas de procesamiento especiales que requieran determinadas acciones personalizadas de ICE deben incluirse en el archivo .cub. El nombre de estas tablas debe tener un carácter de subrayado inicial.                                                                                                        |



 

Vea [Archivo .uu. de ejemplo](sample--cub-file.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de un ICE](building-an-ice.md)
</dt> </dl>

 

 



