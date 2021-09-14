---
description: En este tema se proporcionan algunas instrucciones para controlar configuraciones regionales personalizadas en las aplicaciones.
ms.assetid: 2622e2b3-b952-4666-a440-85d73d11c5e0
title: Trabajar con configuraciones regionales personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab0e59446496ae2985860c0fd6b1bd5bddde084
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069804"
---
# <a name="working-with-custom-locales"></a>Trabajar con configuraciones regionales personalizadas

En este tema se proporcionan algunas instrucciones para controlar [configuraciones regionales personalizadas](custom-locales.md) en las aplicaciones. Es mejor preparar todo el código fuente con estas consideraciones en mente, ya que la aplicación no controla si las configuraciones regionales personalizadas están instaladas en el sistema operativo.

## <a name="handle-locale_stime-constant-correctly"></a>Controlar correctamente la \_ constante LOCALE STIME

Si tiene una aplicación anterior que usa [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) para obtener el separador de tiempo obsoleto indicado por [LOCALE \_ STIME](locale-stime-constants.md), la aplicación puede no analizar el formato de hora. Recuerde que el carácter que separa las horas de los minutos es distinto del carácter que separa los minutos de los segundos.

> [!Note]  
> Al programar para configuraciones regionales personalizadas, recuerde que son inusuales. Prácticamente todos los campos disponibles para NLS tienen que hacer frente a un comportamiento inusual. Por ejemplo, el formato de hora 12H34'12'' es legítimo y generalmente comprensible. Sin embargo, muchas aplicaciones hacen suposiciones sobre los separadores de tiempo que pueden interrumpir las longitudes del búfer o mostrar campos.

 

## <a name="distinguish-among-supplemental-locales"></a>Distinguir entre configuraciones regionales complementarias

Todas las configuraciones regionales complementarias usan la [ \_ constante LOCALE CUSTOM \_ UNSPECIFIED](locale-custom-constants.md) para el [identificador de configuración regional](locale-identifiers.md). Como regla, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) no puede distinguir entre configuraciones regionales complementarias, pero [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) puede porque usa nombres de configuración [regional](locale-names.md) en lugar de identificadores de configuración regional. La aplicación puede recuperar información sobre una configuración regional complementaria determinada solo cuando esa configuración regional es la configuración regional de usuario seleccionada actualmente. A continuación, la aplicación puede llamar [**a GetLocaleInfo y**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) pasar la constante [LOCALE USER \_ \_ DEFAULT](locale-user-default.md) como identificador de configuración regional.

## <a name="handle-replacement-locales"></a>Controlar las configuraciones regionales de reemplazo

Para conservar la confiabilidad de Windows, recuerde que una configuración regional de reemplazo compatible con la aplicación no puede modificar el identificador de configuración regional de la configuración regional reemplazada. Ninguna de las configuraciones regionales de reemplazo puede modificar las propiedades de ordenación Windows.

Aunque una configuración regional de reemplazo puede cambiar el calendario predeterminado, debe conservar el valor predeterminado original en algún lugar de la lista de calendarios disponibles. Por ejemplo, la configuración regional tailandesa (omisión) usa el calendario tailandés Desáneo como valor predeterminado. Un administrador puede crear una configuración regional de reemplazo que use el calendario localizado gregoriano. Sin embargo, la lista de calendarios disponibles sigue conteniendo una entrada para el calendario tailandés Desatenciones.

En el caso de las configuraciones regionales de reemplazo, la aplicación generalmente debe consultar información específica de la configuración regional en lugar de intentar un "acceso directo" basado en el conocimiento de una configuración regional determinada. Por ejemplo, cuando [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale) recupera la configuración regional actual como inglés (Estados Unidos), podría ser realmente una configuración regional de reemplazo que debería tener efecto.

## <a name="customize-calendars"></a>Personalizar calendarios

Las aplicaciones pueden personalizar los nombres de día y mes para calendarios gregorianos, pero no para calendarios no gregorianos. De forma similar, NLS no admite la creación de calendarios personalizados definidos por el usuario. Para obtener más información, vea [Fecha y calendario.](date-and-calendar.md)

## <a name="handle-sorting-sequences"></a>Controlar secuencias de ordenación

Una configuración regional complementaria puede usar cualquier secuencia de ordenación definida por Microsoft. Una configuración regional de reemplazo debe usar la misma secuencia de ordenación que la configuración regional que reemplaza. NLS no admite la creación de secuencias de ordenación definidas por el usuario. Para obtener más información, vea [Control de la ordenación en las aplicaciones.](handling-sorting-in-your-applications.md)

## <a name="localize-custom-locale-information"></a>Localización de información de configuración regional personalizada

NLS no proporciona un mecanismo para la localización de información de configuración regional personalizada. Por lo tanto, la constante [LOCALE \_ SLANGUAGE](locale-slanguage.md) o [LOCALE \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md) que se usa como identificador de configuración regional para una configuración regional personalizada siempre recupera los valores asociados a [LOCALE \_ SNATIVELANGNAME](locale-snative-constants.md) o [LOCALE \_ SNATIVELANGUAGENAME.](locale-snative-constants.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la compatibilidad con idiomas nacionales](using-national-language-support.md)
</dt> <dt>

[Configuraciones regionales personalizadas](custom-locales.md)
</dt> <dt>

[Fecha y calendario](date-and-calendar.md)
</dt> <dt>

[Control de la ordenación en las aplicaciones](handling-sorting-in-your-applications.md)
</dt> </dl>

 

 



