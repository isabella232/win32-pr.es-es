---
description: XAudio2 es una API multiplataforma que se ha enviado para su uso en Xbox 360, así como en las versiones de Windows, incluidas Windows XP, Windows Vista, Windows 7 y Windows 8.
ms.assetid: 875b44c4-30d6-8a6e-0cfc-9beb8c46f1b4
title: Versiones de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c9facfe357c323bd8f7b607460a8f59bd062fe
ms.sourcegitcommit: 010f524cd6098a5941de77907d4d6ae7871f8af1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "105689602"
---
# <a name="xaudio2-versions"></a>Versiones de XAudio2

XAudio2 es una API multiplataforma que se ha enviado para su uso en Xbox 360, así como en las versiones de Windows, incluidas Windows XP, Windows Vista, Windows 7 y Windows 8. En la consola Xbox 360, XAudio2 se envía como una biblioteca estática que se compila en el archivo ejecutable principal del juego. En Windows, XAudio2 se proporciona como una biblioteca de vínculos dinámicos (DLL) instalada en las carpetas del sistema del sistema operativo.

## <a name="xaudio-29-windows-10-and-redistributable-for-windows-7-and-windows-8x"></a>XAudio 2,9 (Windows 10 y Redistributable para Windows 7 y Windows 8. x)

La versión 2,9 de XAudio2 se incluye como parte de Windows 10, XAUDIO2 \_9.DLL, junto con XAudio 2,8, para admitir aplicaciones antiguas. También está disponible una [versión redistribuible de XAudio 2,9](xaudio2-redistributable.md) para Windows 7 SP1, Windows 8 y Windows 8.1.

XAudio 2.9 se ha actualizado con los cambios siguientes:

-   Nuevas marcas de creación: \_ el \_ motor de depuración de xaudio2, el motor de detención de xaudio2 cuando está \_ \_ \_ \_ inactivo, xaudio2 \_ 1024 \_ Quantum
-   la compatibilidad con xWMA está disponible en esta versión de XAudio2.
-   La función [**CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo) se admite en la versión de Windows 10 de XAudio 2,9.
-   [**XAUDIO2FX \_ Ahora, los \_ parámetros de reverberación**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) incluyen el valor *SideDelay* para los sistemas 7,1.
-   La función [**ReverbConvertI3DL2ToNative**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-reverbconverti3dl2tonative) ahora incluye el parámetro booleano *sevenDotOneReverb* que habilita la reverberación 7,1.

## <a name="xaudio-28-windows-8x"></a>XAudio 2,8 (Windows 8. x)

La versión 2,8 de XAudio2 se incluye hoy como componente del sistema en Windows 8, XAUDIO2 \_8.DLL. Está disponible "bandeja de entrada" y no requiere redistribución con una aplicación. Se recomienda usar el kit de desarrollo de software (SDK) de Windows para Windows 8 para desarrollar en XAudio2; el Windows SDK para Windows 8 contiene la biblioteca de encabezado e importación necesaria para vincular estáticamente con XAUDIO2 \_8.DLL.

XAudio2 2,8 se ha actualizado con los cambios siguientes:

-   Esta versión es compatible con el desarrollo de aplicaciones de la tienda Windows. la API de XAudio2 se puede usar en las aplicaciones de la tienda Windows de C++/DirectX.
-   [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) es una llamada a la API de Win32 plana y ya no crea un CLSID de XAudio2. Se ha quitado la compatibilidad con la creación de instancias de XAudio2 mediante CoCreateInstance.
-   Ahora, el proceso de creación llama implícitamente a la función Initialize y se ha quitado de la interfaz [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .
-   La funcionalidad de enumeración de dispositivos se ha quitado de XAudio2; las funciones GetDeviceDetails y GetDeviceCount se han quitado de la interfaz [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) . Las aplicaciones que desean representar en otros dispositivos de audio en el sistema deben pasar una cadena de identificador de dispositivo a [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) en lugar de un índice de dispositivo. El dispositivo de representación de audio predeterminado todavía se puede crear sin enumeración.
-   [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) tiene una función agregada [**IXAudio2MasteringVoice:: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) para que devuelve la máscara de canal para el dispositivo de salida de destino.
-   Las bibliotecas [X3DAudio](x3daudio.md) y [XAPOFX](xapofx-overview.md) se combinan en XAudio2. El código de la aplicación sigue usando encabezados independientes, X3DAUDIO. H y XPOFX. H, pero ahora se vincula a una única biblioteca de importación, XAUDIO2 \_ 8. lib.
-   la compatibilidad con xWMA no está disponible en esta versión de XAudio2; no se admitirá xWMA como formato de búfer de audio al llamar a CreateSourceVoice. Ahora se recomienda el objeto lector de Media Foundation Source para descodificar una gran variedad de formatos multimedia en búferes PCM en memoria.
-   [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) Now toma cuatro parámetros en lugar de dos. Los parámetros más recientes especifican los datos iniciales como parte de la creación de [XAPOFX](xapofx-overview.md) .

## <a name="xaudio-27-and-earlier-windows-7"></a>XAudio 2,7 y versiones anteriores (Windows 7)

Todas las versiones anteriores de XAudio2 para su uso en aplicaciones se han proporcionado como archivos dll redistribuibles en el SDK de DirectX. La primera versión de XAudio2, XAudio2 2,0, se incluyó en la versión de marzo de 2008 del SDK de DirectX. La última versión que se incluye en el SDK de DirectX era XAudio2 2,7, disponible en la última versión del SDK de DirectX de junio de 2010.

El SDK de DirectX heredado ya no está disponible en las descargas de Microsoft debido a la retirada de todo el contenido con firma SHA-1. El 2010 de junio era la versión final del ciclo de vida.

Las versiones anteriores de XAudio2 no se pueden usar para compilar aplicaciones de la tienda Windows para Windows 8.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> <dt>

[Conceptos clave de XAudio2](xaudio2-key-concepts.md)
</dt> </dl>

[Guía del desarrollador para la versión redistribuible de XAudio 2.9](xaudio2-redistributable.md)
</dt> </dl>
 

 
