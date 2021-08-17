---
title: IAgentCharacterEx GetLanguageID
description: IAgentCharacterEx GetLanguageID
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0eeee052111ef0acbb843f4362ca0bfd3b40ab7d154ef0c46c43f6c2d0e0f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105553"
---
# <a name="iagentcharacterexgetlanguageid"></a>IAgentCharacterEx::GetLanguageID

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

Recupera el identificador de idioma establecido para el carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*
</dt> <dd>

Dirección de una variable que recibe la configuración del identificador de idioma para el carácter.

</dd> </dl>

Entero Long que especifica el identificador de idioma del carácter. El identificador de idioma (LANGID) de un carácter es un valor de 16 bits definido por Windows, que consta de un identificador de idioma principal y un identificador de idioma secundario. Los ejemplos siguientes son valores para algunos idiomas. Para determinar los valores de otros lenguajes, consulte la documentación del SDK de plataforma.



| Lenguaje              | ID     | Lenguaje              | ID     |
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



 

Si no establece este identificador de idioma para el carácter, el identificador de idioma del carácter será el identificador de idioma del sistema actual.

Esta configuración también determina el idioma de la salida de TTS, el texto del globo de palabras, los comandos del menú emergente del carácter y el motor de reconocimiento de voz. Para determinar si hay un motor de reconocimiento de voz compatible disponible para el lenguaje del carácter, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) o [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

> [!Note]  
> Si el identificador de idioma se establece en un idioma que admite texto bidireccional (como árabe o hebreo), pero el sistema que ejecuta la aplicación no tiene instalada la compatibilidad bidireccional, el texto aparecerá en el globo de palabras en orden lógico en lugar de mostrarse.

 

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx:SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 




