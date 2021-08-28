---
title: Perfiles del sistema
description: Perfiles del sistema
ms.assetid: 5f687aae-cf9b-4b2d-a3aa-d130b443fbf3
keywords:
- Windows SDK de formato multimedia, perfiles del sistema
- Formato de sistemas avanzados (ASF), perfiles de sistema
- ASF (formato de sistemas avanzados), perfiles de sistema
- Windows SDK de formato multimedia, iDs de perfil
- Formato de sistemas avanzados (ASF), iDs de perfil
- ASF (formato de sistemas avanzados), iDs de perfil
- perfiles del sistema, lista de
- profile IDs (IDs de perfil)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6389f82e93a0b27c079bd75ded9eb7d35d78a380ab72d244c5443c07f4c9ed5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807745"
---
# <a name="system-profiles"></a>Perfiles del sistema

La tabla siguiente contiene la lista completa de perfiles de sistema admitidos. Cada perfil de la lista tiene un nombre y un identificador de perfil. El identificador de perfil es una constante establecida en el valor GUID asignado al perfil del sistema. Para usar los iDs de perfil del sistema en el código, debe incluir wmsysprf.h en la aplicación. Para obtener ejemplos que muestran cómo cargar un perfil de sistema, vea [Para cargar un perfil de sistema.](to-load-a-system-profile.md)

> [!IMPORTANT]
> Los perfiles que se enumeran a continuación usan la versión 8 Windows códecs De audio multimedia Windows vídeo multimedia. No hay perfiles de sistema predefinidos que usen los códecs Windows serie Media 9. Puede crear su propio perfil Windows serie Media 9 mediante un perfil de la versión 8 como punto de partida. Para obtener más información, [vea Reusing Stream Configurations](reusing-stream-configurations.md).

 



