---
description: Instale los ensamblados Win32 convirtiéndolos en un componente de Microsoft Windows Installer paquete que instala o actualiza su aplicación.
ms.assetid: 09aecb55-ed45-45b3-b27a-d0946223392a
title: Instalación de ensamblados Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d47847c0c69185a28fa41bbe5c5a05deec1e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652505"
---
# <a name="installation-of-win32-assemblies"></a>Instalación de ensamblados Win32

Instale los ensamblados Win32 convirtiéndolos en un componente de Microsoft Windows Installer paquete que instala o actualiza su aplicación. Al crear la tabla [MsiAssembly](msiassembly-table.md) y la [tabla MsiAssemblyName](msiassemblyname-table.md), se identifica el componente en la \_ columna componente como un ensamblado. El instalador establecerá la propiedad [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) en la versión de archivo de Sxs.dll en los sistemas operativos que pueden admitir ensamblados Win32 y sin establecer esta propiedad en caso contrario.

En Windows Vista y Windows XP, Windows Installer no escribe información de ensamblado en el registro. Además, se pueden utilizar ensamblados compartidos, ensamblados privados y ensamblados en paralelo. Para obtener más información, vea [ensamblados compartidos](shared-assemblies.md), [ensamblados privados](private-assemblies.md)y [ensamblados en paralelo](side-by-side-assemblies.md).

En las secciones siguientes se describe cómo crear un paquete de Windows Installer para instalar los ensamblados de Win32 como compartidos, privados o en paralelo en diferentes sistemas operativos Windows.

-   [Instalación de ensamblados Win32 para el uso compartido en paralelo en Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [Instalar ensamblados Win32 para el uso privado de una aplicación en Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 



