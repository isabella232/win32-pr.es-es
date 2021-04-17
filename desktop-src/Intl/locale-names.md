---
description: Un nombre de configuración regional se basa en las convenciones de etiquetado de idioma de RFC 4646 (Windows Vista y versiones posteriores) y se representa mediante la configuración regional \_ SNAME.
ms.assetid: 221aae7b-3a7c-4995-ae78-50d97de436d8
title: Nombres de configuración regional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9808db94615cba4416c12995b9c969eaaf5a3fee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687937"
---
# <a name="locale-names"></a>Nombres de configuración regional

Un nombre de [configuración regional](locales-and-languages.md) se basa en las convenciones de etiquetado de idioma de RFC 4646 (Windows Vista y versiones posteriores) y se representa mediante la [configuración regional \_ SNAME](locale-sname.md). Normalmente, `<language>-<REGION>` se usa el patrón. Aquí, Language es un código de idioma ISO 639 en minúscula. Los códigos de ISO 639-1 se usan cuando están disponibles. De lo contrario, se usan códigos de ISO 639-2/T. REGIÓN especifica un identificador de país o región ISO 3166-1 en mayúsculas. Por ejemplo, el nombre de configuración regional para inglés (Estados Unidos) es "en-US" y el nombre de configuración regional de Divehi (Maldivas) es "DV-MV".

> [!Note]  
> La [longitud máxima del \_ nombre \_ \_ de configuración regional](locale-name-constants.md) constante proporciona la longitud máxima de un nombre de configuración regional. Incluye espacio para un carácter nulo de terminación.

 

Si la configuración regional es una configuración regional neutra (ninguna región), el valor de [ \_ SNAME de configuración regional](locale-sname.md) sigue el patrón `<language>` . Si se trata de una configuración regional neutra para la que el script es significativo, el patrón es `<language>-<Script>` .

Si una configuración regional se debe distinguir de otra configuración regional para el mismo idioma y región con un script diferente, el valor de SNAME de configuración regional \_ sigue el patrón `<language>-<Script>-<REGION>` , donde el script es un código de script [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html) de mayúscula inicial. Por ejemplo, el \_ valor de SNAME de configuración regional para la configuración regional específica uzbeko (latín, Uzbekistán) es "UZ-latn-UZ". El componente de script no se incluye en los casos en los que un lenguaje se escribe normalmente en un solo script.

Los criterios de ordenación de las configuraciones regionales se designan utilizando los identificadores de criterio de [ordenación](sort-order-identifiers.md), por ejemplo, ordenar \_ valores predeterminados. Para distinguir entre dos o más criterios de ordenación para el mismo idioma y región, el nombre de la configuración regional sigue el patrón `<language>-<REGION>\_<sort order>` . Si debe distinguir el script y el criterio de ordenación, el nombre sigue el patrón `<language>-<Script>-<REGION>\_<sort order>` . El criterio de ordenación predeterminado nunca se especifica explícitamente, solo el criterio de ordenación alternativo. Por ejemplo, Húngaro (Hungría) con \_ el valor predeterminado de Sort o la ordenación numéricamente equivalente, el \_ \_ valor predeterminado Húngaro se designa como "Hu-Hu". Húngaro (Hungría) con el criterio de ordenación el orden \_ Húngaro \_ técnico está designado como "HU-Hu \_ technl".

En el caso de una [configuración regional de reemplazo](custom-locales.md), el nombre de la configuración regional debe ser el mismo que el nombre de la configuración regional que se va a reemplazar. En el caso de una configuración regional complementaria, el nombre de la configuración regional debe seguir el patrón de `<language>-<REGION>-x-<custom>` o `<language>-<Script>-<REGION>-x-<custom>` , donde `<custom>` es una cadena alfanumérica específica de la configuración regional complementaria. Por ejemplo, una configuración regional complementaria específica de una empresa denominada Fabricam podría llamarse "en-US-x-Fabricam".

Una aplicación puede recuperar los nombres de configuración regional actuales mediante las funciones [**GetSystemDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlocalename) y [**GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename) . Aunque cada subproceso puede recuperar y establecer su propio identificador de configuración regional con [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale) y establecerlo con [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale), no hay funciones análogas para obtener y establecer la configuración regional por nombre.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuraciones regionales e idiomas](locales-and-languages.md)
</dt> <dt>

[Configuraciones regionales personalizadas](custom-locales.md)
</dt> <dt>

[Identificadores de configuración regional](locale-identifiers.md)
</dt> <dt>

[Identificadores de criterio de ordenación](sort-order-identifiers.md)
</dt> </dl>

 

 



