---
description: Guía del desarrollador para la versión redistribuible de XAudio 2.9
ms.assetid: ''
title: Guía del desarrollador para la versión redistribuible de XAudio 2.9
ms.topic: article
ms.date: 10/17/2019
ms.openlocfilehash: a87c2dc44179f2c189270dfa91d2cf2696ea98a7
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104003470"
---
# <a name="developer-guide-for-redistributable-version-of-xaudio-29"></a>Guía del desarrollador para la versión redistribuible de XAudio 2.9

Hay disponible una versión de XAudio 2,9 como [paquete NuGet](/nuget/what-is-nuget). Los desarrolladores pueden redistribuir esta versión de XAudio 2,9 con sus aplicaciones. Esto permite que una aplicación use XAudio 2,9 en versiones anteriores de Windows que no incluyen XAudio 2,9 como parte de la imagen de sistema operativo. El uso de este redistribuible es preferible que redistribuir XAudio 2,7 desde el SDK de DirectX, ya que XAudio 2,7 no se ha actualizado desde 2010.

## <a name="supported-platforms"></a>Plataformas compatibles

El paquete NuGet XAudio 2,9 (*Microsoft. XAudio2. Redist. \* . nupkg*) incluye una versión de 32 bits y una versión de 64 bits de un archivo DLL que implementa la API de XAudio 2,9. El archivo DLL se denomina XAUDIO2 \_9REDIST.DLL. Este archivo DLL funcionará en Windows 7 SP1, Windows 8, Windows 8.1 y Windows 10.

Cuando el archivo DLL se usa en un sistema de Windows 10, comprueba el número de versión del \_9.DLL de XAUDIO2 que forma parte del sistema operativo y, si el sistema operativo es más reciente, delegará todas las llamadas de API a XAUDIO2 \_9.DLL en el sistema operativo. Esto garantiza que las aplicaciones siempre usen la versión más reciente de XAudio 2,9 que está disponible en la plataforma actual.

La DLL no está pensada para Xbox One. Si se usa en Xbox One, el archivo DLL siempre delegará todas las llamadas de API a XAUDIO2 \_9.DLL en el sistema operativo Xbox One.

El archivo DLL no está diseñado para aplicaciones UWP. Las aplicaciones UWP deben usar el \_9.DLL de XAUDIO2 que forma parte del sistema operativo.

## <a name="installing-the-nuget-package"></a>Instalación del paquete de NuGet

La forma más fácil de instalar el paquete NuGet es usar el [Administrador de paquetes Nuget](/nuget/consume-packages/install-use-packages-visual-studio) en Microsoft Visual Studio. Si lo hace, el archivo de proyecto de Visual Studio se actualizará automáticamente para incluir *Microsoft. XAudio2. Redist. targets*. El archivo *. targets* agrega la carpeta include con los archivos de encabezado de XAudio2 a la colección de rutas de acceso de inclusión del proyecto. El archivo *. targets* también realizará su. DLL o. Vínculo EXE con XAUDIO2REDIST. LIB y XAPOBASEREDIST. Obj.

La biblioteca XAPOBASEREDIST. LIB solo es necesario si tiene previsto impement un objeto de procesamiento de XAudio personalizado (XAPO) y puede quitarlo de *Microsoft. XAudio2. Redist. targets* si no se usa.

También puede usar otras herramientas para extraer el contenido del paquete de NuGet, o incluso cambiar el nombre de la extensión de archivo a. zip y extraer los archivos con cualquier herramienta de extractor de ZIP.

## <a name="compiling-your-app"></a>Compilar la aplicación

### <a name="choosing-which-headers-to-include"></a>Elección de los encabezados que se van a incluir

