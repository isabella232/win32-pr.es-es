---
description: Instale ensamblados Win32 haciendo que sea un componente del paquete de Microsoft Windows Installer que instala o actualiza la aplicación.
ms.assetid: 09aecb55-ed45-45b3-b27a-d0946223392a
title: Instalación de ensamblados win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c680d53e1c4702bab3b9a24920b18a2fdb644a86c41207712ec3726a310a8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633845"
---
# <a name="installation-of-win32-assemblies"></a>Instalación de ensamblados win32

Instale ensamblados Win32 haciendo que sea un componente del paquete de Microsoft Windows Installer que instala o actualiza la aplicación. Al crear la tabla [MsiAssembly y](msiassembly-table.md) la [tabla MsiAssemblyName](msiassemblyname-table.md), se identifica el componente de la columna Component \_ como un ensamblado. El instalador establecerá la propiedad [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) en la versión de archivo de Sxs.dll en sistemas operativos que puedan admitir ensamblados Win32 y no establecerá esta propiedad en caso contrario.

En Windows Vista y Windows XP, Windows Installer no escribe información de ensamblado en el Registro. Además, se pueden usar ensamblados compartidos, ensamblados privados y ensamblados en paralelo. Para obtener información, [vea Ensamblados compartidos](shared-assemblies.md), [Ensamblados privados](private-assemblies.md)y [Ensamblados en paralelo.](side-by-side-assemblies.md)

En las secciones siguientes se describe cómo crear un paquete de Windows Installer para instalar ensamblados Win32 como compartidos, privados o en paralelo en diferentes sistemas operativos Windows compartidos.

-   [Instalación de ensamblados Win32 para el uso compartido en paralelo en Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [Instalación de ensamblados Win32 para el uso privado de una aplicación en Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 



