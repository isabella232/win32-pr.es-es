---
description: Las aplicaciones que se basan en los recursos de la red para la instalación a petición son susceptibles a errores de origen si la ubicación de origen debe cambiar por cualquier motivo o se daña.
ms.assetid: 3d6a0524-d5df-4d4c-b861-d4a7da95ce40
title: Resistencia de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46944804db1c4b91c6c6757303fd2af90638b12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000950"
---
# <a name="source-resiliency"></a>Resistencia de origen

Las aplicaciones que se basan en los recursos de la red para [la instalación a petición](installation-on-demand.md) son susceptibles a errores de origen si la ubicación de origen debe cambiar por cualquier motivo o se daña. El Windows Installer proporciona resistencia de origen para las características que se instalan a petición mediante una lista de origen. La lista de origen contiene las ubicaciones buscadas por el instalador para los paquetes de instalación. Las entradas de esta lista pueden ser ubicaciones de red, localizadores de recursos uniformes (URL) o discos compactos. Si se produce un error en uno de estos orígenes, el instalador puede probar de forma rápida y sencilla el siguiente.

El desarrollador de aplicaciones no necesita incorporar ninguna información especial en el paquete del instalador para garantizar la resistencia del origen. Una vez instalada la aplicación, el instalador tiene el comportamiento de agregar el último origen que se usa correctamente como una entrada en la lista de origen. De forma predeterminada, este origen es la ubicación desde la que se instala inicialmente el paquete del instalador y es igual que la propiedad [**SourceDir**](sourcedir.md) .

Un administrador del sistema puede cambiar la lista de origen aplicando una [transformación](merges-and-transforms.md) o cambiando la propiedad [**SourceList**](sourcelist.md) desde la línea de comandos o en la [tabla de propiedades](property-table.md).

El instalador comienza a buscar un origen comprobando la ubicación de origen usada más recientemente en la lista de origen. Si se produce un error en la búsqueda, el instalador busca la lista de orígenes de red, los orígenes de medios y, por último, los orígenes de URL. Los administradores del sistema pueden cambiar este orden de búsqueda mediante la Directiva del sistema [SearchOrder](searchorder.md) . Si se produce un error en estas búsquedas, el instalador puede presentar un [cuadro de diálogo de exploración](browse-dialog.md) para que el usuario pueda buscar el origen manualmente. No se puede mostrar el cuadro de diálogo examinar si el nivel de la interfaz de usuario está establecido en ninguno. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

Normalmente, el instalador solo debe mostrar un cuadro de diálogo examinar si el usuario actual es un administrador o si la instalación no requiere privilegios elevados. Un administrador puede controlar la presentación del cuadro de diálogo examinar a los usuarios con las directivas [DisableBrowse](disablebrowse.md) y [AllowLockDownBrowse](allowlockdownbrowse.md) . Un administrador también controla si los usuarios pueden instalar aplicaciones de orígenes ubicados en medios mediante las directivas [DisableMedia](disablemedia.md) y [AllowLockDownMedia](allowlockdownmedia.md) . El uso de estas directivas depende de la versión de Windows Installer. Para obtener más información, consulte lo siguiente:

-   [Directiva de resistencia de origen](source-resiliency-policy-windows-installer-version-2-0.md)

 

 



