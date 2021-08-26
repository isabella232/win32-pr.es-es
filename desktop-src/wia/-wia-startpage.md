---
description: Windows Adquisición de imágenes (WIA) es la plataforma de adquisición de imágenes fijas de la familia de sistemas operativos Windows a partir de Windows Edition Edition (Windows Me) y Windows XP.
ms.assetid: 8f32422e-25ec-48bc-9d79-57dbb3b53e93
title: Adquisición de imágenes de Windows (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e467d76f054a8cccb4c309f69b211d0d3d6fbe949625324c871319028aa78ebc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057023"
---
# <a name="windows-image-acquisition-wia"></a>Adquisición de imágenes de Windows (WIA)

Windows Adquisición de imágenes (WIA) es la plataforma de adquisición de imágenes fijas de la familia de sistemas operativos Windows a partir de Windows Edition Edition (Windows Me) y Windows XP.

-   [Introducción](#introduction)
-   [Ventajas de Windows image acquisition 2.0](#benefits-of-windows-image-acquisition-20)
    -   [Para escritores de aplicaciones](#for-application-writers)
    -   [Para fabricantes de dispositivos](#for-device-manufactures)
    -   [Para usuarios del analizador](#for-scanner-users)
-   [Desarrollo de la adquisición Windows imágenes](#development-of-windows-image-acquisition)
-   [Introducción a la adquisición Windows imágenes](#overview-of-windows-image-acquisition)
-   [Hechos sobre Windows image acquisition 2.0](#facts-about-windows-image-acquisition-20)
-   [Audiencia para desarrolladores](#developer-audience)
-   [Requisitos en tiempo de ejecución](#run-time-requirements)
-   [Temas de WIA](#wia-topics)

## <a name="introduction"></a>Introducción

La plataforma WIA permite que las aplicaciones de imágenes y gráficos interactúen con el hardware de creación de imágenes y normaliza la interacción entre diferentes aplicaciones y escáneres. Esto permite que esas distintas aplicaciones hablen con esos distintos escáneres e interactúen con ellos sin necesidad de que los escritores de aplicaciones y los fabricantes de escáneres personalice su aplicación o controladores para cada combinación de aplicación y dispositivo.

![gráfico que muestra la arquitectura básica de wia como una capa de dos vías entre aplicaciones de creación de imágenes y dispositivos. ](images/wia-diagram1.png)

## <a name="benefits-of-windows-image-acquisition-20"></a>Ventajas de Windows image acquisition 2.0

WIA proporciona ventajas a los desarrolladores de aplicaciones, fabricantes de dispositivos y usuarios de escáner que necesitan interactuar con el hardware de creación de imágenes.

### <a name="for-application-writers"></a>Para escritores de aplicaciones

-   Windows un proceso de certificación para controladores WIA, por lo que se garantiza que las aplicaciones WIA sean compatibles de nivel base con todos los escáneres basados en WIA.
-   Los controladores WIA se cargan en el proceso del servicio WIA, lo que proporciona un entorno de controlador más estable.
-   Las aplicaciones se pueden iniciar desde el botón de examen del analizador a través de eventos de inserción compatibles con el subsistema WIA.
-   WiA incluye un filtro de segmentación predeterminado del que pueden aprovechar todos los controladores. De este modo, las aplicaciones no tienen que escribir código para el examen de varias regiones con fines como separar un gran número de fotos distribuidas en un escáner plano.

### <a name="for-device-manufactures"></a>Para fabricantes de dispositivos

-   El proceso de certificación de controladores WIA ayuda a los desarrolladores de controladores a establecer que su controlador es compatible con WIA.
-   Los controladores WIA pueden aprovechar un filtro de segmentación integrado, un filtro de procesamiento de imágenes y un controlador de errores, si deciden hacerlo.
-   Los escáneres basados en WIA funcionan directamente en Windows con aplicaciones de análisis de Windows como Windows fax y examen y Paint.
-   Los controladores de WIA ofrecen una mejor integración Windows, como la experiencia completa del dispositivo.
-   Windows La versión vista incluye un controlador de clase WSD-WIA que permite que todos los dispositivos compatibles con el protocolo Web Services for Scanner (WS-Scan) funcionen con aplicaciones WIA sin ningún controlador ni software adicional.

### <a name="for-scanner-users"></a>Para usuarios del analizador

-   Los escáneres basados en WIA se pueden usar Windows aplicaciones como fax y Windows y digitalización y Paint sin necesidad de software adicional.
-   Las aplicaciones y escáneres basados en WIA también pueden aprovechar los complementos de WIA, como el filtro de segmentación, que permite características como el procesamiento de varias imágenes en el analizador y el examen de todos ellos en archivos individuales sin intervención del usuario.
-   Los dispositivos basados en WIA ofrecen una integración mucho mejor con otras características Windows, como la característica Fase de dispositivo para Windows 7.
-   WIA proporciona una experiencia de análisis más sólida, estable y confiable mediante el aislamiento del controlador y la aplicación.

## <a name="development-of-windows-image-acquisition"></a>Desarrollo de la adquisición Windows imagen

La arquitectura de creación de imágenes de Windows 2000 y Windows 95 o posterior constaba de una abstracción de hardware de bajo nivel, Still Image Architecture (KPI) y un conjunto de API de alto nivel conocido como TCONEXIÓN. En Windows se introdujo XP Windows WIA. WIA es una arquitectura de creación de imágenes que se basa en LANTO y no requiere TWAIN, aunque TWAIN todavía se admite junto con WIA.

WIA 1.0 se introdujo en Windows Me y Windows XP y admite escáneres, cámaras digitales y equipos de vídeo digital. WIA 2.0 se publicó con Windows Vista. WIA 2.0 está destinado a escáneres, pero sigue ofreciendo compatibilidad con aplicaciones y dispositivos WIA 1.0 heredados a través de una capa de compatibilidad de WIA 1.0 a WIA 2.0 proporcionada por el servicio WIA. Sin embargo, se quitó la compatibilidad con contenido de vídeo de WIA para Windows Vista. Se recomienda Windows API de dispositivos portátiles (WPD) para cámaras digitales y equipos de vídeo digital en el futuro. WiA 1.0, así como los controladores T ODBC de T VLAN todavía se admiten directamente en Windows Vista y Windows 7 junto con controladores de dispositivo WIA 2.0 nativos y aplicaciones de creación de imágenes.

## <a name="overview-of-windows-image-acquisition"></a>Introducción a la adquisición Windows imágenes

WIA proporciona un marco que permite a un dispositivo presentar sus funcionalidades únicas al sistema operativo y permite que las aplicaciones de creación de imágenes invoque esas funcionalidades únicas.

La plataforma WIA incluye un protocolo de adquisición de datos, un modelo de controlador de dispositivo e interfaz (DDI), una API y un servicio WIA dedicado. La plataforma también incluye un conjunto de controladores de modo kernel integrados que admiten la comunicación con dispositivos de creación de imágenes conectados localmente a través de las interfaces USB, serie/paralela, SCSI y FireWire. El subsistema WIA también incluye una capa de compatibilidad transparente que permite que las aplicaciones compatibles con TJDBC empleen y usen dispositivos basados en controladores WIA.

Los dispositivos de creación de imágenes conectados a la red que admiten el protocolo Servicios web para dispositivos (WSD) también se pueden usar desde aplicaciones de creación de imágenes compatibles con WIA en Windows Vista y Windows 7 de forma estándar a través de un controlador de clase WSD-WIA que se incluye como parte de Windows Vista. El controlador de clase convierte las llamadas WIA en llamadas WSD y viceversa, y hace que las aplicaciones WIA ya existentes funcionen con escáneres basados en WSD sin ningún controlador adicional.

Los controladores DE WIA se incluyen en un componente de interfaz de usuario (UI) y un componente de controlador principal, cargados en dos espacios de proceso diferentes: la interfaz de usuario en el espacio de la aplicación y el núcleo del controlador en el espacio del servicio WIA. El servicio se ejecuta en el contexto del sistema local en Windows XP y se ejecuta en el contexto de servicio local a partir de Windows Server 2003 y Windows Vista para mejorar la seguridad frente a errores o controladores malintencionados.

![gráfico que muestra la arquitectura de wia y cómo funciona como servicio.](images/wia-arch.png)

El conjunto de API de WIA expone las aplicaciones de creación de imágenes para mantener la funcionalidad de hardware de adquisición de imágenes al proporcionar compatibilidad con:

-   Enumeración de dispositivos de adquisición de imágenes disponibles.
-   Crear conexiones a varios dispositivos simultáneamente.
-   Consultar las propiedades de los dispositivos de forma estándar y ampliable.
-   Adquisición de datos del dispositivo mediante mecanismos de transferencia estándar y de alto rendimiento.
-   Mantener las propiedades de imagen entre transferencias de datos.
-   Notificación del estado del dispositivo y control de eventos de examen.

Windows compatibilidad con scripting agregado a WIA mediante la publicación de la biblioteca de automatización de WIA en 2002 que se incorporó en Windows Vista como capa de automatización de adquisición de imágenes (WIA) de Windows y sigue formando parte de Windows 7. La biblioteca de automatización de WIA proporciona funcionalidades de adquisición de imágenes de un extremo a otro para entornos de desarrollo de aplicaciones habilitados para automatización y lenguajes de programación como Microsoft Visual Basic 6.0, Active Server Pages (ASP), VBScript y C \# .

Para Windows 7, las API de WIA tienen compatibilidad adicional para complementar la compatibilidad con el examen de inserción ya existente.

-   Examen iniciado por el dispositivo configurado automáticamente con parámetros de examen configurados en el analizador en el panel frontal del dispositivo.
-   Selección de origen automática para el examen iniciado por el dispositivo.

## <a name="facts-about-windows-image-acquisition-20"></a>Hechos sobre Windows image acquisition 2.0

-   El mecanismo de transferencia de datos de WIA 2.0 se basa en secuencias. La abstracción de secuencias elimina la distinción entre los distintos tipos de transferencia y también permite el intercambio de metadatos acordados mutuamente entre el dispositivo y la aplicación.
-   El subsistema WIA 2.0 también incluye un complemento básico de controlador de filtro de procesamiento de imágenes que el controlador del analizador puede reemplazar opcionalmente, si el controlador decide proporcionar un filtro de procesamiento de imágenes personalizado. El filtro integrado permite el procesamiento posterior de las imágenes adquiridas a través del analizador. El filtro de procesamiento de imágenes también permite vistas previas de software activas cuando se ajustan valores pequeños, como el brillo y el contraste.
-   El filtro de segmentación es otro componente útil de WIA que puede reemplazarse por un filtro más personalizado por el controlador del analizador. El filtro de segmentación se puede usar para el examen en varias regiones. El examen en varias regiones, por ejemplo, permite que una aplicación detecte automáticamente regiones de examen diferentes sin intervención del usuario, como la identificación de un grupo de fotos de forma aleatoria en la pantalla plana del escáner.
-   WIA 2.0 proporciona un controlador de errores reemplazable o extensible para controlar correctamente y, posiblemente, recuperarse de errores y retrasos de software, hardware y configuración. El controlador de errores es otro componente de WIA que el controlador del analizador puede reemplazar por una versión más personalizada. Esta extensión proporciona mensajes de estado y error durante las adquisiciones de datos, como "Lamp warming up", "Cover open", "Paper jam" y así sucesivamente. Esta extensión también permite una compatibilidad más limpia con "Cancelar operaciones".

## <a name="developer-audience"></a>Audiencia de los desarrolladores

La API de WIA está diseñada para que la usen los programadores de C/C++. Es necesario estar familiarizado Windows interfaz gráfica de usuario y el modelo de objetos componentes (COM).

Para desarrolladores familiarizados con Microsoft Visual Basic 6.0, Active Server Pages (ASP) o scripting, WIA proporciona una capa de automatización para Windows XP Service Pack 1 (SP1) o posterior que se basa y simplifica el acceso a la base proporcionada por C/C++. Para obtener información sobre la capa de automatización, [vea Windows capa de automatización de adquisición de imágenes.](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)

> [!Note]  
> La capa de automatización de WIA reemplaza Windows de creación de imágenes (WIA) 1.0.

 

## <a name="run-time-requirements"></a>Requisitos del tiempo de ejecución

Las aplicaciones que usan la API de WIA requieren Windows XP o posterior.

## <a name="wia-topics"></a>Temas de WIA

Los temas de WIA se organizan como se muestra en la tabla siguiente.



|  Tema                                                                                                                            | Descripción                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Acerca de Windows adquisición de imágenes](-wia-about-windows-image-acquisition.md)                                                  | Información general sobre WIA                                                                     |
| [Windows Controladores de adquisición de imágenes](/windows-hardware/drivers/image/windows-image-acquisition-drivers)                  | Desarrollo de controladores WIA                                                                            |
| [Windows Capa de automatización de adquisición de imágenes](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage) | Capa de automatización de WIA                                                                              |
| [WIA Tutorial](-wia-wia-tutorial.md)                                                                                        | Tutorial del código incluido en el kit de desarrollo de software (SDK) que se centra en tareas específicas |
| [Referencia](-wia-reference.md)                                                                                              | Información sobre interfaces, métodos, objetos y tipos de datos de WIA usados en C/C++ y scripting.      |



 

 

 
