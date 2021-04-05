---
description: Modo de reproducción no representativo de VMR (asignador personalizado)
ms.assetid: 0381f862-2f16-4b4d-be48-40f7fe151585
title: Modo de reproducción no representativo de VMR (asignador personalizado)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad9cd4dcb5e5b2f1965d49c7f31b4ef8c9ebd78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815246"
---
# <a name="vmr-renderless-playback-mode-custom-allocator-presenters"></a>Modo de reproducción no representativo de VMR (asignador personalizado)

En el modo de reproducción sin representación, VMR no realiza la representación. En su lugar, utiliza un asignador personalizado proporcionado por la aplicación. Este modo es útil para juegos y otros tipos de aplicaciones que tienen efectos de vídeo sofisticados. El modo de reproducción sin representación permite que las aplicaciones creen y controlen su propia superficie de DirectDraw (VMR-7) o la superficie de Direct3D (VMR-9), y para tener acceso a los bits de vídeo en el momento de la presentación.

En el modo sin procesar, VMR-9 no carga automáticamente su componente de mezclador.

En el modo de reproducción sin procesar, la aplicación realiza las siguientes tareas:

-   Administra la ventana de reproducción.
-   Asigna el objeto DirectDraw o Direct3D y el búfer de fotogramas final.
-   Notifica al resto del sistema de reproducción del objeto que se está usando.
-   Presenta el búfer de fotogramas en el momento correcto.
-   Controla todos los cambios en el modo de resolución, supervisa los cambios y las pérdidas superficiales. Debe informar al resto del sistema de reproducción de estos eventos.

La VMR hace lo siguiente:

-   Controla todo el control de tiempo relacionado con la presentación del fotograma de vídeo.
-   Proporciona información de control de calidad a la aplicación y al resto del sistema de reproducción.
-   Presenta una interfaz coherente con los componentes de nivel superior del sistema de reproducción, que no son conscientes de que la aplicación proporciona la asignación de búfer de fotogramas y realiza la representación.
-   Proporciona cualquier combinación de secuencias de vídeo que puede ser necesaria antes de la representación.

Dado que el mezclador realiza el desentrelazado, el asignador-presentador siempre recibe fotogramas desentrelazados. Para obtener más información, consulte [configuración de preferencias de desentrelazado](setting-deinterlace-preferences.md).

Para obtener más información acerca de cómo proporcionar un asignador personalizado, vea los temas siguientes:

-   [Proporcionar un Allocator-Presenter personalizado para VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md)
-   [Suministro de un Allocator-Presenter personalizado para VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md)
-   [Sincronizar la VMR con la frecuencia de actualización del monitor](synchronizing-the-vmr-to-the-monitors-refresh-rate.md)

 

 



