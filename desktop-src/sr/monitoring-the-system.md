---
title: Supervisando el sistema
description: Supervisando el sistema
ms.assetid: e0318aca-4e3e-4272-ba31-c770d6b05272
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da7d18f42ac091b9c73c4d9a9ac3929bed235310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418321"
---
# <a name="monitoring-the-system"></a>Supervisando el sistema

Restaurar sistema en Windows Vista y versiones posteriores guarda una copia del volumen al generar un punto de restauración. Restaurar sistema requiere un mínimo de 300 MB de espacio libre en disco en la unidad del sistema durante la instalación.

Restaurar sistema en Windows XP supervisa un conjunto básico de archivos de aplicación y del sistema, y archiva los Estados de estos archivos antes de que se realicen cambios en el sistema. Restaurar sistema también guarda una instantánea completa del registro y algunos archivos del sistema dinámicos. Restaurar sistema requiere un mínimo de 200 MB de espacio libre en disco en la unidad del sistema durante la instalación. Cuando la cantidad de espacio libre en disco cae por debajo de 50 MB en cualquier unidad, Restaurar sistema cambia al modo de espera y deja de crear puntos de restauración. En ese momento se eliminan todos los puntos de restauración. Restaurar sistema vuelve a activarse y reanuda la creación de puntos de restauración en cuanto 200 MB de espacio libre en disco en la unidad del sistema. Los archivos que se supervisan o excluyen de la supervisión se especifican en el archivo% windir% \\ system32 \\ restore \\Filelist.xml. Para obtener más información, vea [extensiones de nombre de archivo supervisado](monitored-file-extensions.md).

 

 