| Nombre del perfil                                                                      | Id. de perfil                     | Descripción                                                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vídeo multimedia 8 para pc de cartera de colores (225 Kbps)                             | WMProfile \_ V80 \_ 255VideoPDA    | Use este perfil al crear archivos de vídeo para su reproducción en equipos de color más rápidos.                                                                                 |
| Windows Vídeo multimedia 8 para pc de cartera de colores (150 Kbps)                             | WMProfile \_ V80 \_ 150VideoPDA    | Use este perfil al crear archivos de vídeo para su reproducción en la mayoría de los equipos de Pocket.                                                                                         |
| Windows Vídeo multimedia 8 para módems de acceso telefónico o ISDN de canal único (de 28,8 a 56 Kbps) | WMProfile \_ V80 \_ 28856VideoMBR  | Use este perfil de velocidad de bits múltiple para audiencias de destino con módems de acceso telefónico o conexiones ISDN de canal único (el ancho de banda está entre 28,8 Kbps y 56 Kbps).        |
| Windows Vídeo multimedia 8 para LAN, módem por cable o xDSL (de 100 a 768 Kbps)             | WMProfile \_ V80 \_ 100768VideoMBR | Use este perfil de velocidad de bits múltiple para audiencias de destino con conexiones ISDN, LAN, módem de cable o xDSL de doble canal (el ancho de banda está entre 100 Kbps y 500 Kbps). |
| Windows Vídeo multimedia 8 para módems de acceso telefónico o LAN (de 28,8 a 100 Kbps)                | WMProfile \_ V80 \_ 288100VideoMBR | Use este perfil de velocidad de bits múltiple para audiencias de destino con conexiones ISDN de módem de acceso telefónico, LAN o de canal doble (el ancho de banda está entre 28,8 y 100 Kbps).         |
| Windows Vídeo multimedia 8 para módems de acceso telefónico (28,8 Kbps)                              | WMProfile \_ V80 \_ 288Video       | Use este perfil para la entrega de audio y vídeo de baja velocidad de bits a través de conexiones de acceso telefónico de 28,8 Kbps.                                                                          |
| Windows Vídeo multimedia 8 para módems de acceso telefónico (56 Kbps)                                | WMProfile \_ V80 \_ 56Video        | Use este perfil para la entrega de audio y vídeo de baja velocidad de bits a través de conexiones de acceso telefónico de 56 Kbps.                                                                            |
| Windows Vídeo multimedia 8 para red de área local (100 Kbps)                           | WMProfile \_ V80 \_ 100Video       | Use este perfil para la entrega de velocidad de bits media a través de conexiones ISDN, LAN o módem de cable de doble canal.                                                              |
| Windows Vídeo multimedia 8 para red de área local (256 Kbps)                           | WMProfile \_ V80 \_ 256Video       | Use este perfil para contenido de audio y vídeo de alta calidad destinado a la reproducción local o para su descarga y reproducción.                                                     |
| Windows Vídeo multimedia 8 para red de área local (384 Kbps)                           | WMProfile \_ V80 \_ 384Video       | Use este perfil para contenido de audio y vídeo de alta calidad destinado a la reproducción local o para su descarga y reproducción.                                                     |
| Windows Vídeo multimedia 8 para red de área local (768 Kbps)                           | WMProfile \_ V80 \_ 768Video       | Use este perfil para contenido de audio y vídeo de alta calidad destinado a la reproducción local o para su descarga y reproducción.                                                     |
| Windows Vídeo multimedia 8 para banda ancha (KB, 700 Kbps)                              | WMProfile \_ V80 \_ 700VIDEOVideo   | Use este perfil para contenido de audio y vídeo de alta calidad destinado a la reproducción local o a la descarga y reproducción.                                                         |
| Windows Vídeo multimedia 8 para banda ancha (KB, 1400 Kbps)                             | WMProfile \_ V80 \_ 1400VIDEOVideo  | Use este perfil para contenido de audio y vídeo de alta calidad destinado a la reproducción local o para su descarga y reproducción.                                                     |
| Windows Vídeo multimedia 8 para banda ancha (PAL, 384 Kbps)                               | WMProfile \_ V80 \_ 384PALVideo    | Use este perfil para contenido de audio y vídeo de alta calidad destinado a la reproducción local o para su descarga y reproducción.                                                     |
| Windows Vídeo multimedia 8 para banda ancha (PAL, 700 Kbps)                               | WMProfile \_ V80 \_ 700PALVideo    | Use este perfil para contenido de audio y vídeo de alta calidad destinado a la reproducción local o para su descarga y reproducción.                                                     |
| Windows Audio multimedia 8 para módem de acceso telefónico (Mono, 28,8 Kbps)                         | WMProfile \_ V80 \_ 288MonoAudio   | Use este perfil para contenido de radio y música (solo audio).                                                                                                          |
| Windows Audio multimedia 8 para módem de acceso telefónico (radio FM estéreo, 28,8 Kbps)              | WMProfile \_ V80 \_ 288StereoAudio | Use este perfil para contenido de radio y música (solo audio).                                                                                                          |
| Windows Audio multimedia 8 para módem de acceso telefónico (32 Kbps)                                 | WMProfile \_ V80 \_ 32StereoAudio  | Use este perfil para contenido de radio y música (solo audio).                                                                                                          |
| Windows Audio multimedia 8 para módem de acceso telefónico (calidad de CD cercana, 48 Kbps)                | WMProfile \_ V80 \_ 48StereoAudio  | Se usa para la radio, la música y el contenido de audio de uso general.                                                                                                            |
| Windows Audio multimedia 8 para módem de acceso telefónico (calidad de CD, 64 Kbps)                     | WMProfile \_ V80 \_ 64StereoAudio  | Use este perfil para públicos de destino con conexiones a Internet o LAN de alta velocidad.                                                                                  |
| Windows Audio multimedia 8 para ISDN (mejor que la calidad de CD, 96 Kbps)                  | WMProfile \_ V80 \_ 96StereoAudio  | Use este perfil para públicos de destino con conexiones a Internet o LAN de alta velocidad.                                                                                  |
| Windows Audio multimedia 8 para ISDN (mejor que la calidad de CD, 128 Kbps)                 | WMProfile \_ V80 \_ 128StereoAudio | Use este perfil para públicos de destino con conexiones a Internet o LAN de alta velocidad.                                                                                  |
| Windows Vídeo multimedia 8 para módem telefónico (sin audio, 28,8 Kbps)                     | WMProfile \_ V80 \_ 288VideoOnly   | Use este perfil al crear contenido de solo vídeo para públicos de destino con módems de acceso telefónico.                                                                         |
| Windows Vídeo multimedia 8 para módem de acceso telefónico (sin audio, 56 Kbps)                       | WMProfile \_ V80 \_ 56VideoOnly    | Use este perfil al crear contenido de solo vídeo para públicos de destino con módems de acceso telefónico.                                                                         |
| Windows Media 8 Fair Quality based VBR for Broadband                              | WMProfile \_ V80 \_ FAIRVBRVideo   | Perfil de alta calidad basado en la calidad del contenido de VBR que está restringido por la calidad.                                                                                     |
| Windows Media 8 Alta calidad basada en VBR para banda ancha.                             | WMProfile \_ V80 \_ HIGHVBRVideo   | Perfil de alta a mejor calidad basado en el contenido de VBR que está restringido por la calidad.                                                                                     |
| Windows VBR basado en media 8 best quality para banda ancha.                             | WMProfile \_ V80 \_ BESTVBRVideo   | Perfil basado en la mejor calidad para el contenido de VBR que está restringido por la calidad.                                                                                             |



 

Los perfiles del sistema están disponibles localizados para idiomas distintos del inglés. Para obtener más información, vea [Perfiles de sistema localizados.](localized-system-profiles.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMProfileManager::LoadProfileByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)
</dt> <dt>

[**IWMProfileManager2 (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)
</dt> <dt>

[**Trabajar con perfiles**](working-with-profiles.md)
</dt> </dl>

 

 




