---
description: Tablet PC Platform admite una serie de factoids que se usan para aumentar la precisión del reconocimiento.
ms.assetid: 9d5fc370-ba58-438b-8850-f31f0f0f6608
title: Factoids admitidos de la versión 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c24c192bcbda04be7ea25deb0c7b1cb7b392de57c43ce7a509e0ceaac31002
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934355"
---
# <a name="supported-factoids-from-version-1"></a>Factoids admitidos de la versión 1

\[Tenga en cuenta la siguiente descripción de los factoids admitidos en la versión 1 del Kit de desarrollo de software (SDK) de Microsoft Windows XP Tablet PC Edition, pero se recomienda que todos los nuevos desarrollos (para reconocedores de scripts latinos) usen los valores definidos en la enumeración [InputScope.](/windows/win32/api/inputscope/ne-inputscope-inputscope)\]

Tablet PC Platform admite una serie de factoids que se usan para aumentar la precisión del reconocimiento. Al usar factoids, es importante que la entrada esperada coincida exactamente con la definición del factoid. Si la entrada no coincide con la definición del factoid, se sufre la precisión del reconocimiento. Por ejemplo, si se **establece el** factoid Number y el usuario escribe letras, la precisión del reconocimiento de las letras es deficiente.

Ciertos factoids, como **correo electrónico** y **dígito,** son casi idénticos en todos los idiomas. Otros factoids, como **Telephone y** **PostalCode,** varían según el idioma. Examine el formato de cada factoid para ver el idioma que está usando. Puede encontrar una lista de formatos para cada factoid en cada lenguaje en las tablas de los temas siguientes a este tema.

> [!Note]  
> Hay una distinción sutil pero importante entre factoids para idiomas del oeste y factoids para idiomas de Asia Oriental. Los factoids para idiomas occidental se implementan mediante expresiones que describen el resultado deseado. A continuación, el reconocedor se sesgado para generar resultados que coincidan con esta expresión. Los factoids para idiomas de Asia Oriental se implementan especificando un intervalo aceptable de caracteres Unicode. Por ejemplo, el **factoid Date** para idiomas de Asia Oriental acepta solo caracteres Unicode dentro de un intervalo determinado.

 

Los factoids para idiomas del oeste incluyen factoids para inglés (Reino Unido), inglés (Estados Unidos), francés, alemán y español. Los factoids para idiomas de Asia Oriental incluyen factoids para chino (simplificado), chino (tradicional), japonés y coreano.

En las secciones siguientes se muestran los formatos admitidos para cada factoid en cada idioma:

-   [Factoids Common Across Languages](factoids-common-across-languages.md)
-   [Factoids for Western Languages](factoids-for-western-languages.md)
-   [Factoids para idiomas de Asia Oriental](factoids-for-east-asian-languages.md)

Si espera una entrada diferente de los formatos enumerados en las tablas de estas secciones, no use un factoid. Además, los factoids están integrados en el reconocedor para cada idioma. No se pueden usar factoids de un idioma con un reconocedor de otro idioma. Por ejemplo, no puede usar el factoid **teléfono** francés con un reconocedor japonés.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Constantes factoid**](factoid-constants.md)
</dt> <dt>

[Clase Microsoft.Ink.Factoid](/previous-versions/ms583657(v=vs.100))
</dt> </dl>

 

 
