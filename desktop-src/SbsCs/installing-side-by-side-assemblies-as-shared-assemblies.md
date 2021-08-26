---
description: En el procedimiento siguiente se describe cómo instalar ensamblados en paralelo como ensamblados compartidos.
ms.assetid: 272ad1b8-9ea2-4af8-ba0d-c59f4db027e6
title: Instalar ensamblados en paralelo como ensamblados compartidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6348354b224e281135e72697aaa155ce69f4ccd23293f671d733e2bc1cd89dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127515"
---
# <a name="installing-side-by-side-assemblies-as-shared-assemblies"></a>Instalar ensamblados en paralelo como ensamblados compartidos

En el procedimiento siguiente se describe cómo [instalar](about-side-by-side-assemblies-.md) ensamblados en paralelo como [ensamblados compartidos.](/windows/desktop/Msi/shared-assemblies)

**Para instalar un ensamblado en paralelo como un ensamblado compartido**

1.  Firme y cree un catálogo para los archivos del ensamblado.

    Los archivos deben estar firmados para instalarlos como ensamblados en paralelo. Para obtener más información, vea [Crear archivos y catálogos firmados.](creating-signed-files-and-catalogs.md)

2.  Debe instalar ensamblados en paralelo compartidos como componentes de un Windows Installer. Puede ser el mismo paquete de instalación que se usa para instalar o actualizar la aplicación. Si el ensamblado compartido se incluye como parte de varias aplicaciones, debe proporcionar un módulo de combinación que se pueda incorporar a los paquetes de instalación de estas aplicaciones y crear un catálogo para los archivos del ensamblado.

    Windows Se requiere el instalador versión 2.0 o posterior para instalar ensamblados. Para más información, consulte el SDK [Windows Installer](../msi/windows-installer-portal.md) y las secciones de Instalación [de ensamblados Win32.](../msi/installation-of-win32-assemblies.md)

 

 
