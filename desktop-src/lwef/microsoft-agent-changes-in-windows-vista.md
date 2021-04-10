---
title: Cambios del agente de Microsoft en Windows Vista
description: Cambios del agente de Microsoft en Windows Vista
ms.assetid: 2498e8d5-2274-477c-a807-77443c76afb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73af45553f876c413fbea906de2369e888f1483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268905"
---
# <a name="microsoft-agent-changes-in-windows-vista"></a>Cambios del agente de Microsoft en Windows Vista

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Windows Vista incluye algunos cambios en el modo en que el reconocimiento de voz y voz interactúa con Windows Vista.

Microsoft Agent ahora admite componentes de texto a voz y reconocimiento de voz de SAPI 5. Las propiedades TTSModeID y SRModeID del objeto agente todavía se usan para determinar qué voz o reconocedor está seleccionado para el agente y para modificar esta selección. Los modos de SAPI 4 aparecen como cadenas GUID como "{ca141fd0-ac7f-11D1-97a3-006008273000}", mientras que los tokens de SAPI 5 (equivalentes a los modos) aparecen como nombres normales, como "Microsoft Anna". Como en versiones anteriores, el agente realiza una selección predeterminada de los motores TTS y SR. Si los motores de SAPI 5 están instalados, siempre serán preferibles a los motores de SAPI 4 que se puedan instalar. El motor de conversión de texto a voz predeterminado del usuario, tal como se especifica en el panel de control, se usa si su género coincide con el del carácter; de lo contrario, se elige un motor SAPI 5 del mismo sexo si está disponible. Los identificadores de modo especificados directamente en el carácter se omiten si están presentes motores SAPI 5. Las selecciones predeterminadas se pueden comprobar mediante la lectura de las propiedades TTSModeID y SRModeID al principio del script.

Como antes, TTSModeID y SRModeID devolverán una cadena en blanco si no está presente la capacidad de reconocimiento de voz o de texto a voz. Se puede seleccionar un reconocedor o una voz específicos si se establecen estas propiedades en la cadena de modo SAPI 4 adecuada o en el nombre de token de SAPI 5. Después de establecer un token o un modo específico, también puede volver a leer la propiedad para comprobar que su valor ha tomado, lo que indica que el nuevo modo o token está realmente disponible y se ha seleccionado correctamente. Para los desarrolladores que implementan el agente a través de la web, tenga en cuenta que muchos usuarios de vista ya tienen una o más voces de SAPI 5 instaladas, por lo que es posible que desee evitar la descarga automática de las voces de SAPI 4 a menos que el script las solicite específicamente, ya que la voz descargada no se usará.

Los motores de conversión de texto a voz de SAPI 5 usan un conjunto diferente de estándares que SAPI 4 para anotar la voz con el marcado, por ejemplo para cambiar el tono o la velocidad de la voz. En SAPI 4, se usan comandos de "barra diagonal", como/Pit = 170/. En SAPI 5 se usan etiquetas XML, como <PITCH MIDDLE="5"/> . En vista, el agente aceptará ambos tipos de anotaciones en los motores de la "barra diagonal" de las cadenas del método de voz, y los motores de SAPI 4 omitirán las etiquetas XML. Al igual que con las etiquetas de barra diagonal, la compatibilidad con las etiquetas XML de SAPI 5 varía de un proveedor a otro, y algunos proveedores pueden admitir etiquetas adicionales. Para obtener más información sobre las etiquetas XML de SAPI 5, vea la especificación de SAPI 5.

El agente ya no incluye compatibilidad con varios idiomas. Siempre se asume que el idioma usado por el agente es el idioma actual del usuario, registrado con el sistema operativo. La propiedad LanguageID del objeto agente todavía es grabable, pero el agente omite su valor en vista. Por ejemplo, si el idioma del usuario está establecido en Inglés de EE. UU. (&H0409), y usa un programa que establece el ididioma en francés (&H040C), los cuadros de diálogo texto de sugerencia de voz y opciones de caracteres avanzadas seguirán apareciendo en inglés.

 

 




