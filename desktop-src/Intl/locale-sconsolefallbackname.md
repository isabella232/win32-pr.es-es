---
description: configuración regional \_ SCONSOLEFALLBACKNAME
ms.assetid: 36465a1c-085f-4f80-ad3d-5be6eaefe943
title: LOCALE_SCONSOLEFALLBACKNAME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09536167c68a4ec9156a1558960c48778019ae97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687707"
---
# <a name="locale_sconsolefallbackname"></a>configuración regional \_ SCONSOLEFALLBACKNAME

**Windows Vista y versiones posteriores:** Configuración regional preferida que se va a usar para la visualización de la consola. El número máximo de caracteres permitido para esta cadena es 85, incluido un carácter nulo de terminación.

> [!Note]  
> En general, las aplicaciones no deben hacer uso directo de los datos de SCONSOLEFALLBACKNAME de la configuración regional \_ . Para determinar qué recursos de idioma usar en una ventana de la consola, una aplicación debe llamar a [SetThreadUILanguage](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) o [SetThreadPreferredUILanguages](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages). Estas funciones utilizan los datos de reserva de la consola como un factor para elegir un idioma que es legible en la consola, pero no es el único factor determinante. En concreto, la consola está limitada a mostrar caracteres de una única página de códigos. Por ejemplo, el-GR para griego (Grecia) es un idioma de consola válido, pero si la página de códigos de la consola actual es Latin-1 (página de códigos 1252), la consola muestra el texto griego principalmente como una serie de símbolos no encontrados.

 

Si el idioma correspondiente a esta configuración regional es compatible con la consola de, el valor es el mismo que el de la [configuración regional \_ SNAME](locale-sname.md), es decir, se puede usar la propia configuración regional para la presentación de la consola. Sin embargo, la consola no puede mostrar idiomas que solo se pueden representar con [Uniscribe](uniscribe.md). Por ejemplo, la consola no puede mostrar árabe ni los distintos idiomas indios. Por lo tanto, el \_ valor de SCONSOLEFALLBACKNAME de configuración regional para las configuraciones regionales correspondientes a estos idiomas es diferente del valor de configuración regional \_ SNAME.

En el caso de las configuraciones regionales predefinidas, si el valor de reserva es diferente del valor de la propia configuración regional, se usa el valor de la configuración regional neutra. Una configuración regional específica está asociada a un idioma y a un país o región, mientras que una configuración regional neutra está asociada a un idioma, pero no está asociada a ningún país o región. Por ejemplo, ar-SA recurre a "en", no a "en-US". Esta directiva de uso de configuraciones regionales neutras se implementa de forma coherente para las configuraciones regionales predefinidas y se recomienda encarecidamente para las configuraciones regionales personalizadas. Sin embargo, no se aplica la Directiva. En el caso de una configuración regional personalizada, la aplicación puede usar una configuración regional específica en lugar de una configuración regional neutra como reserva.

> [!Note]  
> Ninguna de las funciones descritas en [llamada a las funciones de "nombre de configuración regional"](calling-the--locale-name--functions.md) acepta configuraciones regionales neutras como entradas. Por tanto, los \_ datos de SCONSOLEFALLBACKNAME de la configuración regional son de uso muy limitado. En concreto, ni [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ni [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) aceptan configuraciones regionales neutras como entradas.

 

 

 



