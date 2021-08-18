---
description: Un ensamblado Win32 se puede instalar como un ensamblado compartido y estar disponible para su uso por varias aplicaciones en el equipo. Los ensamblados compartidos deben instalarse mediante un Windows installer usado para instalar o actualizar una aplicación.
ms.assetid: d408b0a9-8dc5-4cd0-93b3-429de7d12b17
title: Ensamblados compartidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1097a0f2bbbc4d91a6206734cb2dead53bb38748b82c0204daff476d3eb663e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628515"
---
# <a name="shared-assemblies"></a>Ensamblados compartidos

Un ensamblado Win32 se puede instalar como un ensamblado compartido y estar disponible para su uso por varias aplicaciones en el equipo. Los ensamblados compartidos deben instalarse mediante un Windows installer usado para instalar o actualizar una aplicación.

Los ensamblados compartidos se instalan como [ensamblados en paralelo.](side-by-side-assemblies.md) El Windows instala ensamblados en paralelo compartidos en la carpeta Winsxs. Los ensamblados no están registrados globalmente en el sistema, pero están disponibles globalmente para cualquier aplicación que especifique una dependencia del ensamblado en un archivo de manifiesto. Para obtener más información, [vea Aplicaciones aisladas y ensamblados en paralelo.](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)

En sistemas operativos anteriores a Windows XP, los ensamblados compartidos normalmente se instalan en la carpeta Windows del sistema y se registran globalmente. La versión instalada más reciente está disponible para cualquier aplicación que se enlaza a ella.

Para obtener información sobre cómo crear un paquete Windows Installer para instalar un ensamblado compartido, vea lo siguiente:

-   [Instalación de ensamblados Win32 para el uso compartido en paralelo en Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [Instalación de ensamblados Win32 para el uso privado de una aplicación en Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 
