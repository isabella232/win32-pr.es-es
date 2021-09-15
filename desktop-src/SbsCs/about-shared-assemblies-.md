---
description: Un ensamblado compartido es un ensamblado disponible para su uso por varias aplicaciones en el equipo.
ms.assetid: E42688E0-83D8-4C64-98A8-1BE82E4348FA
title: Acerca de los ensamblados compartidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed044f2c0f6b8e8e04927035991da651b4c26674
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271796"
---
# <a name="about-shared-assemblies"></a>Acerca de los ensamblados compartidos

Un ensamblado compartido es un ensamblado disponible para su uso por varias aplicaciones en el equipo. En Windows Vista y Windows [XP,](about-side-by-side-assemblies-.md) los ensamblados en paralelo se pueden instalar como ensamblados compartidos. Los ensamblados compartidos en paralelo no están registrados globalmente en el sistema, pero están disponibles globalmente para las aplicaciones que especifican una dependencia del ensamblado en [los manifiestos](manifests.md). Diferentes aplicaciones que se ejecutan al mismo tiempo pueden compartir varias versiones de ensamblados en paralelo. Para obtener más información, vea Acerca de las aplicaciones aisladas y los [ensamblados en paralelo.](about-isolated-applications-and-side-by-side-assemblies.md) Por ejemplo, los [ensamblados](supported-microsoft-side-by-side-assemblies.md) en paralelo admitidos de Microsoft incluidos con Windows XP suelen usarse como ensamblados compartidos por varias aplicaciones.

Los ensamblados compartidos en paralelo se instalan en la carpeta WinSxS. Los publicadores de ensamblados, las aplicaciones y los administradores pueden cambiar la versión de las dependencias de ensamblado en paralelo después de la implementación a través de la [configuración](configuration.md). Los ensamblados compartidos en paralelo se pueden instalar mediante una actualización del sistema operativo o mediante un paquete de Windows Installer que instala o actualiza una aplicación. Para obtener más información, [vea Instalación de ensamblados Win32.](../msi/installation-of-win32-assemblies.md)

Antes de Windows XP, los ensamblados compartidos se registraban globalmente e instalaban en la Windows System. En este caso, la versión instalada más reciente del ensamblado está disponible para cualquier aplicación que se enlaza a él. También se puede instalar un ensamblado en paralelo como un ensamblado privado para el uso exclusivo de una aplicación. Para obtener más información, vea [Ensamblados privados](/windows/desktop/Msi/private-assemblies).

 

 
