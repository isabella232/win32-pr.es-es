---
title: Arquitectura (Text Services Framework)
description: Architecture
ms.assetid: 6ef6ba1f-fcbb-4ede-bc6f-3da66135ea69
keywords:
- Text Services Framework (TSF),arquitectura
- TSF (Text Services Framework),architecture
- servicios de texto, arquitectura
- Aplicaciones habilitadas para TSF, arquitectura
- Text Services Framework (TSF),components
- TSF (Text Services Framework),components
- servicios de texto, componentes
- Aplicaciones habilitadas para TSF, componentes
- Text Services Framework (TSF),applications
- TSF (Text Services Framework),applications
- servicios de texto, aplicaciones
- Aplicaciones habilitadas para TSF, acerca de
- Text Services Framework (TSF),servicios de texto
- TSF (Text Services Framework),servicios de texto
- servicios de texto, acerca de
- Aplicaciones habilitadas para TSF, servicios de texto
- Text Services Framework (TSF), administrador de TSF
- TSF (Text Services Framework),administrador de TSF
- servicios de texto, administrador de TSF
- Aplicaciones habilitadas para TSF, administrador de TSF
- Administrador de TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0a300307b3099b4a28a883d5c830c4078cd0bb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243723"
---
# <a name="architecture-text-services-framework"></a>Arquitectura (Text Services Framework)

Text Services Framework incluye tres componentes principales:

-   **Aplicaciones:** Las operaciones de aplicación suelen incluir visualización, edición directa y almacenamiento de texto. Una aplicación proporciona acceso al texto mediante la implementación de un servidor COM que admite determinadas interfaces y se comunica con TSF mediante interfaces que expone el administrador de TSF. En esta documentación, el término aplicación hace referencia a una aplicación habilitada para TSF, a menos que se especifique lo contrario.
-   **Servicios de texto:** Un servicio de texto funciona como proveedor de texto para una aplicación. Un servicio de texto puede obtener texto de una aplicación y escribir texto en esta. Un servicio de texto también puede asociar datos y propiedades a un bloque de texto. Un servicio de texto se implementa como un servidor COM en proceso que se registra con TSF. Cuando se registra, el usuario interactúa con el servicio de texto mediante la barra de idioma o los métodos abreviados de teclado. Se pueden instalar varios servicios de texto.
-   **Administrador de TSF:** El administrador de TSF funciona como mediador entre una aplicación y uno o varios servicios de texto. Un servicio de texto nunca interactúa directamente con una aplicación. Toda la comunicación pasa a través del administrador de TSF. El sistema operativo implementa el administrador de TSF y no se puede reemplazar. En esta documentación, el término administrador hace referencia al administrador de TSF, a menos que se especifique lo contrario.

En la ilustración siguiente se muestran los elementos arquitectónicos principales de TSF.

![arquitectura del marco de servicios de texto](images/tsf-arch.gif)

Con esta arquitectura, el administrador de TSF proporciona una capa de abstracción entre las aplicaciones y los servicios de texto. Esta capa de abstracción permite que una aplicación y uno o varios servicios de texto compartan texto, y permite al administrador de TSF administrar servicios de texto.

 

 




