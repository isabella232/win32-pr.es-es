---
description: XAudio2 es una API multiplataforma que se ha incluido para su uso en Xbox 360, así como versiones de Windows, como Windows XP, Windows Vista, Windows 7 y Windows 8.
ms.assetid: 875b44c4-30d6-8a6e-0cfc-9beb8c46f1b4
title: Versiones de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fec5f86ec0ef59898c5ce52dffc8acae37101d0bab384f2537b0d2e23cb6ac5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657065"
---
# <a name="xaudio2-versions"></a>Versiones de XAudio2

XAudio2 es una API multiplataforma que se ha incluido para su uso en Xbox 360, así como versiones de Windows, como Windows XP, Windows Vista, Windows 7 y Windows 8. En Xbox 360, XAudio2 se distribuye como una biblioteca estática que se compila en el ejecutable del juego principal. En Windows, XAudio2 se proporciona como una biblioteca de vínculos dinámicos (DLL) instalada en las carpetas del sistema del sistema operativo.

## <a name="xaudio-29-windows-10-and-redistributable-for-windows-7-and-windows-8x"></a>XAudio 2.9 (Windows 10 y redistribuible para Windows 7 y Windows 8.x)

XAudio2 versión 2.9 se incluye como parte de Windows 10, XAUDIO29.DLL, junto con XAudio 2.8 para admitir aplicaciones \_ anteriores. También hay disponible una versión redistribuible de [XAudio 2.9](xaudio2-redistributable.md) para Windows 7 SP1, Windows 8 y Windows 8.1.

XAudio2.9 se ha actualizado con los siguientes cambios:

-   Nuevas marcas de creación: XAUDIO2 \_ DEBUG \_ ENGINE, XAUDIO2 \_ STOP ENGINE WHEN \_ \_ \_ IDLE, XAUDIO2 \_ 1024 \_ QUANTUM
-   La compatibilidad con xWMA está disponible en esta versión de XAudio2.
-   La [**función CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo) se admite en la Windows 10 de XAudio 2.9.
-   [**XAUDIO2FX \_ PARÁMETROS DE \_ REVERB**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) ahora incluye el valor *SideDelay* para sistemas 7.1.
-   La [**función ReverbConvertI3DL2ToNative**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-reverbconverti3dl2tonative) ahora incluye el parámetro *booleano sevenDotOneReverb* que habilita la reverberación 7.1.

## <a name="xaudio-28-windows-8x"></a>XAudio 2.8 (Windows 8.x)

La versión 2.8 de XAudio2 se distribuye hoy en día como un componente del sistema en Windows 8, XAUDIO2 \_8.DLL. Está disponible como "bandeja de entrada" y no requiere redistribución con una aplicación. Se recomienda usar el kit de desarrollo Windows software (SDK) para Windows 8 desarrollar con XAudio2; el SDK Windows para Windows 8 contiene el encabezado y la biblioteca de importación necesarios para la vinculación estática con XAUDIO2 \_8.DLL.

XAudio2 2.8 se ha actualizado con los siguientes cambios:

-   Esta versión admite el Windows de aplicaciones de store. La API XAudio2 se puede usar en aplicaciones de C++/DirectX Windows Store.
-   [**XAudio2Create es**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) una llamada API de Win32 plana y ya no crea un CLSID de XAudio2. Se ha quitado la compatibilidad para crear instancias de XAudio2 de CoCreateInstance.
-   El proceso de creación llama implícitamente a la función Initialize y se ha quitado de la [**interfaz IXAudio2.**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2)
-   La funcionalidad de enumeración de dispositivos se ha quitado de XAudio2; Las funciones GetDeviceDetails y GetDeviceCount se han quitado de la [**interfaz IXAudio2.**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) Las aplicaciones que quieran representarse en otros dispositivos de audio del sistema deben pasar una cadena de identificador de dispositivo a [**CreateMasteringVoice en**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) lugar de un índice de dispositivo. El dispositivo de representación de audio predeterminado todavía se puede crear sin enumeración.
-   [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) tiene una función [**agregada IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) para que devuelve la máscara de canal para el dispositivo de salida de destino.
-   Las [bibliotecas X3DAudio](x3daudio.md) y [XAPOFX](xapofx-overview.md) se combinan en XAudio2. El código de la aplicación todavía usa encabezados independientes, X3DAUDIO. H y XPOFX. H, pero ahora se vincula a una sola biblioteca de importación, XAUDIO2 \_ 8.LIB.
-   La compatibilidad con xWMA no está disponible en esta versión de XAudio2; xWMA no se admite como formato de búfer de audio al llamar a CreateSourceVoice. Ahora se recomienda el Media Foundation lector de origen para la decodificación de una amplia variedad de formatos multimedia en búferes PCM en memoria.
-   [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) ahora toma cuatro parámetros en lugar de dos. Los parámetros más recientes especifican los datos iniciales como parte de [la creación de XAPOFX.](xapofx-overview.md)

## <a name="xaudio-27-and-earlier-windows-7"></a>XAudio 2.7 y versiones anteriores (Windows 7)

Todas las versiones anteriores de XAudio2 para su uso en aplicaciones se han proporcionado como archivos DLL redistribuibles en el SDK de DirectX. La primera versión de XAudio2, XAudio2 2.0, se incluye en la versión de marzo de 2008 del SDK de DirectX. La última versión que se entrenó en el SDK de DirectX fue XAudio2 2.7, disponible en la última versión del SDK de DirectX en junio de 2010.

El SDK de DirectX heredado ya no está disponible en las descargas de Microsoft debido a la retirada de todo el contenido firmado sha-1. Junio de 2010 fue la versión de fin de ciclo de vida.

Las versiones anteriores de XAudio2 no se pueden usar para compilar Windows store para Windows 8.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> <dt>

[Conceptos clave de XAudio2](xaudio2-key-concepts.md)
</dt> </dl>

[Guía del desarrollador para la versión redistribuible de XAudio 2.9](xaudio2-redistributable.md)
</dt> </dl>
 

 
