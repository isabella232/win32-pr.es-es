---
title: Paneles de tareas de servicio
description: Paneles de tareas de servicio
ms.assetid: f626fa85-7590-4e87-bd5c-7ffdcb14be8b
keywords:
- Reproductor de Windows Media en línea, paneles de tareas de servicio
- tiendas en línea, paneles de tareas de servicio
- tipo 2 tiendas en línea, paneles de tareas de servicio
- Reproductor de Windows Media en línea, paneles de tareas
- tiendas en línea, paneles de tareas
- tiendas en línea de tipo 2, paneles de tareas
- Reproductor de Windows Media, paneles de tareas de servicio
- Reproductor de Windows Media,paneles de tareas
- paneles de tareas de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d445e3fa5393dddb8e3dcc835317c8e5a284cb46f0a4a0e2b1f65fe2ea2d7b30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646515"
---
# <a name="service-task-panes"></a>Paneles de tareas de servicio

En Reproductor de Windows Media 10, los proveedores de tiendas en línea pueden configurar Reproductor de Windows Media para mostrar hasta tres paneles de tareas, denominados paneles de tareas de servicio. Cada panel de tareas de servicio se representa mediante un botón personalizable Reproductor de Windows Media muestra en el lado derecho de la barra de tareas Características.

Cada panel de tareas de servicio hospeda una página web que es la interfaz de usuario de una característica de tienda en línea determinada. El documento XML ServiceInfo define la apariencia de los paneles de tareas de servicio. En este documento, los paneles de tareas de servicio se representan mediante tres elementos: **ServiceTask1,** **ServiceTask2** y **ServiceTask3.** Estos paneles de tareas de servicio están diseñados para proporcionar lo siguiente:

-   Un servicio de música.
-   Un servicio de vídeo.
-   Un servicio de radio.

Puede colocar estas características en Reproductor de Windows Media en cualquier orden que quiera, pero **ServiceTask1** debe ser el panel de tareas principal para participar en la actividad comercial.

La página web hospedada en cada panel de tareas de servicio tiene acceso al **objeto** Externo. Este objeto proporciona métodos, propiedades y un evento que proporcionan una funcionalidad especial para las páginas web de Reproductor de Windows Media. Por ejemplo, puede usar el evento y las propiedades de **External** para que la apariencia de la página web coincida con la combinación de colores que el usuario ha elegido para Reproductor de Windows Media.

En Reproductor de Windows Media 11, no hay paneles de tareas de servicio. En su lugar, hay una sola **pestaña Tiendas en** línea, que hospeda la página web principal de la tienda en línea activa. En el documento ServiceInfo, la **pestaña Tiendas en** línea se representa mediante el elemento **ServiceTask1;** Se omiten los elementos **ServiceTask2** y **ServiceTask3.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de las tiendas en línea de tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Objeto externo para almacenes en línea de tipo 2**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**Documento ServiceInfo para una tienda en línea de tipo 2**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> </dl>

 

 




