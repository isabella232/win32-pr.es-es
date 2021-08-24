---
title: Instrucción VarFileInfo BLOCK
description: Describe la forma del bloque de información de variable.
ms.assetid: 81c7f5df-78fa-4571-9dad-a6c3e932471e
keywords:
- Menús de instrucción VarFileInfo BLOCK y otros recursos
topic_type:
- apiref
api_name:
- VarFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e15b4bf57a14d6bae6dd5b83c8ea86e38830113fbcfbbaa27b143bf02bb130e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846975"
---
# <a name="varfileinfo-block-statement"></a>Instrucción VarFileInfo BLOCK

Define un bloque de información de variables.

``` syntax
BLOCK "VarFileInfo" { VALUE "Translation", langID, charsetID . . . }
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*
</dt> <dd>

Uno de los identificadores de idioma especificados en la sección Comentarios.

</dd> <dt>

<span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*
</dt> <dd>

Uno de los identificadores de juego de caracteres especificados en la sección Comentarios.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Se puede proporcionar más de un par de identificadores, pero cada par debe estar separado del par anterior con una coma.

El *parámetro langID* especifica uno de los siguientes códigos de idioma.



| Código   | Idioma            | Código   | Idioma                  |
|--------|---------------------|--------|---------------------------|
| 0x0401 | Árabe              | 0x0415 | Polaco                    |
| 0x0402 | Búlgaro           | 0x0416 | Portugués (Brasil)       |
| 0x0403 | Catalán             | 0x0417 | Rhaeto-Romanic            |
| 0x0404 | Chino tradicional | 0x0418 | Rumano                  |
| 0x0405 | Checo               | 0x0419 | Ruso                   |
| 0x0406 | Danés              | 0x041A | Croato-Serbian (latino)    |
| 0x0407 | Alemán              | 0x041B | Eslovaco                    |
| 0x0408 | Griego               | 0x041C | Albanés                  |
| 0x0409 | Inglés de EE. UU.        | 0x041D | Sueco                   |
| 0x040A | Español en español   | 0x041E | Tailandés                      |
| 0x040B | Finés             | 0x041F | Turco                   |
| 0x040C | Francés              | 0x0420 | Urdu                      |
| 0x040D | Hebreo              | 0x0421 | Bahasa                    |
| 0x040E | Húngaro           | 0x0804 | Chino simplificado        |
| 0x040F | Islandés           | 0x0807 | Alemán suizo              |
| 0x0410 | Italiano             | 0x0809 | Reino Unido Inglés              |
| 0x0411 | Japonés            | 0x080A | Español (México)          |
| 0x0412 | Coreano              | 0x080C | Francés belga            |
| 0x0413 | Neerlandés               | 0x0C0C | Francés canadiense           |
| 0x0414 | Noruego: Bokmal  | 0x100C | Francés suizo              |
| 0x0810 | Italiano de Suiza       | 0x0816 | Portugués (Portugal)     |
| 0x0813 | Neerlandés neerland       | 0x081A | Serbo-Croatian (cirílico) |
| 0x0814 | Noruego: Nyno norwegian | ?      | ?                         |



 

El *parámetro charsetID* especifica uno de los siguientes identificadores de juego de caracteres:



| Identificador | Juego de caracteres              |
|------------|----------------------------|
| 0          | ASCII de 7 bits                |
| 932        | Japón (Shift – JIS X-0208) |
| 949        | Corea (Mayús – KSC 5601)   |
| 950        | Taiwán (Big5)              |
| 1200       | Unicode                    |
| 1250       | Latin-2 (Europa Oriental) |
| 1251       | Cirílico                   |
| 1252       | Multilingüe               |
| 1253       | Griego                      |
| 1254       | Turco                    |
| 1255       | Hebreo                     |
| 1256       | Árabe                     |



 

 

 




