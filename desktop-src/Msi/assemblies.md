---
description: Windows Installer puede instalar, quitar y actualizar ensamblados y ensamblados Win32 utilizados por el Common Language Runtime de Microsoft .NET Framework.
ms.assetid: 88bee87c-fed2-45e9-8d8c-a5bbcc77f266
title: Ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb0f2b91a46287262848aaa2174d6bec6688d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667041"
---
# <a name="assemblies"></a>Ensamblados

Windows Installer puede instalar, quitar y actualizar ensamblados y ensamblados Win32 utilizados por el Common Language Runtime de Microsoft .NET Framework. Un ensamblado se controla mediante el Windows Installer como un componente instalador único. Todos los archivos que forman un ensamblado deben estar contenidos en un único componente del instalador que se enumera en la tabla de [componentes](component-table.md) .

Windows Installer que se ejecutan en Windows Vista y Windows XP pueden instalar ensamblados en paralelo. Los ensamblados en paralelo pueden compartir de forma segura ensamblados entre varias aplicaciones y pueden desplazar los efectos negativos del uso compartido de ensamblados, como conflictos de DLL. En lugar de una versión única de un ensamblado que asume la compatibilidad con versiones anteriores de todas las aplicaciones, el uso compartido de ensamblados en paralelo permite que varias versiones de un ensamblado COM o Win32 se ejecuten simultáneamente en el sistema. Esta funcionalidad mejorada para aislar las aplicaciones es una parte importante del marco de Microsoft .NET. Para obtener más información, vea [aplicaciones aisladas y ensamblados en paralelo](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

En las secciones siguientes se describe el uso de ensamblados con el Windows Installer.

-   [Agregar ensamblados a un paquete](adding-assemblies-to-a-package.md)
-   [Instalar y quitar ensamblados](installing-and-removing-assemblies.md)
-   [Actualizar ensamblados](updating-assemblies.md)
-   [Modos de reinstalación de los ensamblados de Common Language Runtime](reinstallation-modes-of-common-language-runtime-assemblies.md)
-   [Claves del registro de ensamblado escritas por Windows Installer](assembly-registry-keys-written-by-windows-installer-.md)

Para obtener información sobre la instalación de aplicaciones COM y COM+ 1,0, vea [instalar una aplicación com+ con el Windows Installer](installing-a-com--application-with-the-windows-installer.md), [instalar un componente com en una ubicación privada](installing-a-com-component-to-a-private-location.md)y [convertir un componente com en un paquete existente privado](make-a-com-component-in-an-existing-package-private.md).

 

 
