---
description: Modo de reproducción sin representación de VMR (asignador-presentadores personalizados)
ms.assetid: 0381f862-2f16-4b4d-be48-40f7fe151585
title: Modo de reproducción sin representación de VMR (asignador-presentadores personalizados)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad9cd4dcb5e5b2f1965d49c7f31b4ef8c9ebd78
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272836"
---
# <a name="vmr-renderless-playback-mode-custom-allocator-presenters"></a>Modo de reproducción sin representación de VMR (asignador-presentadores personalizados)

En el modo de reproducción sin representación, vmr no realiza la representación. En su lugar, usa un asignador-presentador personalizado proporcionado por la aplicación. Este modo es útil para juegos y otros tipos de aplicaciones que tienen sofisticados efectos de vídeo. El modo de reproducción sin representación permite a las aplicaciones crear y controlar su propia superficie de DirectDraw (VMR-7) o Direct3D (VMR-9) y acceder a los bits de vídeo en tiempo de presentación.

En modo sin representación, VMR-9 no carga automáticamente su componente mezclador.

En el modo de reproducción sin representación, la aplicación realiza las siguientes tareas:

-   Administra la ventana de reproducción.
-   Asigna el objeto DirectDraw o Direct3D y el búfer de fotogramas final.
-   Notifica al resto del sistema de reproducción el objeto que se está utilizando.
-   Presenta el búfer de fotogramas en el momento correcto.
-   Controla todos los cambios en modo de resolución, supervisa los cambios y las pérdidas de superficie. Debe informar al resto del sistema de reproducción de estos eventos.

VmR hace lo siguiente:

-   Controla todos los tiempos relacionados con la presentación del fotograma de vídeo.
-   Proporciona información de control de calidad a la aplicación y al resto del sistema de reproducción.
-   Presenta una interfaz coherente con los componentes ascendentes del sistema de reproducción, que no son conscientes de que la aplicación proporciona la asignación del búfer de fotogramas y realiza la representación.
-   Proporciona cualquier combinación de secuencias de vídeo que puedan ser necesarias antes de la representación.

Dado que el mezclador realiza el desenlace, el asignador-presentador siempre recibió fotogramas desenlazados. Para obtener más información, vea [Establecer preferencias de desinterlace](setting-deinterlace-preferences.md).

Para obtener más información sobre cómo proporcionar un asignador-presentador personalizado, vea los temas siguientes:

-   [Suministro de un Allocator-Presenter personalizado para VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md)
-   [Suministro de un Allocator-Presenter personalizado para VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md)
-   [Sincronización de vmr con la frecuencia de actualización del monitor](synchronizing-the-vmr-to-the-monitors-refresh-rate.md)

 

 



