---
description: La plataforma de Tablet PC admite una serie de Factoids que se usan para aumentar la precisión del reconocimiento.
ms.assetid: 9d5fc370-ba58-438b-8850-f31f0f0f6608
title: Factoids admitido de la versión 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad6d08b91a457d38a3eb8543200eb1919eb2bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678493"
---
# <a name="supported-factoids-from-version-1"></a>Factoids admitido de la versión 1

\[Tenga en cuenta que la siguiente descripción de Factoids admitida en la versión 1 del kit de desarrollo de software (SDK) de Microsoft Windows XP Tablet PC Edition todavía es compatible con los reconocedores, pero se recomienda que todos los nuevos desarrollos (para los reconocedores de scripts latinos) usen los valores definidos en la enumeración [InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope) .\]

La plataforma de Tablet PC admite una serie de Factoids que se usan para aumentar la precisión del reconocimiento. Cuando se usa Factoids, es importante que la entrada esperada coincida exactamente con la definición de Factoid. Si la entrada no coincide con la definición de Factoid, la precisión del reconocimiento se ve afectada. Por ejemplo, si se establece el **número** Factoid y el usuario escribe letras, la precisión del reconocimiento de las letras es deficiente.

Ciertos Factoids, como el **correo electrónico** y el **dígito**, son casi idénticos en todos los idiomas. Otros Factoids, como **teléfono** y **CódigoPostal**, varían según el idioma. Examine el formato de cada Factoid para el idioma que está usando. Puede encontrar una lista de formatos para cada Factoid en cada idioma en las tablas de los temas que se indican a continuación de este tema.

> [!Note]  
> Existe una diferencia sutil pero importante entre Factoids para los idiomas occidentales y Factoids para los idiomas de Asia oriental. Factoids para idiomas occidentales se implementa mediante expresiones que describen el resultado deseado. Después, el reconocedor se sesga para generar resultados que coincidan con esta expresión. Factoids para idiomas de Asia oriental se implementan mediante la especificación de un intervalo aceptable de caracteres Unicode. Por ejemplo, la **fecha** Factoid para los idiomas de Asia oriental solo acepta caracteres Unicode dentro de un intervalo determinado.

 

Factoids para idiomas occidentales incluyen Factoids para inglés (Reino Unido), Inglés (Estados Unidos), Francés, alemán y español. Factoids para idiomas de Asia oriental son Factoids para chino (simplificado), Chino (tradicional), Japonés y coreano.

En las secciones siguientes se muestran los formatos admitidos para cada Factoid en cada idioma:

-   [Factoids común entre idiomas](factoids-common-across-languages.md)
-   [Factoids para idiomas occidentales](factoids-for-western-languages.md)
-   [Factoids para idiomas de Asia oriental](factoids-for-east-asian-languages.md)

Si espera que la entrada sea diferente de los formatos enumerados en las tablas de estas secciones, no use un Factoid. Además, los Factoids están integrados en el reconocedor para cada idioma. No se puede usar Factoids desde un idioma con un reconocedor de otro idioma. Por ejemplo, no puede usar el **teléfono** francés Factoid con un reconocedor japonés.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Constantes de Factoid**](factoid-constants.md)
</dt> <dt>

[Clase Microsoft. Ink. Factoid](/previous-versions/ms583657(v=vs.100))
</dt> </dl>

 

 
