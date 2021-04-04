---
description: Una aplicación de consola de MUI puede admitir la configuración del sistema o la configuración específica de la aplicación para sus idiomas de interfaz de usuario. En este tema se describe el filtrado de idiomas para este tipo de aplicación.
ms.assetid: 6d3c491f-3f5e-4592-aada-49b8b415b497
title: Filtrar idiomas en una aplicación de consola de MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d484835af211f59cc559f8e1cd0dd414af13a8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910121"
---
# <a name="filtering-languages-in-a-mui-console-application"></a>Filtrar idiomas en una aplicación de consola de MUI

Una aplicación de consola de MUI puede admitir la configuración del sistema o la configuración específica de la aplicación para sus idiomas de interfaz de usuario. En este tema se describe el filtrado de idiomas para este tipo de aplicación.

## <a name="limit-the-languages-to-display"></a>Limitar los idiomas para mostrar

A diferencia de las ventanas gráficas, la consola de Windows no puede mostrar [scripts complejos](uniscribe-glossary.md), como árabe, hebreo, persa, Hindi, Urdu, tailandés y muchos otros. Por lo tanto, la consola no puede mostrar muchos idiomas de la interfaz de usuario en ninguna circunstancia.

La consola de solo puede mostrar caracteres de la [Página de códigos OEM](code-pages.md) única asociada al idioma actual para aplicaciones no Unicode. Para cada página de códigos de OEM, la consola de usa una fuente determinada, y es posible que esto no proporcione una cobertura completa para esa página de códigos.

Estas limitaciones relacionadas con la consola reducen el número de idiomas de interfaz de usuario que la consola de puede mostrar en un equipo determinado. Por ejemplo, si el idioma actual de las aplicaciones que no son Unicode es el japonés y el usuario intenta mostrar texto en alemán en la consola, los caracteres con diéresis no se muestran correctamente. Si el idioma actual de las aplicaciones que no son Unicode es el alemán y el usuario desea mostrar texto en japonés en la consola, los resultados son mucho peores, lo que representa el texto prácticamente incomprensible.

> [!Note]  
> Al proporcionar compatibilidad con la consola para las aplicaciones de MUI, recuerde que la consola solo proporciona compatibilidad limitada para los [editores de métodos de entrada](input-method-manager.md).

 

## <a name="set-the-language-for-console-output"></a>Establecer el idioma para la salida de la consola

En Windows Vista y versiones posteriores, una aplicación de consola establece el idioma para que admita la presentación de la consola mediante una llamada a [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages). En esta llamada, la aplicación pasa el \_ \_ filtro de la consola de MUI en el parámetro *dwFlags* y **null** para *pwszLanguagesBuffer*. Una alternativa es llamar a [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) con un identificador de idioma de 0. Esta configuración hace que la función Seleccione el idioma que mejor admite la presentación de la consola.

En Windows XP, la aplicación solo puede establecer el idioma para la salida de la consola mediante una llamada a [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) con un identificador de idioma de 0.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de las preferencias de idioma de la aplicación](setting-application-language-preferences.md)
</dt> </dl>

 

 
