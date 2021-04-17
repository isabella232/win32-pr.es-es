---
description: Recuperar y establecer la información de configuración regional
ms.assetid: 7675f826-76be-4361-a82c-9573040a7e72
title: Recuperar y establecer la información de configuración regional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f9faa8749073016862587330776f32e65749b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686716"
---
# <a name="retrieving-and-setting-locale-information"></a>Recuperar y establecer la información de configuración regional

La aplicación debe poder recuperar y establecer información específica sobre los [idiomas y configuraciones regionales](locales-and-languages.md)disponibles. Cada elemento de información de configuración regional, como el nombre de un determinado día de la semana o el carácter que se usa como separador decimal, tiene una constante correspondiente. Las constantes disponibles se definen en [constantes de información de configuración regional](locale-information-constants.md).

La aplicación siempre almacena y manipula la información de configuración regional como una cadena terminada en NULL. No se permiten datos binarios, y los valores numéricos deben especificarse como texto. Cada tipo de información tiene un formato determinado. Además, se vinculan varios tipos juntos para que el cambio de un tipo cambie también el valor del otro tipo.

Para recuperar la información de configuración regional, la aplicación llama a [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con la constante que corresponde a la información requerida. La aplicación puede llamar a [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) para establecer un elemento de información de configuración regional.

> [!Note]  
> Aunque es posible que se admita un [identificador de configuración regional](locale-identifiers.md) , no está disponible para su uso por parte de una aplicación a menos que también esté instalada la configuración regional correspondiente.

 

Dado que la mayoría de las constantes de información de configuración regional se excluyen mutuamente, solo se puede controlar un tipo de información a la vez. Las excepciones a esta regla son la [configuración regional \_ use \_ CP \_ ACP](locale-use-cp-acp.md), el número de retorno de la [configuración regional \_ \_ ](locale-return-constants.md)y la [configuración regional \_ NOUSEROVERRIDE](locale-nouseroverride.md), que se pueden combinar con otras constantes mediante un binario o.

> [!Caution]  
> No se recomienda el uso de la configuración regional \_ NOUSEROVERRIDE ya que deshabilita las preferencias del usuario.

 

Al igual que una serie de aplicaciones, por ejemplo Microsoft Active Directory, la aplicación puede mantener sus cadenas en una base de datos ordenable. Para obtener más información, vea [controlar la ordenación en las aplicaciones](handling-sorting-in-your-applications.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la compatibilidad con National Language](using-national-language-support.md)
</dt> <dt>

[Constantes de información de configuración regional](locale-information-constants.md)
</dt> <dt>

[Controlar la ordenación en las aplicaciones](handling-sorting-in-your-applications.md)
</dt> <dt>

[Trabajar con configuraciones regionales personalizadas](working-with-custom-locales.md)
</dt> </dl>

 

 



