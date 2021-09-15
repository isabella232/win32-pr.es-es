---
description: En el procedimiento siguiente se describe cómo instalar ensamblados en paralelo como ensamblados compartidos.
ms.assetid: 272ad1b8-9ea2-4af8-ba0d-c59f4db027e6
title: Instalar ensamblados en paralelo como ensamblados compartidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4e796fb371a299f508945371fea926c5d56a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271519"
---
# <a name="installing-side-by-side-assemblies-as-shared-assemblies"></a>Instalar ensamblados en paralelo como ensamblados compartidos

En el procedimiento siguiente se describe cómo [instalar](about-side-by-side-assemblies-.md) ensamblados en paralelo como [ensamblados compartidos.](/windows/desktop/Msi/shared-assemblies)

**Para instalar un ensamblado en paralelo como un ensamblado compartido**

1.  Firme y cree un catálogo para los archivos del ensamblado.

    Los archivos deben estar firmados para instalarlos como ensamblados en paralelo. Para obtener más información, vea [Crear archivos y catálogos firmados.](creating-signed-files-and-catalogs.md)

2.  Debe instalar ensamblados en paralelo compartidos como componentes de un Windows Installer. Puede ser el mismo paquete de instalación que se usa para instalar o actualizar la aplicación. Si el ensamblado compartido se incluye como parte de varias aplicaciones, debe proporcionar un módulo de combinación que se pueda incorporar a los paquetes de instalación de estas aplicaciones y crear un catálogo para los archivos del ensamblado.

    Windows Se requiere el instalador versión 2.0 o posterior para instalar ensamblados. Para más información, consulte el SDK [Windows Installer](../msi/windows-installer-portal.md) y las secciones de Instalación [de ensamblados Win32.](../msi/installation-of-win32-assemblies.md)

 

 
