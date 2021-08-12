---
title: Creación de una Windows de Administrador de dispositivos multimedia
description: Creación de una Windows de Administrador de dispositivos multimedia
ms.assetid: 6a200bd9-19dd-4130-acb4-e038b469c334
keywords:
- Windows Creación de Administrador de dispositivos multimedia, creación de aplicaciones
- Administrador de dispositivos, crear aplicaciones
- Windows Guía de programación Administrador de dispositivos multimedia
- Administrador de dispositivos,guía de programación
- guía de programación, aplicaciones de escritorio
- guía de programación, Windows media Administrador de dispositivos
- guía de programación, complementos
- guía de programación, creación de aplicaciones
- Windows Aplicaciones Administrador de dispositivos multimedia, aplicaciones de escritorio
- Administrador de dispositivos aplicaciones de escritorio
- Windows Archivos Administrador de dispositivos, complementos
- Administrador de dispositivos,complemento
- complementos, crear
- complementos, guía de programación
- aplicaciones de escritorio, crear
- crear Windows aplicaciones Administrador de dispositivos multimedia, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba468d4d9a04176847259087b8ba2626c2ffa3e0cac089f8433993320a7e125
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585562"
---
# <a name="creating-a-windows-media-device-manager-application"></a>Creación de una Windows de Administrador de dispositivos multimedia

En esta sección se describe cómo usar Windows media Administrador de dispositivos en la aplicación. El término "aplicación" aquí significa un ejecutable, como un reproductor multimedia, o un complemento COM, como un complemento de medición.

Microsoft incluye varios proveedores de servicios con Windows XP y Reproductor de Windows Media 10, incluido un proveedor de servicios MTP, un proveedor de servicios Windows CE (para dispositivos que ejecutan Windows CE y usan el protocolo RAPI, como Pocket PC) y un proveedor de servicios para dispositivos de categoría de almacenamiento masivo (MSC). También puede crear su propio proveedor de servicios para garantizar la comunicación con su propio dispositivo. Para obtener más información, vea [Crear un proveedor de servicios.](creating-a-service-provider.md)

Hay una serie de proveedores de servicios heredados de terceros que abordan un dispositivo que no es MTP, que no es RAPI o que no es MSC de un fabricante determinado. Estos proveedores de servicios se incluyen en el disco del controlador incluido con estos dispositivos.

Una aplicación que usa Windows Media Administrador de dispositivos debe realizar los pasos siguientes.

1.  **Conozca los problemas de privacidad relacionados con el desarrollo de una aplicación.** Consulte [Declaración de privacidad](privacy-statement.md) para obtener información sobre algunos problemas de privacidad relacionados con el desarrollo de Windows media Administrador de dispositivos aplicación.
2.  **Incluya los archivos de encabezado y biblioteca necesarios para la aplicación.** Consulte [Biblioteca requerida y Archivos de encabezado para una aplicación para](required-library-and-header-files-for-an-application.md) obtener información sobre los archivos que necesitará incluir en el proyecto.
3.  **Autentique la aplicación y adquiera la interfaz IWMDMDevice raíz.** La primera tarea que una aplicación debe hacer para usar Windows media Administrador de dispositivos es autenticarse a sí misma. Este proceso comprueba la identidad de la aplicación para Windows Media Administrador de dispositivos mediante un certificado ficticio para la funcionalidad limitada de Windows Media Administrador de dispositivos o mediante un certificado oficial para la funcionalidad completa. Para obtener más información, vea [Authenticating the Application](authenticating-the-application.md).
4.  **Enumerar los dispositivos conectados.** El primer paso para comunicarse con los dispositivos es averiguar qué dispositivos están conectados y accesibles para Windows Media Administrador de dispositivos. Para obtener más información, [vea Enumerar dispositivos.](enumerating-devices.md)
5.  **Compruebe el estado de los componentes drm del dispositivo.** Para usar archivos protegidos con DRM, se debe crear un dispositivo en alguna versión de Windows Media DRM para dispositivos portátiles, y los componentes drm deben estar actualizados. Antes de empezar a controlar los archivos en el dispositivo, es mejor ver si el dispositivo admite archivos protegidos con DRM y si el dispositivo debe actualizarse. Para obtener más información, vea [Control de contenido protegido en la aplicación](handling-protected-content-in-the-application.md).
6.  **Explorar un dispositivo.** Una vez que haya encontrado el dispositivo que desea, puede explorar el contenido de ese dispositivo. Para obtener más información, vea [Exploración de un dispositivo.](exploring-a-device.md)
7.  **Leer archivos del dispositivo y escribir archivos en el dispositivo.** Después de conocer el diseño del dispositivo, puede empezar a transferir archivos hacia y desde el dispositivo. Para obtener más información, vea [Leer archivos desde el dispositivo y](reading-files-from-the-device.md) Escribir archivos en el [dispositivo.](writing-files-to-the-device.md)
8.  **Cree listas de reproducción en el dispositivo.** Un tipo de archivo que puede escribir en el dispositivo es un archivo abstracto, que es una colección de referencias a otros archivos. Aunque la capacidad de escribir archivos abstractos en un dispositivo depende del proveedor de servicios y del dispositivo, generalmente solo los dispositivos MTP tienen esta funcionalidad. Para obtener más información, vea [Crear una lista de reproducción en el dispositivo](creating-a-playlist-on-the-device.md).

Además de estos pasos, hay varias características más que puede habilitar en la aplicación:

-   **Notificaciones**: Puede permitir que la aplicación reciba notificaciones cuando los dispositivos se conecten o se desconecten del equipo. Para obtener más información, vea [Habilitación de notificaciones.](enabling-notifications.md)
-   **Registro.** Windows El Administrador de dispositivos utiliza un objeto de registro que guarda un registro de sus acciones en un archivo de texto local. Puede agregar mensajes a este registro para ayudarle a analizar errores o rendimiento en la aplicación. Para obtener más información, vea [Habilitación del registro.](enabling-logging.md)
-   **Uso de contenido de medición.** Puede recuperar estadísticas de uso de contenido para las licencias que conceden este derecho. A continuación, estas estadísticas se pueden enviar a un servidor web para calcular los pagos de canon a los propietarios de contenido. Para obtener más información, vea [Uso de contenido de medición.](metering-content-usage.md)

**Una nota de precaución**

Es posible que la aplicación tenga que trabajar con una variedad de dispositivos, incluidos algunos que no ha desarrollado y con los que nunca ha probado el código. Estos dispositivos podrían o no responder con precisión a consultas y comandos, o implementar MTP u otras especificaciones. Asegúrese de incluir una sólida funcionalidad de comprobación de errores y reserva para hacer frente a lo inesperado. Programa a la defensiva.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 




