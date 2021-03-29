---
title: Paneles de tareas de servicio
description: Paneles de tareas de servicio
ms.assetid: f626fa85-7590-4e87-bd5c-7ffdcb14be8b
keywords:
- Windows Media Player tiendas en línea, paneles de tareas de servicio
- tiendas en línea, paneles de tareas de servicio
- tipo 2 tiendas en línea, paneles de tareas de servicio
- Windows Media Player tiendas en línea, paneles de tareas
- tiendas en línea, paneles de tareas
- tipo 2 tiendas en línea, paneles de tareas
- Media Player de Windows, paneles de tareas de servicio
- Media Player de Windows, paneles de tareas
- paneles de tareas de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f882e46a7252792db5b551b25869c7711f9d31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075868"
---
# <a name="service-task-panes"></a>Paneles de tareas de servicio

En Windows Media Player 10, los proveedores de tiendas en línea pueden configurar Windows Media Player para mostrar hasta tres paneles de tareas, denominados paneles de tareas de servicio. Cada panel de tareas de servicio se representa mediante un botón personalizable que Windows Media Player muestra en el lado derecho de la barra de tareas de características.

Cada panel de tareas de servicio hospeda una página web que es la interfaz de usuario para una determinada característica de tienda en línea. La apariencia de los paneles de tareas de servicio se define mediante el documento XML de ServiceInfo. En este documento, los paneles de tareas de servicio se representan mediante tres elementos: **ServiceTask1**, **ServiceTask2** y **ServiceTask3**. Estos paneles de tareas de servicio están diseñados para proporcionar lo siguiente:

-   Un servicio de música.
-   Un servicio de vídeo.
-   Un servicio de radio.

Puede colocar estas características en Windows Media Player en el orden que desee, pero **ServiceTask1** debe ser el panel de tareas principal para participar en la actividad comercial.

La página web hospedada en cada panel de tareas de servicio tiene acceso al objeto **externo** . Este objeto proporciona métodos, propiedades y un evento que proporcionan una funcionalidad especial para las páginas web en Windows Media Player. Por ejemplo, puede usar el evento y las propiedades de **externa** para que la apariencia de la página web coincida con la combinación de colores que el usuario haya elegido para Windows Media Player.

En Windows Media Player 11, no hay paneles de tareas de servicio. En su lugar, hay una sola pestaña **tiendas en línea** , que hospeda la página web principal de la tienda en línea activa. En el documento ServiceInfo, la pestaña **tiendas en línea** se representa mediante el elemento **ServiceTask1** . se omiten los elementos **ServiceTask2** y **ServiceTask3** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Objeto externo para las tiendas en línea de tipo 2**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**Documento ServiceInfo para una tienda en línea de tipo 2**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> </dl>

 

 




