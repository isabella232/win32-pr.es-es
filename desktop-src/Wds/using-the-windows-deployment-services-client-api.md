---
title: Uso de la API de cliente de Servicios de implementación de Windows
description: En entornos donde no se puede usar una solución estándar de servicios de implementación de Windows (WDS) para instalar Windows, la API del cliente de WDS permite a los desarrolladores escribir aplicaciones de implementación personalizadas.
ms.assetid: abe2a7c7-989a-456e-80df-90d5b816db38
keywords:
- Servicios de implementación de Windows servicios de implementación de Windows, uso de la API de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 872422a5c84bf1d8ea7c3688b122ba2389c1e968
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077897"
---
# <a name="using-the-windows-deployment-services-client-api"></a>Uso de la API de cliente de Servicios de implementación de Windows

En entornos donde no se puede usar una solución estándar de servicios de implementación de Windows (WDS) para instalar Windows, la API del cliente de WDS permite a los desarrolladores escribir aplicaciones de implementación personalizadas. Las aplicaciones pueden usar esta API para comunicarse con el servidor WDS y obtener información acerca de las imágenes del sistema disponibles en el servidor. Las aplicaciones cliente de WDS personalizadas deben cumplir las siguientes directrices.

## <a name="install-the-wds-role-on-the-server"></a>Instalación del rol de WDS en el servidor

-   Servicios de implementación de Windows (WDS) es la versión revisada de los servicios de instalación remota (RIS). necesitará el rol de servidor de WDS en el servidor para implementar soluciones de cliente de WDS personalizadas.
-   WDS reemplaza a RIS como componente estándar a partir de Windows Server 2008 y Windows Server 2003 con Service Pack 2 (SP2).
-   Debe actualizar el servidor de RIS a WDS en Windows Server 2003 con Service Pack 1 (SP1). Puede instalar el rol de servidor de WDS con el [Kit de instalación automatizada de Windows (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).

## <a name="start-windows-pe-20"></a>Iniciar Windows PE 2,0

Se debe iniciar Windows PE 2,0, si aún no se ha iniciado. El cliente WDS y los archivos dll auxiliares solo se cargan mediante setup.exe cuando está en la fase de Microsoft Entorno de preinstalación de Windows (Windows PE 2,0) del proceso de instalación.

-   Cuando un nuevo equipo se conecta a la red, se puede usar la tecnología de entorno de ejecución previo al arranque (PXE) integrada para descargar el programa de arranque de red. Para obtener más información acerca del arranque con PXE en un equipo para instalar Windows, consulte [la guía paso a paso de actualización de servicios de implementación de Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)).
-   Una imagen de arranque de RAMDISK de Windows PE 2,0 puede almacenarse en. Formato WIM y descargado como parte del proceso de arranque de red. Windows PE se puede cargar y ejecutar directamente desde ese medio.

## <a name="open-a-session-with-the-wds-server"></a>Abrir una sesión con el servidor WDS

El cliente WDS debe abrir una sesión con un servidor WDS.

-   Use la función [**WdsCliCreateSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession) para abrir una sesión con un servidor WDS. Esta función toma el nombre o la dirección IP del servidor y recibe la dirección del identificador de la sesión de cliente de WDS.
-   Si al abrir la sesión con el servidor se requiere la autenticación del cliente WDS, la aplicación debe proporcionar la dirección de una estructura [**\_ \_ CRED**](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred) de la CLI de WDS que contenga las credenciales del cliente al llamar a la función [**WdsCliCreateSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession) . La aplicación puede usar la función [**WdsCliAuthorizeSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliauthorizesession) para convertir una sesión anónima en una sesión autenticada.
-   Cuando la sesión abierta con la función [**WdsCliCreateSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession) ya no es necesaria, la aplicación debe usar la función [**WdsCliClose**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliclose) para cerrar el identificador y los recursos de liberación que mantiene la sesión.

## <a name="enumerate-system-images-on-the-wds-server"></a>Enumerar imágenes del sistema en el servidor WDS

El cliente WDS puede usar la API para enumerar las imágenes del sistema en el servidor WDS.

