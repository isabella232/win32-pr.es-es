---
description: El sonido espacial de Microsoft es la solución de nivel de plataforma de Microsoft para la compatibilidad con el sonido espacial en Xbox, Windows y HoloLens 2, lo que permite envolver y elevación (por encima o por debajo del agente de escucha) las indicaciones de audio.
ms.assetid: 4F962F1A-CA4A-4018-BA97-516EA3519650
title: 'Sonido espacial para desarrolladores '
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 09/18/2020
ms.openlocfilehash: 9db3614ea7932af874da351e7a92980d51b90011
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/04/2021
ms.locfileid: "104555254"
---
# <a name="spatial-sound-for-developers"></a>Sonido espacial para desarrolladores 
> [!Note] 
> Esta documentación está destinada a un público del desarrollador. Para permitir que el usuario final habilite el sonido espacial en el dispositivo, consulte [Cómo activar el sonido espacial en Windows 10](https://support.microsoft.com/help/4563140/how-to-turn-on-spatial-sound-in-windows-10).

El sonido espacial de Microsoft es la solución de nivel de plataforma de Microsoft para la compatibilidad con el sonido espacial en Xbox, Windows y HoloLens 2, lo que permite envolver y elevación (por encima o por debajo del agente de escucha) las indicaciones de audio. El sonido espacial puede aprovecharse en aplicaciones de escritorio de Windows (Win32), así como en aplicaciones de Plataforma universal de Windows (UWP) en plataformas admitidas. Las API de sonido espacial permiten a los desarrolladores crear objetos de audio que emiten audio desde posiciones en el espacio 3D. Los objetos de audio dinámico permiten emitir audio a partir de una posición arbitraria en el espacio, que puede cambiar con el tiempo. También puede especificar que los objetos de audio emitan sonido desde uno de 17 canales estáticos predefinidos (8.1.4.4) que pueden representar oradores reales o virtualizados. El usuario selecciona el formato de salida real y se puede abstraer de las implementaciones de sonido espacial de Microsoft. el audio se presentará a los altavoces, auriculares y receptores de Home Theater existentes sin necesidad de cambios de contenido o código. La plataforma es totalmente compatible con la codificación Dolby Atmos en tiempo real para la salida de auriculares HDMI y estéreo, DTS: X para auriculares y Windows Sonic para la codificación de auriculares para auriculares estéreo. Por último, las aplicaciones de sonido espacial de Microsoft se comparan mediante la Directiva de combinación del sistema, y su audio también se mezclará con aplicaciones que no sean compatibles con espacial. La compatibilidad con el sonido espacial de Microsoft también se integra en Media Foundation; las aplicaciones que usan Media Foundation pueden reproducir contenido de Dolby Atmos correctamente sin ninguna implementación adicional.

El sonido espacial con el sonido espacial de Microsoft es compatible con los televisores, los cines domésticos y las barras de sonido compatibles con Dolby Atmos. El sonido espacial también puede usarse con cualquier par de auriculares que el consumidor pueda poseer, con audio representado por la plataforma usando Windows Sonic para auriculares, Dolby Atmos para auriculares o auricular de DTS: X.


## <a name="enabling-microsoft-spatial-sound"></a>Habilitar el sonido espacial de Microsoft

Tanto si es un desarrollador como un consumidor, un usuario debe habilitar el sonido espacial de Microsoft en su dispositivo con el fin de oír sonido espacial.

### <a name="windows"></a>Windows
En los equipos de Windows, esto se hace a través de la página de propiedades de un dispositivo de salida de sonido determinado. En el panel de control de **sonido** , seleccione un dispositivo de salida y haga clic en **propiedades del dispositivo**. En la sección **sonido espacial** de la página, si el dispositivo admite sonido espacial, puede seleccionar uno de los formatos disponibles en la lista desplegable **formato de sonido espacial** .

![Habilitar sonido espacial en el panel de control de sonido](images/spatialsoundsettingswindows1.png)

También puede habilitar el sonido espacial de Microsoft haciendo clic con el botón secundario en el icono de **volumen** en la barra de tareas.

![Habilitar sonido espacial en la barra de tareas](images/spatialsoundsettingswindows2.png)

### <a name="xbox-one"></a>Xbox One
En Xbox One, las capacidades de sonido espacial de Microsoft siempre están disponibles para el consumidor y se habilitan a través de la aplicación configuración en **General-> volumen & salida de audio**.


![habilitación del sonido espacial en Xbox One en la aplicación de configuración ](images/audiosettingsbitstream.png)

Después de seleccionar Dolby Atmos para Home Theater como "formato fragmentada", la compatibilidad con este formato se comprueba a través de datos de identificación de pantalla extendida (EDID) de HDMI. Si el dispositivo HDMI no admite el formato, se muestra un mensaje de error al usuario. Tenga en cuenta que la primera vez que se selecciona esta opción, el usuario debe descargar la aplicación de acceso Dolby.

Si se selecciona un formato distinto de "fragmentada out" para **audio HDMI** , se deshabilita la lista desplegable **formato de fragmentada** .

![sonido espacial deshabilitado en Xbox One en la aplicación de configuración ](images/audiosettingsplain.png)

Seleccione Dolby Atmos para auriculares, auricular de DTS: X o Windows Sonic para auriculares en la lista desplegable **formato de auriculares** en **audio de auriculares**

![habilitación de sonido espacial para auriculares en Xbox One en la aplicación de configuración ](images/audiosettingsheadphone.png)

Cuando el sonido espacial de Microsoft no está disponible (por ejemplo, al reproducirse en altavoces estéreo de portátiles integrados, o si el usuario no ha habilitado explícitamente el sonido espacial de Microsoft por encima de este), el número de objetos dinámicos disponibles devueltos por [**ISpatialAudioClient:: GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) a una aplicación será 0.

### <a name="hololens-2"></a>HoloLens 2

En HoloLens 2, el sonido espacial de Microsoft está habilitado de forma predeterminada y usa la descarga de DSP de hardware diseñada específicamente para Windows Sonic para auriculares.

## <a name="microsoft-spatial-sound-and-audio-middleware"></a>Middleware de audio y sonido espacial de Microsoft

Muchos desarrolladores de aplicaciones y juegos usan soluciones de motor de representación de audio de terceros, que a menudo incluyen herramientas sofisticadas de creación y reproducción. Microsoft se ha asociado con varios de estos proveedores de soluciones para implementar el sonido espacial de Microsoft en sus entornos de creación existentes. Con frecuencia, esto significa que las API descritas aquí se abstraen de la vista de la aplicación. se encapsulan como complementos de procesamiento de señal digital (DSP) en los que la aplicación puede crear instancias y que el implementador de audio de la aplicación puede usar para combinar en una cama de canal de sonido espacial de Microsoft, o enviar voces individuales a complementos de instancia de objeto dinámicos según sea necesario. Póngase en contacto con su proveedor de soluciones de middleware de audio para conocer su nivel de compatibilidad con el sonido espacial de Microsoft.

## <a name="microsoft-spatial-sound-for-audio-renderers"></a>Sonido espacial de Microsoft para representadores de audio

Muchos representadores de audio se dirigen a un punto de conexión [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) de la API de sesión de audio de Windows (WASAPI), donde la aplicación alimenta los búferes de datos de audio mixtos y con formato conforme a un receptor de audio de WASAPI; los búferes entregados se consumen para la combinación con otros clientes, el procesamiento de nivel de sistema final y la representación.

Los puntos de conexión espaciales de sonido espacial de Microsoft se implementan como [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), que tiene muchas similitudes con **IAudioClient**. Admite objetos de sonido *estáticos* que forman una cama de canales, con compatibilidad para canales de hasta 8.1.4.4 (8 canales alrededor del agente de escucha: izquierda, derecha, central, lateral izquierda, lado derecho, atrás a la izquierda, atrás a la derecha y atrás; 1 canal de efectos de baja frecuencia; 4 canales por encima del agente de escucha; 4 canales debajo del agente de escucha). Y admiten objetos de sonido *dinámicos* , que se pueden colocar de forma arbitraria en el espacio 3D.

El patrón de codificación de implementación general para **ISpatialAudioClient** es:

-   Cree objetos de audio estáticos o dinámicos.
-   Inserte en cada fotograma el búfer de audio de cada objeto para que el sistema pueda representarlo.
-   Actualice las posiciones 3D de los objetos dinámicos a petición, con tanta frecuencia (o con poca frecuencia) como quiera la aplicación.

Tenga en cuenta que el formato de salida actual (altavoces o auriculares; Windows Sonic para auriculares, Dolby Atmos o DTS: X) se abstrae de la implementación anterior; el desarrollador de la aplicación puede centrarse en el sonido espacial sin necesidad de dinamizar en función del formato. Las aplicaciones que desean que su comportamiento diverge en función del formato de salida pueden consultar el formato en uso, pero la abstracción significa que no es necesario que una aplicación administre estos formatos.

## <a name="microsoft-spatial-sound-integration-with-audio-renderers"></a>Integración de sonido espacial de Microsoft con representadores de audio

Dado que [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) es un receptor de audio que consume datos, un representador de audio tiene varias opciones para interactuar con él y enviarle datos de audio. Existen tres técnicas de integración de uso frecuente (y para los títulos que usan middleware de audio, puede ver que los complementos equivalentes están disponibles en función de estas opciones):

-   **panorámicas de 7.1.4 y de mastering**: los representadores que ya admiten 7,1 puntos de conexión pueden optar por agregar simplemente compatibilidad con los cuatro canales de alto adicionales que admite la cama de canales estáticos de **ISpatialAudioClient** . Cualquier panorámica del canal que anteriormente hacía (probablemente ya se aprovechaban las coordenadas x, y, z) puede actualizarse para incluir ahora estos canales de altura. Esto suele ofrecer la menor interrupción a los flujos de trabajo de representador y de audio de la aplicación, señal, flujo y control de combinación. A través de los auriculares, tenga en cuenta que la combinación de aplicaciones completa se encontrará espacial, por lo que incluso la música estéreo se percibe como "externalizada" desde el agente de escucha.
-   **Mantener el punto de conexión existente, además de agregar un bus de 7.1.4 (y panorámicas)**: algunos títulos pueden optar por mantener dos puntos de conexión: su punto de conexión de WASAPI estéreo existente (para el contenido "directo a los oídos" no destinado a ser espacial) junto con una superficie de canal estática de **ISpatialAudioClient** compatible con 7.1.4 (o incluso hasta 8.1.4.4). Por supuesto, la administración de interacciones entre dos mezclas presenta más desafíos a los creadores de contenido, aunque se mantiene la sincronización, ya que las instancias WASAPI y ISAC activas en un momento dado usan el mismo tamaño de búfer y reloj para el procesamiento.
-   **Usar objetos de sonido dinámicos para ciertas voces o submezclas**: ofrecer quizás el posicionamiento más detallado o preciso, pero que puede crear una opacidad de combinación, esta técnica implica el uso de objetos de sonido dinámicos de **ISpatialAudioClient** . Tenga en cuenta que los metadatos y el búfer de audio se entregan al representador, por lo que estos sonidos serán opacos para el resto de la combinación de aplicaciones. Además, puesto que hay un número limitado de objetos de sonido dinámicos disponibles, el representador tendrá que considerar la posibilidad de implementar técnicas de priorización, la selección, la colocalización de sonido, la combinación en la cama del canal estático, etc. Los juegos solían usar esta técnica para sonidos individuales "prominente", como un helicóptero que se desplazará sobre el agente de escucha.

Los representadores también pueden mezclar y coincidir entre estos enfoques.

## <a name="microsoft-spatial-sound-runtime-resource-implications"></a>Implicaciones de recursos del entorno de ejecución de sonido espacial de Microsoft

En Windows y Xbox, el número de voces disponibles varía en función del formato en uso. Los formatos Dolby Atmos admiten un total de 32 objetos activos (por lo que si se usa una cama de canal 7.1.4, 20 objetos de sonido dinámico adicionales pueden estar activos). Windows Sonic para auriculares admite un total de 128 objetos activos, con el canal de efectos de baja frecuencia (LFE) que no se cuenta realmente como un objeto, por lo que cuando se usa una cama de canal de 8.1.4.4, 112 objetos de sonido dinámicos pueden estar activos.

En el caso de las aplicaciones Plataforma universal de Windows que se ejecutan en consolas de juegos de Xbox One, la codificación en tiempo real (para Dolby Atmos para Home Theater, Dolby Atmos para auriculares, auricular de DTS: X y Windows Sonic para auriculares) se realiza en hardware sin costo de CPU.

| Formato                       | Número máximo de objetos estáticos (superficie de canal) | Máximo de objetos dinámicos <br> Xbox One | Máximo de objetos dinámicos <br> Windows | Máximo de objetos dinámicos <br> HoloLens 2
|------------------------------|----------------------------------|-------------------------------------------|------------------------------------------|------------------------------------------|
| Dolby Atmos (HDMI)           | 12 (7.1.4)                       | 20                                        | 20                                       | N/D |
| Dolby Atmos (auriculares & altavoces integrados)     | 17 (8.1.4.4)                     | 16                                        | 16                                       | N/D |
| Auricular de DTS: X (auriculares) | 17 (8.1.4.4)        | 16                                        | 32                                      | N/D |
| Windows Sonic para auriculares | 17 (8.1.4.4)        | 15                                        | 112                                      | 31 |


Las aplicaciones también deben tener en cuenta las implicaciones de recursos siguientes:

-   **Ancho de banda de almacenamiento/disco**: el contenido lineal creado previamente en 7.1.4 suele ser mayor que el contenido lineal de 7,1 (aunque los códecs perceptual ya aprovechan las ventajas de la correlación de canales para hacer esto mucho menos que los canales reales del 50% de los datos de audio)
-   **Otros costos de procesamiento de señal digital**: algunos efectos globales anteriores pueden convertirse en instancias por objeto de sonido dinámico. Además, es posible que algunos creadores de contenido deseen actualizar algunos efectos de DSP para admitir canales adicionales o usarlos de forma única.

## <a name="microsoft-spatial-sound-and-sound-spatialization-cues"></a>Señales de sonido espacial de Microsoft y de espacialización de sonido

El sonido espacial de Microsoft se centra en la simulación de posicionamiento sonoro en una esfera idónea alrededor del agente de escucha. Windows Sonic para auriculares, auricular de DTS: X y Dolby Atmos implementan la asignación y la virtualización de altavoces en los auriculares, pero tenga en cuenta que muchos otros aspectos de la simulación espacial de sonido, que normalmente se implementan de forma habilitada para el creador de contenido, se dejan en los motores existentes. Los creadores de contenido siguen usando las herramientas de juego y los procesos existentes que tenían previamente para tales indicaciones espaciales como Doppler, atenuación y filtrado basados en distancias, oclusión y obstruccion y reverberación ambiental.

## <a name="additional-resources"></a>Recursos adicionales

-   [Repositorio de github de ejemplos de sonido espacial de Microsoft](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio)
-   Dolby ofrece una serie de recursos de soporte relacionados con Dolby Atmos y la aplicación Dolby Access en <https://developer.dolby.com> .

## <a name="spatial-sound-interfaces"></a>Interfaces de sonido espacial



| Interfaz                                                                              | Descripción                                                                                                                    |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)                                     | Permite a un cliente crear secuencias de audio que emiten audio a partir de una posición en el espacio 3D.                                          |
| [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)                                     | Representa un objeto que proporciona los datos de audio que se van a representar a partir de una posición en el espacio 3D, relativa al usuario.                |
| [**ISpatialAudioObjectRenderStream**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)             | Proporciona métodos para controlar una secuencia de representación de objetos de audio espacial, incluido el inicio, la detención y el restablecimiento de la secuencia. |
| [**ISpatialAudioObjectRenderStreamNotify**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstreamnotify) | Proporciona notificaciones para que los clientes de audio espacial respondan a los cambios en el estado de un ISpatialAudioObjectRenderStream.     |



 

> [!Note]  
> Al usar las interfaces de [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) en un título del kit de desarrollo de Xbox One (XDK), primero debe llamar a **EnableSpatialAudio** antes de llamar a [**IMMDeviceEnumerator:: EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) o [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Si no lo hace, se producirá un \_ error de E NOinterface en la llamada a Activate. **EnableSpatialAudio** solo está disponible para los títulos de XDK y no es necesario llamarlo para plataforma universal de Windows aplicaciones que se ejecutan en Xbox One, ni para dispositivos que no son de Xbox One.

 

## <a name="spatial-sound-structures"></a>Estructuras de sonido espacial



| Estructura                                                                                                 | Descripción                                                                  |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) | Representa los parámetros de activación de una secuencia de representación de audio espacial.          |
| [**SpatialAudioClientActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioclientactivationparams)                          | Representa los parámetros de activación opcionales para una secuencia de representación de audio espacial. |



 

## <a name="spatial-sound-enumerations"></a>Enumeraciones de sonido espacial



| Enumeración                                | Descripción                                   |
|--------------------------------------------|-----------------------------------------------|
| [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) | Especifica el tipo de un ISpatialAudioObject. |



 

 

 



