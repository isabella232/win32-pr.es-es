---
title: Uso de la API de cliente de Servicios de implementación de Windows
description: En entornos donde no se puede usar una solución Windows Deployment Services (WDS) estándar para instalar Windows, la API del cliente WDS permite a los desarrolladores escribir aplicaciones de implementación personalizadas.
ms.assetid: abe2a7c7-989a-456e-80df-90d5b816db38
keywords:
- Windows Deployment Services Windows Deployment Services , mediante la API de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6840f8327d1576a51d1f3d6cb7b097aaef87abc674bbbba0a004919ef5ce8366
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760245"
---
# <a name="using-the-windows-deployment-services-client-api"></a>Uso de la API de cliente de Servicios de implementación de Windows

En entornos donde no se puede usar una solución Windows Deployment Services (WDS) estándar para instalar Windows, la API del cliente WDS permite a los desarrolladores escribir aplicaciones de implementación personalizadas. Las aplicaciones pueden usar esta API para comunicarse con el servidor WDS para obtener información sobre las imágenes del sistema disponibles en el servidor. Las aplicaciones cliente de WDS personalizadas deben cumplir las siguientes directrices.

## <a name="install-the-wds-role-on-the-server"></a>Instalación del rol WDS en el servidor

-   Windows Deployment Services (WDS) es la versión revisada de Servicios de instalación remota (RIS), necesitará el rol de servidor WDS en el servidor para implementar soluciones de cliente WDS personalizadas.
-   WDS reemplaza RIS como componente estándar a partir de Windows Server 2008 y Windows Server 2003 por Service Pack 2 (SP2).
-   Debe actualizar el servidor RIS a WDS en Windows Server 2003 con Service Pack 1 (SP1). Puede instalar el rol de servidor WDS con Windows [Automated Installation Kit (WAIK).](https://www.microsoft.com/download/details.aspx?id=10333)

## <a name="start-windows-pe-20"></a>Iniciar Windows PE 2.0

Windows Pe 2.0 debe iniciarse, si aún no se ha iniciado. El cliente WDS y los archivos DLL compatibles solo se cargan mediante setup.exe cuando se encuentra en la fase del entorno de preinstalación de Microsoft Windows (Windows PE 2.0) del procesamiento de la instalación.

-   Cuando un nuevo equipo está conectado a la red, se puede usar la tecnología integrada de entorno de ejecución previa al arranque (PXE) para descargar el Programa de arranque de red. Para obtener más información sobre el arranque PXE de un equipo para instalar Windows, vea La guía paso a paso de actualización de [Windows Deployment Services](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)).
-   Una imagen de arranque de RAMDISK Windows PE 2.0 se puede almacenar en . Formato WIM y descargado como parte del proceso de arranque de red. Windows A continuación, PE se puede cargar y ejecutar directamente desde ese medio.

## <a name="open-a-session-with-the-wds-server"></a>Abrir una sesión con el servidor WDS

El cliente WDS debe abrir una sesión con un servidor WDS.

-   Use la [**función WdsCliCreateSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession) para abrir una sesión con un servidor WDS. Esta función toma el nombre o la dirección IP del servidor y recibe la dirección del identificador de la sesión de cliente de WDS.
-   Si la apertura de la sesión con el servidor requerirá la autenticación del cliente WDS, la aplicación debe proporcionar la dirección de una estructura [**\_ \_ CRED**](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred) de la CLI de WDS que contenga las credenciales de cliente al llamar a la función [**WdsCliCreateSession.**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession) La aplicación puede usar la [**función WdsCliAuthorizeSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliauthorizesession) para convertir una sesión anónima en una sesión autenticada.
-   Cuando la sesión abierta con la función [**WdsCliCreateSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession) ya no es necesaria, la aplicación debe usar la [**función WdsCliClose**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliclose) para cerrar el identificador y liberar los recursos que mantiene la sesión.

## <a name="enumerate-system-images-on-the-wds-server"></a>Enumerar imágenes del sistema en el servidor WDS

El cliente wds puede usar la API para enumerar las imágenes del sistema en el servidor WDS.

