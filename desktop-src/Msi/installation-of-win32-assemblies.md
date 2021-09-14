---
description: Instale ensamblados Win32 al convertirlos en un componente del paquete de Microsoft Windows Installer que instala o actualiza la aplicación.
ms.assetid: 09aecb55-ed45-45b3-b27a-d0946223392a
title: Instalación de ensamblados Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d47847c0c69185a28fa41bbe5c5a05deec1e66
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171781"
---
# <a name="installation-of-win32-assemblies"></a>Instalación de ensamblados Win32

Instale ensamblados Win32 al convertirlos en un componente del paquete de Microsoft Windows Installer que instala o actualiza la aplicación. Al crear la tabla [MsiAssembly y](msiassembly-table.md) la [tabla MsiAssemblyName](msiassemblyname-table.md), identifica el componente de la columna \_ Component como un ensamblado. El instalador establecerá la propiedad [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) en la versión de archivo de Sxs.dll en sistemas operativos que puedan admitir ensamblados Win32 y no establecerá esta propiedad en caso contrario.

En Windows Vista y Windows XP, Windows instalador no escribe información de ensamblado en el Registro. Además, se pueden usar ensamblados compartidos, ensamblados privados y ensamblados en paralelo. Para obtener información, [vea Ensamblados compartidos](shared-assemblies.md), [Ensamblados privados](private-assemblies.md)y [Ensamblados en paralelo.](side-by-side-assemblies.md)

En las secciones siguientes se describe cómo crear un paquete del instalador de Windows para instalar ensamblados Win32 como compartidos, privados o en paralelo en sistemas operativos Windows diferentes.

-   [Instalación de ensamblados Win32 para el uso compartido en paralelo en Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [Instalación de ensamblados Win32 para el uso privado de una aplicación en Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 



