---
title: Obtener acceso a un motor de voz en el código
description: Obtener acceso a un motor de voz en el código
ms.assetid: ddfe0552-a29e-4ce4-b608-c131efbe300b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d81841f6f287d36a6ac01fa77294b1754eeb9b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105695581"
---
# <a name="accessing-a-speech-engine-in-your-code"></a>Obtener acceso a un motor de voz en el código

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Para usar un motor de voz determinado en el código, use la API del agente para establecer el motor. En el caso de los motores de entrada de voz, use [**SRModeID**](https://www.bing.com/search?q=**SRModeID**), especificando el identificador de modo del motor. Sin embargo, tenga en cuenta que el motor debe estar instalado. Para determinar si el motor está presente, puede consultar **SRModeID**. El motor debe coincidir con la configuración de [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) del carácter. Por ejemplo, no se puede establecer **SRModeID** en un identificador de modo de motor de reconocimiento de voz de alemán para un carácter cuyo **LanguageID** es francés.

**Identificadores de modo de motor de entrada de voz**



| Voz                                    | Identificadores de modo                             |
|------------------------------------------|--------------------------------------|
| Microsoft Speech reconocimiento Engine v 4.0 | {D8905400-B5C8-11D0-B968020AFDB1B9C} |



 

Compruebe y establezca el valor de [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) y [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) del carácter en el código antes de intentar definir la gramática de los parámetros de voz de los objetos de **comando** de la aplicación. Considere también la posibilidad de comprobar el explorador o el idioma del sistema para asegurarse de que coincida con la configuración de los usuarios. Puede producirse un error en el motor si intenta definir una gramática para un idioma que no coincide con el motor.

Un juego de caracteres para la salida de texto a voz (TTS) se puede compilar con una preferencia de identificador de modo predeterminada del motor de salida de voz. Cuando se carga el carácter, si el motor está instalado y coincide con el [**LanguageID**](https://www.bing.com/search?q=**LanguageID**)del carácter, el agente intentará cargar ese ID. de modo para la salida de voz. Si el motor no está presente o tiene un **LanguageID** distinto, el agente intentará cargar el primer identificador de modo que encuentre que coincida con el **LanguageID** del carácter, pero seguirá configurando la velocidad y el valor de tono compilados del carácter.

Tenga en cuenta que, dado que todos los caracteres suministrados por el agente de Microsoft se compilan para usar el motor de la voz de Lernout & Hauspie TruVoice americana como el motor de salida de voz predeterminado, se ajusta la configuración de velocidad y de paso de los caracteres para este lenguaje y motor. Por lo tanto, al usar otros motores de TTS o motores de otros idiomas, es posible que los caracteres no hablen con el paso o la velocidad óptimos. Aunque la aplicación o la página web no pueden escribir los valores de propiedad de [**paso**](/previous-versions/ms809428(v=msdn.10)) y [**velocidad**](https://www.bing.com/search?q=**Speed**) , puede incluir etiquetas [Pit](pit-tag.md) (tono) y [SPD](spd-tag.md) (velocidad) en el texto de salida que cambiará temporalmente el paso y la velocidad de un utterance determinado. Sin embargo, el uso de las etiquetas Pit y SPD no cambiará las propiedades de la **velocidad** y el **paso** . Consulte [programar el control de Microsoft Agent](programming-the-microsoft-agent-control.md) y las [etiquetas de salida de voz del agente de Microsoft](microsoft-agent-speech-output-tags.md) para obtener más información.

También debe instalar los binarios de los archivos en tiempo de ejecución (SPCHAPI.exe) de SAPI 4.0 al usar otros motores TTS compatibles con SAPI que el motor en inglés TruVoice de L&H con los caracteres proporcionados por el agente de Microsoft para que los motores se enumeren correctamente. En la página web, incluya la siguiente etiqueta de objeto para instalar automáticamente el componente:

``` syntax
<OBJECT width=0 height=0
CLASSID="CLSID:0C7F3F20-8BAB-11d2-9432-00C04F8EF48F"
CODEBASE="#VERSION=4,0,0,0">
</OBJECT>
```

Para consultar o establecer un identificador de modo del motor, use [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**). Con **TTSModeID** , puede establecer un identificador de modo que sea diferente del [**LanguageID**](https://www.bing.com/search?q=**LanguageID**)del carácter. Por ejemplo, puede establecer un carácter alemán para hablar con un identificador de modo francés. Los identificadores de modo del motor de salida de voz no solo definen qué motor se usa, sino que también se corresponden con las voces específicas admitidas para un motor. También puede usar el editor de caracteres del agente de Microsoft o las herramientas incluidas en la [documentación del SDK de Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx) para consultar los identificadores de modo de los motores TTS instalados en el sistema.

**Identificadores de modo de salida de voz**



| Voz                                       | Identificadores de modo                               |
|---------------------------------------------|----------------------------------------|
| Hembra adulto \# 1, Inglés de EE. UU., L&H TruVoice  | {CA141FD0-AC7F-11D1-97A3-006008273008} |
| Adultos hembra \# 2, Inglés de EE. UU., L&H TruVoice  | {CA141FD0-AC7F-11D1-97A3-006008273009} |
| Hombre de adulto \# 1, Inglés de EE. UU., L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273000} |
| Adulto de adultos \# 2, Inglés de EE. UU., L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273001} |
| Hombre \# de adulto 3, Inglés de EE. UU., L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273002} |
| Adulto masculino \# 4, Inglés de EE. UU., L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273003} |
| Hombre de adulto \# 5, Inglés de EE. UU., L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273004} |
| Hombre de adulto \# 6, Inglés de EE. UU., L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273005} |
| Adulto masculino \# 7, Inglés de EE. UU., L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273006} |
| Adulto macho \# 8, Inglés de EE. UU., L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273007} |
| Carol, Inglés británico, L&H TTS3000         | {227A0E40-A92A-11d1-B17B-0020AFED142E} |
| Peter, Inglés británico, L&H TTS3000         | {227A0E41-A92A-11d1-B17B-0020AFED142E} |
| Alicia, holandés, L&H TTS3000                   | {A0DDCA40-A92C-11d1-B17B-0020AFED142E} |
| Alexander, holandés, L&H TTS3000               | {A0DDCA41-A92C-11d1-B17B-0020AFED142E} |
| Véronique, Francés, L&H TTS3000              | {0879A4E0-A92C-11d1-B17B-0020AFED142E} |
| Pierre, Francés, L&H TTS3000                 | {0879A4E1-A92C-11d1-B17B-0020AFED142E} |
| Anna, alemán, L&H TTS3000                   | {3A1FB760-A92B-11d1-B17B-0020AFED142E} |
| Stefan, alemán, L&H TTS3000                 | {3A1FB761-A92B-11d1-B17B-0020AFED142E} |
| Bárbara, Italiano, L&H TTS3000               | {7EF71700-A92D-11d1-B17B-0020AFED142E} |
| Stefano, Italiano, L&H TTS3000               | {7EF71701-A92D-11d1-B17B-0020AFED142E} |
| Naoko, Japonés, L&H TTS3000                | {A778E060-A936-11d1-B17B-0020AFED142E} |
| Kenji, Japonés, L&H TTS3000                | {A778E061-A936-11d1-B17B-0020AFED142E} |
| Shin-ah, Coreano, L&H TTS3000                | {12E0B720-A936-11d1-B17B-0020AFED142E} |
| Jun-Ho, Coreano, L&H TTS3000                 | {12E0B721-A936-11d1-B17B-0020AFED142E} |
| Juliana, Portugués (Brasil), L&H TTS3000   | {8AA08CA0-A1AE-11d3-9BC5-00A0C967A2D1} |
| Alexandre, Portugués (Brasil), L&H TTS3000 | {8AA08CA1-A1AE-11d3-9BC5-00A0C967A2D1} |
| Svetlana, Ruso, L&H TTS3000              | {06377F80-D48E-11d1-B17B-0020AFED142E} |
| Boris, Ruso, L&H TTS3000                 | {06377F81-D48E-11d1-B17B-0020AFED142E} |
| Carmen, español, L&H TTS3000                | {2CE326E0-A935-11d1-B17B-0020AFED142E} |
| Julio, español, L&H TTS3000                 | {2CE326E1-A935-11d1-B17B-0020AFED142E} |



 

> [!Note]  
> Existe una diferencia entre el CLSID de instalación de un motor de voz y su identificador de modo. Del mismo modo, un motor de voz también tiene un identificador de motor, pero este identificador no es aplicable en la API del agente.

 

 

 