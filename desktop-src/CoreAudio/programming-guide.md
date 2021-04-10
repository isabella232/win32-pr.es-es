---
description: Guía de programación
ms.assetid: 825c7cd7-dc66-47b6-a1b6-d10101daebb3
title: Guía de programación de audio básica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb99369058983ebac7205053efdf967bbb8c36d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275070"
---
# <a name="core-audio-programming-guide"></a>Guía de programación de audio básica

En esta sección de la guía se explican los conceptos y las características de las API de audio principales de Windows Vista y se describe cómo usarlas en la programación de aplicaciones.

Esta sección contiene los temas siguientes.



| Tema                                                                                                                      | Descripción                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Componentes de audio de modo de usuario](user-mode-audio-components.md)                                                               | A través de las interfaces de bajo nivel de las API de audio principales, un cliente puede tener acceso a los componentes del sistema que administran y mezclan secuencias de audio.                                                                        |
| [Audio de modo de usuario protegido (PUMA)](protected-user-mode-audio--puma-.md)                                                   | Describe las actualizaciones del audio en modo de usuario protegido (PUMA), el motor de audio de modo de usuario en el entorno protegido (PE), que proporciona un entorno más seguro para el procesamiento y la representación de audio.              |
| [Dispositivos de punto de conexión de audio](audio-endpoint-devices.md)                                                                       | Un dispositivo de punto de conexión de audio es una abstracción de software que permite interacciones sencillas con los dispositivos de audio, como los micrófonos y los altavoces.                                                              |
| [Sesiones de audio](audio-sessions.md)                                                                                       | Una sesión de audio es una abstracción de software que permite a un cliente administrar una colección de secuencias de audio relacionadas como una sola unidad.                                                                           |
| [Controles de volumen](volume-controls.md)                                                                                     | El sistema integra su configuración de volumen basada en directivas con la configuración de volumen del usuario de una manera lógica y coherente.                                                                                      |
| [Administración de flujos](stream-management.md)                                                                                 | La API de sesión de audio de Windows (WASAPI) proporciona un cliente con un conjunto completo de métodos para crear y administrar secuencias de audio.                                                                             |
| [Topologías de dispositivos](device-topologies.md)                                                                                 | La API de DeviceTopology permite a un cliente detectar los controles de audio que se encuentran a lo largo de las distintas rutas de acceso de datos en el hardware de audio.                                                                          |
| [Uso de la interfaz IKsControl para tener acceso a las propiedades de audio](using-the-ikscontrol-interface-to-access-audio-properties.md) | Es posible que una aplicación de audio especializada tenga que usar la interfaz IKsControl para tener acceso a las propiedades de un adaptador de audio.                                                                                     |
| [Interoperabilidad con las API de audio heredadas](interoperability-with-legacy-audio-apis.md)                                     | Las características clave de las API de audio principales en Windows Vista se pueden incorporar en las aplicaciones existentes que usan DirectSound, DirectShow y las funciones **waveOutXxx** y **waveInXxx** de multimedia de Windows. |
| [Sonido espacial](spatial-sound.md)                                                                                         | Proporciona instrucciones sobre el uso de Windows Sonic, la solución de nivel de plataforma de Microsoft para la compatibilidad con el sonido espacial en Xbox y Windows, lo que permite envolver y elevación (por encima o por debajo del agente de escucha) las indicaciones de audio. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de audio principales](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



