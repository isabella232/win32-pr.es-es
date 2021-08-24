---
description: Los idiomas occidental se definen como inglés (Reino Unido), inglés (Estados Unidos), francés, alemán y español.
ms.assetid: d4728506-7484-4c4c-a5ae-e98d699f7e76
title: Factoids for Western Languages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e417c9662252213d761760a1486f9808a2d18bc3236073fe8c8d7746c396beb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936545"
---
# <a name="factoids-for-western-languages"></a>Factoids for Western Languages

Los idiomas occidental se definen como inglés (Reino Unido), inglés (Estados Unidos), francés, alemán y español. Los formatos de cada factoid que se muestran en la tabla siguiente son específicos del reconocedor de cada idioma. Por ejemplo, el **factoid De** teléfono es diferente en cada idioma. Además, cada factoid es específico de un reconocedor determinado. Por ejemplo, el factoid **de teléfono** francés solo se puede usar con el reconocedor francés.

> [!Note]  
> Además de los siguientes factoids, todos los lenguajes usan los factoids enumerados en [Factoids Common Across Languages](factoids-common-across-languages.md).

 



| Factoid              | Definición                                                                                                                                                                                                                                                                                                                                                                                                           | Ejemplos                                                                                                                                                                                                                                                            |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nombre de archivo**         | Establece el sesgo de una ruta de acceso de nombre de archivo. El nombre no puede incluir los caracteres<br/> / " < > \|<br/> Los caracteres \* y ? se incluyen en este factoid para habilitar la búsqueda. Además, se admiten caracteres extendidos en idiomas europeos.<br/>                                                                                                                                                    | c:<br/> \\\\nombre de directorio \\ nombrearchivo<br/> \\\\directory1 \\ directory2 \\ filename<br/> \\\\directoryname \\ \* .\*<br/> ¿Nombre.?<br/> myfile.doc<br/>                                                                                |
| **SystemDictionary** | Habilita solo el diccionario del sistema. Esto resulta útil si una aplicación consulta si una palabra está en el diccionario del sistema. Establezca factoid en **SystemDictionary y** llame al [**método IsStringSupported.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported)<br/>                                                                                                                                                 | El modelo de lenguaje predeterminado incluye la gramática del idioma, así como el diccionario del sistema. Este factoid sesgo el reconocimiento solo hacia las palabras que aparecen en el diccionario del sistema. Cada lenguaje tiene su propio diccionario del sistema.<br/>                   |
| **WordList**         | Habilita solo la lista de palabras. Si el elemento factoid está establecido en **WordList** pero no se asigna ninguna lista de palabras a [**InkRecognizerContext**](inkrecognizercontext-class.md) [(RecognizerContext](/previous-versions/ms552546(v=vs.100)) en código administrado), se usa el diccionario de usuarios. Para obtener más información sobre listas de palabras y diccionarios, vea [Using Application Dictionaries](using-application-dictionaries.md).<br/> | Esta factoid sesgo el reconocedor para devolver solo las palabras de la lista de palabras. Por ejemplo, para permitir que el usuario escriba un color en un formulario, puede usar este factoid y una lista de palabras que contenga "Verde", "Rojo", "Azul", "Blanco" y otros colores.<br/> |



 

Las siguientes combinaciones de factoids solo se admiten en idiomas del oeste. No se admiten otras combinaciones de factoids en esta versión de las interfaces de programación de aplicaciones (API) de la plataforma tablet PC. Estas combinaciones de factoid emplean un operador **LÓGICO OR,** por lo que la entrada puede coincidir con cualquiera de los factoids de la expresión.



| Combinación de factoid     | Definición                                                                   |
|-------------------------|------------------------------------------------------------------------------|
| **WebWordList**         | El **elemento factoid** web o la lista de palabras.<br/>                             |
| **EmailWordList**       | El **factoid** email o la lista de palabras.<br/>                           |
| **FilenameWebWordList** | El **factoid** nombre de archivo, **el factoid web** o la lista de palabras.<br/> |



 

En los temas siguientes se muestran los formatos admitidos para cada idioma occidental.

-   [Factoids en inglés (en todo el mundo)](english--worldwide--factoids.md)
-   [Inglés (Estados Unidos) Factoids](english--united-states--factoids.md)
-   [Factoids francés](french-factoids.md)
-   [Factoids en alemán](german-factoids.md)
-   [Factoids español](spanish-factoids.md)

 

