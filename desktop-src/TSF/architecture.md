---
title: Arquitectura (marco de trabajo de servicios de texto)
description: Architecture
ms.assetid: 6ef6ba1f-fcbb-4ede-bc6f-3da66135ea69
keywords:
- Plataforma de servicios de texto (TSF), arquitectura
- TSF (marco de trabajo de servicios de texto), arquitectura
- servicios de texto, arquitectura
- Aplicaciones habilitadas para TSF, arquitectura
- Text Services Framework (TSF), componentes
- TSF (marco de trabajo de servicios de texto), componentes
- servicios de texto, componentes
- Aplicaciones habilitadas para TSF, componentes
- Text Services Framework (TSF), aplicaciones
- TSF (marco de trabajo de servicios de texto), aplicaciones
- servicios de texto, aplicaciones
- Aplicaciones habilitadas para TSF, acerca de
- Text Services Framework (TSF), servicios de texto
- TSF (marco de trabajo de servicios de texto), servicios de texto
- servicios de texto, acerca de
- Aplicaciones habilitadas para TSF, servicios de texto
- Text Services Framework (TSF), administrador de TSF
- TSF (marco de trabajo de servicios de texto), administrador de TSF
- servicios de texto, administrador de TSF
- Aplicaciones habilitadas para TSF, administrador de TSF
- Administrador de TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0a300307b3099b4a28a883d5c830c4078cd0bb
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104571252"
---
# <a name="architecture-text-services-framework"></a>Arquitectura (marco de trabajo de servicios de texto)

El marco de trabajo de servicios de texto incluye tres componentes principales:

-   **Aplicaciones:** Las operaciones de aplicación suelen incluir la visualización, la edición directa y el almacenamiento de texto. Una aplicación proporciona acceso al texto implementando un servidor COM que admite ciertas interfaces y se comunica con TSF mediante interfaces que expone el administrador de TSF. En esta documentación, el término "aplicación" hace referencia a una aplicación habilitada para TSF, a menos que se especifique lo contrario.
-   **Servicios de texto:** Un servicio de texto funciona como un proveedor de texto en una aplicación. Un servicio de texto puede obtener texto y escribir texto en una aplicación. Un servicio de texto también puede asociar datos y propiedades con un bloque de texto. Un servicio de texto se implementa como un servidor en proceso COM que se registra a sí mismo con TSF. Cuando se registra, el usuario interactúa con el servicio de texto mediante la barra de idioma o los métodos abreviados de teclado. Se pueden instalar varios servicios de texto.
-   **Administrador de TSF:** El administrador de TSF funciona como un mediador entre una aplicación y uno o más servicios de texto. Un servicio de texto nunca interactúa directamente con una aplicación. Todas las comunicaciones pasan a través del administrador de TSF. El sistema operativo implementa el administrador TSF y no se puede reemplazar. En esta documentación, el término administrador hace referencia al administrador de TSF, a menos que se especifique lo contrario.

En la ilustración siguiente se muestran los elementos arquitectónicos principales de TSF.

![arquitectura del marco de trabajo de servicios de texto](images/tsf-arch.gif)

Con esta arquitectura, el administrador de TSF proporciona una capa de abstracción entre aplicaciones y servicios de texto. Esta capa de abstracción permite a una aplicación y a uno o varios servicios de texto compartir texto, y permite al administrador de TSF administrar servicios de texto.

 

 




