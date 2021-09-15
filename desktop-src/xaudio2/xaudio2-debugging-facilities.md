---
description: La versión de depuración del motor XAudio2 valida los parámetros y proporciona mensajes detallados de advertencia y error.
ms.assetid: a7aaebf9-98d4-e96c-993d-b0d0b7074788
title: Instalaciones de depuración de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc50e710f30969e024078eeaf2660545e1da45c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574193"
---
# <a name="xaudio2-debugging-facilities"></a>Instalaciones de depuración de XAudio2

La versión de depuración del motor XAudio2 valida los parámetros y proporciona mensajes detallados de advertencia y error.

## <a name="setting-the-debug-logging-level-at-run-time"></a>Establecer el nivel de registro de depuración en tiempo de ejecución

Puede establecer el nivel de información de depuración que muestra XAudio2 en cualquier momento rellenando una estructura [**\_ DEBUG \_ CONFIGURATION de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) con las marcas para el nivel de registro deseado y, a continuación, pasar la estructura al método [**IXAudio2::SetDebugConfiguration.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) Los valores pasados al **método IXAudio2::SetDebugConfiguration** siempre invalidan los valores predeterminados establecidos en Windows registro.

## <a name="debug-support"></a>Compatibilidad con depuración

Las instalaciones de depuración siempre están disponibles para XAUDIO2 en Windows 8.

Para las versiones del SDK de DirectX de XAUDIO2, debe usar el motor de depuración de **XAUDIO2 \_ \_** al crear el objeto XAUDIO2 con [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) y el sistema debe tener instalado el entorno de ejecución para desarrolladores del SDK de DirectX para que se pueda realizar la depuración.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instalaciones de depuración](debugging-facilities.md)
</dt> <dt>

[Referencia de programación de XAudio2](programming-reference.md)
</dt> </dl>

 

 
