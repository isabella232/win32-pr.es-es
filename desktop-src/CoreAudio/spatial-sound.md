---
description: Microsoft Spatial Sound es la solución de nivel de plataforma de Microsoft para la compatibilidad con sonido espacial en Xbox, Windows y HoloLens 2, lo que permite indicaciones de audio envolventes y de elevación (por encima o por debajo del agente de escucha).
ms.assetid: 4F962F1A-CA4A-4018-BA97-516EA3519650
title: 'Sonido espacial para desarrolladores '
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 09/18/2020
ms.openlocfilehash: 361b45ab015f9604d2fca743714b6e6868635d2f858c22fa7e107234c66bd656
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088372"
---
# <a name="spatial-sound-for-developers"></a>Sonido espacial para desarrolladores 
> [!Note] 
> Esta documentación está dirigida a un público desarrollador. Para obtener compatibilidad con el usuario final para habilitar el sonido espacial en el [dispositivo,](https://support.microsoft.com/help/4563140/how-to-turn-on-spatial-sound-in-windows-10)consulte Activación del sonido espacial en Windows 10 .

Microsoft Spatial Sound es la solución de nivel de plataforma de Microsoft para la compatibilidad con sonido espacial en Xbox, Windows y HoloLens 2, lo que permite las indicaciones de audio envolventes y de elevación (por encima o por debajo del agente de escucha). El sonido espacial se puede aprovechar Windows de escritorio (Win32), así como aplicaciones de la Plataforma universal de Windows (UWP) en plataformas compatibles. Las API de sonido espacial permiten a los desarrolladores crear objetos de audio que emiten audio desde posiciones en espacio 3D. Los objetos de audio dinámicos permiten emitir audio desde una posición arbitraria en el espacio, lo que puede cambiar con el tiempo. También puede especificar que los objetos de audio emitan sonido desde uno de los 17 canales estáticos predefinidos (8.1.4.4) que pueden representar hablantes reales o virtualizados. El usuario selecciona el formato de salida real y se puede abstraer de las implementaciones de sonido espacial de Microsoft. El audio se presentará a los hablantes existentes, a los micrófonos y a los receptores de salas sin necesidad de realizar cambios en el código ni en el contenido. La plataforma es totalmente compatible con la codificación Dolby Atmos en tiempo real para la salida de sonido estéreo y HDMI, DTS:X para cascos y Windows Sonic para auriculares codificación para estéreo. Por último, las aplicaciones de Sonido espacial de Microsoft cumplen la directiva de combinación del sistema y su audio también se mezclará con aplicaciones que no tienen en cuenta el espacio. La compatibilidad con sonido espacial de Microsoft también se integra en Media Foundation; Las aplicaciones que usan Media Foundation pueden reproducir correctamente contenido de Dolby Atmos sin ninguna implementación adicional.

El sonido espacial con Microsoft Spatial Sound admite televisores, salas de cine y barras de sonido que admiten Dolby Atmos. El sonido espacial también se puede usar con cualquier par de cascos que el consumidor pueda poseer, con audio representado por la plataforma mediante Windows Sonic para auriculares, Dolby Atmos for Headphones o DTS Desenlazado:X.


## <a name="enabling-microsoft-spatial-sound"></a>Habilitación del sonido espacial de Microsoft

Ya sea como desarrollador o consumidor, un usuario debe habilitar Microsoft Spatial Sound en su dispositivo para poder escuchar sonido espacializado.

### <a name="windows"></a>Windows
En Windows equipos, esto se realiza a través de la página de propiedades de un dispositivo de salida de sonido determinado. En el panel **de** control Sonido, seleccione un dispositivo de salida y haga clic en **Propiedades del dispositivo.** En la **sección Sonido espacial** de la página, si el dispositivo admite sonido espacial, puede seleccionar uno de los formatos disponibles en la lista desplegable Formato de **sonido** espacial.

![habilitar el sonido espacial en el panel de control de sonido](images/spatialsoundsettingswindows1.png)

También puede habilitar El sonido espacial de Microsoft haciendo clic con el botón derecho en el **icono Volumen** de la barra de tareas.

![habilitar el sonido espacial desde la barra de tareas](images/spatialsoundsettingswindows2.png)

### <a name="xbox-one"></a>Xbox One
En Xbox One, las funcionalidades de sonido espacial de Microsoft siempre están disponibles para el consumidor y se habilitan a través de la aplicación Configuración en **General -> Volume & salida de audio**.


![habilitar el sonido espacial en Xbox One en la aplicación de configuración ](images/audiosettingsbitstream.png)

Después de seleccionar Dolby Atmos para el cine principal como "formato de secuencia de bits", la compatibilidad con este formato se comprueba a través de datos de identificación de pantalla extendida (EDID) de HDMI. Si el dispositivo HDMI no admite el formato, se muestra un mensaje de error al usuario. Tenga en cuenta que para seleccionar esta opción la primera vez es necesario que el usuario descargue Dolby Access aplicación.

Si se selecciona un formato distinto de "Bitstream out" para **el audio HDMI,** la lista **desplegable Formato de** secuencia de bits está deshabilitada.

![sonido espacial deshabilitado en Xbox One en la aplicación de configuración ](images/audiosettingsplain.png)

Seleccione Dolby Atmos for Headphones, DTS Headset:X o Windows Sonic para auriculares en la lista desplegable **Formato** de casco en **Audio de casco.**

![habilitar el sonido espacial para los cascos en Xbox One en la aplicación de configuración ](images/audiosettingsheadphone.png)

Cuando Microsoft Spatial Sound no está disponible (por ejemplo, al reproducir en altavoces estéreo de portátiles incrustados o si el usuario no ha habilitado explícitamente Microsoft Spatial Sound por encima), el número de objetos dinámicos disponibles devueltos por [**ISpatialAudioClient::GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) a una aplicación será 0.

### <a name="hololens-2"></a>HoloLens 2

En HoloLens 2, Microsoft Spatial Sound está habilitado de forma predeterminada y usa la descarga de DSP de hardware diseñada específicamente para Windows Sonic para auriculares.

## <a name="microsoft-spatial-sound-and-audio-middleware"></a>Middleware de audio y sonido espacial de Microsoft

Muchos desarrolladores de aplicaciones y juegos usan soluciones de motor de representación de audio de terceros, que a menudo incluyen sofisticadas herramientas de creación y de reproducción. Microsoft se ha asociado con varios de estos proveedores de soluciones para implementar Microsoft Spatial Sound en sus entornos de creación existentes. Esto suele significar que las API que se analizan aquí se abstrae de la vista de la aplicación. se encapsulan como complementos de procesamiento de señales digitales (DSP) de los que la aplicación puede crear instancias y que el implementador de audio de la aplicación puede usar para mezclar con un canal de sonido espacial de Microsoft, una submezcla o enviar voces individuales a los complementos de instancia de objeto dinámico según sea necesario. Consulte con el proveedor de soluciones de middleware de audio para obtener su nivel de compatibilidad con Microsoft Spatial Sound.

## <a name="microsoft-spatial-sound-for-audio-renderers"></a>Sonido espacial de Microsoft para representadores de audio

Muchos representadores de audio tienen como destino un punto de conexión [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) de Windows Audio Session API (WASAPI), donde la aplicación alimenta búferes de datos de audio mixtos y conformes al formato a un receptor de audio WASAPI. a continuación, los búferes entregados se consumen para mezclarse con otros clientes, el procesamiento final de nivel de sistema y la representación.

Los puntos de conexión espaciales de Sonido espacial de Microsoft se implementan como [**ISpatialAudioClient,**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)que tiene muchas similitudes con **IAudioClient.** Admite  objetos de sonido estáticos que forman un canal, con compatibilidad con hasta 8.1.4.4 canales (8 canales alrededor del agente de escucha: Left, Right, Center, Side Left, Side Right, Back Left, Back Right y Back Center; 1 canal de efectos de baja frecuencia; 4 canales por encima del agente de escucha; 4 canales por debajo del agente de escucha). Y admite objetos *de* sonido dinámicos, que se pueden colocar arbitrariamente en un espacio 3D.

El patrón de codificación de implementación general **para ISpatialAudioClient** es:

-   Cree objetos de audio estáticos o dinámicos.
-   Feed each object's audio buffer each frame so the system can render it. (Alimentar el búfer de audio de cada objeto para que el sistema pueda representarlo).
-   Actualice las posiciones 3D de los objetos dinámicos a petición, con la frecuencia (o con poca frecuencia) que desee la aplicación.

Tenga en cuenta que el formato de salida actual (altavoces o micrófonos; Windows Sonic para auriculares, Dolby Atmos o DTS Spatial:X) se abstrae de la implementación anterior: el desarrollador de la aplicación puede centrarse en el sonido espacial sin necesidad de dinamear en función del formato. Las aplicaciones que quieren que su comportamiento divergen en función del formato de salida pueden consultar el formato en uso, pero la abstracción significa que no es necesaria una aplicación para controlar estos formatos.

## <a name="microsoft-spatial-sound-integration-with-audio-renderers"></a>Integración de sonido espacial de Microsoft con representadores de audio

Dado [**que ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) es un receptor de audio que consume datos, un representador de audio tiene varias opciones para interactuar con él y entregarle datos de audio. Hay tres técnicas de integración que se usan habitualmente (y para los títulos que usan middleware de audio, es posible que vea complementos equivalentes disponibles en función de estas opciones):

-   **7.1.4 Panners y mastering voice:** los representadores que ya admiten puntos de conexión 7.1 pueden optar por simplemente agregar compatibilidad con los cuatro canales de altura adicionales que admite el canal estático **ISpatialAudioClient.** Cualquier movimiento panorámico del canal que haya hecho anteriormente (probablemente ya esté aprovechando las coordenadas x,y, z) se puede actualizar para incluir ahora estos canales de alto. Esto a menudo ofrece la menor interrupción en los flujos de trabajo de audio del representador y la aplicación, la señal, el flujo y el control de combinación. En los micrófonos, tenga en cuenta que la combinación de aplicaciones completa se espacializará, por lo que incluso la música estéreo se puede percibir como "externalizada" desde el agente de escucha.
-   Mantener el punto de conexión existente, además de agregar un bus **7.1.4 (y panners):** algunos títulos pueden optar por mantener dos puntos de conexión: su punto de conexión WASAPI estéreo existente (para el contenido "directo a las manos" no diseñado para espacializarse) junto con un canal estático **ISpatialAudioClient** compatible con 7.1.4 (o incluso hasta 8.1.4.4). Por supuesto, la administración de interacciones entre dos mezclas presenta desafíos adicionales para los creadores de contenido, aunque se mantiene la sincronización, ya que las instancias de WASAPI e ISAC activas en un momento dado usan el mismo tamaño de búfer y el mismo reloj para el procesamiento.
-   Usar objetos de sonido dinámicos para determinadas voces o **submezclas:** ofrecer quizás el posicionamiento más detallado o preciso, pero potencialmente crear opacidad de mezcla, esta técnica implica el uso de objetos de sonido dinámicos **ISpatialAudioClient.** Tenga en cuenta que los metadatos más el búfer de audio se entregan al representador, por lo que estos sonidos serán opacos para el resto de la combinación de aplicaciones. Además, dado que hay un número limitado de objetos de sonido dinámicos disponibles, el representador deberá considerar la posibilidad de implementar técnicas de priorización: la selección, la coofiación de sonido, la mezcla con el canal estático, y así sucesivamente. Los juegos han usado con frecuencia esta técnica para sonidos individuales de "héroe", como un juego de fondo que se desplazará por encima del agente de escucha.

Los representadores también pueden mezclar y coincidir entre estos enfoques.

## <a name="microsoft-spatial-sound-runtime-resource-implications"></a>Implicaciones de recursos de Microsoft Spatial Sound Runtime

En Windows y Xbox, el número de voces disponibles varía en función del formato en uso. Los formatos Dolby Atmos admiten 32 objetos activos totales (por lo que si se está utilizando un canal de 7.1.4, pueden estar activos 20 objetos de sonido dinámicos adicionales). Windows Sonic para auriculares admite 128 objetos activos totales, y el canal de efectos de baja frecuencia (LFE) no se cuenta realmente como un objeto ; por lo tanto, cuando se usa un canal de 8.1.4.4, pueden estar activos 112 objetos de sonido dinámicos.

En el caso de las aplicaciones de la Plataforma universal de Windows que se ejecutan en consolas de juegos de Xbox One, la codificación en tiempo real (para Dolby Atmos para el cine en casa, Dolby Atmos for Headphones, DTS Consola:X y Windows Sonic para auriculares) se realiza en hardware sin costo de CPU.

| Formato                       | Max Static Objects (Channel Bed) | Máximo de objetos dinámicos <br> Xbox One | Máximo de objetos dinámicos <br> Windows | Máximo de objetos dinámicos <br> HoloLens 2
|------------------------------|----------------------------------|-------------------------------------------|------------------------------------------|------------------------------------------|
| Dolby Atmos (HDMI)           | 12 (7.1.4)                       | 20                                        | 20                                       | N/D |
| Dolby Atmos (& altavoces integrados)     | 17 (8.1.4.4)                     | 16                                        | 16                                       | N/D |
| Dts- -X (cascos) | 17 (8.1.4.4)        | 16                                        | 32                                      | N/D |
| Windows Sonic para auriculares | 17 (8.1.4.4)        | 15                                        | 112                                      | 31 |


Las aplicaciones también deben tener en cuenta las siguientes implicaciones de recursos:

-   ancho de banda de **Storage/disco:** el contenido lineal preautorizado en 7.1.4 normalmente será mayor que 7.1 contenido lineal (aunque los códecs perceptuales ya suelen aprovechar la correlación del canal para que esto sea mucho menor que el 50 % de canales reales de datos de audio)
-   **Otros costos de procesamiento de señales digitales:** algunos efectos globales anteriores ahora pueden convertirse en instancias por objeto de sonido dinámico. Además, es posible que algunos creadores de contenido quieran actualizar algunos efectos de DSP para admitir canales adicionales o usarlos de forma única.

## <a name="microsoft-spatial-sound-and-sound-spatialization-cues"></a>Indicaciones de espacialización de sonido espacial y sonido de Microsoft

Microsoft Spatial Sound se centra en la simulación de posicionamiento de sonido en una esfera idealizada alrededor del agente de escucha. Windows Sonic para auriculares, DTS Spatial:X y Dolby Atmos implementan la asignación y virtualización del hablante para los auriculares, pero tenga en cuenta que muchos otros aspectos de la simulación espacial sólida, ya implementada normalmente de maneras habilitadas para el creador de contenido, se quedan en los motores existentes. Los creadores de contenido siguen usando las herramientas y los procesos de juego existentes que anteriormente tenían para indicaciones espaciales como Doppler, atenuación y filtrado basados en la distancia, oclusión y agotamiento, y reverberación ambiental.

## <a name="additional-resources"></a>Recursos adicionales

-   [Repositorio de GitHub de ejemplos de Sonido espacial de Microsoft](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio)
-   Dolby ofrece una serie de recursos de soporte técnico relacionados con Dolby Atmos y Dolby Access aplicación en <https://developer.dolby.com> .

## <a name="spatial-sound-interfaces"></a>Interfaces de sonido espacial



| Interfaz                                                                              | Descripción                                                                                                                    |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)                                     | Permite a un cliente crear secuencias de audio que emiten audio desde una posición en espacio 3D.                                          |
| [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)                                     | Representa un objeto que proporciona datos de audio que se representarán desde una posición en el espacio 3D, en relación con el usuario.                |
| [**ISpatialAudioObjectRenderStream**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)             | Proporciona métodos para controlar una secuencia de representación de objeto de audio espacial, incluido el inicio, la detención y el restablecimiento de la secuencia. |
| [**ISpatialAudioObjectRenderStreamNotify**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstreamnotify) | Proporciona notificaciones para que los clientes de audio espacial respondan a los cambios en el estado de un ISpatialAudioObjectRenderStream.     |



 

> [!Note]  
> Al usar las interfaces [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) en un título del Kit de desarrollo de Xbox One (XDK), primero debe llamar a **EnableSpatialAudio** antes de llamar a [**IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) o [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). Si no lo hace, se devolverá un \_ error E NOINTERFACE de la llamada a Activate. **EnableSpatialAudio** solo está disponible para los títulos de XDK y no es necesario llamar a para las aplicaciones de plataforma universal de Windows que se ejecutan en Xbox One ni para dispositivos que no Xbox One.

 

## <a name="spatial-sound-structures"></a>Estructuras de sonido espacial



| Estructura                                                                                                 | Descripción                                                                  |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) | Representa los parámetros de activación para una secuencia de representación de audio espacial.          |
| [**SpatialAudioClientActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioclientactivationparams)                          | Representa parámetros de activación opcionales para una secuencia de representación de audio espacial. |



 

## <a name="spatial-sound-enumerations"></a>Enumeraciones de sonido espacial



| Enumeración                                | Descripción                                   |
|--------------------------------------------|-----------------------------------------------|
| [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) | Especifica el tipo de un objeto ISpatialAudioObject. |



 

 

 



