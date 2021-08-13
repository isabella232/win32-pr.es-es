---
description: Restaurar sistema supervisa y registra automáticamente los cambios clave del sistema en el equipo de un usuario. Para obtener más información, vea Restaurar sistema.
ms.assetid: 5fc345ff-8a47-4372-806f-64b8c271fd2d
title: Restaurar sistema y el instalador de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48b8de832208f2bee301a1a159da058ba0f97cf2ecbd74892cb809e1186fbb65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624103"
---
# <a name="system-restore-points-and-the-windows-installer"></a>Restaurar sistema y el instalador de Windows

Restaurar sistema supervisa y registra automáticamente los cambios clave del sistema en el equipo de un usuario. Para obtener más información, [vea Restaurar sistema](../sr/system-restore-portal.md).

El sistema crea puntos de restauración del sistema y también los crea Windows instalador cuando se instala o quita software.

En Windows XP, el instalador puede crear puntos de control durante la primera instalación de una aplicación y durante su eliminación. El instalador solo crea puntos de control en estos casos cuando el cambio se ejecuta con al menos una interfaz [*de usuario básica.*](b-gly.md) Normalmente, [el sistema o](user-interface-levels.md) una aplicación que debe controlar la creación de un punto de control inician las instalaciones con el nivel de interfaz de usuario establecido en Ninguno. Para obtener más información, [vea Restaurar sistema](../sr/system-restore-portal.md).

En las empresas con muchas aplicaciones pequeñas, los administradores pueden decidir deshabilitar los puntos de control desde dentro del instalador para mejorar el rendimiento. Para obtener más información, [vea LimitSystemRestoreCheckpointing](limitsystemrestorecheckpointing.md) o Establecer un punto de [restauración a partir de una acción personalizada.](setting-a-restore-point-from-a-custom-action.md)

A partir Windows Installer 5.0, la propiedad [**MSIFASTINSTALL**](msifastinstall.md) se puede establecer para evitar que una instalación genere un punto de restauración del sistema.

 

 
