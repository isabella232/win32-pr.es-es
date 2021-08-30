---
title: Cambios de Microsoft Agent en Windows Vista
description: Cambios de Microsoft Agent en Windows Vista
ms.assetid: 2498e8d5-2274-477c-a807-77443c76afb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b9b4e1104152bb21a2ed120d749d92907c1f6be6f2392c299db639cd483bf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961205"
---
# <a name="microsoft-agent-changes-in-windows-vista"></a>Cambios de Microsoft Agent en Windows Vista

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Windows Vista presenta algunos cambios en la forma en que el reconocimiento de voz y voz interactúa con Windows Vista.

Microsoft Agent ahora admite componentes de text-to-speech y reconocimiento de voz de SAPI 5. Las propiedades TTSModeID y SRModeID del objeto Agent se siguen utilizando para determinar qué voz o reconocedor está seleccionado para el agente y modificar esta selección. Los modos SAPI 4 aparecen como cadenas GUID como "{ca141fd0-ac7f-11d1-97a3-006008273000}", mientras que los tokens de SAPI 5 (equivalentes a los modos) aparecen como nombres normales, como "Microsoft Anna". Al igual que en versiones anteriores, el agente realizará una elección predeterminada de motores de TTS y SR. Si se instalan motores de SAPI 5, siempre se preferirán a los motores de SAPI 4 que se puedan instalar. El motor de texto a voz predeterminado del usuario, tal como se especifica en el panel de control, se usa si su género coincide con el del carácter; de lo contrario, se elige un motor SAPI 5 del mismo sexo si hay uno disponible. Los identificadores de modo especificados directamente en el carácter se omiten si hay motores SAPI 5 presentes. Las selecciones predeterminadas se pueden comprobar mediante la lectura de las propiedades TTSModeID y SRModeID al principio del script.

Como antes, TTSModeID y SRModeID devolverán una cadena en blanco si la funcionalidad text-to-speech o reconocimiento de voz no está presente. Se puede seleccionar una voz o un reconocedor específicos estableciendo estas propiedades en la cadena de modo SAPI 4 adecuada o en el nombre del token de SAPI 5. Después de establecer un modo o token específico, también puede volver a leer la propiedad para comprobar que su valor ha tomado, lo que indica que el nuevo modo o token estaba realmente disponible y se seleccionó correctamente. Para los desarrolladores que implementan el Agente a través de la Web, tenga en cuenta que muchos usuarios de Vista ya tendrán una o varias voces de SAPI 5 instaladas, por lo que es posible que quiera evitar la descarga automática de voces de SAPI 4 a menos que el script las solicite específicamente, ya que la voz descargada no terminaría usándose.

Los motores de texto a voz de SAPI 5 usan un conjunto diferente de estándares que SAPI 4 para anotar la voz con marcado, por ejemplo, para cambiar el tono o la velocidad de la voz. En SAPI 4 se usan comandos de "barra diagonal", como /pit=170/. En SAPI 5 se usan etiquetas XML, como \<PITCH MIDDLE="5"/> . En Vista, los motores de SAPI 5 omitirán ambos tipos de anotaciones en los comandos de "barra diagonal" de cadenas de método Speak y los motores de SAPI 4 omitirán las etiquetas XML. Al igual que con las etiquetas de barra diagonal, la compatibilidad con etiquetas XML de SAPI 5 varía de proveedor a proveedor, y algunos proveedores pueden admitir etiquetas adicionales. Para obtener más información sobre las etiquetas XML de SAPI 5, consulte especificación de SAPI 5.

El agente ya no incluye compatibilidad con varios idiomas. Siempre se supone que el idioma usado por el Agente es el idioma actual del usuario, tal y como está registrado en el sistema operativo. La propiedad LanguageID del objeto Agent todavía se puede escribir, pero el Agente en Vista omite su valor. Por ejemplo, si el idioma del usuario está establecido en inglés de Estados Unidos (&H0409) y usa un programa que establece languageID en francés (&H040C), el texto de la sugerencia de voz y los diálogos Opciones avanzadas de caracteres seguirán apareciendo en inglés.

 

 




