---
description: Windows La versión 2.0 del instalador comienza a buscar un origen comprobando la ubicación de origen usada más recientemente en la lista de origen, después la lista de orígenes de red, después los orígenes multimedia y, por último, los orígenes de dirección URL.
ms.assetid: 21b1a31e-efe3-4d45-b1c5-fe6ed9b19fed
title: Directiva de resistencia de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 605c420198234405c23cb9672ca25c621b76390e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266100"
---
# <a name="source-resiliency-policy"></a>Directiva de resistencia de origen

El instalador comienza a buscar un origen comprobando la ubicación de origen usada más recientemente en la lista de origen, después la lista de orígenes de red, después los orígenes multimedia y, por último, los orígenes de dirección URL. Para obtener más información, vea [Resistencia de origen.](source-resiliency.md) Si se produce un error en la búsqueda, el instalador puede presentar un cuadro de [diálogo Examinar](browse-dialog.md) que permite al usuario buscar el origen manualmente. El cuadro de diálogo Examinar no se puede mostrar si los niveles [de la interfaz de usuario](user-interface-levels.md) están establecidos en Ninguno. Un administrador controla la presentación del cuadro de diálogo Examinar a los usuarios estableciendo la directiva del sistema.

Con Windows instalador, los no administradores de forma predeterminada no pueden usar el cuadro de diálogo Examinar para buscar orígenes de aplicaciones administradas en medios y no pueden instalar aplicaciones administradas. Un administrador permite que un administrador que no es administrador examine o instale aplicaciones administradas desde medios mediante las directivas [AllowLockdownBrowse](allowlockdownbrowse.md) [y AllowLockdownMedia.](allowlockdownmedia.md) Un administrador deshabilita la capacidad de examinar o instalar aplicaciones desde medios mediante las directivas [DisAbleBrowse](disablebrowse.md) [y DisAbleMedia.](disablemedia.md)

En la tabla siguiente se resume el uso de estas directivas del sistema en Windows Instalador.



| Directiva del sistema                                  | Aplicación no administradora de usuarios no administradores                                                                                                             | Aplicación administrada por el usuario que no es administrador                                                                                                                 | Aplicación administrada por el administrador no administrada                                                                                               |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AllowLockdownBrowse](allowlockdownbrowse.md) | Los usuarios pueden instalar aplicaciones no administradas mediante orígenes ubicados en medios. Los usuarios pueden examinar los medios para buscar los orígenes de aplicaciones no administradas.<br/>    | Los usuarios no pueden instalar aplicaciones administradas mediante orígenes ubicados en medios. Los usuarios pueden buscar en los medios los orígenes de las aplicaciones administradas.<br/>      | Los administradores pueden instalar aplicaciones mediante orígenes ubicados en medios. Los administradores pueden examinar los medios para buscar los orígenes de aplicaciones.<br/>    |
| [AllowLockdownMedia](allowlockdownmedia.md)   | Los usuarios pueden instalar aplicaciones no administradas mediante orígenes ubicados en medios. Los usuarios pueden examinar los medios para buscar los orígenes de aplicaciones no administradas.<br/>    | Los usuarios pueden instalar aplicaciones administradas mediante orígenes ubicados en medios. Los usuarios no pueden examinar los medios de los orígenes de las aplicaciones administradas.<br/>      | Los administradores pueden instalar aplicaciones mediante orígenes ubicados en medios. Los administradores pueden examinar los medios para buscar los orígenes de aplicaciones.<br/>    |
| *Valor predeterminado*                                      | Los usuarios pueden instalar aplicaciones no administradas mediante orígenes ubicados en medios. Los usuarios pueden examinar los medios para buscar los orígenes de aplicaciones no administradas.<br/>    | Los usuarios no pueden instalar aplicaciones administradas mediante orígenes ubicados en medios. Los usuarios no pueden examinar los medios de los orígenes de las aplicaciones administradas.<br/>   | Los administradores pueden instalar aplicaciones mediante orígenes ubicados en medios. Los administradores pueden examinar los medios para buscar los orígenes de aplicaciones.<br/>    |
| [DisAbleBrowse](disablebrowse.md)             | Los usuarios pueden instalar aplicaciones no administradas mediante orígenes ubicados en medios. Los usuarios no pueden examinar los medios para buscar los orígenes de aplicaciones no administradas.<br/> | Los usuarios no pueden instalar aplicaciones administradas mediante orígenes ubicados en medios. Los usuarios no pueden examinar los medios de los orígenes de las aplicaciones administradas. .<br/> | Los administradores pueden instalar aplicaciones mediante orígenes ubicados en medios. Los administradores no pueden examinar los medios de los orígenes de aplicaciones.<br/> |
| [DisAbleMedia](disablemedia.md)               | Los usuarios no pueden instalar aplicaciones no administradas mediante orígenes ubicados en medios. Los usuarios pueden examinar los medios para buscar los orígenes de aplicaciones no administradas.<br/> | Los usuarios no pueden instalar aplicaciones administradas mediante orígenes ubicados en medios. Los usuarios no pueden examinar los medios de los orígenes de las aplicaciones administradas.<br/>   | Los administradores no pueden instalar aplicaciones mediante orígenes ubicados en medios. Los administradores pueden examinar los medios para buscar los orígenes de aplicaciones.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Resistencia de origen](source-resiliency.md)
</dt> </dl>

 

 




