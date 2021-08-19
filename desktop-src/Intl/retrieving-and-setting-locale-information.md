---
description: Recuperar y establecer información de configuración regional
ms.assetid: 7675f826-76be-4361-a82c-9573040a7e72
title: Recuperar y establecer información de configuración regional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d02c2bb58328529781309ce8284310acbcb6fb545ecdc076df295cd020344a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130315"
---
# <a name="retrieving-and-setting-locale-information"></a>Recuperar y establecer información de configuración regional

La aplicación debe poder recuperar y establecer información específica sobre las [configuraciones regionales y los idiomas disponibles.](locales-and-languages.md) Cada elemento de información de configuración regional, como el nombre de un día determinado de la semana o el carácter utilizado como separador decimal, tiene una constante correspondiente. Las constantes disponibles se definen en [Constantes de información de configuración regional](locale-information-constants.md).

La aplicación siempre almacena y manipula la información de configuración regional como una cadena terminada en NULL. No se permite ningún dato binario y los valores numéricos deben especificarse como texto. Cada tipo de información tiene un formato determinado. Además, varios tipos están vinculados entre sí para que cambiar un tipo cambie también el valor del otro tipo.

Para recuperar información de configuración regional, la aplicación llama a [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con la constante que corresponde a la información necesaria. La aplicación puede llamar a [**SetLocaleInfo para**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) establecer un elemento de información de configuración regional.

> [!Note]  
> Aunque es [posible que se admite](locale-identifiers.md) un identificador de configuración regional, no está disponible para su uso por parte de una aplicación a menos que también esté instalada la configuración regional correspondiente.

 

Dado que la mayoría de las constantes de información de configuración regional son mutuamente excluyentes, solo se puede controlar un tipo de información a la vez. Las excepciones a esta regla son [LOCALE \_ USE CP \_ \_ ACP,](locale-use-cp-acp.md) [LOCALE RETURN \_ \_ NUMBER](locale-return-constants.md)y [LOCALE \_ NOUSEROVERRIDE,](locale-nouseroverride.md)que se pueden combinar con otras constantes mediante un OR binario.

> [!Caution]  
> No se recomienda encarecidamente el uso de \_ LOCALE NOUSEROVERRIDE, ya que deshabilita las preferencias del usuario.

 

Al igual que varias aplicaciones, por ejemplo Microsoft Active Directory, la aplicación puede mantener sus cadenas en una base de datos que se puede ordenar. Para obtener más información, vea [Control de la ordenación en las aplicaciones.](handling-sorting-in-your-applications.md)

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

 

 



