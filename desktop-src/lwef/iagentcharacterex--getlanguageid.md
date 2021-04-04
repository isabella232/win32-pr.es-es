---
title: IAgentCharacterEx GetLanguageID
description: IAgentCharacterEx GetLanguageID
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9679538f93d779acc6272dccada824585c4449f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076079"
---
# <a name="iagentcharacterexgetlanguageid"></a>IAgentCharacterEx::GetLanguageID

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

Recupera el conjunto de IDENTIFICADOres de idioma para el carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*
</dt> <dd>

Dirección de una variable que recibe la configuración de identificador de idioma para el carácter.

</dd> </dl>

Entero largo que especifica el identificador de idioma del carácter. El identificador de idioma (LANGID) de un carácter es un valor de 16 bits definido por Windows, que consta de un identificador de idioma principal y un identificador de idioma secundario. Los ejemplos siguientes son valores para algunos idiomas. Para determinar los valores otros lenguajes, consulte la documentación del SDK de la plataforma.



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



 

Si no establece este identificador de idioma para el carácter, el ID. de idioma del carácter será el ID. de idioma del sistema actual.

Esta configuración también determina el idioma de la salida de TTS, el texto de globo de palabras, los comandos del menú emergente del carácter y el motor de reconocimiento de voz. Para determinar si hay un motor de reconocimiento de voz compatible disponible para el idioma del carácter, use [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md) o [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md).

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

> [!Note]  
> Si el identificador de idioma se establece en un idioma que admite texto bidireccional (como el árabe o el hebreo), pero el sistema que ejecuta la aplicación no tiene instalada la compatibilidad bidireccional, el texto aparecerá en el globo de palabras en lugar de en el orden de visualización.

 

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx: SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 