-   Use la función [**WdsCliFindFirstImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage) para obtener un identificador de la primera imagen e inicializar la enumeración de imágenes en el servidor WDS.
-   Use la función [**WdsCliFindNextImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage) para incrementar la enumeración iniciada por la función [**WdsCliFindFirstImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage) . La función **WdsCliFindNextImage** obtiene el identificador de la imagen siguiente.
-   Utilice la función [**WdsCliGetImageIndex**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageindex) para obtener el índice de imagen de la imagen actual. Este valor solo es válido hasta que se vuelvan a usar las funciones [**WdsCliFindNextImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage) o [**WdsCliClose**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliclose) .
-   Utilice la función [**WdsCliGetEnumerationFlags**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetenumerationflags) para obtener marcas de información sobre el filtrado de imágenes.

## <a name="get-information-about-images"></a>Obtener información acerca de las imágenes

El cliente WDS puede usar la API para obtener información sobre las imágenes en un servidor WDS. Las siguientes funciones obtienen información acerca de la imagen actual. Dado que las funciones [**WdsCliFindFirstImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage) y [**WdsCliFindNextImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage) cambian el valor de identificador de imagen actual, la aplicación debe almacenar cualquier información que obtenga y necesitará en el futuro antes de volver a llamar a las funciones **WdsCliFindFirstImage** o **WdsCliFindNextImage** .

-   Utilice la función [**WdsCliGetImageArchitecture**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagearchitecture) para obtener la arquitectura de procesador de la imagen actual.
-   Utilice la función [**WdsCliGetImagePath**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagepath) para obtener la ruta de acceso relativa al archivo de imagen que contiene la imagen actual.
-   Use la función [**WdsCliGetImageSize**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagesize) para obtener el tamaño de la imagen.
-   Use la función [**WdsCliGetImageVersion**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageversion) para obtener la versión de la imagen.
-   Utilice la función [**WdsCliGetImageLanguage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguage) para obtener el idioma predeterminado de la imagen actual.
-   Utilice la función [**WdsCliGetImageLanguages**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguages) para obtener una matriz de lenguajes admitidos por la imagen actual.
-   Use [**WdsCliGetImageLastModifiedTime**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelastmodifiedtime) devuelve la hora de la última modificación de la imagen actual.
-   Utilice la función [**WdsCliGetImageName**](/windows/win32/api/WdsClientApi/nf-wdsclientapi-wdscligetimagename) para obtener el nombre de la imagen actual.
-   Utilice la función [**WdsCliGetImageDescription**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagedescription) para obtener la descripción de la imagen actual.
-   Utilice la función [**WdsCliGetImageGroup**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagegroup) para obtener el nombre del grupo de imágenes de la imagen actual.
-   Utilice la función [**WdsCliGetImageHalName**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehalname) para obtener el nombre de la capa de abstracción de hardware (HAL) de la imagen actual.

## <a name="log-wds-client-events"></a>Registrar eventos de cliente de WDS

La funcionalidad de registro de la biblioteca de cliente de WDS permite enviar eventos de progreso de la instalación desde el cliente al servidor WDS.

-   Use la función [**WdsCliInitializeLog**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliinitializelog) para inicializar el registro para la sesión de cliente de WDS.
-   Utilice la función [**WdsCliLog**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclilog) para escribir mensajes de eventos en el registro del servidor WDS.
-   En Windows Server 2008, el servidor WDS escribe eventos de cliente en un registro de eventos específico de la aplicación que se pueden ver a través de eventvwr.exe, así como el registro de seguimiento de depuración. En Windows Server 2003 con el registro de depuración habilitado, el servidor WDS escribirá eventos de cliente en el archivo de registro que se encuentra en% WINDIR% \\ Tracing \\ WDSServer. log. El registro de cliente de WDS debe estar habilitado en el servidor para capturar estos eventos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la API de servicios de implementación de Windows](about-the-windows-deployment-services-api.md)
</dt> <dt>

[Uso de la API de servidor de Servicios de implementación de Windows](using-the-windows-deployment-services-server-api.md)
</dt> </dl>

 

 