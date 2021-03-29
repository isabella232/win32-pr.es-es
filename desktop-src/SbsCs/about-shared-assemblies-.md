---
description: Un ensamblado compartido es un ensamblado disponible para que lo usen varias aplicaciones del equipo.
ms.assetid: E42688E0-83D8-4C64-98A8-1BE82E4348FA
title: Acerca de los ensamblados compartidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed044f2c0f6b8e8e04927035991da651b4c26674
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652657"
---
# <a name="about-shared-assemblies"></a>Acerca de los ensamblados compartidos

Un ensamblado compartido es un ensamblado disponible para que lo usen varias aplicaciones del equipo. En Windows Vista y Windows XP, los [ensamblados en paralelo](about-side-by-side-assemblies-.md) se pueden instalar como ensamblados compartidos. Los ensamblados en paralelo compartidos no se registran globalmente en el sistema, pero están disponibles globalmente para las aplicaciones que especifican una dependencia en el ensamblado en los [manifiestos](manifests.md). Varias aplicaciones que se ejecutan al mismo tiempo pueden compartir varias versiones de ensamblados en paralelo. Para obtener más información, vea [acerca de las aplicaciones aisladas y los ensamblados en paralelo](about-isolated-applications-and-side-by-side-assemblies.md). Por ejemplo, los [ensamblados en paralelo de Microsoft](supported-microsoft-side-by-side-assemblies.md) que se incluyen con Windows XP suelen usarse como ensamblados compartidos por varias aplicaciones.

Los ensamblados en paralelo compartidos se instalan en la carpeta WinSxS. Los publicadores de ensamblados, las aplicaciones y los administradores pueden cambiar la versión de las dependencias de ensamblado en paralelo después de la implementación a través de la [configuración](configuration.md). Los ensamblados en paralelo compartidos pueden instalarse mediante una actualización del sistema operativo o un paquete de Windows Installer que instala o actualiza una aplicación. Para obtener más información, vea [instalación de ensamblados Win32](../msi/installation-of-win32-assemblies.md).

Antes de Windows XP, los ensamblados compartidos se registraban globalmente y se instalaban en la carpeta del sistema de Windows. En este caso, la versión instalada más reciente del ensamblado está disponible para cualquier aplicación que se enlaza a ella. Un ensamblado simultáneo también se puede instalar como un ensamblado privado para el uso exclusivo de una aplicación. Para obtener más información, vea [Ensamblados privados](/windows/desktop/Msi/private-assemblies).

 

 
