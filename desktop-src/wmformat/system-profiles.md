---
title: Perfiles del sistema
description: Perfiles del sistema
ms.assetid: 5f687aae-cf9b-4b2d-a3aa-d130b443fbf3
keywords:
- Windows Media Format SDK, perfiles del sistema
- Advanced Systems Format (ASF), perfiles del sistema
- ASF (formato de sistemas avanzados), perfiles del sistema
- SDK de Windows Media Format, ID. de perfil
- Advanced Systems Format (ASF), ID. de perfil
- ASF (formato de sistemas avanzados), ID. de perfil
- perfiles del sistema, lista de
- ID. de perfil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeca66023e6de6aba9c07a6bcb84a73756e316a8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788829"
---
# <a name="system-profiles"></a>Perfiles del sistema

La tabla siguiente contiene la lista completa de los perfiles del sistema admitidos. Cada perfil de la lista tiene un nombre y un identificador de perfil. El ID. de perfil es una constante establecida en el valor GUID asignado al perfil del sistema. Para utilizar los identificadores de perfil del sistema en el código, debe incluir wmsysprf. h en la aplicación. Para obtener ejemplos que muestran cómo cargar un perfil del sistema, consulte [para cargar un perfil del sistema](to-load-a-system-profile.md).

> [!IMPORTANT]
> Los perfiles que se enumeran a continuación usan los códecs Windows Media Audio y Windows Media Video de la versión 8. No hay perfiles de sistema predefinidos que utilicen los códecs de la serie Windows Media 9. Puede crear su propio perfil de Windows Media 9 series con un perfil de la versión 8 como punto de partida. Para obtener más información, vea [reutilizar las configuraciones de Stream](reusing-stream-configurations.md).

 



