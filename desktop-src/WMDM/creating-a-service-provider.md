---
title: Creación de un proveedor de servicios
description: Creación de un proveedor de servicios
ms.assetid: 7da27fe2-8a57-4adb-94b2-448b6362dc33
keywords:
- Windows Media Administrador de dispositivos, creación de proveedores de servicios
- Administrador de dispositivos, creación de proveedores de servicios
- Windows Media Administrador de dispositivos, guía de programación
- Administrador de dispositivos, guía de programación
- Guía de programación, proveedores de servicios
- Guía de programación, Administrador de dispositivos de Windows Media
- Guía de programación, crear proveedores de servicios
- Windows Media Administrador de dispositivos, proveedores de servicios
- Administrador de dispositivos, proveedores de servicios
- proveedores de servicios, crear
- crear proveedores de servicios, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8469c3d656d151457ed818ea6b4192a3c79ed061
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695622"
---
# <a name="creating-a-service-provider"></a>Creación de un proveedor de servicios

Un proveedor de servicios es un componente que actúa como intermediario entre una aplicación y un dispositivo. Windows Media Administrador de dispositivos enruta las solicitudes de la aplicación al proveedor de servicios, que es responsable de comunicarse con el dispositivo o realizar la acción solicitada. Normalmente, un proveedor de servicios se comunica con un controlador para habilitar la comunicación con el dispositivo. Un proveedor de servicios es un componente COM que implementa las interfaces llamadas por Windows Media Administrador de dispositivos. La interfaz raíz del objeto de proveedor de servicios es [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider). Después de obtener esta interfaz, Windows Media Administrador de dispositivos puede obtener otras interfaces a través de la implementación del proveedor de servicios de varios métodos. Las interfaces que debe implementar un proveedor de servicios se enumeran en [interfaces obligatorias y opcionales](mandatory-and-optional-interfaces.md). La jerarquía de interfaces se muestra en [interfaces para proveedores de servicios](interfaces-for-service-providers.md).

> [!Note]  
> No debe intentar crear un proveedor de servicios MTP; en su lugar, debe usar el proveedor de servicios MTP y los controladores proporcionados por Microsoft.

 

Antes de intentar crear un proveedor de servicios, debe comprender perfectamente qué llamadas realizará una aplicación en un proveedor de servicios. Lea [creación de una aplicación de administrador de dispositivos de Windows Media](creating-a-windows-media-device-manager-application.md) para obtener una idea de las tareas básicas y llamadas que una aplicación realizará en un proveedor de servicios cuando intente comunicarse con un dispositivo.

En la siguiente lista se muestran los pasos principales para desarrollar un proveedor de servicios:

1.  Incluya (y, opcionalmente, compile) el encabezado y los archivos de biblioteca necesarios para el proyecto. Consulte las [bibliotecas y encabezados necesarios de un proveedor de servicios](required-libraries-and-headers-for-a-service-provider.md) para obtener la lista de archivos necesarios.
2.  Implemente todas las demás interfaces de proveedor de servicios obligatorias u opcionales (consulte [interfaces obligatorias y opcionales](mandatory-and-optional-interfaces.md)). Normalmente, se llamará a las interfaces en este orden:
    -   [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
    -   [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider)/2
    -   [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice)
    -   [**IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice)/2
    -   [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage)
    -   [**IMDSPStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage)/2/3
3.  Asegúrese de que el proveedor de servicios o el dispositivo instalan las claves del registro adecuadas durante la instalación. Estas claves especifican parámetros de dispositivo, registran el proveedor de servicios como complemento y habilitan las notificaciones de Plug and Play para la llegada y eliminación de dispositivos. Consulte [parámetros del dispositivo](device-parameters.md), [registro del proveedor de servicios](registering-the-service-provider.md)y [habilitación de PNP para dispositivos](enabling-pnp-for-devices.md).
4.  En la creación de instancias de la clase, autentique el proveedor de servicios en el constructor. Para ello, cree una clase [CSecureChannelServer](csecurechannelserver-class.md) y establezca el certificado. Implemente la interfaz [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) y llame a los métodos de la clase CSecureChannelServer con instancias anteriores. Consulte [autenticación del proveedor de servicios](authenticating-the-service-provider.md) para obtener información sobre cómo crear una instancia de la clase CSecureChannelServer e implementar los métodos IComponentAuthenticate.
5.  Windows Media Administrador de dispositivos consultará a su proveedor de servicios para obtener una lista de dispositivos conectados mediante una llamada a [**IMDServiceProvider2:: CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) o [**IMDServiceProvider:: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices), en función de si el proveedor de servicios administra plug and Play dispositivos. El proveedor de servicios debe devolver una lista de objetos [**IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice) que representen los dispositivos conectados. Consulte [enumeración de dispositivos](enumerating-devices-service-provider.md) para obtener más detalles.
6.  Antes de controlar cualquier llamada, compruebe que se ha establecido un canal seguro. Llame a [**CSecureChannelServer:: fIsAuthenticated**](/previous-versions/bb231600(v=vs.85)) antes de realizar cualquier acción. Si se produce un error en esta llamada, se devuelve WMDM \_ E \_ NOTCERTIFIED.
7.  Necesitará un par de certificado/clave emitido por Microsoft para poder controlar el material protegido con DRM. Consulte [control del contenido protegido en el proveedor de servicios](handling-protected-content-in-the-service-provider.md) para obtener más información.
8.  Para permitir que el dispositivo se sincronice automáticamente con Windows Media Player, debe cumplir los requisitos enumerados en [Habilitar la sincronización con windows media Player](enabling-synchronization-with-windows-media-player.md).
9.  Para habilitar el dispositivo para que aparezca en el explorador de Windows, debe realizar algunos pasos especiales, que se detallan en [requisitos de los reproductores de audio portátiles que aparecen en el explorador de Windows](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 