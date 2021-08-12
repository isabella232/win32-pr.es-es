---
title: Creación de un proveedor de servicios
description: Creación de un proveedor de servicios
ms.assetid: 7da27fe2-8a57-4adb-94b2-448b6362dc33
keywords:
- Windows Creación de Administrador de dispositivos, creación de proveedores de servicios
- Administrador de dispositivos, crear proveedores de servicios
- Windows Guía de programación Administrador de dispositivos multimedia
- Administrador de dispositivos,guía de programación
- guía de programación, proveedores de servicios
- guía de programación, Windows media Administrador de dispositivos
- guía de programación, creación de proveedores de servicios
- Windows Media Administrador de dispositivos,proveedores de servicios
- Administrador de dispositivos,proveedores de servicios
- proveedores de servicios, crear
- crear proveedores de servicios, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1f5b6abfba6b143e0a8ab7913ed1c1f53bbdeb3104a6a8450e438843349598
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585859"
---
# <a name="creating-a-service-provider"></a>Creación de un proveedor de servicios

Un proveedor de servicios es un componente que actúa como intermediario entre una aplicación y un dispositivo. Windows El Administrador de dispositivos enruta las solicitudes de la aplicación al proveedor de servicios, que luego es responsable de comunicarse con el dispositivo o realizar la acción solicitada. Normalmente, un proveedor de servicios se comunica con un controlador para habilitar la comunicación con el dispositivo. Un proveedor de servicios es un componente COM que implementa las interfaces a las que llama Windows Media Administrador de dispositivos. La interfaz raíz del objeto de proveedor de servicios [**es IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider). Después de obtener esta interfaz, Windows Media Administrador de dispositivos pueden obtener otras interfaces a través de la implementación del proveedor de servicios de varios métodos. Las interfaces que debe implementar un proveedor de servicios se enumeran en [Interfaces obligatorias y opcionales](mandatory-and-optional-interfaces.md). La jerarquía de interfaces se muestra en [Interfaces for Service Providers](interfaces-for-service-providers.md).

> [!Note]  
> No debe intentar crear un proveedor de servicios MTP; en su lugar, debe usar el proveedor de servicios MTP y los controladores proporcionados por Microsoft.

 

Antes de intentar crear un proveedor de servicios, debe comprender exhaustivamente qué llamadas realizará una aplicación en un proveedor de servicios. Lea Creating a Windows Media Administrador de dispositivos Application (Creación de una aplicación de [Windows Media Administrador de dispositivos)](creating-a-windows-media-device-manager-application.md) para obtener una idea de las tareas básicas y las llamadas que realizará una aplicación en un proveedor de servicios cuando intente comunicarse con un dispositivo.

En la lista siguiente se muestran los pasos clave para desarrollar un proveedor de servicios:

1.  Incluya (y, opcionalmente, compile) los archivos de encabezado y biblioteca necesarios para el proyecto. Consulte [Bibliotecas y encabezados necesarios para un proveedor de servicios](required-libraries-and-headers-for-a-service-provider.md) para obtener la lista de archivos necesarios.
2.  Implemente todas las demás interfaces de proveedor de servicios obligatorias u opcionales (vea [Interfaces obligatorias y opcionales).](mandatory-and-optional-interfaces.md) Normalmente, se llamará a las interfaces en este orden:
    -   [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
    -   [**ImDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider)/2
    -   [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice)
    -   [**IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice)/2
    -   [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage)
    -   [**IMDSPStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage)/2/3
3.  Asegúrese de que el proveedor de servicios o el dispositivo instala las claves del Registro adecuadas durante la instalación. Estas claves especifican los parámetros del dispositivo, registran el proveedor de servicios como un complemento y habilitan Plug and Play notificaciones para la llegada y eliminación del dispositivo. Vea [Parámetros del dispositivo](device-parameters.md), Registrar el proveedor de [servicios](registering-the-service-provider.md)y [Habilitar PnP para dispositivos](enabling-pnp-for-devices.md).
4.  Al crear instancias de la clase, autentique el proveedor de servicios en el constructor. Para ello, cree una [clase CSecureChannelServer](csecurechannelserver-class.md) y establezca el certificado. Implemente [**la interfaz IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) y llame a los métodos de la clase CSecureChannelServer a la que se llamó anteriormente. Consulte [Autenticación del proveedor de](authenticating-the-service-provider.md) servicios para obtener información sobre cómo crear instancias de la clase CSecureChannelServer e implementar los métodos IComponentAuthenticate.
5.  Windows Media Administrador de dispositivos consultará al proveedor de servicios para obtener una lista de dispositivos conectados mediante una llamada a [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) o [**IMDServiceProvider::EnumDevices,**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices)en función de si el proveedor de servicios controla Plug and Play dispositivos. El proveedor de servicios debe devolver una lista de [**objetos IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice) que representan los dispositivos conectados. Consulte [Enumeración de dispositivos](enumerating-devices-service-provider.md) para obtener más detalles.
6.  Antes de controlar cualquier llamada, compruebe que se ha establecido un canal seguro. Llame [**a CSecureChannelServer::fIsAuthenticated antes**](/previous-versions/bb231600(v=vs.85)) de realizar cualquier acción. Si se produce un error en esta llamada, devuelva WMDM \_ E \_ NOTCERTIFIED.
7.  Necesitará un par de certificados y claves emitido por Microsoft para poder controlar el material protegido con DRM. Consulte [Control de contenido protegido en el proveedor de servicios](handling-protected-content-in-the-service-provider.md) para obtener más información.
8.  Para permitir que el dispositivo se sincronice automáticamente con Reproductor de Windows Media, debe cumplir los requisitos enumerados en Habilitación de la sincronización [con Reproductor de Windows Media](enabling-synchronization-with-windows-media-player.md).
9.  Para permitir que el dispositivo aparezca en Windows Explorer, debe realizar algunos pasos especiales, que se detallan en Requisitos para que los reproductores de audio portátiles aparezcan [en Windows Explorer](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación**](programming-guide.md)
</dt> </dl>

 

 