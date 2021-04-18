---
description: En el procedimiento siguiente se describe cómo instalar ensamblados en paralelo como ensamblados compartidos.
ms.assetid: 272ad1b8-9ea2-4af8-ba0d-c59f4db027e6
title: Instalar ensamblados en paralelo como ensamblados compartidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4e796fb371a299f508945371fea926c5d56a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497236"
---
# <a name="installing-side-by-side-assemblies-as-shared-assemblies"></a>Instalar ensamblados en paralelo como ensamblados compartidos

En el procedimiento siguiente se describe cómo instalar [ensamblados en paralelo](about-side-by-side-assemblies-.md) como [ensamblados compartidos](/windows/desktop/Msi/shared-assemblies).

**Para instalar un ensamblado en paralelo como un ensamblado compartido**

1.  Firmar y crear un catálogo para los archivos del ensamblado.

    Los archivos deben estar firmados para instalarlos como ensamblados en paralelo. Para obtener más información, vea [crear archivos y catálogos firmados](creating-signed-files-and-catalogs.md).

2.  Debe instalar ensamblados en paralelo compartidos como componentes de un paquete de Windows Installer. Puede ser el mismo paquete de instalación que se usa para instalar o actualizar la aplicación. Si el ensamblado compartido se envía como parte de varias aplicaciones, debe proporcionar un módulo de combinación que se puede incorporar en estos paquetes de instalación de aplicaciones y crear un catálogo para los archivos del ensamblado.

    Se necesita Windows Installer versión 2,0 o posterior para instalar los ensamblados. Para obtener más información, vea el SDK de [Windows Installer](../msi/windows-installer-portal.md) y las secciones de [instalación de ensamblados Win32](../msi/installation-of-win32-assemblies.md).

 

 
