---
description: Recuperar y establecer información de configuración regional
ms.assetid: 7675f826-76be-4361-a82c-9573040a7e72
title: Recuperar y establecer información de configuración regional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f9faa8749073016862587330776f32e65749b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171954"
---
# <a name="retrieving-and-setting-locale-information"></a>Recuperar y establecer información de configuración regional

La aplicación debe poder recuperar y establecer información específica sobre las [configuraciones regionales y los idiomas disponibles.](locales-and-languages.md) Cada elemento de información de configuración regional, como el nombre de un día determinado de la semana o el carácter utilizado como separador decimal, tiene una constante correspondiente. Las constantes disponibles se definen en [Constantes de información de configuración regional.](locale-information-constants.md)

La aplicación siempre almacena y manipula la información de configuración regional como una cadena terminada en NULL. No se permite ningún dato binario y los valores numéricos deben especificarse como texto. Cada tipo de información tiene un formato determinado. Además, varios tipos están vinculados entre sí para que cambiar un tipo cambie también el valor del otro tipo.

Para recuperar información de configuración regional, la aplicación llama a [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx con**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) la constante que corresponde a la información necesaria. La aplicación puede llamar a [**SetLocaleInfo para**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) establecer un elemento de información de configuración regional.

> [!Note]  
> Aunque es [posible que se admite](locale-identifiers.md) un identificador de configuración regional, no está disponible para su uso por una aplicación a menos que también esté instalada la configuración regional correspondiente.

 

Puesto que la mayoría de las constantes de información de configuración regional son mutuamente excluyentes, solo se puede controlar un tipo de información a la vez. Las excepciones a esta regla son [LOCALE \_ USE CP \_ \_ ACP](locale-use-cp-acp.md), [LOCALE RETURN \_ \_ NUMBER](locale-return-constants.md)y [LOCALE \_ NOUSEROVERRIDE,](locale-nouseroverride.md)que se pueden combinar con otras constantes mediante un binario OR.

> [!Caution]  
> No se recomienda encarecidamente el uso de \_ LOCALE NOUSEROVERRIDE, ya que deshabilita las preferencias del usuario.

 

Al igual que una serie de aplicaciones, por ejemplo Microsoft Active Directory, la aplicación puede mantener sus cadenas en una base de datos ordenable. Para obtener más información, vea [Control de la ordenación en las aplicaciones.](handling-sorting-in-your-applications.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la compatibilidad con idiomas nacionales](using-national-language-support.md)
</dt> <dt>

[Constantes de información de configuración regional](locale-information-constants.md)
</dt> <dt>

[Control de la ordenación en las aplicaciones](handling-sorting-in-your-applications.md)
</dt> <dt>

[Trabajar con configuraciones regionales personalizadas](working-with-custom-locales.md)
</dt> </dl>

 

 



