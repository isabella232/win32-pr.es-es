---
title: Versiones de XInput
description: XInput es una API multiplataforma que se ha enviado para su uso en Xbox y Windows.
ms.assetid: e89a6c81-f170-4385-f942-3606f9747244
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3d3624b8ea12872058ed1d874aa242a5806aec2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255932"
---
# <a name="xinput-versions"></a>Versiones de XInput

XInput es una API multiplataforma que se ha enviado para su uso en Xbox y Windows. En Xbox, XInput se distribuye como una biblioteca estática que se compila en el archivo ejecutable del juego principal. En Windows, XInput se proporciona como un archivo DLL que se instala en las carpetas del sistema operativo.

Actualmente hay tres versiones actuales del archivo DLL de XInput. Elija la versión adecuada de XInput en función de la funcionalidad de XInput que use y las versiones de Windows que desea admitir.

- XInput 1.4: XInput 1.4 se distribuye como parte de Windows 10. Use esta versión para compilar aplicaciones para UWP.
- XInput 9.1.0: XInput 9.1.0 se distribuye como parte de Windows Vista, Windows 7 y Windows 8. Use esta versión si la aplicación de escritorio está pensada para ejecutarse en estas versiones de Windows y usa la funcionalidad básica de XInput.
- XInput 1.3: XInput 1.3 se distribuye como componente redistribuible en el SDK de DirectX con compatibilidad con Windows Vista, Windows 7 y Windows 8. Use esta versión si la aplicación de escritorio está pensada para ejecutarse en estas versiones de Windows y necesita funcionalidad que no sea compatible con XInput 9.1.0.

## <a name="xinput-14"></a>XInput 1.4

XInput 1.4 se distribuye hoy en día como un componente del sistema en Windows 8 como XINPUT1 \_4.DLL. Está disponible como "bandeja de entrada" y no requiere redistribución con una aplicación. El Windows Software Development Kit (SDK) contiene el encabezado y la biblioteca de importación para la vinculación estática con XINPUT1 \_4.DLL. Para descargar el SDK Windows 8, consulte [Descargas para desarrollar aplicaciones de escritorio.](https://developer.microsoft.com/windows/downloads/)

XInput 1.4 tiene estas principales ventajas con respecto a otras versiones de XInput:

-   Esta es la única versión que se puede usar en las aplicaciones de C++/DirectX Windows Store.
-   La nueva [**función XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) proporciona una cadena de identificador de dispositivo de audio que puede usar para abrir un dispositivo de audio o voz maestro XAudio2 para un casco asociado a un controlador común de Xbox. La [**función XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) no está disponible en esta versión.
-   Proporciona informes de funcionalidades mejoradas del dispositivo, como XINPUT \_ \_ CAPS WIRELESS, XINPUT \_ CAPS \_ FFB \_ SUPPORTED, XINPUT \_ CAPS PMD SUPPORTED y XINPUT CAPS NO NAVIGATION flags e \_ \_ \_ \_ \_ \_ \_ informes más precisos de XINPUT CAPS VOICE \_ SUPPORTED. Estas marcas se combinan en el miembro **Flags** de la [**estructura XINPUT \_ CAPABILITIES.**](/windows/desktop/api/XInput/ns-xinput-xinput_capabilities) La [**función XInputGetCapabilities**](/windows/desktop/api/XInput/nf-xinput-xinputgetcapabilities) devuelve **XINPUT \_ CAPABILITIES**.

### <a name="xinput-910"></a>XInput 9.1.0

Al igual que XInput 1.4, XInput 9.1.0 se distribuye hoy como componente del sistema en Windows 10, Windows 8.x, Windows 7 y Windows Vista como XINPUT9 \_ 1 \_0.DLL. Se mantiene principalmente por compatibilidad con versiones anteriores con las aplicaciones existentes. Tiene un conjunto de funciones reducido, por lo que se recomienda usar XInput 1.4, si es posible. Pero es conveniente usar para aplicaciones que deben ejecutarse en versiones de nivel inferior de Windows pero que no necesitan la funcionalidad de audio adicional proporcionada por XInput 1.4 o XInput 1.3.

El SDK Windows contiene el encabezado y la biblioteca de importación para vincular estáticamente con XINPUT9 \_ 1 \_0.DLL.

XInput 9.1.0 tiene estas desventajas con respecto a otras versiones de XInput:

-   Por motivos de compatibilidad con versiones anteriores, [**XInputGetCapabilities**](/windows/desktop/api/XInput/nf-xinput-xinputgetcapabilities) en esta versión de XInput devuelve información de funcionalidad fija. Independientemente del dispositivo de controlador común de Xbox conectado, **XInputGetCapabilities** en XInput 9.1.0 siempre informará de un subtipo de dispositivo de GAMEPAD. No devolverá el bit de funcionalidad \_ XINPUT CAPS \_ WIRELESS incluso si hay un dispositivo inalámbrico conectado.
-   No se puede determinar el casco para un identificador de usuario determinado. La [**función XInputGetAudioDeviceIds**](/windows/desktop/api/XInput/nf-xinput-xinputgetaudiodeviceids) no está disponible y la función [**XInputGetDSoundAudioDeviceGuids**](/windows/desktop/api/XInput/nf-xinput-xinputgetdsoundaudiodeviceguids) no devolverá resultados en Windows 8.x o Windows 10.
-   Las [**funciones XInputEnable**](/windows/desktop/api/XInput/nf-xinput-xinputenable), [**XInputGetBatteryInformation**](/windows/desktop/api/XInput/nf-xinput-xinputgetbatteryinformation)y [**XInputGetKeystroke**](/windows/desktop/api/XInput/nf-xinput-xinputgetkeystroke) no están disponibles.

### <a name="xinput-13"></a>XInput 1.3

Algunas versiones anteriores de XInput se han proporcionado como archivos DLL redistribuibles en el SDK de DirectX. La primera versión redistribuible de XInput, XInput 1.1, se envió en la versión de abril de 2006 del SDK de DirectX. La última versión que se ha incluido en el SDK de DirectX era XInput 1.3, disponible en la versión de junio de 2010 del SDK de DirectX heredado. *El SDK de DirectX ya no está disponible en descargas de Microsoft.*

Puede usar XInput 1.3 para aplicaciones que admiten versiones de nivel inferior de Windows y requieren funcionalidad no proporcionada por XInput 9.1.0 (es decir, informes de subtipo correctos, compatibilidad con audio, compatibilidad explícita con informes de batería, entre otros).
