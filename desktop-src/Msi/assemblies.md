---
description: Windows El instalador puede instalar, quitar y actualizar ensamblados y ensamblados win32 usados por Common Language Runtime de Microsoft .NET Framework.
ms.assetid: 88bee87c-fed2-45e9-8d8c-a5bbcc77f266
title: Ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb0f2b91a46287262848aaa2174d6bec6688d0b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159066"
---
# <a name="assemblies"></a>Ensamblados

Windows El instalador puede instalar, quitar y actualizar ensamblados y ensamblados win32 usados por Common Language Runtime de Microsoft .NET Framework. El instalador de Windows controla un ensamblado como un único componente del instalador. Todos los archivos que constituyen un ensamblado deben estar contenidos por un único componente del instalador que se muestra en la [tabla Componente](component-table.md) .

Windows El instalador que se Windows Vista y Windows XP pueden instalar ensamblados en paralelo. Los ensamblados en paralelo pueden compartir ensamblados de forma segura entre varias aplicaciones y pueden compensar los efectos negativos del uso compartido de ensamblados, como los conflictos de DLL. En lugar de una sola versión de un ensamblado que asume la compatibilidad con versiones anteriores con todas las aplicaciones, el uso compartido de ensamblados en paralelo permite que varias versiones de un ensamblado COM o Win32 se ejecuten simultáneamente en el sistema. Esta funcionalidad mejorada para aislar aplicaciones es una parte importante de microsoft .NET Framework. Para obtener más información, [vea Aplicaciones aisladas y ensamblados en paralelo.](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)

En las secciones siguientes se describe el uso de ensamblados con Windows Installer.

-   [Agregar ensamblados a un paquete](adding-assemblies-to-a-package.md)
-   [Instalación y eliminación de ensamblados](installing-and-removing-assemblies.md)
-   [Actualizar ensamblados](updating-assemblies.md)
-   [Modos de reinstalación de ensamblados de Common Language Runtime](reinstallation-modes-of-common-language-runtime-assemblies.md)
-   [Claves del Registro de ensamblado escritas por Windows instalador](assembly-registry-keys-written-by-windows-installer-.md)

Para obtener información sobre cómo instalar aplicaciones COM y COM+ 1.0, vea Installing [a COM+ Application with the Windows Installer](installing-a-com--application-with-the-windows-installer.md), Installing a COM Component to a Private [Location](installing-a-com-component-to-a-private-location.md)y Make a COM Component in an Existing [Package Private](make-a-com-component-in-an-existing-package-private.md).

 

 
