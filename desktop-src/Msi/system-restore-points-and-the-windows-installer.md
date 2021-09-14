---
description: Restaurar sistema supervisa y registra automáticamente los cambios clave del sistema en el equipo de un usuario. Para obtener más información, vea Restaurar sistema.
ms.assetid: 5fc345ff-8a47-4372-806f-64b8c271fd2d
title: Restaurar sistema points and the Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7fe9bd4b8e22f5aee7e49d3e4c452378f402e7b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069635"
---
# <a name="system-restore-points-and-the-windows-installer"></a>Restaurar sistema points and the Windows Installer

Restaurar sistema supervisa y registra automáticamente los cambios clave del sistema en el equipo de un usuario. Para obtener más información, [vea Restaurar sistema](../sr/system-restore-portal.md).

El sistema crea puntos de restauración del sistema y también los crea Windows Instalador cuando se instala o quita software.

En Windows XP, el instalador puede crear puntos de control durante la primera instalación de una aplicación y durante su eliminación. El instalador solo crea puntos de control en estos casos cuando el cambio se ejecuta con al menos una interfaz [*de usuario básica.*](b-gly.md) Las instalaciones que tienen [el nivel de interfaz](user-interface-levels.md) de usuario establecido en Ninguno suelen iniciarse por el sistema o una aplicación que debe controlar la creación de un punto de control. Para obtener más información, [vea Restaurar sistema](../sr/system-restore-portal.md).

En las empresas con muchas aplicaciones pequeñas, los administradores pueden decidir deshabilitar los puntos de control desde dentro del instalador para mejorar el rendimiento. Para obtener más información, [vea LimitSystemRestoreCheckpointing](limitsystemrestorecheckpointing.md) o Establecer un punto de [restauración a partir de una acción personalizada.](setting-a-restore-point-from-a-custom-action.md)

A partir Windows Installer 5.0, la propiedad [**MSIFASTINSTALL**](msifastinstall.md) se puede establecer para evitar que una instalación genere un punto de restauración del sistema.

 

 
