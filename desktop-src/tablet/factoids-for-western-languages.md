---
description: Los idiomas occidentales se definen como inglés (Reino Unido), Inglés (Estados Unidos), Francés, alemán y español.
ms.assetid: d4728506-7484-4c4c-a5ae-e98d699f7e76
title: Factoids para idiomas occidentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de98cfce0203a2a3a94509d6586c1596390ca16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082163"
---
# <a name="factoids-for-western-languages"></a>Factoids para idiomas occidentales

Los idiomas occidentales se definen como inglés (Reino Unido), Inglés (Estados Unidos), Francés, alemán y español. Los formatos de cada Factoid que se muestran en la tabla siguiente son específicos para el reconocedor de cada idioma. Por ejemplo, el **teléfono** Factoid es diferente en cada idioma. Además, cada Factoid es específico de un reconocedor determinado. Por ejemplo, el **teléfono** francés Factoid solo se puede usar con el reconocedor francés.

> [!Note]  
> Además de los siguientes Factoids, todos los lenguajes usan el Factoids indicado en [Factoids común](factoids-common-across-languages.md)en todos los idiomas.

 



| Factoid              | Definición                                                                                                                                                                                                                                                                                                                                                                                                           | Ejemplos                                                                                                                                                                                                                                                            |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nombre de archivo**         | Establece el sesgo para una ruta de acceso de nombre de archivo. El nombre no puede incluir los caracteres<br/> /" < > \|<br/> Los caracteres \* y? se incluyen en este Factoid para habilitar la búsqueda. Además, los caracteres extendidos se admiten en idiomas europeos.<br/>                                                                                                                                                    | c:<br/> \\\\directoryname \\ nombre de archivo<br/> \\\\directory1 \\ directory2 \\ nombreDeArchivo<br/> \\\\directoryname \\ \* .\*<br/> nombre de archivo.?<br/> myfile.doc<br/>                                                                                |
| **SystemDictionary** | Habilita solo el Diccionario del sistema. Esto resulta útil si una aplicación consulta si una palabra está en el Diccionario del sistema. Establezca Factoid en **SystemDictionary** y llame al método [**IsStringSupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported) .<br/>                                                                                                                                                 | El modelo de lenguaje predeterminado incluye la gramática del idioma, así como el Diccionario del sistema. Este Factoid sesga el reconocimiento hacia solo las palabras que se producen en el Diccionario del sistema. Cada idioma tiene su propio diccionario del sistema.<br/>                   |
| **Palabras**         | Habilita solo la lista de palabras. Si el valor de Factoid está establecido en lista de **palabras** pero no se ha asignado ninguna lista de palabras a [**InkRecognizerContext**](inkrecognizercontext-class.md) ([RecognizerContext](/previous-versions/ms552546(v=vs.100)) en código administrado), se usa el Diccionario de usuario. Para obtener más información sobre las listas de palabras y los diccionarios, vea [uso de diccionarios de aplicación](using-application-dictionaries.md).<br/> | Este Factoid sesga el reconocedor para que solo devuelva palabras de la lista de palabras. Por ejemplo, para permitir que el usuario escriba un color en un formulario, puede usar este Factoid y una lista de palabras que contenga "verde", "rojo", "azul", "blanco" y otros colores.<br/> |



 

Las siguientes combinaciones de Factoids solo se admiten para idiomas occidentales. Otras combinaciones de Factoids no se admiten en esta versión de las interfaces de programación de aplicaciones (API) de plataforma de Tablet PC. Estas combinaciones Factoid emplean un operador **or** lógico, por lo que la entrada puede coincidir con cualquiera de los Factoids de la expresión.



| Combinación de Factoid     | Definición                                                                   |
|-------------------------|------------------------------------------------------------------------------|
| **WebWordList**         | La Factoid **Web** o la lista de palabras.<br/>                             |
| **EmailWordList**       | Factoid de **correo electrónico** o la lista de palabras.<br/>                           |
| **FilenameWebWordList** | El **nombre de archivo** Factoid o la Factoid **Web** o la lista de palabras.<br/> |



 

En los temas siguientes se muestran los formatos admitidos para cada idioma occidental.

-   [Inglés (en todo el mundo) Factoids](english--worldwide--factoids.md)
-   [Inglés (Estados Unidos) Factoids](english--united-states--factoids.md)
-   [Francés Factoids](french-factoids.md)
-   [Alemán Factoids](german-factoids.md)
-   [Factoids Español](spanish-factoids.md)

 

