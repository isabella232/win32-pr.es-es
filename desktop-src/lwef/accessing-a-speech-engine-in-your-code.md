---
title: Acceso a un motor de voz en el código
description: Acceso a un motor de voz en el código
ms.assetid: ddfe0552-a29e-4ce4-b608-c131efbe300b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d81841f6f287d36a6ac01fa77294b1754eeb9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474279"
---
# <a name="accessing-a-speech-engine-in-your-code"></a>Acceso a un motor de voz en el código

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Para usar un motor de voz determinado en el código, use la API del agente para establecer el motor. Para los motores de entrada de voz, use [**SRModeID**](https://www.bing.com/search?q=**SRModeID**)y especifique el identificador de modo para el motor. Sin embargo, tenga en cuenta que el motor debe estar instalado. Para determinar si el motor está presente, puede consultar **SRModeID**. El motor debe coincidir con la configuración [**de LanguageID del**](https://www.bing.com/search?q=**LanguageID**) carácter. Por ejemplo, no puede establecer **SRModeID en un** identificador de modo del motor de reconocimiento de voz alemán para un carácter cuyo **LanguageID** sea francés.

**IDs del modo del motor de entrada de voz**



| Voz                                    | IDs de modo                             |
|------------------------------------------|--------------------------------------|
| Microsoft Speech Recognition Engine v4.0 | {D8905400-B5C8-11D0-B968020AFDB1B9C} |



 

Compruebe y establezca [**languageID**](https://www.bing.com/search?q=**LanguageID**) y [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) del carácter en el código antes de intentar definir la gramática de los parámetros de voz de los objetos **Command** de la aplicación. Considere también la posibilidad de comprobar el explorador o el idioma del sistema para que pueda estar seguro de que coincide con la configuración de los usuarios. El motor puede producir un error si intenta definir una gramática para un idioma que el motor no coincide.

Un juego de caracteres para la salida de texto a voz (TTS) se puede compilar con una preferencia de identificador de modo del motor de salida de voz predeterminada. Cuando se carga el carácter, si el motor está instalado y coincide con el [**LanguageID**](https://www.bing.com/search?q=**LanguageID**)del carácter, el Agente intentará cargar ese identificador de modo para la salida de voz. Si el motor no está presente o tiene un **LanguageID** diferente, el Agente intentará cargar el primer identificador de modo que encuentre que coincida con el **LanguageID** del carácter, pero sigue estableciendo la velocidad compilada y la configuración de tono del carácter.

Tenga en cuenta que, dado que todos los caracteres proporcionados por Microsoft Agent se compilan para usar el motor inglés de Lernout & Pie TruVoice American como motor de salida de voz predeterminado, la velocidad y la configuración de tono de los caracteres se optimizan para este idioma y motor. Por lo tanto, cuando se usan otros motores de TTS o motores de otros lenguajes, es posible que los caracteres no hablen a la velocidad o el tono óptimos. Aunque la aplicación o página web no puede escribir los valores de propiedad [**Pitch**](/previous-versions/ms809428(v=msdn.10)) y [**Speed,**](https://www.bing.com/search?q=**Speed**) puede incluir etiquetas [Pit](pit-tag.md) (pitch) y [Spd](spd-tag.md) (speed) en el texto de salida que cambiarán temporalmente el tono y la velocidad de una expresión determinada. Sin embargo, el uso de las etiquetas Pit y Spd no cambiará las propiedades **Pitch** **y Speed.** Consulte [Programación del control de Microsoft Agent y](programming-the-microsoft-agent-control.md) las etiquetas de salida de voz de Microsoft [Agent](microsoft-agent-speech-output-tags.md) para obtener más información.

También debe instalar los archivos binarios en tiempo de ejecución de SAPI 4.0a (SPCHAPI.exe) al usar otros motores TTS compatibles con SAPI que el motor L&H TruVoice American English con los caracteres proporcionados por Microsoft Agent para que los motores se enumere correctamente. En la página web, incluya la siguiente etiqueta Object para instalar automáticamente el componente:

``` syntax
<OBJECT width=0 height=0
CLASSID="CLSID:0C7F3F20-8BAB-11d2-9432-00C04F8EF48F"
CODEBASE="#VERSION=4,0,0,0">
</OBJECT>
```

Para consultar o establecer el identificador de modo de un motor, use [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**). Con **TTSModeID** puede establecer un identificador de modo diferente del [**languageID del carácter.**](https://www.bing.com/search?q=**LanguageID**) Por ejemplo, puede establecer un carácter en alemán para que hable con un identificador de modo francés. Los IDs del modo de salida de voz no solo definen qué motor se usa, sino que también se corresponden con voces específicas compatibles con un motor. También puede usar el Editor de caracteres de Microsoft Agent o las herramientas incluidas en la documentación del SDK de Voz de [Microsoft](https://msdn.microsoft.com/library/ee705648.aspx) para consultar los IDs de modo de los motores de TTS instalados en el sistema.

**IDs del modo de salida de voz**



| Voz                                       | IDs de modo                               |
|---------------------------------------------|----------------------------------------|
| Adult Female \# 1, US English, L&H TruVoice  | {CA141FD0-AC7F-11D1-97A3-006008273008} |
| Adult Female \# 2, US English, L&H TruVoice  | {CA141FD0-AC7F-11D1-97A3-006008273009} |
| Adult Male \# 1, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273000} |
| Adult Male \# 2, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273001} |
| Adult Male \# 3, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273002} |
| Adult Male \# 4, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273003} |
| Adult Male \# 5, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273004} |
| Adult Male \# 6, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273005} |
| Adult Male \# 7, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273006} |
| Adult Male \# 8, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273007} |
| Carol, inglés inglés, L&H TTS3000         | {227A0E40-A92A-11d1-B17B-0020AFED142E} |
| Peter, inglés inglés, L&H TTS3000         | {227A0E41-A92A-11d1-B17B-0020AFED142E} |
| Hala, Neerlandés, L&H TTS3000                   | {A0DDCA40-A92C-11d1-B17B-0020AFED142E} |
| Alexander, Dutch, L&H TTS3000               | {A0DDCA41-A92C-11d1-B17B-0020AFED142E} |
| Sincronizaronique, Francés, L&H TTS3000              | {0879A4E0-A92C-11d1-B17B-0020AFED142E} |
| Frances, L&H TTS3000                 | {0879A4E1-A92C-11d1-B17B-0020AFED142E} |
| Anna, German, L&H TTS3000                   | {3A1FB760-A92B-11d1-B17B-0020AFED142E} |
| Stefan, German, L&H TTS3000                 | {3A1FB761-A92B-11d1-B17B-0020AFED142E} |
| Ángela, Italiano, L&H TTS3000               | {7EF71700-A92D-11d1-B17B-0020AFED142E} |
| Hora, Italiano, L&H TTS3000               | {7EF71701-A92D-11d1-B17B-0020AFED142E} |
| Nako, Japonés, L&H TTS3000                | {A778E060-A936-11d1-B17B-0020AFED142E} |
| Kenji, Japonés, L&H TTS3000                | {A778E061-A936-11d1-B17B-0020AFED142E} |
| Nila-Ah, Coreano, L&H TTS3000                | {12E0B720-A936-11d1-B17B-0020AFED142E} |
| Jun-Ho, coreano, L&H TTS3000                 | {12E0B721-A936-11d1-B17B-0020AFED142E} |
| Pauloa, Portugués (Brasil), L&H TTS3000   | {8AA08CA0-A1AE-11d3-9BC5-00A0C967A2D1} |
| Paulo, Portugués (Brasil), L&H TTS3000 | {8AA08CA1-A1AE-11d3-9BC5-00A0C967A2D1} |
| Sfplana, Ruso, L&H TTS3000              | {06377F80-D48E-11d1-B17B-0020AFED142E} |
| Boris, Russian, L&H TTS3000                 | {06377F81-D48E-11d1-B17B-0020AFED142E} |
| Así, Español, L&H TTS3000                | {2CE326E0-A935-11d1-B17B-0020AFED142E} |
| Julio, Español, L&H TTS3000                 | {2CE326E1-A935-11d1-B17B-0020AFED142E} |



 

> [!Note]  
> Hay una diferencia entre el CLSID de instalación de un motor de voz y su identificador de modo. Del mismo modo, un motor de voz también tiene un identificador de motor, pero este identificador no es aplicable en la API del agente.

 

 

 