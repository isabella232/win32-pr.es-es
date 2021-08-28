---
title: Supervisando el sistema
description: Supervisando el sistema
ms.assetid: e0318aca-4e3e-4272-ba31-c770d6b05272
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b26be8b5527af1ffb8dfc9e2626fee9248dc28c25babbb7feb345c7d77da4ed7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047366"
---
# <a name="monitoring-the-system"></a>Supervisando el sistema

Restaurar sistema en Windows Vista y versiones posteriores guarda una copia del volumen al generar un punto de restauración. Restaurar sistema requiere un mínimo de 300 MB de espacio libre en disco en la unidad del sistema durante la instalación.

Restaurar sistema en Windows XP supervisa un conjunto básico de archivos del sistema y de la aplicación, archivando los estados de estos archivos antes de que se realicen cambios en el sistema. Restaurar sistema también guarda una instantánea completa del Registro y algunos archivos dinámicos del sistema. Restaurar sistema requiere un mínimo de 200 MB de espacio libre en disco en la unidad del sistema durante la instalación. Cuando la cantidad de espacio libre en disco es inferior a 50 MB en cualquier unidad, Restaurar sistema cambia al modo en espera y deja de crear puntos de restauración. Todos los puntos de restauración se eliminan en ese momento. Restaurar sistema reactiva y reanuda la creación de puntos de restauración tan pronto como 200 MB de espacio en disco esté libre en la unidad del sistema. Los archivos que se supervisan o excluyen de la supervisión se especifican en el archivo %windir% \\ system32 \\ restore \\Filelist.xml. Para obtener más información, [vea Extensiones de nombre de archivo supervisado.](monitored-file-extensions.md)

 

 




