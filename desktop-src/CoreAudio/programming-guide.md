---
description: Obtenga información sobre los conceptos y características de las API de audio principales de Windows Vista y cómo usarlas en la programación de aplicaciones.
ms.assetid: 825c7cd7-dc66-47b6-a1b6-d10101daebb3
title: Guía de programación de audio principal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2b8f65d0c5508cd821b49a42b4b89ea42859390913a30534319d5ef7c79224f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088395"
---
# <a name="core-audio-programming-guide"></a>Guía de programación de audio principal

En esta sección de guía se explican los conceptos y características de las API de audio principales de Windows Vista y se describe cómo usarlas en la programación de aplicaciones.

Esta sección contiene los temas siguientes.



| Tema                                                                                                                      | Descripción                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Componentes de audio en modo de usuario](user-mode-audio-components.md)                                                               | A través de las interfaces de bajo nivel de las API de audio principales, un cliente puede acceder a los componentes del sistema que administran y mezclan secuencias de audio.                                                                        |
| [Audio en modo de usuario protegido (IAM)](protected-user-mode-audio--puma-.md)                                                   | Describe las actualizaciones de Audio en modo de usuario protegido (PEM), el motor de audio en modo de usuario en el entorno protegido (PE), que proporciona un entorno más seguro para el procesamiento y la representación de audio.              |
| [Dispositivos de punto de conexión de audio](audio-endpoint-devices.md)                                                                       | Un dispositivo de punto de conexión de audio es una abstracción de software que permite interacciones fáciles de usar con dispositivos de audio, como micrófonos y altavoces.                                                              |
| [Sesiones de audio](audio-sessions.md)                                                                                       | Una sesión de audio es una abstracción de software que permite a un cliente administrar una colección de secuencias de audio relacionadas como una sola unidad.                                                                           |
| [Controles de volumen](volume-controls.md)                                                                                     | El sistema integra su configuración de volumen basada en directivas con la configuración de volumen del usuario de una manera lógica y coherente.                                                                                      |
| [Administración de flujos](stream-management.md)                                                                                 | La Windows Audio Session API (WASAPI) proporciona a un cliente un conjunto completo de métodos para crear y administrar secuencias de audio.                                                                             |
| [Topologías de dispositivo](device-topologies.md)                                                                                 | DeviceTopology API permite a un cliente detectar los controles de audio que se encuentran a lo largo de las distintas rutas de acceso de datos del hardware de audio.                                                                          |
| [Uso de la interfaz IKsControl para acceder a las propiedades de audio](using-the-ikscontrol-interface-to-access-audio-properties.md) | Es posible que una aplicación de audio especializada necesite usar la interfaz IKsControl para acceder a las propiedades de un adaptador de audio.                                                                                     |
| [Interoperabilidad con las API de audio heredadas](interoperability-with-legacy-audio-apis.md)                                     | Las características clave de las API de audio principales de Windows Vista se pueden incorporar a las aplicaciones existentes que usan DirectSound, DirectShow y las funciones **waveOutXxx** y **waveInXxx** multimedia de Windows. |
| [Sonido espacial](spatial-sound.md)                                                                                         | Proporciona instrucciones para usar Windows Sonic, la solución de nivel de plataforma de Microsoft para la compatibilidad con el sonido espacial en Xbox y Windows, lo que permite indicaciones de audio envolventes y de elevación (por encima o por debajo del agente de escucha). |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de audio principal](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



