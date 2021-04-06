---
description: Windows Installer versión 2,0 comienza a buscar un origen mediante la comprobación de la ubicación de origen usada más recientemente en la lista de origen, la lista de orígenes de red, los orígenes de medios y, por último, los orígenes de URL.
ms.assetid: 21b1a31e-efe3-4d45-b1c5-fe6ed9b19fed
title: Directiva de resistencia de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 605c420198234405c23cb9672ca25c621b76390e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002365"
---
# <a name="source-resiliency-policy"></a>Directiva de resistencia de origen

El instalador comienza a buscar un origen mediante la comprobación de la ubicación de origen usada más recientemente en la lista de origen, la lista de orígenes de red, los orígenes multimedia y, por último, los orígenes de URL. Para obtener más información, consulte [resistencia del origen](source-resiliency.md). Si se produce un error en la búsqueda, el instalador puede presentar un [cuadro de diálogo de exploración](browse-dialog.md) que permita al usuario buscar el origen manualmente. No se puede mostrar el cuadro de diálogo examinar si el nivel de la [interfaz de usuario](user-interface-levels.md) está establecido en ninguno. Un administrador controla la presentación del cuadro de diálogo de exploración a los usuarios mediante la configuración de la Directiva del sistema.

Con Windows Installer, de forma predeterminada, los no administradores no pueden usar el cuadro de diálogo examinar para buscar orígenes de aplicaciones administradas en medios y no pueden instalar aplicaciones administradas. Un administrador permite a un no administrador examinar o instalar aplicaciones administradas desde un medio mediante las directivas [AllowLockdownBrowse](allowlockdownbrowse.md) y [AllowLockdownMedia](allowlockdownmedia.md) . Un administrador deshabilita la capacidad de examinar o instalar aplicaciones desde un medio mediante las directivas [DisAbleBrowse](disablebrowse.md) y [DisAbleMedia](disablemedia.md) .

En la tabla siguiente se resume el uso de estas directivas del sistema en Windows Installer.



| Directiva del sistema                                  | Aplicación no administrada de usuario no administrador                                                                                                             | Aplicación administrada por el usuario no administrador                                                                                                                 | Aplicación administrada de aplicaciones no administradas de administrador                                                                                               |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AllowLockdownBrowse](allowlockdownbrowse.md) | Los usuarios pueden instalar aplicaciones no administradas mediante orígenes ubicados en medios. Los usuarios pueden examinar los medios de los orígenes de aplicaciones no administradas.<br/>    | Los usuarios no pueden instalar aplicaciones administradas mediante orígenes ubicados en medios. Los usuarios pueden examinar los elementos multimedia de los orígenes de las aplicaciones administradas.<br/>      | Los administradores pueden instalar aplicaciones mediante orígenes ubicados en medios. Los administradores pueden examinar los medios de los orígenes de las aplicaciones.<br/>    |
| [AllowLockdownMedia](allowlockdownmedia.md)   | Los usuarios pueden instalar aplicaciones no administradas mediante orígenes ubicados en medios. Los usuarios pueden examinar los medios de los orígenes de aplicaciones no administradas.<br/>    | Los usuarios pueden instalar aplicaciones administradas mediante orígenes ubicados en medios. Los usuarios no pueden examinar los elementos multimedia para los orígenes de las aplicaciones administradas.<br/>      | Los administradores pueden instalar aplicaciones mediante orígenes ubicados en medios. Los administradores pueden examinar los medios de los orígenes de las aplicaciones.<br/>    |
| *Valor predeterminado*                                      | Los usuarios pueden instalar aplicaciones no administradas mediante orígenes ubicados en medios. Los usuarios pueden examinar los medios de los orígenes de aplicaciones no administradas.<br/>    | Los usuarios no pueden instalar aplicaciones administradas mediante orígenes ubicados en medios. Los usuarios no pueden examinar los elementos multimedia para los orígenes de las aplicaciones administradas.<br/>   | Los administradores pueden instalar aplicaciones mediante orígenes ubicados en medios. Los administradores pueden examinar los medios de los orígenes de las aplicaciones.<br/>    |
| [DisAbleBrowse](disablebrowse.md)             | Los usuarios pueden instalar aplicaciones no administradas mediante orígenes ubicados en medios. Los usuarios no pueden examinar los elementos multimedia para los orígenes de aplicaciones no administradas.<br/> | Los usuarios no pueden instalar aplicaciones administradas mediante orígenes ubicados en medios. Los usuarios no pueden examinar los elementos multimedia para los orígenes de las aplicaciones administradas. .<br/> | Los administradores pueden instalar aplicaciones mediante orígenes ubicados en medios. Los administradores no pueden examinar los elementos multimedia para los orígenes de aplicaciones.<br/> |
| [DisAbleMedia](disablemedia.md)               | Los usuarios no pueden instalar aplicaciones no administradas mediante orígenes ubicados en medios. Los usuarios pueden examinar los medios de los orígenes de aplicaciones no administradas.<br/> | Los usuarios no pueden instalar aplicaciones administradas mediante orígenes ubicados en medios. Los usuarios no pueden examinar los elementos multimedia para los orígenes de las aplicaciones administradas.<br/>   | Los administradores no pueden instalar aplicaciones mediante orígenes ubicados en medios. Los administradores pueden examinar los medios de los orígenes de las aplicaciones.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resistencia de origen](source-resiliency.md)
</dt> </dl>

 

 




