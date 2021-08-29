---
title: IAgentCharacterEx SetLanguageID
description: IAgentCharacterEx SetLanguageID
ms.assetid: 064f4c3c-1871-4372-9796-5b53f05c6d9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85eecd54f7642a0f82cef5fc8846c10b562f0474aa166beee7056e62782e780c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477861"
---
# <a name="iagentcharacterexsetlanguageid"></a>IAgentCharacterEx::SetLanguageID

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetLanguageID(
   long langID  // language ID setting of character
); 
```

Establece el identificador de idioma establecido para el carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*
</dt> <dd>

La configuración del identificador de idioma para el carácter.

</dd> </dl>

Entero Long que especifica el identificador de idioma del carácter. El identificador de idioma (LANGID) de un carácter es un valor de 16 bits definido por Windows, que consta de un identificador de idioma principal y un identificador de idioma secundario. Puede usar los siguientes valores para los idiomas especificados. Para más información, consulte la documentación de Platform SDK.



| Lenguaje              | ID     |  Lenguaje             | ID     |
|-----------------------|--------|-----------------------|--------|
| Árabe (Emiratos Árabes)        | 0x0401 | Italiano               | 0x0410 |
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
| Húngaro             | 0x040E |                       |        |



 

Si no establece el identificador de idioma del carácter, su identificador de idioma será el identificador de idioma del sistema actual si está instalado el archivo DLL de idioma del Agente correspondiente; De lo contrario, el idioma del carácter será inglés (EE. UU.).

Esta propiedad también determina el idioma del texto del globo de palabras, los comandos del menú emergente del carácter y el motor de reconocimiento de voz. También determina el idioma predeterminado para la salida de TTS. Para determinar si hay un motor de voz compatible disponible para el lenguaje del carácter, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) o [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).

Si intenta establecer el identificador de idioma de un carácter y los recursos de idioma del Agente, la página de códigos o una fuente de presentación para el identificador de idioma no está disponible, el Agente devuelve un error y el identificador de idioma del carácter permanece en su última configuración. Al establecer esta propiedad no se devuelve un error si no hay motores de voz que coincidan con el idioma.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

> [!Note]  
> Si establece el identificador de idioma del carácter en un idioma que admita texto bidireccional (como árabe o hebreo), pero el sistema que ejecuta la aplicación no tiene instalada la compatibilidad bidireccional, el texto aparecerá en el globo de palabras en orden lógico en lugar de mostrarse.

 

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx:GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 




