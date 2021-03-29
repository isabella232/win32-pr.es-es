---
title: Diseño de animación
description: Diseño de animación
ms.assetid: 8812e4cc-9062-4c65-81ef-229bd29534cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7d6cf86cfe115ec209fb305f0ae017951bd7f41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994109"
---
# <a name="animation-design"></a>Diseño de animación

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

### <a name="image-design"></a>Diseño de imagen

Use la paleta Microsoft Office al diseñar los caracteres para minimizar los posibles problemas de realización de la paleta. Evite seleccionar un color de transparencia similar a los colores que usa en el documento.

### <a name="sounds"></a>Sonidos

El agente de Microsoft le permite reproducir sonidos en las animaciones. Se recomienda no incluir sonidos para las animaciones **inactivas** . Esto se debe a que no habrá un retraso en el medio de la animación, si el agente tiene que cargar el archivo DLL de multimedia del sistema.

### <a name="frame-size"></a>Tamaño de marco

Los asistentes de Office típicos son 123 x 93 píxeles. Aunque puede crear caracteres de otros tamaños, se escalarán a 123 x 93 en la galería de asistentes.

### <a name="frame-transition"></a>Transición de fotogramas

Todas las animaciones, excepto **adiós**, **saludo**, **Mostrar** y **ocultar** , deben comenzar y finalizar con la animación RestPose. Microsoft Office no reproduce animaciones de **devolución** explícitas, por lo que no debe definirlas. Todas las animaciones también deben tener una bifurcación de salida. Exit Branching nos permite "acelerar y finalizar" la animación actual antes de llamar a la siguiente animación. Si no proporciona una bifurcación de salida, la transición entre animaciones puede ser irregular.

### <a name="character-properties"></a>Propiedades de caracteres

Microsoft Agent le permite establecer las propiedades [**Name**](name-property.md), [**Description**](description-property.md) y [**ExtraData**](extradata-property.md) del carácter. Microsoft Office usa el campo **ExtraData** para contener una o varias frases de introducción y frases de recordatorio. Microsoft Office elige de las otras frases de introducción para colocar en el globo de voz en la galería de asistentes. Usamos las frases de recordatorio cuando recibe un recordatorio de Outlook.

El campo [**ExtraData**](extradata-property.md) tiene el formato siguiente:

IntroPhrase1~~IntroPhrase2~~IntroPhrase3 ^ ^ ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3

Las frases de introducción están separadas por un par de caracteres de tilde (~), seguidos de frases de recordatorio. Estas frases de recordatorio también se separan mediante un par de caracteres de tilde. Los dos conjuntos de frases se separan con dos caracteres de intercalación (^^). No hay ningún límite en cuanto al número de cada tipo de frase, salvo que debe haber al menos una de cada.

 

 




