---
description: En este tema se proporcionan algunas instrucciones para administrar configuraciones regionales personalizadas en las aplicaciones.
ms.assetid: 2622e2b3-b952-4666-a440-85d73d11c5e0
title: Trabajar con configuraciones regionales personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab0e59446496ae2985860c0fd6b1bd5bddde084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001436"
---
# <a name="working-with-custom-locales"></a>Trabajar con configuraciones regionales personalizadas

En este tema se proporcionan algunas instrucciones para administrar [configuraciones regionales personalizadas](custom-locales.md) en las aplicaciones. Es mejor preparar todo el código fuente teniendo en cuenta estas consideraciones, ya que la aplicación no controla si las configuraciones regionales personalizadas están instaladas en el sistema operativo.

## <a name="handle-locale_stime-constant-correctly"></a>Controlar la \_ constante STime de configuración regional correctamente

Si tiene una aplicación anterior que usa [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) para obtener el separador de hora obsoleto indicado por la [configuración regional \_ STime](locale-stime-constants.md), la aplicación puede no analizar el formato de hora. Recuerde que el carácter que separa las horas de los minutos es distinto del carácter que separa los minutos de los segundos.

> [!Note]  
> Al programar para configuraciones regionales personalizadas, recuerde que son inusuales. Prácticamente todos los campos disponibles para NLS tienen que hacer frente a un comportamiento inusual. Por ejemplo, el formato de hora 12H34 ' 12 ' ' es legítimo y suele ser comprensible. Sin embargo, muchas aplicaciones realizan suposiciones acerca de los separadores de hora que pueden romper la longitud del búfer o mostrar los campos.

 

## <a name="distinguish-among-supplemental-locales"></a>Distinguir entre configuraciones regionales complementarias

Todas las configuraciones regionales complementarias usan la constante [ \_ personalizada no \_ especificada](locale-custom-constants.md) de la configuración regional para el [identificador de configuración regional](locale-identifiers.md). Como norma general, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) no puede distinguir entre las configuraciones regionales complementarias, pero [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) puede ser porque usa [nombres de configuración regional](locale-names.md) en lugar de identificadores de configuración regional. La aplicación puede recuperar información acerca de una configuración regional complementaria determinada solo cuando esa configuración regional es la configuración regional del usuario actualmente seleccionada. A continuación, la aplicación puede llamar a [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) y pasar el [ \_ \_ valor predeterminado del usuario de la configuración regional](locale-user-default.md) como identificador de configuración regional.

## <a name="handle-replacement-locales"></a>Controlar las configuraciones regionales de reemplazo

Para conservar la confiabilidad de Windows, recuerde que una configuración regional de reemplazo que admita la aplicación no puede modificar el identificador de configuración regional de la configuración regional reemplazada. Ninguna de las configuraciones regionales de reemplazo puede modificar las propiedades de ordenación de Windows.

Aunque una configuración regional de reemplazo puede cambiar el calendario predeterminado, debe conservar el valor predeterminado original en alguna parte de la lista de calendarios disponibles. Por ejemplo, la configuración regional tailandesa (Tailandia) utiliza el calendario budista tailandés como valor predeterminado. Un administrador puede crear una configuración regional de reemplazo que use el calendario gregoriano adaptado. Sin embargo, la lista de calendarios disponibles sigue conteniendo una entrada para el calendario budista tailandés.

En el caso de las configuraciones regionales de reemplazo, la aplicación generalmente debe consultar la información específica de la configuración regional en lugar de intentar un "acceso directo" en función del conocimiento de una determinada configuración regional. Por ejemplo, cuando [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale) recupera la configuración regional actual como inglés (Estados Unidos), es posible que se tratase de una configuración regional de reemplazo que se debe permitir que surta efecto.

## <a name="customize-calendars"></a>Personalizar calendarios

Las aplicaciones pueden personalizar los nombres de día y mes para los Calendarios gregorianos, pero no para los calendarios no gregorianos. Del mismo modo, NLS no admite la creación de calendarios personalizados definidos por el usuario. Para obtener más información, vea [fecha y calendario](date-and-calendar.md).

## <a name="handle-sorting-sequences"></a>Administrar secuencias de ordenación

Una configuración regional complementaria puede usar cualquier secuencia de ordenación definida por Microsoft. Una configuración regional de reemplazo debe utilizar la misma secuencia de ordenación que la configuración regional que reemplaza. NLS no admite la creación de secuencias de ordenación definidas por el usuario. Para obtener más información, vea [controlar la ordenación en las aplicaciones](handling-sorting-in-your-applications.md).

## <a name="localize-custom-locale-information"></a>Localizar información de configuración regional personalizada

NLS no proporciona un mecanismo para localizar información de configuración regional personalizada. Por lo tanto, la configuración regional de la configuración regional [ \_ SLANGUAGE](locale-slanguage.md) o la [ \_ SLOCALIZEDLANGUAGENAME de configuración](locale-slocalized-constants.md) regional usada como identificador de configuración regional para una configuración regional personalizada siempre recupera los valores asociados a la configuración regional [ \_ SNATIVELANGNAME](locale-snative-constants.md) o la [configuración regional \_ SNATIVELANGUAGENAME](locale-snative-constants.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la compatibilidad con National Language](using-national-language-support.md)
</dt> <dt>

[Configuraciones regionales personalizadas](custom-locales.md)
</dt> <dt>

[Fecha y calendario](date-and-calendar.md)
</dt> <dt>

[Controlar la ordenación en las aplicaciones](handling-sorting-in-your-applications.md)
</dt> </dl>

 

 



