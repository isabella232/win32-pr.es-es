---
description: Restaurar sistema supervisa y registra automáticamente los cambios del sistema de claves en el equipo de un usuario. Para obtener más información, consulte Restaurar sistema.
ms.assetid: 5fc345ff-8a47-4372-806f-64b8c271fd2d
title: Puntos de restauración del sistema y el Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7fe9bd4b8e22f5aee7e49d3e4c452378f402e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677526"
---
# <a name="system-restore-points-and-the-windows-installer"></a>Puntos de restauración del sistema y el Windows Installer

Restaurar sistema supervisa y registra automáticamente los cambios del sistema de claves en el equipo de un usuario. Para obtener más información, consulte [Restaurar sistema](../sr/system-restore-portal.md).

Los puntos de restauración del sistema los crea el sistema y también los crea Windows Installer cuando se instala o se quita software.

En Windows XP, el instalador puede crear puntos de control durante la primera instalación de una aplicación y durante su eliminación. El instalador solo crea puntos de control en estos casos cuando el cambio se ejecuta con al menos una [*interfaz de usuario básica*](b-gly.md). Las instalaciones que tienen el [nivel de interfaz de usuario](user-interface-levels.md) establecido en None normalmente las inicia el sistema o una aplicación que debe administrar la creación de un punto de control. Para obtener más información, consulte [Restaurar sistema](../sr/system-restore-portal.md).

En organizaciones con muchas aplicaciones pequeñas, los administradores pueden decidir deshabilitar los puntos de comprobación desde el instalador para mejorar el rendimiento. Para obtener más información, vea [LimitSystemRestoreCheckpointing](limitsystemrestorecheckpointing.md) o [establecer un punto de restauración desde una acción personalizada](setting-a-restore-point-from-a-custom-action.md).

A partir de Windows Installer 5,0, la propiedad [**MSIFASTINSTALL**](msifastinstall.md) se puede establecer para impedir que una instalación genere un punto de restauración del sistema.

 

 
