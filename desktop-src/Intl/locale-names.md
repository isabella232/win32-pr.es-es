---
description: Un nombre de configuración regional se basa en las convenciones de etiquetado de idioma de RFC 4646 (Windows Vista y versiones posteriores) y se representa mediante LOCALE \_ SNAME.
ms.assetid: 221aae7b-3a7c-4995-ae78-50d97de436d8
title: Nombres de configuración regional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9808db94615cba4416c12995b9c969eaaf5a3fee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274436"
---
# <a name="locale-names"></a>Nombres de configuración regional

Un [nombre de configuración](locales-and-languages.md) regional se basa en las convenciones de etiquetado de idioma de RFC 4646 (Windows Vista y versiones posteriores) y se representa mediante [LOCALE \_ SNAME](locale-sname.md). Por lo general, se usa `<language>-<REGION>` el patrón . En este caso, el idioma es un código de idioma ISO 639 en minúsculas. Los códigos de ISO 639-1 se usan cuando están disponibles. De lo contrario, se usan códigos de ISO 639-2/T. REGION especifica un identificador de país o región ISO 3166-1 en mayúsculas. Por ejemplo, el nombre de la configuración regional para inglés (Estados Unidos) es "en-US" y el nombre de la configuración regional de Divehi (Vervas) es "dv-MV".

> [!Note]  
> La constante [LOCALE \_ NAME MAX \_ \_ LENGTH](locale-name-constants.md) proporciona la longitud máxima de un nombre de configuración regional. Incluye espacio para un carácter nulo de terminación.

 

Si la configuración regional es una configuración regional neutra (sin región), el valor [ \_ SNAME de LOCALE](locale-sname.md) sigue el patrón `<language>` . Si es una configuración regional neutra para la que el script es significativo, el patrón es `<language>-<Script>` .

Si una configuración regional debe distinguirse de otra configuración regional para el mismo idioma y región mediante un script diferente, el valor de LOCALE SNAME sigue el patrón , donde Script es un código de \_ `<language>-<Script>-<REGION>` script ISO [15924](https://www.unicode.org/iso15924/iso15924-codes.html) en mayúsculas iniciales. Por ejemplo, el valor de LOCALE SNAME para la configuración regional específica \_ Uzuzuz (latino, uz-Latn-UZ) es "uz-Latn-UZ". El componente de script no se incluye en los casos en los que un lenguaje se escribe normalmente en un solo script.

Los criterio de ordenación de las configuraciones regionales se designan mediante [identificadores de criterio de](sort-order-identifiers.md)ordenación, por ejemplo, SORT \_ DEFAULT. Para distinguir dos o más ordenaciones para el mismo idioma y región, el nombre de la configuración regional sigue el patrón `<language>-<REGION>\_<sort order>` . Si debe distinguir el script y el criterio de ordenación, el nombre sigue el patrón `<language>-<Script>-<REGION>\_<sort order>` . El criterio de ordenación predeterminado nunca se especifica explícitamente, solo el criterio de ordenación alternativo. Por ejemplo, el húngaro (húngaro) con SORT DEFAULT o el equivalente numéricamente SORT HUNGARIAN DEFAULT se \_ \_ \_ designa como "hu-HU". Se designa \_ \_ "hu-HU technl" al húngaro (húngaro) con el criterio de ordenación SORT HUNGARIAN \_ TECHNICAL.

Para una [configuración regional de reemplazo](custom-locales.md), el nombre de la configuración regional debe ser el mismo que el nombre de la configuración regional que se va a reemplazar. Para una configuración regional complementaria, el nombre de la configuración regional debe seguir el patrón de o , donde es una cadena `<language>-<REGION>-x-<custom>` `<language>-<Script>-<REGION>-x-<custom>` alfanumérica específica de la configuración regional `<custom>` complementaria. Por ejemplo, una configuración regional complementaria específica de una empresa llamada Fabricam podría denominarse "en-US-x-fabricam".

Una aplicación puede recuperar los nombres de configuración regional actuales mediante las funciones [**GetSystemDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlocalename) y [**GetUserDefaultLocaleName.**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename) Aunque cada subproceso puede recuperar y establecer su propio identificador de configuración regional con [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale) y establecerlo con [**SetThreadLocale,**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)no hay ninguna función análoga para obtener y establecer la configuración regional por nombre.

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

 

 



