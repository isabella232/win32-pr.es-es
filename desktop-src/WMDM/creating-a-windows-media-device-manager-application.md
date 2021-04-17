---
title: Crear una aplicación de Windows Media Administrador de dispositivos
description: Crear una aplicación de Windows Media Administrador de dispositivos
ms.assetid: 6a200bd9-19dd-4130-acb4-e038b469c334
keywords:
- Windows Media Administrador de dispositivos, creación de aplicaciones
- Administrador de dispositivos, creación de aplicaciones
- Windows Media Administrador de dispositivos, guía de programación
- Administrador de dispositivos, guía de programación
- Guía de programación, aplicaciones de escritorio
- Guía de programación, Administrador de dispositivos de Windows Media
- Guía de programación, Complementos
- Guía de programación, creación de aplicaciones
- Windows Media Administrador de dispositivos, aplicaciones de escritorio
- Administrador de dispositivos, aplicaciones de escritorio
- Administrador de dispositivos de Windows Media, Complementos
- Administrador de dispositivos, INSP
- complementos, crear
- complementos, guía de programación
- aplicaciones de escritorio, crear
- crear aplicaciones de Windows Media Administrador de dispositivos, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b50a2dfce057b993f84c0aca4c8f45796f67ba8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695278"
---
# <a name="creating-a-windows-media-device-manager-application"></a>Crear una aplicación de Windows Media Administrador de dispositivos

En esta sección se describe cómo usar Administrador de dispositivos de Windows Media en la aplicación. El término "aplicación" aquí significa un archivo ejecutable, como un reproductor de media o un complemento COM, como un complemento de medición.

Microsoft incluye varios proveedores de servicios con Windows XP y Windows Media Player 10, incluido un proveedor de servicios de MTP, un proveedor de servicios Windows CE (para dispositivos que ejecutan Windows CE y el uso del protocolo RAPI, como Pocket PC) y un proveedor de servicios para dispositivos de categoría de almacenamiento masivo (MSC). También puede crear su propio proveedor de servicios para garantizar la comunicación con su propio dispositivo; para obtener más información, vea [crear un proveedor de servicios](creating-a-service-provider.md).

Hay una serie de proveedores de servicios heredados de terceros que abordan un dispositivo no MTP, no RAPI o no es un fabricante determinado. Estos proveedores de servicios se incluyen en el disco del controlador incluido con estos dispositivos.

Una aplicación que utiliza Windows Media Administrador de dispositivos debe realizar los pasos siguientes.

1.  **Tenga en cuenta los problemas de privacidad implicados en el desarrollo de una aplicación.** Vea la [declaración de privacidad](privacy-statement.md) para obtener información sobre algunos problemas de privacidad relacionados con el desarrollo de una aplicación de Windows Media administrador de dispositivos.
2.  **Incluya los archivos de encabezado y de biblioteca necesarios para la aplicación.** Vea [archivos de encabezado y biblioteca necesarios para que una aplicación](required-library-and-header-files-for-an-application.md) obtenga información sobre qué archivos necesita incluir en el proyecto.
3.  **Autentique la aplicación y adquiera la interfaz IWMDMDevice raíz.** La primera tarea que debe realizar una aplicación para usar Windows Media Administrador de dispositivos es autenticarse. Este proceso comprueba la identidad de la aplicación en Windows Media Administrador de dispositivos mediante un certificado ficticio para la funcionalidad limitada de Administrador de dispositivos de Windows Media o el uso de un certificado oficial para una funcionalidad completa. Para obtener más información, consulte [autenticar la aplicación](authenticating-the-application.md).
4.  **Enumerar los dispositivos conectados.** El primer paso para comunicarse con los dispositivos es averiguar qué dispositivos están conectados y accesibles para Windows Media Administrador de dispositivos. Para obtener más información, vea [enumerar dispositivos](enumerating-devices.md).
5.  **Compruebe el estado de los componentes de DRM del dispositivo.** Para usar archivos protegidos con DRM, se debe crear un dispositivo en alguna versión de DRM de Windows Media para dispositivos portátiles, y los componentes de DRM deben estar actualizados. Antes de empezar a controlar archivos en el dispositivo, es mejor ver si el dispositivo admite archivos protegidos con DRM y si es necesario actualizar el dispositivo. Para obtener más información, consulte [control del contenido protegido en la aplicación](handling-protected-content-in-the-application.md).
6.  **Explore un dispositivo.** Una vez que haya encontrado el dispositivo que desea, puede explorar el contenido de dicho dispositivo. Para obtener más información, consulte [explorar un dispositivo](exploring-a-device.md).
7.  **Leer archivos del dispositivo y escribir archivos en el dispositivo.** Una vez que conozca el diseño del dispositivo, puede empezar a transferir archivos hacia y desde el dispositivo. Para obtener más información, consulte [leer archivos del dispositivo](reading-files-from-the-device.md) y [escribir archivos en el dispositivo](writing-files-to-the-device.md).
8.  **Cree listas de reproducción en el dispositivo.** Un tipo de archivo que se puede escribir en el dispositivo es un archivo abstracto, que es una colección de referencias a otros archivos. Aunque la capacidad de escribir archivos abstractos en un dispositivo depende del proveedor de servicios y del dispositivo, generalmente solo los dispositivos MTP tienen esta capacidad. Para obtener más información, consulte [crear una lista de reproducción en el dispositivo](creating-a-playlist-on-the-device.md).

Además de estos pasos, hay varias características más que puede habilitar en la aplicación:

-   **Notificaciones**: Puede permitir que la aplicación reciba notificaciones cuando los dispositivos se conectan o desconectan del equipo. Para obtener más información, consulte [habilitación de notificaciones](enabling-notifications.md).
-   **Registro.** Windows Media Administrador de dispositivos usa un objeto de registro que guarda un registro de sus acciones en un archivo de texto local. Puede agregar mensajes a este registro para ayudarle a analizar los errores o el rendimiento de la aplicación. Para obtener más información, vea [Habilitar el registro](enabling-logging.md).
-   **Uso de contenido de disponibilidad.** Puede recuperar estadísticas de uso de contenido para las licencias que conceden este derecho. Estas estadísticas se pueden enviar a un servidor web para calcular los pagos de regalías a los propietarios de contenido. Para obtener más información, vea [uso de contenido de medición](metering-content-usage.md).

**Nota de precaución**

Es posible que la aplicación tenga que trabajar con una variedad de dispositivos, incluidos algunos que no ha desarrollado y que nunca ha probado el código. Estos dispositivos pueden o no responder con precisión a las consultas y comandos, o implementar MTP u otras especificaciones. Asegúrese de incluir una sólida comprobación de errores y una funcionalidad de reserva para tratar con el inesperado. Programe la defensa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 




