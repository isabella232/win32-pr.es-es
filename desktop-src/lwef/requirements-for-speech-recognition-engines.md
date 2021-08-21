---
title: Requisitos de los motores de reconocimiento de voz
description: Requisitos de los motores de reconocimiento de voz
ms.assetid: 41aca5da-c680-41c1-b070-af291cb0c8e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1315d395e3053d5f6f71fd7f8ff17cb815bea26fc4875878da74dd77113d5e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975755"
---
# <a name="requirements-for-speech-recognition-engines"></a>Requisitos de los motores de reconocimiento de voz

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Un motor de reconocimiento de voz también debe ser un motor de comando y control (C&C) totalmente compatible según SAPI 4.0. Debe admitir varias gramáticas en el formato binario descrito en la especificación y permitir que esas gramáticas se activen o desactiven en tiempo real.

Tenga en cuenta que SAPI 4.0 requiere que los motores de reconocimiento de voz admitan interfaces Unicode de caracteres anchos. Sin embargo, para admitir estas interfaces, el motor no debe depender de la conversión de datos Unicode a ANSI, ya que es posible que el motor no funcione correctamente en algunos sistemas. Por ejemplo, un motor japonés que convierte Unicode en ANSI puede no funcionar en un sistema de Microsoft Windows 95 en inglés.

Además, para que se considere compatible con Microsoft Agent, el motor debe devolver objetos de resultados tras el reconocimiento correcto de una frase (a través de ISRGramNotifySinkW::P hraseFinish). Estos objetos de resultados deben admitir ISRResBasic, como requiere la especificación. Además, deben admitir ISRResScore. Aunque Microsoft Agent se ejecutará con un motor que solo admita ISRResBasic, o incluso con un motor que no devuelva objetos de resultados, el rendimiento suele ser significativamente más deficiente con estos motores. Muchas aplicaciones usan los valores de confianza proporcionados por el motor para controlar cómo responden a varios comandos.

 

 




