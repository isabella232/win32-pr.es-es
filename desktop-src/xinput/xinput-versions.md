---
title: Versiones de XInput
description: XInput es una API multiplataforma que se ha enviado para su uso en Xbox y Windows.
ms.assetid: e89a6c81-f170-4385-f942-3606f9747244
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3d3624b8ea12872058ed1d874aa242a5806aec2
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "103914014"
---
# <a name="xinput-versions"></a>Versiones de XInput

XInput es una API multiplataforma que se ha enviado para su uso en Xbox y Windows. En Xbox, XInput se envía como una biblioteca estática que se compila en el ejecutable principal del juego. En Windows, XInput se proporciona como un archivo DLL que se instala en las carpetas del sistema del sistema operativo.

Actualmente hay tres versiones actuales del archivo DLL de XInput. Elija la versión adecuada de XInput en función de la funcionalidad de XInput que use y de las versiones de Windows que desee admitir.

- XInput 1,4: XInput 1,4 se incluye como parte de Windows 10. Use esta versión para compilar aplicaciones para UWP.
- XInput 9.1.0: XInput 9.1.0 se incluye como parte de Windows Vista, Windows 7 y Windows 8. Use esta versión si la aplicación de escritorio está diseñada para ejecutarse en estas versiones de Windows y usa la funcionalidad básica de XInput.
- XInput 1,3: XInput 1,3 se distribuye como componente redistribuible en el SDK de DirectX compatible con Windows Vista, Windows 7 y Windows 8. Use esta versión si la aplicación de escritorio está diseñada para ejecutarse en estas versiones de Windows y necesita una funcionalidad que no sea compatible con XInput 9.1.0.

## <a name="xinput-14"></a>XInput 1,4

XInput 1,4 se distribuye hoy como componente del sistema en Windows 8 como XINPUT1 \_4.DLL. Está disponible "bandeja de entrada" y no requiere redistribución con una aplicación. El kit de desarrollo de software (SDK) de Windows contiene la biblioteca de encabezado e importación para vincular estáticamente con XINPUT1 \_4.DLL. Para descargar el SDK de Windows 8, consulte [descargas para desarrollar aplicaciones de escritorio](https://developer.microsoft.com/windows/downloads/).

XInput 1,4 tiene estas ventajas principales con respecto a otras versiones de XInput:

-   Esta es la única versión que se puede usar en las aplicaciones de la tienda Windows de C++/DirectX.
-   La nueva función [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) proporciona una cadena de identificador de dispositivo de audio que puede usar para abrir un dispositivo de voz o audio de maestro de XAudio2 para un casco conectado a un controlador común de Xbox. La función [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) no está disponible en esta versión.
-   Proporciona informes de funcionalidades mejoradas de los dispositivos, como la \_ \_ conexión inalámbrica de los Cap de XInput, los \_ Cap \_ de XInput FFB \_ compatibles, las Cap de XInput \_ PMD compatibles y las \_ \_ \_ mayúsculas \_ de XInput sin \_ marcas de navegación y la generación de informes más precisos de las Cap de XInput \_ \_ \_ Estas marcas se combinan en el miembro **Flags** de la estructura de [**\_ funcionalidades de XInput**](/windows/desktop/api/XInput/ns-xinput-xinput_capabilities) . La función [**XInputGetCapabilities**](/windows/desktop/api/XInput/nf-xinput-xinputgetcapabilities) devuelve **\_ funcionalidades de XInput**.

### <a name="xinput-910"></a>9.1.0 de XInput

Como XInput 1,4, XInput 9.1.0 se distribuye hoy como componente del sistema en Windows 10, Windows 8. x, Windows 7 y Windows Vista como XINPUT9 \_ 1 \_0.DLL. Se mantiene principalmente para la compatibilidad con versiones anteriores de las aplicaciones existentes. Tiene un conjunto de funciones reducidas, por lo que se recomienda usar XInput 1,4, si es posible. Sin embargo, es conveniente utilizar para las aplicaciones que se deben ejecutar en versiones de nivel inferior de Windows, pero que no necesitan la funcionalidad de audio adicional proporcionada por XInput 1,4 o XInput 1,3.

El Windows SDK contiene el encabezado y la biblioteca de importación para vincular estáticamente con XINPUT9 \_ 1 \_0.DLL.

XInput 9.1.0 tiene estas desventajas en otras versiones de XInput:

-   Por motivos de compatibilidad con versiones anteriores, [**XInputGetCapabilities**](/windows/desktop/api/XInput/nf-xinput-xinputgetcapabilities) en esta versión de XInput devuelve información de funcionalidad fija. Independientemente del dispositivo de controlador común de Xbox conectado, **XInputGetCapabilities** en XInput 9.1.0 siempre notificará un subtipo de dispositivo de controlador de juegos. No devolverá el bit de capacidad inalámbrica de los límites de XINPUT, \_ \_ incluso si un dispositivo inalámbrico está conectado.
-   No se puede determinar el casco para un identificador de usuario determinado. La función [**XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) no está disponible y la función [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) no devolverá resultados en Windows 8. x o Windows 10.
-   Las funciones [**XInputEnable**](/windows/desktop/api/XInput/nf-xinput-xinputenable), [**XInputGetBatteryInformation**](/windows/desktop/api/XInput/nf-xinput-xinputgetbatteryinformation)y [**XInputGetKeystroke**](/windows/desktop/api/XInput/nf-xinput-xinputgetkeystroke) no están disponibles.

### <a name="xinput-13"></a>XInput 1,3

Algunas versiones anteriores de XInput se han proporcionado como archivos dll redistribuibles en el SDK de DirectX. La primera versión redistribuible de XInput, XInput 1,1, se incluye en la versión de abril de 2006 del SDK de DirectX. La última versión que se incluye en el SDK de DirectX fue XInput 1,3, disponible en la versión de junio de 2010 del SDK de DirectX heredado. *El SDK de DirectX ya no está disponible en las descargas de Microsoft*.

Puede usar XInput 1,3 para aplicaciones que admiten versiones de nivel inferior de Windows y requieren funcionalidad no proporcionada por XInput 9.1.0 (es decir, informes de subtipos correctos, compatibilidad de audio, compatibilidad con informes de batería explícita, etc.).
