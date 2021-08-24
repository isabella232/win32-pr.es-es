---
description: Windows La versión 2.0 del instalador comienza a buscar un origen comprobando la ubicación de origen usada más recientemente en la lista de orígenes, después la lista de orígenes de red, los orígenes multimedia y, por último, los orígenes de direcciones URL.
ms.assetid: 21b1a31e-efe3-4d45-b1c5-fe6ed9b19fed
title: Directiva de resistencia de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4951c1183da8998986863fe5dae744fc58c23387306c91153b50ab63e38e0a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039715"
---
# <a name="source-resiliency-policy"></a>Directiva de resistencia de origen

El instalador comienza a buscar un origen comprobando la ubicación de origen usada más recientemente en la lista de orígenes, después la lista de orígenes de red, los orígenes multimedia y, por último, los orígenes de direcciones URL. Para obtener más información, vea [Resistencia de origen.](source-resiliency.md) Si se produce un error en la búsqueda, el instalador puede presentar un [cuadro de diálogo Examinar](browse-dialog.md) que permite al usuario buscar el origen manualmente. No se puede mostrar el cuadro de diálogo Examinar si los niveles [de la interfaz de](user-interface-levels.md) usuario están establecidos en Ninguno. Un administrador controla la presentación del cuadro de diálogo Examinar a los usuarios estableciendo la directiva del sistema.

Con Windows instalador, los administradores que no son administradores de forma predeterminada no pueden usar el cuadro de diálogo Examinar para buscar orígenes de aplicaciones administradas en medios y no pueden instalar aplicaciones administradas. Un administrador permite que un no administrador examine o instale aplicaciones administradas desde medios mediante las directivas [AllowLockdownBrowse](allowlockdownbrowse.md) [y AllowLockdownMedia.](allowlockdownmedia.md) Un administrador deshabilita la capacidad de examinar o instalar aplicaciones desde medios mediante las directivas [DisAbleBrowse](disablebrowse.md) [y DisAbleMedia.](disablemedia.md)

En la tabla siguiente se resume el uso de estas directivas del sistema en Windows Installer.



| Directiva del sistema                                  | Aplicación no administradora de usuarios no administradores                                                                                                             | Aplicación administrada por el usuario que no es administrador                                                                                                                 | Aplicación administrada por el administrador aplicación no administrada                                                                                               |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AllowLockdownBrowse](allowlockdownbrowse.md) | Los usuarios pueden instalar aplicaciones no administradas mediante orígenes ubicados en medios. Los usuarios pueden examinar los medios de los orígenes de aplicaciones no administradas.<br/>    | Los usuarios no pueden instalar aplicaciones administradas mediante orígenes ubicados en medios. Los usuarios pueden examinar los medios de los orígenes de las aplicaciones administradas.<br/>      | Los administradores pueden instalar aplicaciones mediante orígenes ubicados en medios. Los administradores pueden examinar los medios de los orígenes de aplicaciones.<br/>    |
| [AllowLockdownMedia](allowlockdownmedia.md)   | Los usuarios pueden instalar aplicaciones no administradas mediante orígenes ubicados en medios. Los usuarios pueden examinar los medios de los orígenes de aplicaciones no administradas.<br/>    | Los usuarios pueden instalar aplicaciones administradas mediante orígenes ubicados en medios. Los usuarios no pueden examinar los medios de los orígenes de las aplicaciones administradas.<br/>      | Los administradores pueden instalar aplicaciones mediante orígenes ubicados en medios. Los administradores pueden examinar los medios de los orígenes de aplicaciones.<br/>    |
| *Predeterminado*                                      | Los usuarios pueden instalar aplicaciones no administradas mediante orígenes ubicados en medios. Los usuarios pueden examinar los medios de los orígenes de aplicaciones no administradas.<br/>    | Los usuarios no pueden instalar aplicaciones administradas mediante orígenes ubicados en medios. Los usuarios no pueden examinar los medios de los orígenes de las aplicaciones administradas.<br/>   | Los administradores pueden instalar aplicaciones mediante orígenes ubicados en medios. Los administradores pueden examinar los medios de los orígenes de aplicaciones.<br/>    |
| [DisAbleBrowse](disablebrowse.md)             | Los usuarios pueden instalar aplicaciones no administradas mediante orígenes ubicados en medios. Los usuarios no pueden examinar los medios de los orígenes de aplicaciones no administradas.<br/> | Los usuarios no pueden instalar aplicaciones administradas mediante orígenes ubicados en medios. Los usuarios no pueden examinar los medios de los orígenes de las aplicaciones administradas. .<br/> | Los administradores pueden instalar aplicaciones mediante orígenes ubicados en medios. Los administradores no pueden examinar los medios de los orígenes de aplicaciones.<br/> |
| [DisAbleMedia](disablemedia.md)               | Los usuarios no pueden instalar aplicaciones no administradas mediante orígenes ubicados en medios. Los usuarios pueden examinar los medios de los orígenes de aplicaciones no administradas.<br/> | Los usuarios no pueden instalar aplicaciones administradas mediante orígenes ubicados en medios. Los usuarios no pueden examinar los medios de los orígenes de las aplicaciones administradas.<br/>   | Los administradores no pueden instalar aplicaciones mediante orígenes ubicados en medios. Los administradores pueden examinar los medios de los orígenes de aplicaciones.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resistencia de origen](source-resiliency.md)
</dt> </dl>

 

 