-   Use la [**función WdsCliFindFirstImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage) para obtener un identificador para la primera imagen e inicializar la enumeración de imágenes en el servidor WDS.
-   Use la [**función WdsCliFindNextImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage) para incrementar la enumeración iniciada por la [**función WdsCliFindFirstImage.**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage) La **función WdsCliFindNextImage** obtiene el identificador de la siguiente imagen.
-   Use la [**función WdsCliGetImageIndex**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageindex) para obtener el índice de imagen de la imagen actual. Este valor solo es válido hasta que se vuelvan a usar las funciones [**WdsCliFindNextImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage) o [**WdsCliClose.**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliclose)
-   Use la [**función WdsCliGetEnumerationFlags**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetenumerationflags) para obtener marcas de información sobre el filtrado de imágenes.

## <a name="get-information-about-images"></a>Obtener información sobre las imágenes

El cliente de WDS puede usar la API para obtener información sobre las imágenes en un servidor WDS. Las funciones siguientes obtienen información sobre la imagen actual. Dado que las funciones [**WdsCliFindFirstImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage) y [**WdsCliFindNextImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage) cambian el valor del identificador de imagen actual, la aplicación debe almacenar cualquier información que reciba y necesitará en el futuro antes de llamar de nuevo a las funciones **WdsCliFindFirstImage** **o WdsCliFindNextImage.**

-   Use la [**función WdsCliGetImageArchitecture**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagearchitecture) para obtener la arquitectura del procesador de la imagen actual.
-   Use la [**función WdsCliGetImagePath para**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagepath) obtener la ruta de acceso relativa al archivo de imagen que contiene la imagen actual.
-   Use la [**función WdsCliGetImageSize**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagesize) para obtener el tamaño de la imagen.
-   Use la [**función WdsCliGetImageVersion**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageversion) para obtener la versión de la imagen.
-   Use la [**función WdsCliGetImageLanguage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguage) para obtener el idioma predeterminado de la imagen actual.
-   Use la [**función WdsCliGetImageLanguages**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguages) para obtener una matriz de idiomas compatibles con la imagen actual.
-   Usar [**WdsCliGetImageLastModifiedTime**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelastmodifiedtime) devuelve la hora de la última modificación de la imagen actual.
-   Use la [**función WdsCliGetImageName**](/windows/win32/api/WdsClientApi/nf-wdsclientapi-wdscligetimagename) para obtener el nombre de la imagen actual.
-   Use la [**función WdsCliGetImageDescription**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagedescription) para obtener la descripción de la imagen actual.
-   Use la [**función WdsCliGetImageGroup para**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagegroup) obtener el nombre del grupo de imágenes para la imagen actual.
-   Use la [**función WdsCliGetImageHalName para**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehalname) obtener el nombre de capa de abstracción de hardware (CL) de la imagen actual.

## <a name="log-wds-client-events"></a>Registrar eventos de cliente WDS

La funcionalidad de registro de la biblioteca cliente de WDS permite enviar eventos de progreso de instalación desde el cliente al servidor WDS.

-   Use la [**función WdsCliInitializeLog**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliinitializelog) para inicializar el registro de la sesión de cliente de WDS.
-   Use la [**función WdsCliLog**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclilog) para escribir mensajes de evento en el registro del servidor WDS.
-   En Windows Server 2008, el servidor WDS escribe eventos de cliente en un registro de eventos específico de la aplicación que se puede ver a través de eventvwr.exe así como el registro de seguimiento de depuración. En Windows Server 2003 con el registro de depuración habilitado, el servidor WDS escribirá eventos de cliente en el archivo de registro ubicado en %windir% \\ tracing \\ wdsserver.log. El registro de cliente WDS debe estar habilitado en el servidor para capturar estos eventos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la API Windows Deployment Services](about-the-windows-deployment-services-api.md)
</dt> <dt>

[Uso de la API de servidor de Servicios de implementación de Windows](using-the-windows-deployment-services-server-api.md)
</dt> </dl>

 

 