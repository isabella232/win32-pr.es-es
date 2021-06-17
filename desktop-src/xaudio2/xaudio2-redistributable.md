---
description: Guía del desarrollador para la versión redistribuible de XAudio 2.9
ms.assetid: ''
title: Guía del desarrollador para la versión redistribuible de XAudio 2.9
ms.topic: article
ms.date: 10/17/2019
ms.openlocfilehash: a73ebd01d599446dc96e1e6735d8af572203a23b
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262597"
---
# <a name="developer-guide-for-redistributable-version-of-xaudio-29"></a>Guía del desarrollador para la versión redistribuible de XAudio 2.9

Una versión de XAudio 2.9 está disponible como un [paquete NuGet](/nuget/what-is-nuget). Los desarrolladores pueden redistribuir esta versión de XAudio 2.9 con sus aplicaciones. Esto permite que una aplicación use XAudio 2.9 en versiones anteriores de Windows que no incluyan XAudio 2.9 como parte de la imagen de sistema operativo. El uso de esta redistribuible es preferible a la redistribución de XAudio 2.7 desde el SDK de DirectX, ya que XAudio 2.7 no se ha actualizado desde 2010.

Asegúrese de visitar la página de [aterrizaje de DirectX](https://devblogs.microsoft.com/directx/landing-page/) para obtener más recursos para los desarrolladores de DirectX.

## <a name="supported-platforms"></a>Plataformas compatibles

El paquete NuGet XAudio 2.9 (*Microsoft.XAudio2.Redist. \* . nupkg*) incluye una versión de 32 bits y una versión de 64 bits de un archivo DLL que implementa la API de XAudio 2.9. El archivo DLL se denomina XAUDIO2 \_9REDIST.DLL. Este archivo DLL funcionará en Windows 7 SP1, Windows 8, Windows 8.1 y Windows 10.

Cuando el archivo DLL se usa en un sistema Windows 10, comprueba el número de versión del9.DLL XAUDIO2 que forma parte del sistema operativo y, si el sistema operativo es más reciente, delegará todas las llamadas API a \_ XAUDIO29.DLL en \_ el sistema operativo. Esto garantiza que las aplicaciones siempre usen la versión más reciente de XAudio 2.9 que está disponible en la plataforma actual.

El archivo DLL no está pensado para Xbox One. Si se usa en Xbox One, el archivo DLL siempre delegará todas las llamadas API a XAUDIO2 \_9.DLL en el Xbox One operativo.

El archivo DLL no está pensado para aplicaciones para UWP. Las aplicaciones para UWP deben usar el \_9.DLL XAUDIO2 que forma parte del sistema operativo.

## <a name="installing-the-nuget-package"></a>Instalación del paquete de NuGet

La manera más fácil de instalar el paquete NuGet es usar el Administrador de paquetes [NuGet](/nuget/consume-packages/install-use-packages-visual-studio) en Microsoft Visual Studio. Si lo hace, el archivo Visual Studio proyecto se actualizará automáticamente para incluir *Microsoft.XAudio2.Redist.targets.* El *archivo .targets* agrega la carpeta Include con los archivos de encabezado de XAudio2 a la colección de rutas de acceso de include del proyecto. El *archivo .targets* también hará que el .DLL o .EXE vínculo con XAUDIO2REDIST. LIB y XAPOBASEREDIST. Lib.

Biblioteca XAPOBASEREDIST. LIB solo es necesario si tiene previsto acotar un objeto de procesamiento XAudio (XAPO) personalizado y puede quitarlo de *Microsoft.XAudio2.Redist.targets* si no se usa.

También puede usar otras herramientas para extraer el contenido del paquete NuGet o incluso cambiar el nombre de la extensión de archivo a .zip y extraer los archivos con cualquier herramienta extractora ZIP.

> También hay un puerto ``xaudio2redist`` disponible para [vc++ Administrador de paquetes](https://github.com/microsoft/vcpkg).

## <a name="compiling-your-app"></a>Compilación de la aplicación

### <a name="choosing-which-headers-to-include"></a>Elección de los encabezados que se incluirán

El paquete NuGet XAudio 2.9 incluye los mismos archivos de encabezado XAudio2 que se incluyen en Windows 10 SDK. Sin embargo, los archivos de encabezado han tenido algunos ajustes para asegurarse de que puede usarlos al tener como destino explícitamente todas las plataformas [compatibles,](#supported-platforms)incluidas las versiones anteriores de Windows.

Si instala el paquete [NuGet](#installing-the-nuget-package) mediante el Administrador de paquetes NuGet en Microsoft Visual Studio, la ruta de acceso a los archivos de encabezado se coloca delante de la ruta de acceso a los archivos de encabezado Windows SDK encabezado. Esto significa que si el código del proyecto incluye XAUDIO2. Encabezado H, recogerá el encabezado multiplataforma del paquete NuGet. Este suele ser el comportamiento deseado.

Debe tener cuidado si agregar manualmente la ruta de acceso a los encabezados de include al proyecto, ya que especificarlos en el orden incorrecto puede provocar el XAUDIO2 específico de la [versión del sistema operativo. H](/windows/win32/api/xaudio2/) que se va a incluir desde Windows SDK, en lugar de la versión multiplataforma de XAUDIO2.H.

Para que la inclusión de encabezados sea menos propensa a errores, el paquete NuGet contiene una versión de cada encabezado con "REDIST" anexado. Por ejemplo, además de XAUDIO2. H, el paquete NuGet también incluye XAUDIO2REDIST.H. Si lo prefiere, el código puede incluir directamente XAUDIO2REDIST. H para eliminar cualquier ambigüedad sobre qué archivo de encabezado se está utilizando. Al incluir -REDIST. La versión H de un archivo de encabezado, el orden en el que los directorios de archivo de incluyen se enumeran en el archivo de proyecto no importa.

Tenga en cuenta que si la aplicación también se compila para Xbox One, debe seguir incluyendo XAUDIO2. H al compilar para Xbox One, ya que algunas API específicas Xbox One se excluyen de XAUDIO2REDIST.H. Este paquete NuGet no está pensado para Xbox One.

### <a name="loading-the-dll"></a>Carga del archivo DLL

Se recomienda vincular la aplicación con XAUDIO2REDIST. LIB e instale XAUDIO2 \_9REDIST.DLL en la misma carpeta que el ejecutable de la aplicación. Esto hará que el9REDIST.DLL XAUDIO2 se cargue en cuanto \_ se inicia el archivo ejecutable. Sin embargo, si lo prefiere, puede usar [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para cargar XAUDIO2 \_9REDIST.DLL a petición. Esta es una buena solución si la aplicación no siempre necesita usar las API de XAudio2. Pero si lo hace, debe mantener el9REDIST.DLL XAUDIO2 cargado hasta que se cierre la aplicación, ya que intentar descargar el archivo DLL puede provocar un bloqueo si un subproceso en segundo plano sigue ejecutando código en el \_ archivo DLL.

A diferencia de la versión anterior de XAudio 2.7, no es posible usar CoCreateInstance para cargar el archivo DLL.

### <a name="verifying-the-dll-signature"></a>Comprobación de la firma del archivo DLL

El archivo binario9REDIST.DLL XAUDIO2 \_ está firmado por Microsoft mediante una firma SHA-2. Cualquier código que intente validar la firma, por ejemplo, módulos anti-cheat para juegos, debe admitir SHA-2. Tenga en cuenta que Windows 7 SP1 no era compatible originalmente con SHA-2 y requiere una actualización para agregar esa funcionalidad. La actualización está disponible como [KB4474419](https://support.microsoft.com/help/4474419/sha-2-code-signing-support-update).

## <a name="testing"></a>Prueba

### <a name="spatial-sound-in-newer-versions-of-windows-10"></a>Sonido espacial en versiones más recientes de Windows 10

A partir de la Windows 10 1903, XAudio 2.9 usa automáticamente el sonido [envolvente virtual](#spatial-sound-and-virtual-surround), si se cumplen ciertas condiciones. Se recomienda probar juegos que generen sonido multicanal en Windows 10 1903 (o posterior) para comprobar que el juego suena según lo previsto.

#### <a name="enabling-spatial-sound"></a>Habilitación del sonido espacial

El usuario puede habilitar un formato de sonido espacial haciendo clic con el botón derecho en el icono del altavoz en la bandeja del sistema de Windows. 

XAudio 2.9 solo usará el formato de sonido espacial seleccionado del usuario si windows reconoce el proceso que usa la API XAudio2 como un Game Bar juego. Durante el desarrollo, es posible que el proceso aún no se reconozca como un juego por parte del Game Bar. Para cambiar esto, use el teclado Win+G abreviado para abrir el Game Bar mientras se ejecuta el juego. A continuación, haga clic en el icono "Configuración" y active la casilla que dice "Recuerde que se trata de un juego".

#### <a name="opting-out-from-spatial-sound"></a>No participar en el sonido espacial

Hay una manera de rechazar que XAudio2 use el codificador de sonido espacial especificando determinados valores para el parámetro [**AUDIO_STREAM_CATEGORY**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) en [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice). 

El sonido espacial está habilitado para estas categorías:

* AudioCategory_ForegroundOnlyMedia
* AudioCategory_GameEffects
* AudioCategory_GameMedia
* AudioCategory_Movie
* AudioCategory_Media

El sonido espacial no está habilitado si se especifica alguna de las categorías siguientes:

* AudioCategory_Other
* AudioCategory_Communications
* AudioCategory_Alerts
* AudioCategory_SoundEffects
* AudioCategory_GameChat
* AudioCategory_Speech

### <a name="error-handling"></a>Control de errores

Es importante probar que el juego puede controlar un cambio en el dispositivo de audio, por ejemplo, cuando los cascos están conectados o desconectados. Esto debe probarse con micrófonos que solo admiten una frecuencia de muestreo de 44,1 kHz. Muchos micrófonos USB de gama baja y cascos Bluetooth solo admiten 44,1 kHz. La transición entre la frecuencia de muestreo de 48 kHz y la frecuencia de muestreo de 44,1 kHz puede producir un error incluso cuando se usa la característica punto de conexión [de audio virtual.](#virtual-audio-endpoint) El error no se producirá si los cascos también admiten 48 kHz. Tenga en cuenta que la característica punto de conexión de audio virtual no está disponible en Windows 7 SP1.

El código de error devuelto por XAudio 2.9 cuando no se puede recuperar automáticamente de un cambio en el punto de conexión de audio es [XAUDIO2 \_ E \_ DEVICE \_ INVALIDATED](xaudio2-error-codes.md). Sin embargo, se recomienda que las aplicaciones no codimente una dependencia en el código de error que tenga un valor específico.

Para recibir una notificación del error, la aplicación debe implementar la interfaz [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) y proporcionar un puntero a esa interfaz invocando el método [**IXAudio2::RegisterForCallbacks.**](xaudio2-callbacks.md) La API de XAudio2 invocará la implementación de [**la aplicación de IXAudio2EngineCallback::OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror) si se produce un error durante la reproducción.

Tenga en [**cuenta que IXAudio2EngineCallback::OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror) no se invoca necesariamente si la canalización de audio está en pausa. Por ejemplo, si el usuario minimiza la aplicación o la aplicación se suspende por cualquier motivo, la reproducción de audio podría pausarse. Si el cambio en el dispositivo de audio se produce durante este tiempo, el error solo se devuelve cuando la aplicación invoca [**IXAudio2::StartEngine**](/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-startengine) o invoca [**IXAudio2SourceVoice::Start**](/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start). Si la reproducción se puede pausar con la aplicación, debe probar el cambio del dispositivo de audio mientras la reproducción está en pausa, para comprobar que la aplicación todavía puede recuperarse de esta situación.

## <a name="xaudio-29-api-differences-compared-to-xaudio-27"></a>Diferencias de API de XAudio 2.9 en comparación con XAudio 2.7

En esta sección se proporciona un resumen de algunas de las diferencias de API entre XAudio 2.7 y la versión redistribuible de XAudio 2.9.

### <a name="supported-formats"></a>Formatos compatibles

XAudio 2.9 admite estos formatos de entrada en pc:

* PCM lineal de 16 bits
* PCM flotante lineal de 32 bits
* ADPCM de 16 bits
* xWMA

El formato XMA solo se admite en Xbox One.

### <a name="preferred-cpu-core"></a>Núcleo de CPU preferido

Es posible especificar qué núcleo de CPU XAudio 2.9 debe usar para su subproceso de procesamiento de audio. Sin embargo, normalmente se prefiere dejar que XAudio 2.9 elija este valor por sí mismo. Para ello, se establece el parámetro **XAudio2Processor** en la llamada a [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) en XAUDIO2 \_ USE DEFAULT \_ \_ PROCESSOR. 

XAudio 2.9 elegirá un núcleo de CPU diferente en Xbox One que en pc. El método IXAudio2Extension::GetProcessor se puede usar para determinar qué núcleo de CPU ha elegido XAudio2.

### <a name="virtual-audio-endpoint"></a>Punto de conexión de audio virtual

XAudio 2.9 usará un punto de conexión de audio virtual de forma predeterminada, cuando se ejecute Windows 8 o posterior. Esto significa que si el punto de conexión de audio predeterminado cambia mientras se usa XAudio 2.9, intentará cambiar automáticamente al nuevo punto de conexión de audio. Un ejemplo de cuándo puede ocurrir cuando el punto de conexión de audio predeterminado es un par de cascos conectados a través de USB y, a continuación, el usuario desconecta los cascos. Esto hará que los altavoces sean el nuevo punto de conexión de audio predeterminado.

Si la aplicación especifica un formato de audio específico al invocar [**IXAudio2::CreateMasteringVoice,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)puede que XAudio 2.9 no pueda realizar este modificador. Por ejemplo, si la aplicación especificó que Mastering Voice debe usar una frecuencia de muestreo de 48 kHz y el nuevo dispositivo de audio solo admite 44,1 kHz, se producirá un error en el conmutador automático y XAudio 2.9 notificará el error [XAUDIO2 \_ E \_ DEVICE \_ INVALIDATED.](xaudio2-error-codes.md)

Es posible que la aplicación no pueda optar por no usar el punto de conexión de audio virtual pasando la marca [**XAUDIO2 \_ NO VIRTUAL AUDIO \_ \_ \_ CLIENT**](xaudio2-boundary-values-and-flags.md) a [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).

Los puntos de conexión de audio virtual no están disponibles en Windows 7 SP1. La **marca \_ XAUDIO2 NO VIRTUAL AUDIO \_ \_ \_ CLIENT** no tiene ningún efecto en Windows 7 SP1.

### <a name="audio-categories"></a>Categorías de audio

La aplicación debe especificar una categoría para su secuencia de audio. Para ello, se proporciona un valor de la enumeración AudioCategory al invocar el método [**IXAudio2::CreateMasteringVoice.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) Por ejemplo, AudioCategory_GameEffects. La categoría audio puede afectar a cómo Windows procesa el sonido o cómo representa la secuencia de audio en el panel de control de volumen. La categoría de audio también afecta si el [sonido envolvente virtual](#spatial-sound-and-virtual-surround) está habilitado automáticamente.

### <a name="duration-of-audio-processing-quantum"></a>Duración del proceso de audio cuántico

En la mayoría de los equipos, XAudio 2.9 procesa el audio en fragmentos de 10 milisegundos. Esto se denomina el cuántico de procesamiento. Sin embargo, la duración de este cuántico puede ser diferente de 10 milisegundos en algún hardware. Las aplicaciones que necesitan conocer el cuántico exacto pueden invocar el método IXAudio2Extension::GetProcessingQuantum para recuperar el valor.

### <a name="spatial-sound-and-virtual-surround"></a>Sonido espacial y envolvente virtual

A partir de la Windows 10 1903, XAudio 2.9 usa automáticamente el sonido envolvente virtual, si se cumplen ciertas condiciones. Se recomienda probar juegos que generen sonido multicanal en Windows 10 1903 (o posterior) para comprobar que el juego suena según lo previsto. Consulte la [sección de pruebas de sonido](#spatial-sound-in-newer-versions-of-windows-10) espacial para obtener una explicación sobre cómo probar esta característica.

Normalmente, XAudio 2.9 realiza un plegado de cualquier audio multicanal para que coincida con el número "físico" de canales de audio admitidos por el punto de conexión de audio. Por ejemplo, si el juego proporciona un origen de audio de canal 7.1, pero el sonido se reproduce en los cascos, XAudio 2.9 doblerá el audio del canal 7.1 en estéreo, mediante una matriz de plegado estándar del sector. Si el equipo está conectado a un punto de conexión de audio HDMI, el audio del canal 7.1 se transmitirá tal como está a través de la conexión HDMI.

Windows 10 agrega compatibilidad con audio espacial, mediante un codificador centralizado que codifica el audio en un formato de sonido [espacial seleccionado por el](../coreaudio/spatial-sound.md) usuario. Windows 10 incluye un formato de sonido espacial denominado Windows Sonic. Otros formatos, como Dolby Atmos for Headphones, se pueden descargar desde el Microsoft Store. Algunos de los formatos de sonido espacial, como Windows Sonic y Dolby Atmos for Headphones, están diseñados para usarse en puntos de conexión de audio estéreo. Estos formatos se plegan hacia abajo alrededor del sonido en estéreo mediante algoritmos propietarios que logran un efecto de sonido envolvente "virtual". En otras palabras, el agente de escucha puede percibir el sonido que aparece desde diferentes posiciones en el espacio 3D, incluso mientras solo lleva cascos o mientras escucha en un solo par de altavoces estéreo.

Se pueden lograr efectos similares mediante las [API de X3DAudio](x3daudio.md) que se incluyen con XAudio 2.9. La principal diferencia es que X3DAudio requiere que el desarrollador de la aplicación programe explícitamente el audio 3D, mientras que el sonido envolvente virtual se aplica automáticamente a cualquier origen de sonido basado en canal transional.

En Windows 10 1903 y versiones más recientes, los juegos que usan XAudio 2.9 usarán el formato de sonido espacial de todo el sistema que el usuario ha habilitado en el punto de conexión de audio, si lo hay. Esto significa que XAudio 2.9 no realizará el plegado habitual del sonido envolvente a estéreo. En su lugar, la señal de sonido envolvente se entregará al codificador de sonido espacial (por ejemplo, Windows Sonic) para lograr un efecto de sonido envolvente virtual.

### <a name="createhrtfapo"></a>CreateHrtfApo

La [**función CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo) solo está disponible en Windows 10. No se implementa en la versión redistribuible de XAudio 2.9.
