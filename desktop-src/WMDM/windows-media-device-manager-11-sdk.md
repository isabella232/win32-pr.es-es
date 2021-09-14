---
title: Windows SDK de Administrador de dispositivos 11
description: Windows SDK de Administrador de dispositivos 11
ms.assetid: 9c0c9a96-1335-4ae2-9393-bfab0dfe24c6
keywords:
- Windows Media Administrador de dispositivos,about
- Administrador de dispositivos,about
- Protocolo de transferencia de medios (MTP)
- MTP (Protocolo de transferencia de medios)
- Clase Storage masiva (MSC)
- MSC (clase de Storage masiva)
- Windows Aplicaciones de Administrador de dispositivos multimedia, aplicaciones de escritorio
- Administrador de dispositivos aplicaciones de escritorio
- aplicaciones de escritorio, acerca de
- Windows Media Administrador de dispositivos,proveedores de servicios
- Administrador de dispositivos,proveedores de servicios
- proveedores de servicios, acerca de
- Windows Archivos Administrador de dispositivos, complementos
- Administrador de dispositivos,complemento
- complementos, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b167e8244fb6f03a584dfb71255eabfa359c8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249699"
---
# <a name="windows-media-device-manager-11-sdk"></a>Windows SDK de Administrador de dispositivos 11

> [!IMPORTANT]
> Las API Windows Media Administrador de dispositivos están ahora incluidas en el SDK de Windows. No se requiere ninguna descarga adicional del SDK.

 

Microsoft Windows Media Administrador de dispositivos Software Development Kit (SDK) permite compilar aplicaciones de escritorio y componentes que se pueden comunicar con dispositivos portátiles conectados. Windows El Administrador de dispositivos permite a la aplicación o componente enumerar, explorar e intercambiar archivos con un dispositivo, consultar metadatos y solicitar información de recuento de reproducción. Las aplicaciones o componentes basados en Windows Media Administrador de dispositivos tienen una API coherente para comunicarse con una amplia gama de dispositivos, incluidos el Protocolo de transferencia de medios (MTP), la clase Storage masiva (MSC), RAPI y otros dispositivos basados en las versiones más recientes y anteriores de la tecnología de Windows Media.

Puede compilar los siguientes elementos mediante el SDK Windows Media Administrador de dispositivos:

-   Aplicaciones de escritorio, como reproductores multimedia personalizados. Toda comunicación entre una aplicación y un dispositivo portátil debe pasar por Windows Media Administrador de dispositivos, que actúa como agente entre la aplicación, el sistema de administración de derechos digitales de Microsoft y el proveedor de servicios.
-   Proveedores de servicios, que actúan como vínculo de comunicación entre un dispositivo personalizado y una aplicación de escritorio. Aunque Microsoft proporciona una serie de proveedores de servicios que pueden comunicarse con la mayoría de los dispositivos de forma personalizada, puede crear un proveedor de servicios personalizado para personalizar la comunicación entre un dispositivo y una aplicación de escritorio.
-   Complementos, que pueden realizar tareas como solicitar y registrar recuentos de reproducción en los dispositivos. Estos complementos se pueden adjuntar a otras aplicaciones de escritorio, como el Reproductor de Windows Media para enviar información a los proveedores de contenido para controlar los pagos de la canonidad a los intérpretes.

Para descargar el SDK Windows Media Administrador de dispositivos, consulte la [página Windows descarga](https://msdn.microsoft.com/windows/desktop/aa904949) de medios en el sitio web de MSDN.

Este SDK es un componente de Microsoft Windows Media Software Development Kit. Otros componentes incluyen el SDK de Windows Media Format, el SDK de Servicios de Windows Media, el SDK de Windows Media Encoder, el SDK de Windows Media Rights Manager y el SDK de Reproductor de Windows Media.

Esta documentación incluye las secciones siguientes.



| Sección                                            | Descripción                                                                                                                                                                                                                                                     |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introducción](getting-started.md)             | Describe las novedades de esta versión de Windows Media Administrador de dispositivos, proporciona información general sobre cómo funciona Windows Media Administrador de dispositivos, describe lo que será necesario para desarrollar una aplicación o un proveedor de servicios y explica los ejemplos incluidos con el SDK. |
| [Guía de programación](programming-guide.md)         | Describe cómo compilar aplicaciones y proveedores de servicios.                                                                                                                                                                                                      |
| [Referencia de programación](programming-reference.md) | Proporciona información de referencia de C++ para las interfaces, métodos, clases y estructuras compatibles con Windows Media Administrador de dispositivos SDK.                                                                                                                      |
| [*Glosario*](wmdm-glossary.md)                    | Define los términos usados en esta documentación.                                                                                                                                                                                                                       |



 

 

 




