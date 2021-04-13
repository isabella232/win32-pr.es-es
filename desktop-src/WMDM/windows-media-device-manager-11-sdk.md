---
title: SDK de Windows Media Administrador de dispositivos 11
description: SDK de Windows Media Administrador de dispositivos 11
ms.assetid: 9c0c9a96-1335-4ae2-9393-bfab0dfe24c6
keywords:
- Windows Media Administrador de dispositivos, acerca de
- Administrador de dispositivos, acerca de
- Protocolo de transferencia multimedia (MTP)
- MTP (Protocolo de transferencia multimedia)
- Clase de almacenamiento masivo (MSC)
- MSC (clase de almacenamiento masivo)
- Windows Media Administrador de dispositivos, aplicaciones de escritorio
- Administrador de dispositivos, aplicaciones de escritorio
- aplicaciones de escritorio, acerca de
- Windows Media Administrador de dispositivos, proveedores de servicios
- Administrador de dispositivos, proveedores de servicios
- proveedores de servicios, acerca de
- Administrador de dispositivos de Windows Media, Complementos
- Administrador de dispositivos, INSP
- complementos, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b167e8244fb6f03a584dfb71255eabfa359c8e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104421544"
---
# <a name="windows-media-device-manager-11-sdk"></a>SDK de Windows Media Administrador de dispositivos 11

> [!IMPORTANT]
> Las API de Windows Media Administrador de dispositivos se incluyen ahora en el Windows SDK. No es necesario descargar ningún SDK adicional.

 

El kit de desarrollo de software (SDK) de Microsoft Windows Media Administrador de dispositivos le permite crear aplicaciones de escritorio y componentes que pueden comunicarse con dispositivos portátiles conectados. Windows Media Administrador de dispositivos permite que su aplicación o componente Enumere, explore y intercambie archivos con un dispositivo, consulte los metadatos y solicite información de recuento de repeticiones. Las aplicaciones o componentes basados en Windows Media Administrador de dispositivos tienen una API coherente para comunicarse con una amplia gama de dispositivos, como el protocolo de transferencia multimedia (MTP), la clase de almacenamiento masivo (MSC), la RAPI y otros dispositivos creados en las versiones más recientes y anteriores de la tecnología de Windows Media.

Puede compilar los siguientes elementos mediante el SDK de Administrador de dispositivos de Windows Media:

-   Aplicaciones de escritorio, como reproductores multimedia personalizados. Toda la comunicación entre una aplicación y un dispositivo portátil debe pasar a través de Windows Media Administrador de dispositivos, que actúa como agente entre la aplicación, el sistema de administración de derechos digitales de Microsoft y el proveedor de servicios.
-   Proveedores de servicios, que actúan como vínculo de comunicación entre un dispositivo personalizado y una aplicación de escritorio. Aunque Microsoft proporciona varios proveedores de servicios que pueden comunicarse con la mayoría de los dispositivos de la caja, puede crear un proveedor de servicios personalizado para personalizar la comunicación entre un dispositivo y una aplicación de escritorio.
-   Complementos, que pueden realizar tareas como la solicitud y el registro de recuentos de reproducción en dispositivos. Estos complementos se pueden adjuntar a otras aplicaciones de escritorio, como Windows Media Player para enviar información a los proveedores de contenido con el fin de controlar los pagos de regalías a artistas.

Para descargar el SDK de Windows Media Administrador de dispositivos, consulte [la página de descarga de Windows Media](https://msdn.microsoft.com/windows/desktop/aa904949) en el sitio web de MSDN.

Este SDK es un componente del kit de desarrollo de software de Microsoft Windows Media. Otros componentes son el SDK de Windows Media Format, el SDK de Windows Media Services, el SDK de Windows Media Encoder, el SDK de Windows Media Rights Manager y el SDK de Windows Media Player.

En esta documentación se incluyen las siguientes secciones.



| Sección                                            | Descripción                                                                                                                                                                                                                                                     |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introducción](getting-started.md)             | Se describen las novedades de esta versión de Windows Media Administrador de dispositivos, se ofrece información general sobre cómo funciona Windows Media Administrador de dispositivos, se describe lo que se necesita para desarrollar una aplicación o un proveedor de servicios, y se explican los ejemplos que se incluyen con el SDK. |
| [Guía de programación](programming-guide.md)         | Describe cómo crear aplicaciones y proveedores de servicios.                                                                                                                                                                                                      |
| [Referencia de programación](programming-reference.md) | Proporciona información de referencia de C++ para las interfaces, los métodos, las clases y las estructuras compatibles con el SDK de Administrador de dispositivos de Windows Media.                                                                                                                      |
| [*Glosario*](wmdm-glossary.md)                    | Define los términos que se usan en esta documentación.                                                                                                                                                                                                                       |



 

 

 




