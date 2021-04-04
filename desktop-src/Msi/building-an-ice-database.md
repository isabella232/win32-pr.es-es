---
description: Después de seleccionar el ICEs apropiado para la validación, el desarrollador debe recopilar las acciones personalizadas en una base de datos de ICE.
ms.assetid: 69151d5a-be6e-4947-862d-cea65306c536
title: Creación de una base de datos ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51043aa9b3c1591fa3262492c117aba35f23d92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909045"
---
# <a name="building-an-ice-database"></a>Creación de una base de datos ICE

Después de seleccionar el [ICEs](internal-consistency-evaluators-ices.md) apropiado para la validación, el desarrollador debe recopilar las acciones personalizadas en una base de datos de ICE. Un archivo. Cub es una base de datos. msi estándar que solo contiene CIEM y las tablas necesarias. No se puede instalar un archivo. Cub y solo se usa para almacenar y proporcionar acceso a las acciones personalizadas de ICE.

Un archivo. Cub contiene las siguientes tablas de base de datos.



| Tabla                                  | Descripción                                                                                                                                                                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Binario](binary-table.md)             | Archivos de script, dll y exe de las acciones de la aduana de hielo a las que se hace referencia en la tabla CustomAction.                                                                                                                                                                 |
| [CustomAction](customaction-table.md) | Cada registro de esta tabla corresponde a una acción personalizada ICE incluida en el archivo. Cub.                                                                                                                                                                                   |
| \_ICESequence                          | En esta tabla se enumeran las acciones de hielo que se incluyen en el archivo. Cub en su secuencia de ejecución. Las acciones personalizadas de ICE enumeradas en esta tabla se ejecutan llamando a [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea), o bien se ejecutan de forma individual con [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona). |
| [\_Validación](-validation-table.md)  | Esta tabla contiene las entradas de archivo. Cub que se van a combinar en la \_ tabla de validación.                                                                                                                                                                               |
| \_Especial                              | Todas las tablas de procesamiento especiales requeridas por acciones personalizadas específicas de ICE deben incluirse en el archivo. Cub. El nombre de estas tablas debe tener un carácter de subrayado inicial.                                                                                                        |



 

Vea el [archivo Sample. Cub](sample--cub-file.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de un ICE](building-an-ice.md)
</dt> </dl>

 

 