El paquete NuGet de XAudio 2,9 incluye los mismos archivos de encabezado de XAudio2 que se incluyen en el SDK de Windows 10. Sin embargo, los archivos de encabezado se han realizado algunos ajustes para asegurarse de que puede usarlos mientras se dirigen explícitamente a todas las [plataformas compatibles](#supported-platforms), incluidas las versiones anteriores de Windows.

Si [instala el paquete de Nuget](#installing-the-nuget-package) con el administrador de paquetes de nuget en Microsoft Visual Studio, la ruta de acceso a los archivos de encabezado se coloca delante de la ruta de acceso a los archivos de encabezado de Windows SDK. Esto significa que si el código del proyecto incluye XAUDIO2. H, se recogerá el encabezado multiplataforma del paquete NuGet. Este suele ser el comportamiento deseado.

Debe tener cuidado si agregar la ruta de acceso a los encabezados de inclusión manualmente en el proyecto, ya que si se especifican en el orden equivocado, pueden producirse las XAUDIO2 específicas de la versión del sistema operativo [. H](/windows/win32/api/xaudio2/) que se va a incluir en el Windows SDK, en lugar de la versión multiplataforma de XAUDIO2. H.

Para que la inclusión de encabezados sea menos propensa a errores, el paquete NuGet contiene una versión de cada encabezado con "Redist" anexado. Por ejemplo, además de XAUDIO2. H, el paquete NuGet también incluye XAUDIO2REDIST. H. Si lo prefiere, el código puede incluir XAUDIO2REDIST directamente. H para eliminar cualquier ambigüedad sobre el archivo de encabezado que se está usando. Al incluir-Redist. Versión H de un archivo de encabezado, el orden en el que se enumeran los directorios de archivos de inclusión en el archivo del proyecto no importa.

Tenga en cuenta que si la aplicación también se compila para Xbox One, debe seguir incluyendo XAUDIO2. H al compilar para Xbox One, como algunas API específicas de Xbox One se excluyen de XAUDIO2REDIST. H. Este paquete de NuGet no está diseñado para Xbox One.

### <a name="loading-the-dll"></a>Cargar el archivo DLL

Se recomienda vincular la aplicación con XAUDIO2REDIST. LIB e instalar XAUDIO2 \_9REDIST.DLL en la misma carpeta que el ejecutable de la aplicación. Esto hará que se \_ carguen las9REDIST.DLL de XAUDIO2 en cuanto se inicie el archivo ejecutable. Sin embargo, si lo prefiere, puede usar [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw) y [**GETPROCADDRESS**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para cargar XAUDIO2 \_9REDIST.DLL a petición. Esta es una buena solución si la aplicación no siempre necesita usar las API de XAudio2. Pero si lo hace, debe mantener las9REDIST.DLL de XAUDIO2 \_ cargadas hasta que se cierre la aplicación, ya que al intentar descargar el archivo dll se puede producir un bloqueo si un subproceso en segundo plano sigue ejecutando código en el archivo dll.

A diferencia de la versión anterior de XAudio 2,7, no es posible usar CoCreateInstance para cargar el archivo DLL.

### <a name="verifying-the-dll-signature"></a>Comprobando la firma de DLL

El \_ archivo binario9REDIST.DLL de XAUDIO2 está firmado por Microsoft con una firma Sha-2. Cualquier código que intente validar la firma, por ejemplo, los módulos de protección contra los juegos, debe admitir SHA-2. Tenga en cuenta que Windows 7 SP1 no admitía originalmente SHA-2 y requiere una actualización para agregar esa funcionalidad. La actualización está disponible como [KB4474419](https://support.microsoft.com/help/4474419/sha-2-code-signing-support-update).

## <a name="testing"></a>Prueba

### <a name="spatial-sound-in-newer-versions-of-windows-10"></a>Sonido espacial en las versiones más recientes de Windows 10

A partir de la actualización 10 1903 de Windows, XAudio 2,9 utiliza automáticamente el [sonido envolvente virtual](#spatial-sound-and-virtual-surround), si se cumplen ciertas condiciones. Se recomienda probar el juego que genera sonido multicanal en Windows 10 1903 (o posterior) para comprobar que el juego suena según lo previsto.

#### <a name="enabling-spatial-sound"></a>Habilitar el sonido espacial

Para habilitar un formato de sonido espacial, el usuario puede hacer clic con el botón derecho en el icono de altavoz en la bandeja del sistema de Windows. 

XAudio 2,9 solo usará el formato de sonido espacial seleccionado del usuario si el proceso que usa la API de XAudio2 se reconoce como un juego en la barra de juegos de Windows. Durante el desarrollo, es posible que la barra de juego aún no reconozca el proceso como un juego. Para cambiar esta configuración, use el corte de teclado Win + G para abrir la barra de juego mientras el juego se está ejecutando. Después, haga clic en el icono "configuración" y active la casilla que dice "Recuerde que se trata de un juego".

#### <a name="opting-out-from-spatial-sound"></a>No participar en el sonido espacial

Hay una manera de dejar de hacer que XAudio2 use el codificador de sonido espacial especificando ciertos valores para el parámetro [**AUDIO_STREAM_CATEGORY**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) en [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice). 

El sonido espacial está habilitado para estas categorías:

* AudioCategory_ForegroundOnlyMedia
* AudioCategory_GameEffects
* AudioCategory_GameMedia
* AudioCategory_Movie
* AudioCategory_Media

El sonido espacial no está habilitado si se especifica alguna de las siguientes categorías:

* AudioCategory_Other
* AudioCategory_Communications
* AudioCategory_Alerts
* AudioCategory_SoundEffects
* AudioCategory_GameChat
* AudioCategory_Speech

### <a name="error-handling"></a>Control de errores

Es importante probar que el juego puede controlar un cambio en el dispositivo de audio, por ejemplo, cuando los auriculares están enchufados o desconectados. Esto se debe probar con auriculares que solo admiten la velocidad de muestreo de 44,1 kHz. Muchos auriculares USB de low-end y auriculares Bluetooth solo admiten 44,1 kHz. La transición entre la velocidad de muestreo de 48 kHz y la velocidad de muestreo de 44,1 kHz puede producir un error aunque se use la característica de [punto de conexión de audio virtual](#virtual-audio-endpoint) . El error no se producirá si los auriculares también admiten 48 kHz. Tenga en cuenta que la característica de punto de conexión de audio virtual no está disponible en Windows 7 SP1.

El código de error devuelto por XAudio 2,9 cuando no se puede recuperar automáticamente de un cambio en el punto de conexión de audio es el [ \_ dispositivo XAUDIO2 E \_ \_ invalidado](xaudio2-error-codes.md). Sin embargo, se recomienda que las aplicaciones no codifiquen de forma rígida una dependencia del código de error que tenga un valor específico.

Para recibir una notificación del error, la aplicación debe implementar la interfaz [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) y proporcionar un puntero a esa interfaz mediante la invocación del método [**IXAudio2:: RegisterForCallbacks**](xaudio2-callbacks.md) . La API de XAudio2 invocará la implementación de la aplicación de [**IXAudio2EngineCallback:: OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror) si se produce un error durante la reproducción.

Tenga en cuenta que [**IXAudio2EngineCallback:: OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror) no se invoca necesariamente si la canalización de audio está en pausa. Por ejemplo, si el usuario minimiza la aplicación o la aplicación se suspende por cualquier motivo, la reproducción de audio podría estar en pausa. Si el cambio en el dispositivo de audio ocurre durante este tiempo, el error solo se devuelve cuando la aplicación invoca [**IXAudio2:: StartEngine**](/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-startengine) o invoca [**IXAudio2SourceVoice:: Start**](/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start). Si la reproducción se puede pausar con la aplicación, debe probar a cambiar el dispositivo de audio mientras se pausa la reproducción, para comprobar que la aplicación todavía puede recuperarse de esta situación.

## <a name="xaudio-29-api-differences-compared-to-xaudio-27"></a>Diferencias de la API de XAudio 2,9 en comparación con XAudio 2,7

En esta sección se proporciona un resumen de algunas de las diferencias de API entre XAudio 2,7 y la versión redistribuible de XAudio 2,9.

### <a name="supported-formats"></a>Formatos compatibles

XAudio 2,9 admite estos formatos de entrada en PC:

* PCM lineal de 16 bits
* PCM lineal de 32 bits Float
* ADPCM de 16 bits
* xWMA

El formato XMA solo se admite en Xbox One.

### <a name="preferred-cpu-core"></a>Núcleo de CPU preferido

Es posible especificar qué núcleo de CPU XAudio 2,9 debe usar para su subproceso de procesamiento de audio. Sin embargo, suele ser preferible dejar que XAudio 2,9 Elija este valor por sí solo. Esto se hace estableciendo el parámetro **XAudio2Processor** en la llamada a [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) a XAUDIO2 \_ usar el \_ \_ procesador predeterminado. 

XAudio 2,9 elegirá un núcleo de CPU diferente en la Xbox uno que en PC. El método IXAudio2Extension:: GetProcessor se puede usar para determinar qué núcleo de CPU ha elegido.

### <a name="virtual-audio-endpoint"></a>Extremo de audio virtual

XAudio 2,9 usará un punto de conexión de audio virtual de forma predeterminada cuando se ejecute en Windows 8 o posterior. Esto significa que si el punto de conexión de audio predeterminado cambia mientras se usa XAudio 2,9, intentará cambiar automáticamente al nuevo punto de conexión de audio. Un ejemplo de Cuándo esto puede ocurrir cuando el punto de conexión de audio predeterminado es un par de auriculares conectados a través de USB y, a continuación, el usuario desconecta los auriculares. Esto hará que los altavoces sean el nuevo punto de conexión de audio predeterminado.

Si la aplicación especifica un formato de audio específico al invocar [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice), es posible que XAudio 2,9 no pueda realizar este modificador. Por ejemplo, si la aplicación especificó que la voz de mastering debe usar una velocidad de muestreo de 48 kHz y el dispositivo de audio nuevo solo admite 44,1 kHz, se producirá un error en el conmutador automático y XAudio 2,9 informará del error [ \_ \_ \_ invalidado del dispositivo XAUDIO2 e](xaudio2-error-codes.md) .

Es posible que la aplicación no pueda usar el punto de conexión de audio virtual pasando la marca [**XAUDIO2 \_ no \_ virtual \_ audio \_ Client**](xaudio2-boundary-values-and-flags.md) a [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).

Los puntos de conexión de audio virtual no están disponibles en Windows 7 SP1. La marca **XAUDIO2 \_ no \_ virtual \_ audio \_ Client** no tiene ningún efecto en Windows 7 SP1.

### <a name="audio-categories"></a>Categorías de audio

La aplicación debe especificar una categoría para su flujo de audio. Esto se hace proporcionando un valor de la enumeración AudioCategory al invocar el método [**IXAudio2:: CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) . Por ejemplo, AudioCategory_GameEffects. La categoría audio puede afectar a la forma en que Windows procesa el sonido o cómo representa la secuencia de audio en el panel de control del volumen. La categoría audio también afecta a si el [sonido envolvente virtual](#spatial-sound-and-virtual-surround) se habilita automáticamente.

### <a name="duration-of-audio-processing-quantum"></a>Duración del Quantum de procesamiento de audio

En la mayoría de los equipos, XAudio 2,9 procesa el audio en fragmentos de 10 milisegundos. Esto se denomina Quantum de procesamiento. Sin embargo, la duración de este Quantum puede ser diferente de 10 milisegundos en el hardware. Las aplicaciones que necesitan conocer el cuanto exacto pueden invocar el método IXAudio2Extension:: GetProcessingQuantum para recuperar el valor.

### <a name="spatial-sound-and-virtual-surround"></a>Sonido espacial y envolvente virtual

A partir de la actualización 10 1903 de Windows, XAudio 2,9 utiliza automáticamente el sonido envolvente virtual, si se cumplen ciertas condiciones. Se recomienda probar el juego que genera sonido multicanal en Windows 10 1903 (o posterior) para comprobar que el juego suena según lo previsto. Consulte la sección [prueba del sonido espacial](#spatial-sound-in-newer-versions-of-windows-10) para obtener una explicación sobre cómo probar esta característica.

Normalmente, XAudio 2,9 realiza un doblado de cualquier audio multicanal para que coincida con el número "físico" de canales de audio admitidos por el punto de conexión de audio. Por ejemplo, si el juego proporciona un origen de audio de canal 7,1, pero el sonido se reproduce en auriculares, XAudio 2,9 repliega el audio de canal 7,1 en estéreo mediante una matriz de subconjuntos estándar del sector. Si el equipo está conectado a un punto de conexión de audio HDMI, el audio del canal 7,1 se transmitirá tal cual a través de la conexión HDMI.

Windows 10 agrega compatibilidad con el audio espacial mediante un codificador centralizado que codifica el audio en un formato de [sonido espacial](../coreaudio/spatial-sound.md) seleccionado por el usuario. Windows 10 incluye un formato de sonido espacial denominado Windows Sonic. Otros formatos, como Dolby Atmos para auriculares, se pueden descargar desde el Microsoft Store. Algunos de los formatos de sonido espacial, como Windows Sonic y Dolby Atmos para auriculares, están diseñados para usarse en extremos de audio estéreo. Estos formatos repliegan el sonido envolvente en estéreo mediante algoritmos de propiedad que logran un efecto de sonido envolvente "virtual". En otras palabras, el agente de escucha puede percibir un sonido que aparece desde diferentes posiciones en el espacio 3D, incluso aunque solo contenga auriculares o mientras escucha en un solo par de altavoces estéreo.

Se pueden lograr efectos similares mediante las API de [X3DAudio](x3daudio.md) que se incluyen con XAudio 2,9. La principal diferencia es que X3DAudio requiere que el desarrollador de la aplicación programe explícitamente el audio 3D, mientras que el sonido envolvente virtual se aplica automáticamente a cualquier origen de sonido basado en canal de tradional.

En Windows 10 1903 y versiones más recientes, los juegos que usan XAudio 2,9 usarán el formato de sonido espacial para todo el sistema que el usuario haya habilitado en el punto de conexión de audio, si existe. Esto significa que XAudio 2,9 no realizará el plegado habitual del sonido envolvente en estéreo. En su lugar, la señal de sonido envolvente se entregará al codificador de sonido espacial (por ejemplo, Windows Sonic) para lograr un efecto de sonido envolvente virtual.

### <a name="createhrtfapo"></a>CreateHrtfApo

La función [**CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo) solo está disponible en Windows 10. No se implementa en XAudio 2,9 Redistributable.
