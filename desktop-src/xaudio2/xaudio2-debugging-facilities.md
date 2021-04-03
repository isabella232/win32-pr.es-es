---
description: La versión de depuración del motor de XAudio2 valida los parámetros y proporciona mensajes de advertencia y error detallados.
ms.assetid: a7aaebf9-98d4-e96c-993d-b0d0b7074788
title: Funciones de depuración de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc50e710f30969e024078eeaf2660545e1da45c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810459"
---
# <a name="xaudio2-debugging-facilities"></a>Funciones de depuración de XAudio2

La versión de depuración del motor de XAudio2 valida los parámetros y proporciona mensajes de advertencia y error detallados.

## <a name="setting-the-debug-logging-level-at-run-time"></a>Establecer el nivel de registro de depuración en tiempo de ejecución

Puede establecer el nivel de información de depuración que se muestra en XAudio2 en cualquier momento rellenando una estructura de [**\_ \_ configuración de depuración xaudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) con las marcas para el nivel de registro deseado y, después, pasar la estructura al método [**IXAudio2:: SetDebugConfiguration**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) . Los valores que se pasan al método **IXAudio2:: SetDebugConfiguration** siempre invalidan los valores predeterminados que se establecieron en el registro de Windows.

## <a name="debug-support"></a>Compatibilidad con depuración

Las funciones de depuración siempre están disponibles para XAUDIO2 en Windows 8.

En el caso de las versiones del SDK de DirectX de XAUDIO2, debe usar el **\_ \_ motor de depuración xaudio2** al crear el objeto xaudio2 con [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) y el sistema debe tener instalado el entorno de tiempo de ejecución para desarrolladores de DirectX SDK para que se admita la depuración.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de depuración](debugging-facilities.md)
</dt> <dt>

[Referencia de programación de XAudio2](programming-reference.md)
</dt> </dl>

 

 
