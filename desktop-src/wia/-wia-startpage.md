---
description: Adquisición de imágenes de Windows (WIA) es la plataforma de adquisición de imágenes en la familia de sistemas operativos Windows a partir de Windows Millennium Edition (Windows me) y Windows XP.
ms.assetid: 8f32422e-25ec-48bc-9d79-57dbb3b53e93
title: Adquisición de imágenes de Windows (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0ff1f3fb51a4c87d909637a90591336d9d2eb30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541918"
---
# <a name="windows-image-acquisition-wia"></a>Adquisición de imágenes de Windows (WIA)

Adquisición de imágenes de Windows (WIA) es la plataforma de adquisición de imágenes en la familia de sistemas operativos Windows a partir de Windows Millennium Edition (Windows me) y Windows XP.

-   [Introducción](#introduction)
-   [Ventajas de la adquisición de imágenes de Windows 2,0](#benefits-of-windows-image-acquisition-20)
    -   [Para escritores de aplicaciones](#for-application-writers)
    -   [Para los fabricantes de dispositivos](#for-device-manufactures)
    -   [Para usuarios de escáner](#for-scanner-users)
-   [Desarrollo de la adquisición de imágenes de Windows](#development-of-windows-image-acquisition)
-   [Información general sobre la adquisición de imágenes de Windows](#overview-of-windows-image-acquisition)
-   [Datos sobre la adquisición de imágenes de Windows 2,0](#facts-about-windows-image-acquisition-20)
-   [Audiencia para desarrolladores](#developer-audience)
-   [Requisitos de tiempo de ejecución](#run-time-requirements)
-   [Temas de WIA](#wia-topics)

## <a name="introduction"></a>Introducción

La plataforma WIA permite a las aplicaciones de imágenes o gráficos interactuar con el hardware de creación de imágenes y normaliza la interacción entre diferentes aplicaciones y escáneres. Esto permite que las distintas aplicaciones se comuniquen con ellos e interactúen con ellos sin necesidad de que los creadores de aplicaciones y los fabricantes del escáner personalicen su aplicación o los controladores para cada combinación de dispositivo de aplicación.

![gráfico que muestra la arquitectura básica de WIA como una capa bidireccional entre aplicaciones y dispositivos de creación de imágenes. ](images/wia-diagram1.png)

## <a name="benefits-of-windows-image-acquisition-20"></a>Ventajas de la adquisición de imágenes de Windows 2,0

WIA proporciona ventajas a los desarrolladores de aplicaciones, los fabricantes de dispositivos y los usuarios de escáner que necesitan interactuar con el hardware de creación de imágenes.

### <a name="for-application-writers"></a>Para escritores de aplicaciones

-   Windows ejecuta un proceso de certificación para los controladores WIA, por lo que se garantiza que las aplicaciones WIA son compatibles de nivel básico con todos los escáneres basados en WIA.
-   Los controladores WIA se cargan en el proceso del servicio WIA, lo que proporciona un entorno de controladores más estable.
-   Las aplicaciones se pueden iniciar desde el botón examen del escáner a través de eventos de inserciones compatibles con el subsistema WIA.
-   WIA incluye un filtro de segmentación predeterminado con el que todos los controladores pueden aprovecharse; de este modo, las aplicaciones no tienen que escribir código para el análisis de varias regiones con fines como separar un gran número de fotografías distribuidas en un escáner plano.

### <a name="for-device-manufactures"></a>Para los fabricantes de dispositivos

-   El proceso de certificación de los controladores WIA ayuda a los desarrolladores de controladores a establecer que su controlador es compatible con WIA.
-   Los controladores WIA pueden aprovechar un filtro de segmentación integrado, el filtro de procesamiento de imágenes y el controlador de errores, si deciden hacerlo.
-   Los escáneres basados en WIA funcionan correctamente en Windows con las aplicaciones de exploración de Windows, como fax y escáner de Windows y Paint.
-   Los controladores WIA ofrecen una mejor integración con Windows, como la experiencia completa del dispositivo.
-   La versión de Windows Vista incluye un controlador de clase WSD-WIA que permite que todos los dispositivos compatibles con el protocolo Web Services for Scanner (WS-Scan) funcionen con aplicaciones WIA sin ningún controlador o software adicional.

### <a name="for-scanner-users"></a>Para usuarios de escáner

-   Los escáneres basados en WIA se pueden usar desde aplicaciones Windows, como fax y escáner de Windows, y Paint sin necesidad de software adicional.
-   Las aplicaciones y los escáneres basados en WIA también pueden aprovechar las ventajas de los complementos de WIA, como el filtro de segmentación, que permite que dichas características procesen un número de imágenes en el escáner y las analicen en archivos individuales sin la intervención del usuario.
-   Los dispositivos basados en WIA ofrecen una integración mucho mejor con otras características de Windows, como la característica de Device Stage para Windows 7.
-   WIA proporciona una experiencia de exploración más sólida, estable y confiable al aislar el controlador y la aplicación.

## <a name="development-of-windows-image-acquisition"></a>Desarrollo de la adquisición de imágenes de Windows

La arquitectura de la creación de imágenes en Windows 2000 y Windows 95 o posterior consta de una abstracción de hardware de bajo nivel, una arquitectura de imagen fija (STI) y un conjunto de API de alto nivel conocido como TWAIN. En Windows XP y Windows me, se presentó WIA. WIA es una arquitectura de creación de imágenes que se basa en STI y no requiere TWAIN, aunque TWAIN todavía se admite junto con WIA.

WIA 1,0 se presentó en Windows me y Windows XP, y es compatible con escáneres, cámaras digitales y equipos de vídeo digital. WIA 2,0 se lanzó con Windows Vista. WIA 2,0 está orientado a los escáneres, pero sigue ofreciendo compatibilidad con dispositivos y aplicaciones WIA 1,0 heredados a través de un nivel de compatibilidad WIA 1,0 a WIA 2,0 proporcionado por el servicio WIA. Sin embargo, se ha quitado la compatibilidad con el contenido de vídeo de WIA para Windows Vista. En el futuro se recomienda la API de dispositivos portátiles de Windows (WPD) para cámaras digitales y equipos de vídeo digital. Los controladores WIA 1,0 y STI TWAIN todavía se admiten directamente en Windows Vista y Windows 7 junto con los controladores de dispositivos y las aplicaciones de imágenes nativos de WIA 2,0.

## <a name="overview-of-windows-image-acquisition"></a>Información general sobre la adquisición de imágenes de Windows

WIA proporciona un marco de trabajo que permite a un dispositivo presentar sus capacidades únicas en el sistema operativo y permite a las aplicaciones de creación de imágenes invocar esas capacidades únicas.

La plataforma WIA incluye un protocolo de adquisición de datos, un modelo de controlador de dispositivo y una interfaz (DDI), una API y un servicio WIA dedicado. La plataforma también incluye un conjunto de controladores de modo kernel integrados que admiten la comunicación con dispositivos de imágenes conectados localmente a través de las interfaces USB, serie/paralelo, SCSI y FireWire. El subsistema WIA también incluye una capa de compatibilidad transparente que permite a las aplicaciones compatibles con TWAIN emplear y usar dispositivos basados en el controlador WIA.

Los dispositivos de imágenes conectados a la red que admiten el protocolo de servicios web para dispositivos (WSD) también se pueden usar desde aplicaciones de creación de imágenes compatibles con WIA en Windows Vista y Windows 7 de forma integrada a través de un controlador de clase WSD-WIA que se incluye como parte de Windows Vista. El controlador de clase convierte las llamadas de WIA a llamadas WSD y viceversa, y hace que las aplicaciones WIA ya existentes funcionen con escáneres basados en WSD sin ningún controlador adicional.

Los controladores WIA se componen de un componente de interfaz de usuario (IU) y un componente de controlador principal, cargados en dos espacios de proceso diferentes: interfaz de usuario en el espacio de la aplicación y el núcleo del controlador en el espacio del servicio WIA. El servicio se ejecuta en el contexto del sistema local en Windows XP y se ejecuta en el contexto del servicio local a partir de Windows Server 2003 y Windows Vista para mejorar la seguridad contra los controladores erróneos o malintencionados.

![gráfico que muestra la arquitectura de WIA y cómo funciona como servicio.](images/wia-arch.png)

El conjunto de API de WIA expone las aplicaciones de creación de imágenes a la funcionalidad de hardware de adquisición de imagen, ya que proporciona compatibilidad con:

-   Enumeración de los dispositivos de adquisición de imágenes disponibles.
-   Crear conexiones a varios dispositivos simultáneamente.
-   Consultar las propiedades de los dispositivos de forma estándar y ampliable.
-   Adquisición de datos del dispositivo mediante mecanismos de transferencia estándar y de alto rendimiento.
-   Mantenimiento de las propiedades de la imagen entre las transferencias de datos.
-   Notificación del estado del dispositivo y del control de eventos de exploración.

Windows agregó compatibilidad con scripting a WIA al liberar la biblioteca de automatización de WIA en 2002 que se incorporó en Windows Vista como capa de automatización de adquisición de imágenes de Windows (WIA) y sigue siendo parte de Windows 7. La biblioteca de automatización de WIA proporciona capacidades de adquisición de imágenes de un extremo a otro para entornos de desarrollo de aplicaciones habilitadas para automatización y lenguajes de programación como Microsoft Visual Basic 6,0, Active Server Pages (ASP), VBScript y C \# .

En el caso de Windows 7, las API de WIA tienen compatibilidad adicional para complementar la compatibilidad con el análisis de inserciones ya existente.

-   Análisis Iniciado por el dispositivo configurado automáticamente con parámetros de análisis configurados en el escáner en el panel frontal del dispositivo.
-   Selección de origen automática para el examen iniciado por el dispositivo.

## <a name="facts-about-windows-image-acquisition-20"></a>Datos sobre la adquisición de imágenes de Windows 2,0

-   El mecanismo de transferencia de datos de WIA 2,0 se basa en secuencias. La abstracción de la secuencia quita la distinción entre diferentes tipos de transferencia y también permite el intercambio de metadatos acordados mutuamente entre el dispositivo y la aplicación.
-   El subsistema WIA 2,0 también incluye un complemento de controlador de filtro básico de procesamiento de imágenes que, opcionalmente, puede reemplazar el controlador del escáner, si el controlador elige proporcionar un filtro de procesamiento de imágenes personalizado. El filtro integrado permite el procesamiento posterior de las imágenes adquiridas a través del escáner. El filtro de procesamiento de imágenes también habilita las vistas previas de software en directo cuando se ajusta la configuración pequeña, como el brillo y el contraste.
-   El filtro de segmentación es otro práctico componente WIA que se puede reemplazar por un filtro más personalizado por el controlador del escáner. El filtro de segmentación se puede usar para la detección en varias regiones. El análisis de varias regiones, como ejemplo, permite a una aplicación detectar automáticamente distintas regiones de examen sin intervención del usuario, como la identificación de un grupo de fotografías que se basan de forma aleatoria en el escáner plano.
-   WIA 2,0 proporciona un controlador de errores reemplazable y extensible para controlar y, posiblemente, recuperarse de errores de software, hardware y configuración y retrasos. El controlador de errores es otro componente WIA que se puede reemplazar por una versión más personalizada por el controlador del analizador. Esta extensión proporciona mensajes de estado y de error durante las adquisiciones de datos, como "preparación de la lámpara", "cubierta abierta", "atasco de papel", etc. Esta extensión también permite la compatibilidad más limpia con "cancelar operaciones".

## <a name="developer-audience"></a>Audiencia de los desarrolladores

La API WIA está diseñada para que la usen los programadores de C/C++. Es necesario estar familiarizado con la interfaz gráfica de usuario de Windows y con las interfaces del modelo de objetos componentes (COM).

Para los desarrolladores familiarizados con Microsoft Visual Basic 6,0, páginas de Active Server (ASP) o scripting, WIA proporciona un nivel de automatización para Windows XP Service Pack 1 (SP1) o posterior que se basa y simplifica el acceso a la base proporcionada por C/C++. Para obtener información sobre la capa de automatización, consulte [capa de automatización de adquisición de imágenes de Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

> [!Note]  
> El nivel de automatización de WIA sustituye el scripting de adquisición de imágenes de Windows (WIA) 1,0.

 

## <a name="run-time-requirements"></a>Requisitos del tiempo de ejecución

Las aplicaciones que usan la API de WIA requieren Windows XP o posterior.

## <a name="wia-topics"></a>Temas de WIA

Los temas de WIA se organizan como se muestra en la tabla siguiente.



|                                                                                                                              |                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Acerca de la adquisición de imágenes de Windows](-wia-about-windows-image-acquisition.md)                                                  | Información general sobre WIA                                                                     |
| [Controladores de adquisición de imágenes de Windows](/windows-hardware/drivers/image/windows-image-acquisition-drivers)                  | Desarrollo de controladores WIA                                                                            |
| [Nivel de automatización de adquisición de imágenes de Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage) | Nivel de automatización de WIA                                                                              |
| [Tutorial de WIA](-wia-wia-tutorial.md)                                                                                        | Tutorial de código incluido en el kit de desarrollo de software (SDK) que se centra en tareas específicas |
| [Referencia](-wia-reference.md)                                                                                              | Información sobre interfaces, métodos, objetos y tipos de datos de WIA utilizados en C/C++ y en scripting.      |



 

 

 
