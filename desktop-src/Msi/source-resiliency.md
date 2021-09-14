---
description: Las aplicaciones que se basan en recursos de red para la instalación a petición son susceptibles a errores de origen si la ubicación de origen debe cambiar por cualquier motivo o dañarse.
ms.assetid: 3d6a0524-d5df-4d4c-b861-d4a7da95ce40
title: Resistencia de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46944804db1c4b91c6c6757303fd2af90638b12e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266103"
---
# <a name="source-resiliency"></a>Resistencia de origen

Las aplicaciones que se [](installation-on-demand.md) basan en recursos de red para la instalación a petición son susceptibles a errores de origen si la ubicación de origen debe cambiar por cualquier motivo o dañarse. El instalador Windows proporciona resistencia de origen para las características que se instalan a petición mediante una lista de origen. La lista de origen contiene las ubicaciones buscadas por el instalador para los paquetes de instalación. Las entradas de esta lista pueden ser ubicaciones de red, localizadores uniformes de recursos (URL) o discos compactos. Si se produce un error en uno de estos orígenes, el instalador puede probar rápidamente y sin problemas el siguiente.

El desarrollador de aplicaciones no necesita incorporar ninguna información especial en el paquete del instalador para garantizar la resistencia del origen. Una vez instalada la aplicación, el instalador tiene el comportamiento de agregar el último origen usado correctamente como entrada en la lista de origen. De forma predeterminada, este origen es la ubicación desde la que se instala inicialmente el paquete del instalador y es igual que la [**propiedad SourceDir.**](sourcedir.md)

Un administrador del sistema puede cambiar [](merges-and-transforms.md) la lista de origen aplicando una transformación o cambiando la [**propiedad SOURCELIST**](sourcelist.md) desde la línea de comandos o en la [tabla Property](property-table.md).

El instalador comienza a buscar un origen comprobando la ubicación de origen usada más recientemente en la lista de origen. Si se produce un error en esta búsqueda, el instalador busca en la lista de orígenes de red, después en orígenes multimedia y, por último, en orígenes de direcciones URL. Los administradores del sistema pueden cambiar este orden de búsqueda mediante la [directiva del sistema SearchOrder.](searchorder.md) Si se producirá un error en estas búsquedas, el instalador puede presentar un cuadro de [diálogo Examinar](browse-dialog.md) para que el usuario pueda buscar el origen manualmente. No se puede mostrar el cuadro de diálogo Examinar si el nivel de interfaz de usuario está establecido en Ninguno. Para obtener más información, [vea Interfaz de usuario Levels](user-interface-levels.md).

Normalmente, el instalador solo debe mostrar un cuadro de diálogo examinar si el usuario actual es administrador o si la instalación no requiere privilegios elevados. Un administrador puede controlar la presentación del cuadro de diálogo Examinar a los usuarios con las directivas [DisableBrowse](disablebrowse.md) y [AllowLockDownBrowse.](allowlockdownbrowse.md) Un administrador también controla si los usuarios pueden instalar aplicaciones desde orígenes ubicados en medios mediante las directivas [DisableMedia](disablemedia.md) [y AllowLockDownMedia.](allowlockdownmedia.md) El uso de estas directivas depende de la Windows del instalador. Para más información, consulte lo siguiente:

-   [Directiva de resistencia de origen](source-resiliency-policy-windows-installer-version-2-0.md)

 

 



