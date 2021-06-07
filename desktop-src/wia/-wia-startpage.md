---
description: Adquisición de imágenes de Windows (WIA) es la plataforma de adquisición de imágenes fijas de la familia de sistemas operativos Windows a partir de Windows Millennium Edition (Windows Me) y Windows XP.
ms.assetid: 8f32422e-25ec-48bc-9d79-57dbb3b53e93
title: Adquisición de imágenes de Windows (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664b5accaa1312eae3baf6161e41c9c65e718c69
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443096"
---
# <a name="windows-image-acquisition-wia"></a>Adquisición de imágenes de Windows (WIA)

Adquisición de imágenes de Windows (WIA) es la plataforma de adquisición de imágenes fijas de la familia de sistemas operativos Windows a partir de Windows Millennium Edition (Windows Me) y Windows XP.

-   [Introducción](#introduction)
-   [Ventajas de la adquisición de imágenes de Windows 2.0](#benefits-of-windows-image-acquisition-20)
    -   [Para escritores de aplicaciones](#for-application-writers)
    -   [Para fabricantes de dispositivos](#for-device-manufactures)
    -   [Para los usuarios del analizador](#for-scanner-users)
-   [Desarrollo de la adquisición de imágenes de Windows](#development-of-windows-image-acquisition)
-   [Información general sobre la adquisición de imágenes de Windows](#overview-of-windows-image-acquisition)
-   [Hechos sobre la adquisición de imágenes de Windows 2.0](#facts-about-windows-image-acquisition-20)
-   [Audiencia para desarrolladores](#developer-audience)
-   [Requisitos en tiempo de ejecución](#run-time-requirements)
-   [Temas de WIA](#wia-topics)

## <a name="introduction"></a>Introducción

La plataforma WIA permite que las aplicaciones de imágenes y gráficos interactúen con el hardware de creación de imágenes y normaliza la interacción entre diferentes aplicaciones y escáneres. Esto permite a las distintas aplicaciones hablar e interactuar con esos distintos escáneres sin necesidad de que los escritores de aplicaciones y fabricantes de escáneres personalice sus aplicaciones o controladores para cada combinación de dispositivo de aplicación.

![gráfico que muestra la arquitectura básica de wia como una capa de dos vías entre aplicaciones de creación de imágenes y dispositivos. ](images/wia-diagram1.png)

## <a name="benefits-of-windows-image-acquisition-20"></a>Ventajas de la adquisición de imágenes de Windows 2.0

WIA proporciona ventajas a los desarrolladores de aplicaciones, fabricantes de dispositivos y usuarios de escáneres que necesitan interactuar con el hardware de creación de imágenes.

### <a name="for-application-writers"></a>Para escritores de aplicaciones

-   Windows ejecuta un proceso de certificación para los controladores de WIA, por lo que se garantiza que las aplicaciones WIA sean compatibles de nivel base con todos los escáneres basados en WIA.
-   Los controladores WIA se cargan en el proceso del servicio WIA, lo que proporciona un entorno de controlador más estable.
-   Las aplicaciones se pueden iniciar desde el botón de examen del analizador a través de eventos de inserción compatibles con el subsistema WIA.
-   WiA incluye un filtro de segmentación predeterminado que todos los controladores pueden aprovechar. De este modo, las aplicaciones no tienen que escribir código para el examen en varias regiones con fines como separar un gran número de fotos distribuidas en un escáner de pantalla plana.

### <a name="for-device-manufactures"></a>Para fabricantes de dispositivos

-   El proceso de certificación de controladores WIA ayuda a los desarrolladores de controladores a establecer que su controlador es compatible con WIA.
-   Los controladores WIA pueden aprovechar un filtro de segmentación integrado, un filtro de procesamiento de imágenes y un controlador de errores, si deciden hacerlo.
-   Los escáneres basados en WIA funcionan directamente en Windows con aplicaciones de examen de Windows, como Fax y Escáner de Windows y Paint.
-   Los controladores de WIA ofrecen una mejor integración con Windows, como la experiencia completa del dispositivo.
-   La versión de Windows Vista incluye un controlador de clase WSD-WIA que permite que todos los dispositivos compatibles con el protocolo Web Services for Scanner (WS-Scan) funcionen con aplicaciones WIA sin ningún controlador ni software adicional.

### <a name="for-scanner-users"></a>Para los usuarios del analizador

-   Los escáneres basados en WIA se pueden usar desde aplicaciones de Windows como Fax y Escáner de Windows y Paint sin necesidad de software adicional.
-   Las aplicaciones y escáneres basados en WIA también pueden aprovechar los complementos WIA, como el filtro de segmentación, que permite características como el procesamiento de una serie de imágenes en el analizador y el examen de todos ellos en archivos individuales sin intervención del usuario.
-   Los dispositivos basados en WIA ofrecen una integración mucho mejor con otras características de Windows, como la característica Device Stage para Windows 7.
-   WIA proporciona una experiencia de análisis más sólida, estable y confiable mediante el aislamiento del controlador y la aplicación.

## <a name="development-of-windows-image-acquisition"></a>Desarrollo de la adquisición de imágenes de Windows

La arquitectura de creación de imágenes en Windows 2000 y Windows 95 o posterior constaba de una abstracción de hardware de bajo nivel, Still Image Architecture (KPI) y un conjunto de API de alto nivel conocido como TCONEXIÓN. En Windows XP y Windows Me se introdujo WIA. WIA es una arquitectura de creación de imágenes que se basa en EL LUGAR y no requiere T PLUGIN, aunque TWAIN todavía se admite junto con WIA.

WIA 1.0 se introdujo en Windows Me y Windows XP y admite escáneres, cámaras digitales y equipos de vídeo digital. WIA 2.0 se publicó con Windows Vista. WIA 2.0 está destinado a escáneres, pero sigue ofreciendo compatibilidad con aplicaciones y dispositivos WIA 1.0 heredados a través de una capa de compatibilidad de WIA 1.0 a WIA 2.0 proporcionada por el servicio WIA. Sin embargo, se quitó la compatibilidad con contenido de vídeo de WIA para Windows Vista. Se recomienda la API de dispositivos portátiles de Windows (WPD) para cámaras digitales y equipos de vídeo digital en el futuro. Los controladores WIA 1.0, ASÍ como LOS CONTROLADORES T VLAN DE LA VENTANA DE 2017 siguen siendo compatibles directamente con Windows Vista y Windows 7, junto con controladores de dispositivo WIA 2.0 nativos y aplicaciones de creación de imágenes.

## <a name="overview-of-windows-image-acquisition"></a>Información general sobre la adquisición de imágenes de Windows

WIA proporciona un marco que permite a un dispositivo presentar sus funcionalidades únicas al sistema operativo y permite que las aplicaciones de creación de imágenes invoque esas funcionalidades únicas.

La plataforma WIA incluye un protocolo de adquisición de datos, un modelo de controlador de dispositivo e interfaz (DDI), una API y un servicio WIA dedicado. La plataforma también incluye un conjunto de controladores de modo kernel integrados que admiten la comunicación con dispositivos de creación de imágenes conectados localmente a través de las interfaces USB, serie/paralela, SCSI y FireWire. El subsistema WIA también incluye una capa de compatibilidad transparente que permite que las aplicaciones compatibles con TJDBC empleen y usen dispositivos basados en controladores WIA.

Los dispositivos de creación de imágenes conectados a la red que admiten el protocolo De servicios web para dispositivos (WSD) también se pueden usar desde aplicaciones de creación de imágenes compatibles con WIA en Windows Vista y Windows 7 de forma estándar a través de un controlador de clase WSD-WIA que se incluye como parte de Windows Vista. El controlador de clase convierte las llamadas WIA en llamadas WSD y viceversa, y hace que las aplicaciones WIA ya existentes funcionen con escáneres basados en WSD sin ningún controlador adicional.

Los controladores WIA están hechos de un componente de interfaz de usuario (UI) y un componente de controlador principal, cargados en dos espacios de proceso diferentes: la interfaz de usuario en el espacio de la aplicación y el núcleo del controlador en el espacio del servicio WIA. El servicio se ejecuta en el contexto del sistema local en Windows XP y se ejecuta en el contexto de servicio local a partir de Windows Server 2003 y Windows Vista para mejorar la seguridad frente a conductores malintencionados o malintencionados.

![gráfico que muestra la arquitectura de wia y cómo funciona como servicio.](images/wia-arch.png)

El conjunto de API de WIA expone las aplicaciones de creación de imágenes para seguir con la funcionalidad de hardware de adquisición de imágenes al proporcionar compatibilidad con:

-   Enumeración de dispositivos de adquisición de imágenes disponibles.
-   Crear conexiones a varios dispositivos simultáneamente.
-   Consultar las propiedades de los dispositivos de forma estándar y ampliable.
-   Adquisición de datos del dispositivo mediante mecanismos de transferencia estándar y de alto rendimiento.
-   Mantener las propiedades de imagen entre transferencias de datos.
-   Notificación del estado del dispositivo y control de eventos de examen.

Windows agregó compatibilidad con scripting a WIA mediante la publicación de la biblioteca de automatización de WIA en 2002 que se incorporó en Windows Vista como capa de automatización de adquisición de imágenes de Windows (WIA) y sigue formando parte de Windows 7. La biblioteca de automatización de WIA proporciona funcionalidades de adquisición de imágenes de un extremo a otro para entornos de desarrollo de aplicaciones y lenguajes de programación habilitados para la automatización, como Microsoft Visual Basic 6.0, Active Server Pages (ASP), VBScript y \# C.

Para Windows 7, las API de WIA tienen compatibilidad adicional para complementar la compatibilidad con el examen de inserción ya existente.

-   Examen iniciado por el dispositivo configurado automáticamente con parámetros de examen configurados en el analizador en el panel frontal del dispositivo.
-   Selección automática de origen para el examen iniciado por el dispositivo.

## <a name="facts-about-windows-image-acquisition-20"></a>Hechos sobre la adquisición de imágenes de Windows 2.0

-   El mecanismo de transferencia de datos de WIA 2.0 se basa en secuencias. La abstracción de secuencias elimina la distinción entre los distintos tipos de transferencia y también permite el intercambio de metadatos acordados mutuamente entre el dispositivo y la aplicación.
-   El subsistema WIA 2.0 también incluye un complemento básico de controlador de filtro de procesamiento de imágenes que, opcionalmente, es reemplazable por el controlador del analizador, si el controlador decide proporcionar un filtro de procesamiento de imágenes personalizado. El filtro integrado permite el procesamiento posterior de las imágenes adquiridas a través del analizador. El filtro de procesamiento de imágenes también habilita las vistas previas de software activas cuando se ajustan valores pequeños, como el brillo y el contraste.
-   El filtro de segmentación es otro componente de WIA útil que se puede reemplazar por un filtro más personalizado por el controlador del analizador. El filtro de segmentación se puede usar para el examen de varias regiones. El examen en varias regiones, por ejemplo, permite que una aplicación detecte automáticamente diferentes regiones de examen sin intervención del usuario, como la identificación de un grupo de fotos de forma aleatoria en la pantalla plana del escáner.
-   WIA 2.0 proporciona un controlador de errores reemplazable o extensible para controlar correctamente y, posiblemente, recuperarse de errores y retrasos de software, hardware y configuración. El controlador de errores es otro componente de WIA que se puede reemplazar por una versión más personalizada por el controlador del analizador. Esta extensión proporciona mensajes de estado y error durante las adquisiciones de datos, como "Lamp warming up", "Cover open", "Paper jam" y así sucesivamente. Esta extensión también permite una compatibilidad más limpia para "Cancelar operaciones".

## <a name="developer-audience"></a>Audiencia de los desarrolladores

La API de WIA está diseñada para su uso por los programadores de C/C++. Es necesario estar familiarizado con la GUI de Windows y las interfaces del modelo de objetos componentes (COM).

Para desarrolladores familiarizados con Microsoft Visual Basic 6.0, Active Server Pages (ASP) o scripting, WIA proporciona una capa de automatización para Windows XP Service Pack 1 (SP1) o posterior que se basa y simplifica el acceso a la base proporcionada por C/C++. Para obtener información sobre la capa de automatización, vea Capa de automatización de adquisición [de imágenes de Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

> [!Note]  
> La capa de automatización de WIA reemplaza el scripting de adquisición de imágenes de Windows (WIA) 1.0.

 

## <a name="run-time-requirements"></a>Requisitos del tiempo de ejecución

Las aplicaciones que usan la API de WIA requieren Windows XP o posterior.

## <a name="wia-topics"></a>Temas de WIA

Los temas de WIA se organizan como se muestra en la tabla siguiente.



|  Tema                                                                                                                            | Descripción                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Acerca de la adquisición de imágenes de Windows](-wia-about-windows-image-acquisition.md)                                                  | Información general sobre WIA                                                                     |
| [Controladores de adquisición de imágenes de Windows](/windows-hardware/drivers/image/windows-image-acquisition-drivers)                  | Desarrollo de controladores WIA                                                                            |
| [Capa de automatización de adquisición de imágenes de Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage) | Capa de automatización de WIA                                                                              |
| [WIA Tutorial](-wia-wia-tutorial.md)                                                                                        | Tutorial del código incluido en el kit de desarrollo de software (SDK) que se centra en tareas específicas |
| [Referencia](-wia-reference.md)                                                                                              | Información sobre interfaces, métodos, objetos y tipos de datos de WIA usados en C/C++ y scripting.      |



 

 

 
