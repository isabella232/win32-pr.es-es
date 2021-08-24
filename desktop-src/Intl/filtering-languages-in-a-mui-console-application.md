---
description: Una aplicación de consola de MUI puede admitir la configuración del sistema o la configuración específica de la aplicación para sus idiomas de interfaz de usuario. En este tema se describe el filtrado de idiomas para este tipo de aplicación.
ms.assetid: 6d3c491f-3f5e-4592-aada-49b8b415b497
title: Filtrado de idiomas en una aplicación de consola de MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcdd8fc0f7f63b5771f5b75b86ce5e76ab2420d407832d77b731ad952174cee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041325"
---
# <a name="filtering-languages-in-a-mui-console-application"></a>Filtrado de idiomas en una aplicación de consola de MUI

Una aplicación de consola de MUI puede admitir la configuración del sistema o la configuración específica de la aplicación para sus idiomas de interfaz de usuario. En este tema se describe el filtrado de idiomas para este tipo de aplicación.

## <a name="limit-the-languages-to-display"></a>Limitar los idiomas que se mostrarán

A diferencia de una ventana gráfica, la Windows no puede mostrar [scripts](uniscribe-glossary.md)complejos, como árabe, hebreo, persa, hindi, urdu, tailandés y muchos otros. Por lo tanto, la consola no puede mostrar muchos idiomas de interfaz de usuario en ninguna circunstancia.

La consola solo puede mostrar caracteres de la página de [códigos oem](code-pages.md) única asociada al idioma actual para aplicaciones que no son Unicode. Para cada página de códigos oem, la consola usa una fuente determinada y es posible que esto no proporcione cobertura completa para esa página de códigos.

Estas limitaciones relacionadas con la consola reducen el número de idiomas de interfaz de usuario que la consola puede mostrar en un equipo determinado. Por ejemplo, si el idioma actual de las aplicaciones no Unicode es japonés y el usuario intenta mostrar texto en alemán en la consola, los caracteres con umlauts no se muestran correctamente. Si el idioma actual de las aplicaciones no Unicode es alemán y el usuario quiere mostrar texto japonés en la consola, los resultados son mucho peores, lo que representa el texto casi incomprensible.

> [!Note]  
> Al proporcionar compatibilidad con la consola para las aplicaciones DE LAC, recuerde que la consola solo proporciona compatibilidad limitada con [los editores de métodos de entrada](input-method-manager.md).

 

## <a name="set-the-language-for-console-output"></a>Establecer el idioma para la salida de la consola

En Windows Vista y versiones posteriores, una aplicación de consola establece el idioma para admitir la presentación de la consola mediante una llamada a [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages). En esta llamada, la aplicación pasa EL FILTRO DE CONSOLA DE MOMENTO en el parámetro \_ \_ *dwFlags* y **NULL** para *pwszLanguagesBuffer*. Una alternativa es llamar a [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) con un identificador de idioma de 0. Esta configuración hace que la función seleccione el idioma que mejor admite la presentación de la consola.

En Windows XP, la aplicación solo puede establecer el idioma para la salida de la consola mediante una llamada a [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) con un identificador de idioma de 0.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer las preferencias de idioma de la aplicación](setting-application-language-preferences.md)
</dt> </dl>

 

 
