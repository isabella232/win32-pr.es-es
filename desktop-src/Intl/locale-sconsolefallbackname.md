---
description: LOCALE \_ SCONSOLEFALLBACKNAME
ms.assetid: 36465a1c-085f-4f80-ad3d-5be6eaefe943
title: LOCALE_SCONSOLEFALLBACKNAME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4234ea00516f777b4f70adc6127fd7dcf089d687b16ce68df8fbb210057b469b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948500"
---
# <a name="locale_sconsolefallbackname"></a>LOCALE \_ SCONSOLEFALLBACKNAME

**Windows Vista y versiones posteriores:** Configuración regional preferida que se usará para la presentación de la consola. El número máximo de caracteres permitido para esta cadena es 85, incluido un carácter nulo de terminación.

> [!Note]  
> En general, las aplicaciones no deben hacer un uso directo de los datos \_ SCONSOLEFALLBACKNAME de LOCALE. Para determinar qué recursos de lenguaje usar en una ventana de consola, una aplicación debe llamar a [SetThreadUILanguage](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) o [SetThreadPreferredUILanguages](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages). Estas funciones usan los datos de reserva de la consola como factor para elegir un idioma legible en la consola, pero no es el único determinante. En concreto, la consola se limita a mostrar caracteres de una sola página de códigos. Por ejemplo, el-GR para griego (Irlanda) es un idioma de consola válido, pero si la página de códigos actual de la consola es Latin-1 (página de códigos 1252), la consola muestra el texto griego principalmente como una serie de símbolos de caracteres no encontrados.

 

Si el idioma correspondiente a esta configuración regional se admite en la consola, el valor es el mismo que para [LOCALE \_ SNAME](locale-sname.md), es decir, la configuración regional propia se puede usar para la presentación de la consola. Sin embargo, la consola no puede mostrar idiomas que solo se pueden representar con [Uniscribe](uniscribe.md). Por ejemplo, la consola no puede mostrar el árabe ni los distintos idiomas indic. Por lo tanto, el valor \_ de LOCALE SCONSOLEFALLBACKNAME para las configuraciones regionales correspondientes a estos idiomas es diferente del valor de LOCALE \_ SNAME.

En el caso de las configuraciones regionales predefinidas, si el valor de reserva es diferente del valor de la propia configuración regional, se usa el valor de la configuración regional neutra. Una configuración regional específica está asociada a un idioma y a un país o región, mientras que una configuración regional neutra está asociada a un idioma, pero no a ningún país o región. Por ejemplo, ar-SA vuelve a "en", no a "en-US". Esta directiva de uso de configuraciones regionales neutras se implementa de forma coherente para las configuraciones regionales predefinidas y se recomienda encarecidamente para las configuraciones regionales personalizadas. Sin embargo, no se aplica la directiva. Para una configuración regional personalizada, la aplicación puede usar una configuración regional específica en lugar de una configuración regional neutra como reserva.

> [!Note]  
> Ninguna de las funciones descritas en [Llamar a las funciones "Nombre de configuración regional"](calling-the--locale-name--functions.md) acepta configuraciones regionales neutras como entradas. Por lo tanto, los \_ datos SCONSOLEFALLBACKNAME de LOCALE son de uso muy limitado. En concreto, ni [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ni [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) aceptan configuraciones regionales neutras como entradas.

 

 

 



