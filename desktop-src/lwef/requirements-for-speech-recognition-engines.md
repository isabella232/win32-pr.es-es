---
title: Requisitos para los motores de reconocimiento de voz
description: Requisitos para los motores de reconocimiento de voz
ms.assetid: 41aca5da-c680-41c1-b070-af291cb0c8e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9214f13b11a071ec8d8599f0b6dd542884ae05f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994479"
---
# <a name="requirements-for-speech-recognition-engines"></a>Requisitos para los motores de reconocimiento de voz

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Un motor de reconocimiento de voz también debe ser un motor de controles y comandos totalmente compatible (C&C) según SAPI 4,0. Debe admitir varias gramáticas en el formato binario que se describe en la especificación y permitir que dichas gramáticas se activen o desactiven en tiempo real.

Tenga en cuenta que SAPI 4,0 requiere que los motores de reconocimiento de voz admitan las interfaces Unicode de caracteres anchos. Sin embargo, para admitir estas interfaces, el motor no debe depender de la conversión de datos Unicode a ANSI, ya que es posible que el motor no funcione correctamente en algunos sistemas. Por ejemplo, un motor japonés que convierte Unicode en ANSI podría no funcionar en un sistema de Microsoft Windows 95 en inglés.

Además, para que se considere conforme a Microsoft Agent, el motor debe devolver los objetos de resultados tras el reconocimiento correcto de una frase (a través de ISRGramNotifySinkW::P hraseFinish). Estos objetos de resultados deben admitir ISRResBasic, como requiere la especificación. Además, deben admitir ISRResScore. Aunque el agente de Microsoft se ejecutará con un motor que solo admita ISRResBasic, o incluso con un motor que no devuelva ningún objeto de resultados, el rendimiento suele ser mucho más pobre con dichos motores. Muchas aplicaciones usan los valores de confianza proporcionados por el motor para controlar cómo responden a varios comandos.

 

 




