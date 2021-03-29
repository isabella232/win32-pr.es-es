---
title: IAgentCharacterEx SetLanguageID
description: IAgentCharacterEx SetLanguageID
ms.assetid: 064f4c3c-1871-4372-9796-5b53f05c6d9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec8a396c174fd251b1cc7ac8d7e9696c9b9f2d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774413"
---
# <a name="iagentcharacterexsetlanguageid"></a>IAgentCharacterEx::SetLanguageID

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetLanguageID(
   long langID  // language ID setting of character
); 
```

Establece el identificador de idioma establecido para el carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*ididioma*
</dt> <dd>

La configuración del identificador de idioma para el carácter.

</dd> </dl>

Entero largo que especifica el identificador de idioma del carácter. El identificador de idioma (LANGID) de un carácter es un valor de 16 bits definido por Windows, que consta de un identificador de idioma principal y un identificador de idioma secundario. Puede usar los siguientes valores para los idiomas especificados. Para obtener más información, consulte la documentación del SDK de la plataforma.



|                       |        |                       |        |
|-----------------------|--------|-----------------------|--------|
| Árabe (Arabia Saudí)        | 0x0401 | Italiano               | 0x0410 |
| Vasco                | 0x042d | Japonés              | 0x0411 |
| Chino (simplificado)  | 0x0804 | Coreano                | 0x0412 |
| Chino (tradicional) | 0x0404 | Noruego             | 0x0414 |
| Croata              | 0x041A | Polaco                | 0x0415 |
| Checo                 | 0x0405 | Portugués (Portugal) | 0x0816 |
| Danés                | 0x0406 | Portugués (Brasil)   | 0x0416 |
| Neerlandés                 | 0x0413 | Rumano              | 0x0418 |
| Inglés (Gran Bretaña)     | 0x0809 | Ruso               | 0x0419 |
| Inglés (EE.UU.)          | 0x0409 | Eslovaco             | 0x041B |
| Finés               | 0x040B | Esloveno             | 0x0424 |
| Francés                | 0x040C | Español               | 0x0C0A |
| Alemán                | 0x0407 | Sueco               | 0x041D |
| Griego                 | 0x0408 | Tailandés                  | 0x041E |
| Hebreo                | 0x040D | Turco               | 0x041F |
| Húngaro             | 0x040E |                       |        |



 

Si no establece el identificador de idioma para el carácter, su ID. de idioma será el ID. de idioma actual del sistema si está instalado el archivo DLL correspondiente del idioma del agente; de lo contrario, el idioma del carácter será inglés (EE. UU.).

Esta propiedad también determina el idioma del texto del globo de palabras, los comandos del menú emergente del carácter y el motor de reconocimiento de voz. También determina el idioma predeterminado para la salida de TTS. Para determinar si hay un motor de voz compatible disponible para el idioma del carácter, use [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md) o [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md).

Si intenta establecer el identificador de idioma para un carácter y los recursos de idioma del agente, la página de códigos o una fuente de presentación para el ID. de idioma no está disponible, el agente devuelve un error y el identificador de idioma del carácter permanece en su última configuración. Si se establece esta propiedad, no se devuelve un error si no hay ningún motor de voz coincidente para el idioma.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

> [!Note]  
> Si establece el identificador de idioma del carácter en un idioma que admite texto bidireccional (como el árabe o el hebreo), pero el sistema que ejecuta la aplicación no tiene instalada la compatibilidad bidireccional, el texto aparecerá en el globo de palabras en lugar de en el orden de presentación.

 

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx: GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 




