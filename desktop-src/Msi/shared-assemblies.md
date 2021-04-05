---
description: Un ensamblado Win32 se puede instalar como un ensamblado compartido y estar disponible para que lo usen varias aplicaciones del equipo. Los ensamblados compartidos deben instalarse mediante un paquete de Windows Installer utilizado para instalar o actualizar una aplicación.
ms.assetid: d408b0a9-8dc5-4cd0-93b3-429de7d12b17
title: Ensamblados compartidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e99d805614c05838abe9f5c869fc9c072b1fa8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815438"
---
# <a name="shared-assemblies"></a>Ensamblados compartidos

Un ensamblado Win32 se puede instalar como un ensamblado compartido y estar disponible para que lo usen varias aplicaciones del equipo. Los ensamblados compartidos deben instalarse mediante un paquete de Windows Installer utilizado para instalar o actualizar una aplicación.

Los ensamblados compartidos se instalan como [ensamblados en paralelo](side-by-side-assemblies.md). El Windows Installer instala ensamblados en paralelo compartidos en la carpeta WinSxS. Los ensamblados no se registran globalmente en el sistema, pero están disponibles globalmente para cualquier aplicación que especifique una dependencia en el ensamblado en un archivo de manifiesto. Para obtener más información, vea [aplicaciones aisladas y ensamblados en paralelo](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).

En sistemas operativos anteriores a Windows XP, los ensamblados compartidos se instalan normalmente en la carpeta del sistema de Windows y se registran globalmente. La última versión instalada está disponible para cualquier aplicación que se enlaza a ella.

Para obtener información sobre cómo crear un paquete de Windows Installer para instalar un ensamblado compartido, consulte lo siguiente:

-   [Instalación de ensamblados Win32 para el uso compartido en paralelo en Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [Instalar ensamblados Win32 para el uso privado de una aplicación en Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 