| Nombre del perfil                                                                      | ID. de perfil                     | Descripción                                                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media Video 8 para Pocket PC de color (225 Kbps)                             | WMProfile \_ V80 \_ 255VideoPDA    | Use este perfil al crear archivos de vídeo para la reproducción en Pocket PC de color más rápido.                                                                                 |
| Windows Media Video 8 para Pocket PC de color (150 Kbps)                             | WMProfile \_ V80 \_ 150VideoPDA    | Use este perfil al crear archivos de vídeo para la reproducción en la mayoría de los Pocket PC.                                                                                         |
| Windows Media Video 8 para módems de acceso telefónico o ISDN (RDSI) de canal único (de 28,8 a 56 kbps) | WMProfile \_ V80 \_ 28856VideoMBR  | Use este perfil de velocidad de bits múltiple para audiencias de destino con módems de acceso telefónico o conexiones RDSI de canal único (el ancho de banda está entre 28,8 Kbps y 56 kbps).        |
| Windows Media Video 8 para LAN, módem por cable o xDSL (de 100 a 768 Kbps)             | WMProfile \_ V80 \_ 100768VideoMBR | Use este perfil de velocidad de bits múltiple para audiencias de destino con conexiones ISDN, LAN, de módem por cable o xDSL de canal dual (el ancho de banda está entre 100 Kbps y 500 kbps). |
| Windows Media Video 8 para módems de acceso telefónico o LAN (de 28,8 a 100 Kbps)                | WMProfile \_ V80 \_ 288100VideoMBR | Use este perfil de velocidad de bits múltiple para audiencias de destino con conexiones de módem de acceso telefónico, LAN o ISDN de canal dual (el ancho de banda está entre 28,8 y 100 Kbps).         |
| Windows Media Video 8 para módems de acceso telefónico (28,8 Kbps)                              | WMProfile \_ V80 \_ 288Video       | Use este perfil para la entrega de audio y vídeo de baja velocidad de bits a través de conexiones de acceso telefónico de 28,8 kbps.                                                                          |
| Windows Media Video 8 para módems de acceso telefónico (56 kbps)                                | WMProfile \_ V80 \_ 56Video        | Use este perfil para la entrega de audio y vídeo de baja velocidad de bits a través de conexiones de acceso telefónico de 56 kbps.                                                                            |
| Windows Media Video 8 para la red de área local (100 Kbps)                           | WMProfile \_ V80 \_ 100Video       | Use este perfil para la entrega a velocidad de bits medio en conexiones de módem de canal dual, LAN o de cable de dos canales.                                                              |
| Windows Media Video 8 para la red de área local (256 kbps)                           | WMProfile \_ V80 \_ 256Video       | Use este perfil para el contenido de audio o vídeo de alta calidad diseñado para la reproducción local o para su descarga y reproducción.                                                     |
| Windows Media Video 8 para la red de área local (384 Kbps)                           | WMProfile \_ V80 \_ 384Video       | Use este perfil para el contenido de audio o vídeo de alta calidad diseñado para la reproducción local o para su descarga y reproducción.                                                     |
| Windows Media Video 8 para la red de área local (768 Kbps)                           | WMProfile \_ V80 \_ 768Video       | Use este perfil para el contenido de audio o vídeo de alta calidad diseñado para la reproducción local o para su descarga y reproducción.                                                     |
| Windows Media Video 8 para banda ancha (NTSC, 700 Kbps)                              | WMProfile \_ V80 \_ 700NTSCVideo   | Use este perfil para obtener contenido de audio o vídeo de alta calidad destinado a la reproducción o descarga local.                                                         |
| Windows Media Video 8 para banda ancha (NTSC, 1400 kbps)                             | WMProfile \_ V80 \_ 1400NTSCVideo  | Use este perfil para el contenido de audio o vídeo de alta calidad diseñado para la reproducción local o para su descarga y reproducción.                                                     |
| Windows Media Video 8 para banda ancha (PAL, 384 Kbps)                               | WMProfile \_ V80 \_ 384PALVideo    | Use este perfil para el contenido de audio o vídeo de alta calidad diseñado para la reproducción local o para su descarga y reproducción.                                                     |
| Windows Media Video 8 para banda ancha (PAL, 700 Kbps)                               | WMProfile \_ V80 \_ 700PALVideo    | Use este perfil para el contenido de audio o vídeo de alta calidad diseñado para la reproducción local o para su descarga y reproducción.                                                     |
| Windows Media Audio 8 para el módem de acceso telefónico (mono, 28,8 Kbps)                         | WMProfile \_ V80 \_ 288MonoAudio   | Use este perfil para el contenido de radio y música (solo audio).                                                                                                          |
| Windows Media Audio 8 para el módem de acceso telefónico (estéreo de radio FM, 28,8 Kbps)              | WMProfile \_ V80 \_ 288StereoAudio | Use este perfil para el contenido de radio y música (solo audio).                                                                                                          |
| Windows Media Audio 8 para el módem de acceso telefónico (32 Kbps)                                 | WMProfile \_ V80 \_ 32StereoAudio  | Use este perfil para el contenido de radio y música (solo audio).                                                                                                          |
| Windows Media Audio 8 para el módem de acceso telefónico (cerca de la calidad del CD, 48 kbps)                | WMProfile \_ V80 \_ 48StereoAudio  | Se usa para el contenido de audio de uso general, música y radio.                                                                                                            |
| Windows Media Audio 8 para el módem de acceso telefónico (calidad del CD, 64 kbps)                     | WMProfile \_ V80 \_ 64StereoAudio  | Use este perfil para audiencias de destino con conexiones de Internet o LAN de alta velocidad.                                                                                  |
| Windows Media Audio 8 para ISDN (mejor que la calidad del CD, 96 kbps)                  | WMProfile \_ V80 \_ 96StereoAudio  | Use este perfil para audiencias de destino con conexiones de Internet o LAN de alta velocidad.                                                                                  |
| Windows Media Audio 8 para ISDN (mejor que la calidad del CD, 128 kbps)                 | WMProfile \_ V80 \_ 128StereoAudio | Use este perfil para audiencias de destino con conexiones de Internet o LAN de alta velocidad.                                                                                  |
| Windows Media Video 8 para el módem de acceso telefónico (sin audio, 28,8 Kbps)                     | WMProfile \_ V80 \_ 288VideoOnly   | Use este perfil al crear contenido de solo vídeo para audiencias de destino con módems de acceso telefónico.                                                                         |
| Windows Media Video 8 para el módem de acceso telefónico (sin audio, 56 kbps)                       | WMProfile \_ V80 \_ 56VideoOnly    | Use este perfil al crear contenido de solo vídeo para audiencias de destino con módems de acceso telefónico.                                                                         |
| VBR basada en la calidad justa de Windows Media 8 para banda ancha                              | WMProfile \_ V80 \_ FAIRVBRVideo   | Perfil equitativo a alto nivel de calidad para el contenido de VBR que está restringido a la calidad.                                                                                     |
| VBR de alta calidad basada en Windows Media 8 para banda ancha.                             | WMProfile \_ V80 \_ HIGHVBRVideo   | Perfil de alta a mejor calidad basado en el contenido de VBR que tiene la calidad restringida.                                                                                     |
| VBR basada en la mejor calidad de Windows Media 8 para banda ancha.                             | WMProfile \_ V80 \_ BESTVBRVideo   | Perfil de mejor calidad para el contenido de VBR que está restringido a la calidad.                                                                                             |



 

Los perfiles del sistema están disponibles para idiomas distintos del inglés. Para obtener más información, consulte [perfiles del sistema localizados](localized-system-profiles.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMProfileManager::LoadProfileByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)
</dt> <dt>

[**Interfaz IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)
</dt> <dt>

[**Trabajar con perfiles**](working-with-profiles.md)
</dt> </dl>

 

 




